# Summary: Christopher Harrison & Christina Warren, 2026-01-15

**Source:** `knowledge-store/transcripts/2026-01-15-christopher-harrison-christina-warren-app-modernization.md`
**Interviewee:** Christopher Harrison, Senior Developer Advocate, GitHub; Christina Warren, Senior Developer Advocate, GitHub
**Date:** 2026-01-15
**Summarized:** 2026-02-28T07:10:10Z

---

## Key Points

### Why Incremental Modernization Doesn't Happen — Primary Friction Points

- The dominant pattern is "if it works, it doesn't get touched" — modernization is only triggered when new features must be added or something breaks `[02:32]`
- There are no ribbon-cutting ceremonies for maintaining a bridge; organizations celebrate shipping new features but ignore updating to a newer version of Angular or .NET `[03:14]`
- By the time modernization is forced, the system is so far out of date that a full rewrite becomes the only perceived option — and rewrites attract promotion and politics that incremental work cannot `[04:09]`

> "There are no ribbon cutting ceremonies for maintaining a bridge. There's a ribbon cutting ceremony for opening the bridge and then after that we just sort of wind up forgetting about it." `[03:26]`

### Who Is Incentivized to Modernize Continuously

- Rank-and-file developers are most incentivized — modern stacks are easier to find documentation for, and being stuck on an older version directly harms their career trajectory `[05:05]`
- Vendors and contractors, who frequently work in and out of a codebase, also benefit because modern stacks reduce the ramp-up burden and context gaps `[06:10]`
- Engineering managers benefit from reduced cost and complexity: a modern, aligned stack saves money long-term and makes bosses happy `[07:53]`

### Security as a Continuous Modernization Argument

- Outdated microservices running unpatched versions with known CVEs are a real attack vector — Christina cited cases of companies being breached through old services nobody realized were still running `[09:15]`
- When open-source maintainers drop support, organizations often get only six months' notice — staying current means smaller, simpler upgrades versus a multi-year catch-up `[10:19]`

> "Clean as you go, so to speak, it's just going to make your life that much easier." `[11:02]`

### Where AI Helps (and Doesn't) with Modernization

- AI is better at incremental updates than large cross-version migrations because it is a pattern matcher — it performs better when the target pattern already exists in the codebase `[12:43]`
- Knowledge cut-off dates mean AI may lag on very new framework releases; you may need to feed it documentation to compensate `[11:35]`
- Very large version jumps (multiple years, multiple versions) may require incremental AI passes, the same way a human would upgrade an OS incrementally rather than in one shot `[14:01]`

> "It's not like you can just point the AI towards the older content and then say, okay, make this modern for what things are in 2026. It might take running the AI through multiple steps." `[14:16]`

### AI Reading Business Intent from Legacy Code

- The most common use case is not translating code to English business logic — it is helping new team members or developers unfamiliar with a section of the codebase get up to speed quickly `[15:44]`
- Organizations frequently use AI to generate a "v0 documentation" pass because virtually every org has tech debt in the form of outdated docs `[16:35]`
- AI behaves like a new developer who must read the codebase without tribal knowledge — it can make mistakes but can also expose areas of the application that even experienced developers hadn't seen `[16:50]`
- Time-to-first-commit drops significantly when developers have access to Copilot because they can ask unlimited questions without the social cost of bothering colleagues `[17:33]`

> "There's an embarrassment factor... developers will wind up getting stuck in an older version, they don't get to use the newer version, and then in turn, that winds up impacting their career." `[05:24]`

### Can AI Enable Continuous Modernization?

- Continuous modernization is possible but requires classic DevOps infrastructure (regression tests, acceptance tests, CI/CD) already in place — AI cannot substitute for missing test coverage `[21:32]`
- The biggest unlock AI provides is parallel labor: agents can run modernization tasks in parallel, making it feasible for small teams without a dedicated modernization head count `[23:09]`
- Christopher ran Copilot coding agent on a Svelte 4→5 migration by first asking the agent to audit the entire application and map what needs modernization, then directing targeted updates — using MCP servers for framework documentation `[28:44]`

> "There is no magic in AI. The fundamentals don't change." `[20:53]`

### Building and Maintaining Dedicated Modernization Agents

- Start generic: run the agent on the codebase, observe its behavior and errors, then refine the instructions file based on what you learn — even asking the AI to rewrite its own prompt `[33:23]`
- Instructions files are living documents: as models change, as the application changes, and as the team learns, the file should be updated — model updates can change agent behavior in ways that require reprompting `[36:55]`
- Version control the instructions file so you can diff what changed between model versions and clean out instructions the newer model no longer needs `[39:47]`

> "I don't want this to just be a set and forget it. I want to make sure that that's a living document." `[37:00]`

### Why 95% of AI Pilots Fail — Organizational Readiness

- The root cause is treating AI as magic based on polished demos, without going through a proper rollout: setting goals, assigning champions, running training, building a migration plan `[42:26]`
- Champions are essential — people who get colleagues excited, answer questions, and push adoption; cutting off access when usage is low is counterproductive `[43:33]`
- Training must be ongoing, not one-time: the state of LLMs and what they can do changes rapidly, and what was true two years ago is completely outdated `[46:38]`

> "Nobody's gonna roll out a new security tool... without going through a proper rollout... And when we have AI, again, it's just a tool. And so all the exact same rules apply." `[43:11]`

### Organizational Responsibility at Scale

- As teams scale from one developer to thousands, someone needs to own the AI toolchain — similar to having a deployment tool owner — responsible for access, permissions, and custom instructions `[44:55]`
- An "AI guide" (analogous to a coding style guide) covering prompting best practices, agent configuration standards, and file organization conventions would give teams predictability across individuals `[50:45]`
- Even within one team, developers may use different AI tools (Codex, Claude, Copilot) — the instructions and best practices must be tool-agnostic enough to deliver consistent, predictable output regardless `[51:58]`

### GitHub Platform Advantage: Third-Party Agent Support

- The key GitHub differentiator is supporting third-party agents on GitHub itself — teams can use Claude, Gemini, Codex, and Copilot coding agent, all with PRs that land in one centralized platform `[53:08]`
- This gives security and operations teams a single place to manage access, permissions, and oversight across multiple AI tools rather than maintaining multiple dashboards `[54:44]`

> "The one thing that we've got that nobody else has is that third party support all on that one centralized platform and that's right now I think the biggest bell that we should be ringing." `[54:13]`

---

## Notable Quotes

> "By the time it becomes a problem... it's so far out of date that then you end up rewriting the whole thing because that's just where you're at. And that's not caught in part because whoever started to modernize things didn't go back and do their homework." `[03:55]`

> "I can just like give something to Claude and let it cook for eight hours and see what it comes back with. Now I'm still gonna wanna review that code." `[24:31]`

> "If my name is on it, then I'm responsible. So that means that I ultimately is going to have to stop with me even if I only wrote a few of the lines." `[47:27]`

---

## Gaps

- `[NEEDS SOURCE]` "95% of AI pilots fail" statistic cited but source not named `[40:27]`
- `[NEEDS SOURCE]` EW&E mentioned as a good resource on modernization metrics — full name not provided `[20:32]`
- `[NEEDS SOURCE]` Data referenced showing time-to-first-commit drops with Copilot access — no study or link provided `[17:33]`
- `[NEEDS SOURCE]` GitHub permissions for managing AI tools mentioned as newly available — specific feature names not described `[44:55]`
