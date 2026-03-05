# Summary: Idan (GitHub Agentic Workflows), 2026-03-04

**Source:** `knowledge-store/transcripts/2026-03-05-andrea-griffiths-agentic-workflows.md`
**Interviewee:** Idan (last name not stated), GitHub Agentic Workflows team, GitHub; hosted by Andrea Griffiths (GitHub Checkout)
**Date:** 2026-03-04
**Summarized:** 2026-03-05T22:12:35Z

---

## Key Points

### What Agentic Workflows Are

- Agentic Workflows is about pushing the boundaries of what is automatable as part of a repository — detecting doc/code divergence, accessibility standards, performance optimizations `[00:00:26]`
- There is a public GitHub Agentic Workflows website listing all authored workflows `[00:00:50]`
- "We don't even know what all those things are yet." — the space of possible uses is still being discovered `[00:00:48]`

> "Agentic Workflows is really thinking about like, how can we push the boundaries of what is automatable as part of my repository." `[00:00:26]`

### Building a Super Dependabot for Astro

- Idan built an Agentic Workflow for his own Astro-based personal website as a "super Dependabot" `[00:01:07]`
- Framework upgrades are not just version bumps — they require migrations and judgment that standard Dependabot cannot provide `[00:01:30]`
- The workflow is created through the Agents tab of the repo by writing a plain-English description `[00:01:47]`
- Idan described the workflow to Copilot the same way he would describe it to a teammate: check daily for new Astro releases, read changelog and upgrade docs, plan the migration including breaking changes, and create a PR `[00:02:06]`
- Copilot produced a table and changelog highlights in the PR that were not explicitly requested — it inferred what would be useful `[00:03:17]`
- If no upgrade is found, the workflow outputs "no operation" `[00:03:37]`

> "Listen, everyday check if there's a new release from Astro for any of my dependencies. And if yes, look at the changelog, look at the upgrading docs, come up with a plan to do the migration, including dealing with any breaking changes, and then create a PR with all the changes related to the upgrade." `[00:02:06]`

> "You're using AI to create AI." `[00:02:00]`

### How Copilot Turns English into Workflows

- The actual workflow description is just Markdown, just English, with a front matter block `[00:02:35]`
- Agentic Workflows runs on top of GitHub Actions — Idan described it as "if GitHub Actions and Copilot had a baby together" `[00:04:28]`
- The Agentic Workflow compiler takes the Markdown file and turns it into an actual Actions workflow `[00:04:41]`
- Idan did not write the workflow file himself — he prompted Copilot with what he wanted done and it wrote the file `[00:05:34]`
- Copilot instructions or agents.md can be referenced by saying "Pay attention to my agents.md" in plain English `[00:05:56]`

> "Think of it as if GitHub Actions and Copilot had a baby together then this is kind of what it is." `[00:04:29]`

### Setting Guardrails and Safe Outputs

- The front matter block is where guardrails are placed — things the agent should not be able to control `[00:04:46]`
- The `safe outputs` stanza in front matter specifies what the workflow is allowed to do per run; in Idan's example, it can create exactly one pull request `[00:04:52]`
- The workflow is also constrained to specific tools and specific internet domains — not allowed to fetch any domain `[00:05:14]`
- Guardrail enforcement happens outside the agentic loop — "We're basically sticking a firewall between the agent and the internet." `[00:05:27]`
- Andrea raised a use case: Dependabot alerts that can't raise a PR due to breaking changes or low compatibility confidence; Idan's answer is to write in English what you want to happen `[00:04:01]`
- Example response workflow: every time Dependabot opens a PR, look at it, determine additional work needed, try building, find errors, fix them, look at documentation `[00:04:06]`

> "A big part of Agentic Workflows has actually been about how do we stick the right guardrails around the execution of this so that you can have confidence that it's going to do what you ask without doing any of the things that you don't want it to do?" `[00:00:01]`

> "We're basically sticking a firewall between the agent and the internet." `[00:05:27]`

### Exploring the Agentic Workflows Examples Repo

