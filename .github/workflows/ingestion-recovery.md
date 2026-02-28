---
name: Ingestion Agent — Recovery
on:
  workflow_dispatch:
    inputs:
      transcript_filename:
        description: 'Transcript filename to summarize (e.g. 2026-01-15-jane-smith.md)'
        required: true

engine: copilot

permissions:
  contents: read

checkout:
  github-token: ${{ secrets.COPILOT_GITHUB_TOKEN }}

tools:
  github:
    toolsets: [repos]
    github-token: ${{ secrets.COPILOT_GITHUB_TOKEN }}
  edit:

post-steps:
  - name: Commit summary if written
    env:
      TRANSCRIPT_FILENAME: ${{ inputs.transcript_filename }}
      GIT_TOKEN: ${{ secrets.COPILOT_GITHUB_TOKEN }}
      GIT_REPO: ${{ github.repository }}
    run: |
      git add knowledge-store/summaries/
      if git diff --cached --quiet; then
        echo "No changes staged — noop"
      else
        git config user.name "ingestion-agent[bot]"
        git config user.email "ingestion-agent@noreply.github.com"
        git remote set-url origin "https://x-access-token:${GIT_TOKEN}@github.com/${GIT_REPO}.git"
        git commit -m "feat: add summary $TRANSCRIPT_FILENAME [ingestion-agent]"
        git push
      fi
---

# Ingestion Agent — Recovery

You process exactly one file: the transcript specified by `transcript_filename`. Do not list directories. Do not read any other files in the transcripts folder.

## Step 1: Check for existing summary

Use the repos toolset `get_file_contents` tool to fetch `knowledge-store/summaries/{transcript_filename}` from the `main` branch.

- If the file is returned: output `Summary already exists for {transcript_filename} — nothing to do.` and stop immediately.
- If the file is not found (404): continue to Step 2.

Do not list the `knowledge-store/summaries/` directory. Do not read any other files.

## Step 2: Read the transcript

Use the repos toolset `get_file_contents` tool to fetch `knowledge-store/transcripts/{transcript_filename}` from the `main` branch. Read it in full.

If the file is not found, output: `Transcript {transcript_filename} not found on main — cannot proceed.` and stop.

## Step 3: Generate the summary

Produce a summary using this exact format:

```
# Summary: {Interviewee full name}, {YYYY-MM-DD}

**Source:** `knowledge-store/transcripts/{filename}`
**Interviewee:** {Full name, role and company if stated}
**Date:** {Interview date}
**Summarized:** {ISO 8601 timestamp}

---

## Key Points

### {Descriptive heading drawn from the transcript}

- {Key point in the interviewee's own terms} `[HH:MM:SS]`
- {Key point} `[HH:MM:SS]`

> "{Verbatim quote — exact words, no paraphrase}" `[HH:MM:SS]`

### {Next heading}

- {Key point} `[HH:MM:SS]`

## Notable Quotes

> "{Verbatim quote}" `[HH:MM:SS]`

## Gaps

- `[NEEDS SOURCE]` {Something referenced but not elaborated on} `[HH:MM:SS]`
```

**Rules:**
- Every key point must have a timestamp reference in `[HH:MM:SS]` format
- Every quote must be verbatim — exact words, no paraphrase
- Mark every gap with `[NEEDS SOURCE]`
- If the transcript has no timestamps, omit them rather than inventing them

## Step 4: Write the summary

Write the summary content to `knowledge-store/summaries/{transcript_filename}` using the edit tool. Do not use the repos toolset to commit — the post-step will commit and push it automatically.

Once you have written the file, stop. Do not read any other files or take further action.
