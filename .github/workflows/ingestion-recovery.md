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

tools:
  github:
    toolsets: [repos]
    github-token: ${{ secrets.COPILOT_GITHUB_TOKEN }}
---

# Ingestion Agent — Recovery

A transcript is on `main` but has no summary. You will generate the summary and commit it directly to `main` so the state agent can process it.

## Step 1: Check for existing summary

Check whether `knowledge-store/summaries/{transcript_filename}` already exists on `main`.

If it does, output:
> Summary already exists for `{transcript_filename}` — nothing to do.

Then stop.

## Step 2: Read the transcript

Read `knowledge-store/transcripts/{transcript_filename}` from `main` in full.

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

## Step 4: Commit the summary to main

Use the repos toolset to create the file `knowledge-store/summaries/{transcript_filename}` on the `main` branch with the summary content.

Commit message: `feat: add summary {transcript_filename} [ingestion-agent]`

Commit directly to `main`. Do not create a branch. Do not open a PR. The COPILOT_GITHUB_TOKEN configured in this workflow ensures the downstream state agent trigger fires.
