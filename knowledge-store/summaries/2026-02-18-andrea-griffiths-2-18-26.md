# Summary: Tim (GitHub), 2026-02-18

**Source:** `knowledge-store/transcripts/2026-02-18-andrea-griffiths-2-18-26.md`
**Interviewee:** Tim (role and surname not stated; discusses GitHub Copilot coding agent on GitHub Checkout, hosted by Andrea Griffiths)
**Date:** 2026-02-18
**Summarized:** 2026-03-06T05:18:08Z

---

## Key Points

### What Copilot Coding Agent Is

- Copilot coding agent is a coding agent like Agent Mode in VS Code or the Copilot CLI, but it runs in the cloud in the background rather than on a local machine `[0:35]`
- Tasks can be assigned via GitHub issues, the GitHub mobile app, VS Code, Slack, Teams integrations, or the Agents panel `[0:57]`
- The compute layer is GitHub Actions — the same infrastructure used for CI/CD `[2:49]`

> "Copilot coding agent is a coding agent just like Agent Mode in VS Code, for example, or the Copilot CLI, but instead of running on your computer with your local repo in your local state, instead it runs in the cloud in the background." `[0:35]`

### The Agents Panel and Model Picker

- The Agents panel is opened via a button in the top-right corner of GitHub and shows a prompt entry field plus a list of recent sessions `[1:14]`
- A model picker was added over the past couple of months; previously Claude Sonnet 4.5 was always used `[1:31]`
- The model picker is available to Copilot Pro and Pro+ users; it is coming to business and enterprise users in the near future `[1:37]`
- Selecting Claude Opus costs three premium requests instead of the standard rate `[1:54]`

> "Before, we always use Claude Sonnet 4.5 when you were using this background coding agent, but now we give you options." `[1:43]`

### Demo: Delegating Background Tasks

- Tim demonstrated assigning "Add comprehensive unit tests with Jest" to Copilot using GPT-5.2-Codex `[2:10]`
- Once a task is delegated, the user can shut their laptop and disconnect from the internet; Copilot delivers a PR when done `[2:28]`
- Startup time is longer than local agents because the cloud environment needs to spin up `[2:45]`
- The agent can run git, run tests, and run a linter within its own development environment `[3:09]`

### Automated Code Review and Security Scanning

- During a background session, Copilot coding agent automatically runs Copilot code review on its own changes before the developer ever sees the code `[3:31]`
- If code review flags an issue (e.g., overly complex string concatenation), the agent takes that feedback and revises its changes before opening the PR `[3:47]`
- GitHub code scanning for security vulnerabilities runs automatically inside Copilot as it works; this is normally part of GitHub Advanced Security but is included free with the coding agent `[4:10]`
- GitHub secret scanning runs to catch accidental commits of API keys or similar credentials `[4:49]`
- Integration with the GitHub Advisory Database checks any newly installed dependency for known vulnerabilities `[5:03]`
- LLMs may recommend outdated dependency versions because training data can be six months to a year old; the Advisory Database integration helps catch this `[5:15]`

> "We give this away for free with Copilot coding agent just because we want to make sure that all the code that we're generating with AI, we want to make sure that's secure." `[4:27]`

> "Yeah, that's right. It all just happens automatically for you without clicking anything. And it's all going on in the background." `[4:42]`

### Custom Agents for Specialized Workflows

- Custom agents are defined by placing files in `.github/agents/` in a repository `[6:08]`
- Tim demonstrated a "Performance Optimizer" custom agent that benchmarks code before making changes, then benchmarks again afterward to measure impact `[6:17]`
- The Performance Optimizer example achieved a reported 99% improvement on the targeted operation `[7:25]`
- Custom agents can also be shared across an entire organization or enterprise, not just a single repo `[8:02]`

> "I've made a 99% improvement of the performance of this code." `[7:25]`

> "Generally I'd say that Copilot coding agent is going to be great for tasks that are small to medium size, and you've got a really good, clear description of what you want. It's not so good if you're confused and you need to make lots of decisions." `[7:38]`

### Copilot CLI: Continuing Cloud Work Locally

- The Copilot CLI is an agent that runs in a terminal, similar to Claude Code or OpenAI Codex, usable with a Copilot subscription `[8:14]`
- From a cloud coding agent session page, a "Continue in Copilot CLI" option copies a command to the clipboard `[8:42]`
- Running that command lets the user tail cloud logs in the terminal or switch into local mode, which checks out Copilot's cloud branch locally `[9:01]`
- When switching to local mode, Copilot retains context of the original prompt and all work it performed in the cloud `[9:23]`

> "Copilot is going to have the context on what I asked it to do originally. So like the message at the top of the thread, the prompt that I gave it, and it's also going to, you know, know about all the work that it did." `[9:25]`

### Delegating Local CLI Work to the Cloud

- Pressing the ampersand key in the Copilot CLI switches the session into "Delegate changes to remote repository mode" `[9:54]`
- In that mode, the user can type a prompt (e.g., "Add CORS headers to allow requests from any origin") and Copilot executes it in the cloud while the user continues working locally `[10:05]`
- Control-N opens a new local session while the cloud task runs `[10:28]`

### Future Roadmap: Private Mode, Planning, and Reporting

- An upcoming feature will let Copilot work privately first; the developer can then review the work before choosing to open a PR or discard it `[10:58]`
- Private mode will enable a planning workflow: ask Copilot to plan work, review the plan, then start coding — currently not possible because a PR opens immediately `[11:21]`
- Future use cases include asking Copilot to search a repository for performance improvements and return a list of ideas for the developer to triage `[11:38]`
- Copilot could generate quarterly work reports by going through a developer's commits in a repository `[12:04]`
- Copilot could summarize open issues in a repository to help maintainers know what to prioritize `[12:17]`
- These reporting/analysis workflows would run in the background without producing a pull request `[12:24]`

> "One thing we're going to be shipping soon is the ability to have Copilot work privately, and then you can choose to open the PR when you're ready." `[10:57]`

---

## Notable Quotes

> "Copilot coding agent is a coding agent just like Agent Mode in VS Code, for example, or the Copilot CLI, but instead of running on your computer with your local repo in your local state, instead it runs in the cloud in the background." `[0:35]`

> "This is exactly the kind of work that I don't like doing, so that's the kind of thing that I want to give Copilot to do for me in the background." `[2:15]`

> "We give this away for free with Copilot coding agent just because we want to make sure that all the code that we're generating with AI, we want to make sure that's secure." `[4:27]`

> "Generally I'd say that Copilot coding agent is going to be great for tasks that are small to medium size, and you've got a really good, clear description of what you want. It's not so good if you're confused and you need to make lots of decisions." `[7:38]`

> "One thing we're going to be shipping soon is the ability to have Copilot work privately, and then you can choose to open the PR when you're ready." `[10:57]`

---

## Gaps

- `[NEEDS SOURCE]` Tim's full name and official role/team at GitHub are never stated in the transcript `[0:00]`
- `[NEEDS SOURCE]` The exact timeline for bringing the model picker to business and enterprise users is only described as "near future" `[1:40]`
- `[NEEDS SOURCE]` The standard premium request cost for non-Opus models is not specified; only Opus is called out as costing three premium requests `[1:54]`
- `[NEEDS SOURCE]` The shipping timeline for the private/planning mode feature is described as "soon" but no date or release is given `[10:57]`
- `[NEEDS SOURCE]` The mechanism for sharing custom agents across an organization or enterprise is mentioned but not demonstrated or explained `[8:02]`
