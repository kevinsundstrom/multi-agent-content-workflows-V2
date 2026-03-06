# Agent Orchestration

> This document synthesizes what interview sources have said about this topic. It is created and maintained by the living document agent. Every claim is sourced. Do not edit directly.

**Topic:** `agent-orchestration`
**Last synthesized:** 2026-03-05T22:30:16Z
**Interview sources:** 2 — see [Source Index](#source-index)

---

## What Agent Orchestration Makes Possible

Both sources describe agent orchestration in terms of a fundamental expansion of what can be delegated. Matt Nigh frames this as gaining "additional team members" — agents who function like junior engineers available to handle work without waiting on external engineering resources. Idan (GitHub Agentic Workflows team) describes it at a product level as "pushing the boundaries of what is automatable as part of my repository," covering use cases like detecting doc/code divergence, accessibility standards, and performance optimizations.

> "The ROI is that you have a technical agent on the team you can assign work to and you don't have to wait for external people." — Matt Nigh, `[05:26]` · [2026-01-06-matt-nigh-agent-orchestration.md](../summaries/2026-01-06-matt-nigh-agent-orchestration.md)

> "Agentic Workflows is really thinking about like, how can we push the boundaries of what is automatable as part of my repository." — Idan, `[00:00:26]` · [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md)

Both sources independently note that the space of possible uses is still being discovered. Idan stated explicitly: "We don't even know what all those things are yet." Matt described how he and a colleague maintained internal platforms with no dedicated developer by using Copilot agents to handle upgrades, refactors, bug fixes, and security vulnerabilities — including a four-year-old codebase with memory leaks.

---

## The Async Mindset Shift

Both sources describe a significant change in how people must think about their relationship to delegated work — though they frame it from different angles.

Matt Nigh describes the shift as moving from sync AI usage (an individual contributor model where you sit with the tool for hours) to async delegation — assigning work and walking away to attend meetings. He identifies this as the core cultural barrier for engineering managers: those who treat AI like an IC miss the value entirely.

> "That's a shift in your workflow. That's a shift in thinking and how you schedule yourself." — Matt Nigh, `[07:44]` · [2026-01-06-matt-nigh-agent-orchestration.md](../summaries/2026-01-06-matt-nigh-agent-orchestration.md)

> "I now have this new async tool that I can apply an instruction, send it on its merry way, and I can come back one to four hours later, a week later, if I go on vacation" — Matt Nigh, `[08:05]` · [2026-01-06-matt-nigh-agent-orchestration.md](../summaries/2026-01-06-matt-nigh-agent-orchestration.md)

Idan describes this same shift from a personal realization angle — not as a cultural prescription but as something that happened to him as a builder in the space:

> "Now with Agentic Workflows, it's like my relationship with what is possible to delegate has changed overnight, and now the hard part is actually thinking about, 'Wait a minute, that's something I could take off of my plate now,' and realizing what those things are." — Idan, `[00:08:04]` · [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md)

Matt offered a concrete workflow example: Ben Balter blocks five-to-fifteen-minute increments throughout the day exclusively for creating issues, then has dedicated review time the following day. Matt summarized the discipline required: "You need to budget time for creating issues in a way that you probably didn't in the past."

---

## Structuring Work for Agents

Both sources describe how agents receive their instructions, though the mechanisms differ depending on whether the agent is interactive (GitHub Copilot coding agent via issue) or automated (Agentic Workflows via Markdown file).

**Matt Nigh on issues as prompts:** The most important rule is to give agents a "clear sliver of work" with a defined start and finish. One feature may be three separate issues (UI, backend, integration). Planning mode in VS Code or task mode in GitHub chat turns a rough idea into structured, prioritized sub-tasks.

> "Prompts are issues in this new world." — Matt Nigh, `[27:50]` · [2026-01-06-matt-nigh-agent-orchestration.md](../summaries/2026-01-06-matt-nigh-agent-orchestration.md)

> "It's not dissimilar than just delegating work to an employee. You have to write out what you want, you have to write out its goals, and you assign it to co-pilot and BAM." — Matt Nigh, `[05:34]` · [2026-01-06-matt-nigh-agent-orchestration.md](../summaries/2026-01-06-matt-nigh-agent-orchestration.md)

**Idan on plain-English workflow descriptions:** Agentic Workflows are created through the Agents tab of a repo by writing a plain-English description — the same way you would describe the task to a teammate. Idan described his Astro upgrade workflow specification: "Listen, everyday check if there's a new release from Astro for any of my dependencies. And if yes, look at the changelog, look at the upgrading docs, come up with a plan to do the migration, including dealing with any breaking changes, and then create a PR with all the changes related to the upgrade." The actual workflow file is Markdown with a front matter block — Idan did not write it himself; he prompted Copilot with what he wanted done and it wrote the file.

> "You're using AI to create AI." — Idan, `[00:02:00]` · [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md)

> "Think of it as if GitHub Actions and Copilot had a baby together then this is kind of what it is." — Idan, `[00:04:29]` · [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md)

Both sources also mention referencing persistent instruction files (Matt: AGENTS.md, Idan: agents.md or Copilot instructions) to avoid repeating context across every agent invocation.

---

## Guardrails, Governance, and Safe Outputs

The two sources describe different levels of guardrail mechanisms, reflecting that they are discussing different products (interactive Copilot coding agent vs. Agentic Workflows).

**Idan on Agentic Workflows guardrails:** The front matter block in the workflow Markdown file is where hard constraints are placed — things the agent should not be able to control. The `safe outputs` stanza specifies what the workflow is allowed to produce per run (e.g., exactly one pull request). Workflows are also constrained to specific tools and specific internet domains. Critically, this enforcement happens outside the agentic loop itself.

> "A big part of Agentic Workflows has actually been about how do we stick the right guardrails around the execution of this so that you can have confidence that it's going to do what you ask without doing any of the things that you don't want it to do?" — Idan, `[00:00:01]` · [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md)

> "We're basically sticking a firewall between the agent and the internet." — Idan, `[00:05:27]` · [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md)

**Matt Nigh on soft governance via AGENTS.md and monitoring:** Matt describes a less formalized governance model relying on the AGENTS.md file (instructions that appear in every prompt — files the agent must never change, required folder structures, coding standards) and a recommended five-minute monitoring window at kickoff to verify the agent understood intent and correctly fetched referenced files.

> "It's kind of like you have a kid on a bicycle. And once you get them up on the bike and once you see them moving, they're fine, but you want to stand there and watch them get on that bike." — Matt Nigh, `[45:24]` · [2026-01-06-matt-nigh-agent-orchestration.md](../summaries/2026-01-06-matt-nigh-agent-orchestration.md)

`[NEEDS SOURCE]` The specific edge cases the Agentic Workflows team is currently working to resolve are not elaborated — Idan referenced them as a near-term focus area but did not describe them.

---

## Failure Modes

**Matt Nigh** identified two primary failure modes for agents:

1. **Misreading of intention** — the most common failure: the agent interprets vague instructions and pursues work not aligned with the manager's intent.
2. **Hallucination at integration points** — when an MCP server, API, or referenced file fails, the agent may fabricate data rather than flagging the failure.

A third failure mode Matt described involves self-correction: agents can be instructed to "keep working on this until you pass all of your tests," but on long-running problems they may hallucinate passing tests.

> "Agents do sometimes hallucinate and they'll say they have correctly done all of those tests when they haven't, especially if it's a very long-running problem." — Matt Nigh, `[48:33]` · [2026-01-06-matt-nigh-agent-orchestration.md](../summaries/2026-01-06-matt-nigh-agent-orchestration.md)

**Idan** did not enumerate specific failure modes but acknowledged that the near-term team focus is "shaking out edge cases" based on user feedback. He did note that if no upgrade is found, his Astro workflow outputs "no operation" — suggesting graceful handling of null results is a deliberate design consideration.

`[NEEDS SOURCE]` PRU (Premium Request Unit) consumption rules for agent steering — Matt acknowledges uncertainty about when steering triggers an additional PRU cost.

---

## Managing a Fleet of Parallel Agents

This theme was covered only by Matt Nigh; Idan did not address fleet management directly.

Scaling from one agent to a fleet follows the same async principle but requires budgeting dedicated time for issue creation — not relying on Slack or ad-hoc communication. Custom agents are key: different repos can have specialized agents (documentation agent, writing agent, coding standards agent). Sub-issues can structure work: a parent issue can have ten sub-issues each individually assigned to Copilot, though today you cannot assign the parent and have sub-issues automatically picked up.

The primary risk of parallel agents is merge conflicts when two agents modify the same file or code that is a dependency of the other agent's work. Matt's rule: if agents are touching the same files, do not run them in parallel; if touching shared dependency code without deep understanding of those dependencies, single-thread instead.

> "If it's touching the same files, I automatically just won't run parallel agents." — Matt Nigh, `[23:25]` · [2026-01-06-matt-nigh-agent-orchestration.md](../summaries/2026-01-06-matt-nigh-agent-orchestration.md)

`[NEEDS SOURCE]` Idan's perspective on multi-agent or parallel workflow execution within the Agentic Workflows system was not addressed in the available summary.

---

## Real-World Examples and Use Cases

**Matt Nigh** described maintaining internal GitHub platforms (Hub, Mission Control) using Copilot agents: upgrades, refactors, bug fixes, and security vulnerabilities — including a four-year-old codebase with memory leaks — all handled without a dedicated developer.

**Idan** offered two examples:

1. **Astro super Dependabot** — a daily workflow that checks for new Astro releases, reads changelogs and upgrade docs, plans the migration including breaking changes, and creates a PR. Copilot produced a table and changelog highlights in the PR without being explicitly asked to — it inferred what would be useful.

2. **Home Assistant issue triage** — built by Franck (last name not stated), maintainer of one of the busiest open source projects on GitHub. The workflow examines stack traces in bug reports, determines whether the exception terminates in Home Assistant's code or third-party code, and if it is Home Assistant's code, attempts to produce a pull request fixing the problem.

> "Ah, that feels the future right there." — Andrea Griffiths (host), `[00:09:48]` · [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md)

Idan's examples site also included: CI Doctor (detects and fixes failing CI workflows), contribution guidelines, accessibility review, documentation sync, cross-repo workflows, infrastructure, testing and validation, teamwork, and team culture workflows.

`[NEEDS SOURCE]` Franck's last name (Home Assistant maintainer) is not mentioned in the available summary.

---

## Open Source Maintenance as a Priority Use Case

Idan specifically identified open source maintainers as a priority audience for Agentic Workflows. He framed the AI code generation trend as a double-edged sword for maintainers: they get AI assistance, but the volume of incoming contributions can become a firehose.

> "The cost of creating code has gone down significantly. That's a double-edged sword." — Idan, `[00:10:37]` · [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md)

> "Now it can be a firehose that's really difficult to deal with." — Idan, `[00:10:54]` · [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md)

> "At the end of the day, it doesn't matter if the agent is really good. What matters is does it do stuff that is valuable to me? Does it give me more free time for more things that I care about?" — Idan, `[00:09:58]` · [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md)

Matt Nigh did not address open source specifically; his frame was entirely internal team productivity for engineering managers at companies using GitHub.

---

## Source Index

| Interview | Interviewee | Date |
|-----------|-------------|------|
| [2026-01-06-matt-nigh-agent-orchestration.md](../summaries/2026-01-06-matt-nigh-agent-orchestration.md) | Matt Nigh, Director of AI for Everyone, GitHub | 2026-01-06 |
| [2026-03-05-andrea-griffiths-agentic-workflows.md](../summaries/2026-03-05-andrea-griffiths-agentic-workflows.md) | Idan (last name not stated), GitHub Agentic Workflows team; hosted by Andrea Griffiths, GitHub | 2026-03-04 |
