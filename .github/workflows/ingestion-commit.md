---
name: Ingestion Agent — Commit
on:
  pull_request:
    types: [closed]
    paths:
      - 'knowledge-store/transcripts/**.md'

engine: copilot

permissions:
  contents: read
  pull-requests: read
  issues: read

tools:
  github:
    toolsets: [repos, pull_requests, issues]
    github-token: ${{ secrets.COPILOT_GITHUB_TOKEN }}
---

# Ingestion Agent — Commit

A transcript PR has been closed. If it was merged, find the summary that was posted as a review comment and commit it to `knowledge-store/summaries/`. If it was not merged, do nothing.

## Step 1: Check whether the PR was merged

Read the PR using the pull_requests toolset. Check the `merged` field.

If `merged` is false, output:

> PR was closed without merging — nooping.

Then stop. Do not read comments. Do not commit anything.

## Step 2: Identify the transcript files

List the files changed in this PR. Find every `.md` file in `knowledge-store/transcripts/`. These are the transcripts that need summaries committed.

## Step 3: Find the summary comment for each transcript

Read all comments on this PR. For each transcript filename, look for a comment containing the marker:

```
<!-- ingestion-agent-summary:{filename} -->
```

where `{filename}` matches the transcript filename exactly (e.g., `2026-01-15-jane-smith.md`).

The content of that comment — everything from the marker line through the end of the comment — is the summary to commit.

If no matching summary comment exists for a transcript:
- Do not fabricate a summary
- Do not commit anything for that transcript
- Post a new PR comment noting which transcript is missing a summary and that it must be re-processed manually

## Step 4: Commit each summary

For each transcript that has a matching summary comment:

1. Determine the target path: `knowledge-store/summaries/{filename}` where `{filename}` matches the transcript filename exactly
2. Commit the full summary content (including the marker line) to that path using the GitHub API (repos toolset)
3. Use this commit message: `feat: add summary {filename} [ingestion-agent]`

Commit directly to `main`. Do not open a pull request. The commit must use the COPILOT_GITHUB_TOKEN configured in this workflow so that the downstream state agent trigger fires.

Commit each summary as a separate commit. Do not batch multiple summaries into one commit — this makes the trigger chain cleaner and the git history readable.
