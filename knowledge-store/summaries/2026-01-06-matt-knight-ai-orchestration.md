# Summary: Matt Knight, 2026-01-06

**Source:** `knowledge-store/transcripts/2026-01-06-matt-knight-ai-orchestration.md`
**Interviewee:** Matt Knight, Director of AI for Everyone, GitHub
**Date:** 2026-01-06
**Summarized:** 2026-02-28T07:10:10Z

---

## Key Points

### Managers as Agent Managers — The Core ROI Shift

- The primary ROI of agent orchestration for engineering managers is having "additional team members" — agents who function like junior engineers assigned to work without waiting on external engineering resources `[02:40]`
- Concrete example: Matt and Ben maintained internal platforms (Hub, Mission Control) with no dedicated developer by using Copilot agents to handle upgrades, refactors, bug fixes, and security vulnerabilities — including a four-year-old codebase with memory leaks `[03:07]`
- The ROI is not waiting on engineering resources: "as long as the work is something we feel comfortable enough with, we use mission control and agents to basically update, add new features, refactor, improve performance" `[04:04]`

> "The ROI is that you have a technical agent on the team you can assign work to and you don't have to wait for external people." `[05:26]`

### The Async Mindset Shift for Managers

- The biggest cultural shift is moving from sync AI usage (an IC model where you sit with the tool for hours) to async delegation — assigning work and walking away to attend meetings `[05:47]`
- Ben Balter's workflow: blocks five-to-fifteen-minute increments throughout the day exclusively for creating issues, then has dedicated review time the following day `[13:18]`
- Managers who treat AI like an IC — needing hours of focused time — miss the core value; the shift is "I now have this new async tool that I can apply an instruction, send it on its merry way, and I can come back one to four hours later, a week later, if I go on vacation" `[08:05]`

> "That's a shift in your workflow. That's a shift in thinking and how you schedule yourself." `[07:44]`

### Managing a Fleet of Agents

- Scaling from one agent to a fleet follows the same async principle, but requires budgeting dedicated time for issue creation — not relying on Slack or ad-hoc communication `[12:05]`
- Custom agents are key to fleet management: different repos (Hub, Mission Control, onboarding site) can have specialized agents (documentation agent, writing agent, coding standards agent) `[11:13]`
- Sub-issues can be used to structure work: a parent issue can have 10 sub-issues each individually assigned to Copilot, though today you cannot assign the parent and have sub-issues automatically picked up `[15:09]`

> "You need to budget time for creating issues in a way that you probably didn't in the past." `[12:21]`

### When Not to Run Parallel Agents

- The primary risk of parallel agents is merge conflicts when two agents modify the same file or code that is a dependency of the other agent's work `[22:39]`
- Rule: if agents are touching the same files, do not run them in parallel; if touching shared dependency code without deep understanding of those dependencies, single-thread instead `[23:25]`
- For large refactors or code where you are not a technical expert, single-threading allows you to "unravel" mistakes one at a time rather than unwinding a ball of code `[25:20]`

> "If it's touching the same files, I automatically just won't run parallel agents." `[23:25]`

### Writing Effective Agent Specs (Issues as Prompts)

- The most important rule: give agents a "clear sliver of work" with a defined start and finish — one feature may be three separate issues (UI, backend, integration) `[27:00]`
- Planning mode (VS Code) / brainstorm mode / task mode (GitHub chat) turns a rough idea into structured, prioritized sub-tasks via a mini-interview process `[18:34]`
- The recommended workflow: kick off in chat → expand the idea in planning/task mode → ask chat to create the issue in the target repo → open the issue and assign Copilot `[21:05]`

> "Prompts are issues in this new world." `[27:50]`

### Custom Agents and the AGENTS.md File

- The agents.md file is for instructions you would want in every prompt — files the agent must never change, required folder structures, coding standards documents the agent should always reference `[28:53]`
- Value is eliminating repetition: "imagine if you're having to add these extra two to four sentences to every single one and you're having to remember it" across 100 prompts per year `[30:16]`

### Real-Time Steering and Governance

- The most common failure mode is "misreading of intention" — the agent interprets vague instructions and pursues work not aligned with the manager's intent `[31:15]`
- The second common failure: hallucination when an integration point (e.g., an MCP server or API) fails — the agent makes up data rather than flagging the failure `[32:11]`
- Recommended monitoring window: about five minutes at kickoff to verify the agent understood intent and correctly fetched referenced files/docs, then walk away `[45:55]`

> "It's kind of like you have a kid on a bicycle. And once you get them up on the bike and once you see them moving, they're fine, but you want to stand there and watch them get on that bike." `[45:24]`

### Review Workflow

- Start with the session log for complex work — scan (do not read in depth) looking for red flags like failed fetches `[46:38]`
- Copilot's self-generated PR comments are now very detailed — that is where to focus review time, combined with the code itself `[47:17]`
- For self-correction, playwright tests and unit tests are the right mechanism: "keep working on this until you pass all of your tests" — but agents can hallucinate passing tests on long-running problems `[48:33]`

### Use Case Validation — Scale Investment with Complexity

- Monoliths are currently the weakest use case: context windows limit effectiveness on very large codebases; specific, detailed instructions are required `[49:22]`
- The guiding rule: "scale your investment in breaking down the work with the complexity of the work" — the same calculus you would apply when giving instructions to a junior engineer `[49:45]`

---

## Notable Quotes

> "It's not dissimilar than just delegating work to an employee. You have to write out what you want, you have to write out its goals, and you assign it to co-pilot and BAM." `[05:34]`

> "The way you do it is I generally recommend you build an issue for each one, whatever those things are, and simply put, you just spend that time that you're thinking about building out an issue and assigning co-pilot to it to work on." `[12:05]`

> "Agents do sometimes hallucinate and they'll say they have correctly done all of those tests when they haven't, especially if it's a very long-running problem." `[48:33]`

---

## Gaps

- `[NEEDS SOURCE]` Ben Balter referenced as one of the top three Copilot coding agent users at GitHub — specific productivity data not provided in this interview `[01:44]`
- `[NEEDS SOURCE]` Pablo (last name not recalled) referenced as having built a production-grade AI triage process; name and process details not captured `[16:44]`
- `[NEEDS SOURCE]` PRU (Premium Request Unit) consumption rules for agent steering — Matt acknowledges uncertainty about when steering triggers an additional PRU `[39:29]`
- `[NEEDS SOURCE]` Specific blog content on playwright/unit testing for agent self-correction referenced across Microsoft and GitHub — titles/links not provided `[47:48]`
- `[NEEDS SOURCE]` Link shared in Zoom chat showing Hubber Copilot usage patterns from merged PRs — not reproduced in transcript `[51:34]`