- The site has quick starts and a large number of examples `[00:06:27]`
- Example categories: cross-repo workflows, infrastructure, testing and validation, teamwork, team culture, planning `[00:06:45]`
- Specific examples listed: Issue Triage, CI Doctor (detects and fixes failing CI workflows), contribution guidelines, Dependabot-style upgrades, accessibility review, documentation sync `[00:06:57]`
- Andrea noted her own challenge: updating projects without updating docs — Agentic Workflows could automate that `[00:07:29]`
- Idan's reflection: his relationship with what is possible to delegate has changed overnight; the hard part is now identifying what to take off his plate `[00:08:04]`

> "Now with Agentic Workflows, it's like my relationship with what is possible to delegate has changed overnight, and now the hard part is actually thinking about, 'Wait a minute, that's something I could take off of my plate now,' and realizing what those things are." `[00:08:04]`

### Real-World Example: Home Assistant Issue Triage

- Early tester: Franck (last name not stated), maintainer of Home Assistant, one of the busiest open source projects on GitHub `[00:08:43]`
- Maintainer burden at Home Assistant includes sorting out whether bugs are in their code or in third-party integrations (e.g., Samsung robot vacuum) `[00:09:00]`
- Franck created a workflow that examines stack traces in bug reports, determines if the exception terminates in Home Assistant's code or third-party code `[00:09:17]`
- If the bug is in Home Assistant's own code, the workflow attempts to produce a pull request fixing the problem `[00:09:39]`

> "Ah, that feels the future right there." `[00:09:48]`

### What's Next and the Future of Open Source Maintenance

- Near-term focus: shaking out edge cases and enlarging use cases based on feedback from users trying the product `[00:10:10]`
- Idan's priority: using Agentic Workflows to benefit open source maintainers specifically `[00:10:31]`
- The cost of creating code has gone down — a double-edged sword: maintainers get AI help, but the volume of incoming contributions can become a firehose `[00:10:37]`
- Goal: use AI to tip the scales back toward maintainers having more control over their time `[00:10:57]`

> "At the end of the day, it doesn't matter if the agent is really good. What matters is does it do stuff that is valuable to me? Does it give me more free time for more things that I care about?" `[00:09:58]`

> "The cost of creating code has gone down significantly. That's a double-edged sword." `[00:10:37]`

> "Now it can be a firehose that's really difficult to deal with." `[00:10:54]`

---

## Notable Quotes

> "A big part of Agentic Workflows has actually been about how do we stick the right guardrails around the execution of this so that you can have confidence that it's going to do what you ask without doing any of the things that you don't want it to do?" `[00:00:01]`

> "You're using AI to create AI." `[00:02:00]`

> "Think of it as if GitHub Actions and Copilot had a baby together then this is kind of what it is." `[00:04:29]`

> "We're basically sticking a firewall between the agent and the internet." `[00:05:27]`

> "At the end of the day, it doesn't matter if the agent is really good. What matters is does it do stuff that is valuable to me? Does it give me more free time for more things that I care about?" `[00:09:58]`

> "The cost of creating code has gone down significantly. That's a double-edged sword." `[00:10:37]`

> "Now with Agentic Workflows, it's like my relationship with what is possible to delegate has changed overnight, and now the hard part is actually thinking about, 'Wait a minute, that's something I could take off of my plate now,' and realizing what those things are." `[00:08:04]`

---

## Gaps

- `[NEEDS SOURCE]` Idan's last name is never stated in the transcript `[00:00:26]`
- `[NEEDS SOURCE]` Franck's last name (Home Assistant maintainer) is not mentioned `[00:08:45]`
- `[NEEDS SOURCE]` The specific domains the web fetcher was restricted to in the live demo are not enumerated `[00:05:19]`
- `[NEEDS SOURCE]` The specific edge cases the team is currently working to resolve are not elaborated `[00:10:10]`
- `[NEEDS SOURCE]` Andrea mentions she has been "playing a little bit about for maintenance for my own repositories" — what she has built is not described `[00:00:14]`
