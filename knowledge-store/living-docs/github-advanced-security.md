# GitHub Advanced Security

> This document synthesizes what interview sources have said about this topic. It is created and maintained by the living document agent. Every claim is sourced. Do not edit directly.

**Topic:** `github-advanced-security`
**Last synthesized:** 2026-03-06T16:17:35Z
**Interview sources:** 2 — see [Source Index](#source-index)

---

## The Security Challenge AI Code Generation Creates

Saif Gunja and Dan Shanahan described a security gap that predates AI: even before AI code generation, the number of vulnerabilities being found was outpacing the number being fixed, and the backlog of security debt was growing. They argued that AI code generation at 10× throughput makes that gap go exponential — framing AI, in the absence of integrated security tooling, as a potential villain.

> "AI is it becoming this villain of this hero and he says, you know, we kind of came up with a story about AI can be the hero where AI, if you bring security earlier into the lifecycle where AI is generating the code, I, you know, security within CCA, you can prevent vulnerabilities from going into the code base in the first place." — Saif Gunja & Dan Shanahan, `[07:32]` · [2026-01-20-saif-gunja-security-thought-leadership.md](../summaries/2026-01-20-saif-gunja-security-thought-leadership.md)

Their counter-narrative: if security is integrated at the point where AI is generating code — rather than applied after the fact — vulnerabilities can be prevented from entering the codebase at all. They described this shift as moving from "AppSec collapse" to "AppSec renaissance."

> "And so what do you go from this appsec collapse to a potential appsec renaissance where you're using AI both to prevent vulnerabilities from getting into your code base right at the start." — Saif Gunja & Dan Shanahan, `[07:41]` · [2026-01-20-saif-gunja-security-thought-leadership.md](../summaries/2026-01-20-saif-gunja-security-thought-leadership.md)

The "secure by default" framing was identified as the narrative with the most resonance for the security persona — a story that operates on multiple levels: embedding security inside the Copilot Coding Agent, embedding security testing inside the pull request process, and enabling developers to remediate existing vulnerabilities.

> "I love that story. I think that it's a really, really good narrative. And I think that that is maybe a little bit different and adds a little bit more an edge than what we'll see from some of the other competitors in this space." — Saif Gunja & Dan Shanahan, `[10:11]` · [2026-01-20-saif-gunja-security-thought-leadership.md](../summaries/2026-01-20-saif-gunja-security-thought-leadership.md)

`[NEEDS SOURCE]` Current state of competitors' (e.g., Claude/Anthropic) integrated security suite capabilities and roadmap — referenced in the interview as a point of differentiation but not characterized in detail.

---

## Security Capabilities Included by Default with Copilot Coding Agent

Both sources describe a set of security capabilities that run automatically inside Copilot Coding Agent (CCA) without requiring a paid GitHub Advanced Security (GHAS) license.

Saif Gunja and Dan Shanahan described this at a category level: when CCA is prompted to make a change, it runs code security, secret protection, and dependency review checks automatically after making the change. They positioned this as a competitive differentiator.

> "We're the only platform that allows you to, that does by default, static analysis, secret detection, and software composition analysis for fully-agemptic AI generated code, yeah." — Saif Gunja & Dan Shanahan, `[16:10]` · [2026-01-20-saif-gunja-security-thought-leadership.md](../summaries/2026-01-20-saif-gunja-security-thought-leadership.md)

Tim (GitHub Checkout, February 2026) provided more specific detail on each capability. He described three distinct checks running inside the coding agent as it works:

1. **GitHub code scanning** — scans for security vulnerabilities. Tim noted this is normally a component of GitHub Advanced Security but is included free with the coding agent. `[4:10]`
2. **GitHub secret scanning** — catches accidental commits of API keys and similar credentials. `[4:49]`
3. **GitHub Advisory Database integration** — checks any newly installed dependency for known vulnerabilities. Tim identified a specific problem this solves: LLMs may recommend outdated dependency versions because their training data can be six months to a year old; the Advisory Database integration catches vulnerable versions the model might otherwise propose. `[5:03]`

Tim also described the agent running Copilot code review on its own changes before the developer ever sees the code — if code review flags an issue (such as overly complex string concatenation), the agent revises its changes before opening the PR. `[3:31]`

All of this happens without requiring any action from the developer.

> "We give this away for free with Copilot coding agent just because we want to make sure that all the code that we're generating with AI, we want to make sure that's secure." — Tim, `[4:27]` · [2026-02-18-andrea-griffiths-2-18-26.md](../summaries/2026-02-18-andrea-griffiths-2-18-26.md)

> "Yeah, that's right. It all just happens automatically for you without clicking anything. And it's all going on in the background." — Tim, `[4:42]` · [2026-02-18-andrea-griffiths-2-18-26.md](../summaries/2026-02-18-andrea-griffiths-2-18-26.md)

Saif Gunja and Dan Shanahan were explicit about the strategic intent of providing these capabilities for free: to drive awareness of GitHub's security tools. The CCA security checks serve as an awareness driver and differentiator for Copilot; the full paid suite covers everything that happens outside of that context.

`[NEEDS SOURCE]` Exact percentage statistics on vulnerability reduction in CCA-generated code after security checks were introduced — referenced in the Saif/Dan interview as existing data but described as potentially "spicy" to publicize and not shared.

---

## What a Paid GHAS License Adds

Saif Gunja and Dan Shanahan drew a clear line between the free CCA security capabilities and the governance capabilities that require a paid license.

Without a paid GHAS license: no ability to block vulnerabilities from merging into main, no cross-organization visibility, no visibility across repositories, and no aggregate finding counts. The free CCA checks are awareness-only — they surface findings but do not enforce policy.

With a paid license: governance rules that block vulnerabilities from merging across an entire environment, bulk visibility, and bulk remediation.

> "It's governance. It's saying hate like I do not want to allow Developers to be able to introduce security vulnerabilities into the main branch of my repository I want to create a rule across my entire environment that prevents this from happening." — Saif Gunja & Dan Shanahan, `[20:14]` · [2026-01-20-saif-gunja-security-thought-leadership.md](../summaries/2026-01-20-saif-gunja-security-thought-leadership.md)

Tim did not address paid GHAS capabilities or the distinction between free and paid tiers.

`[NEEDS SOURCE]` Shadow AI governance — how GitHub's security products interact with non-CCA AI coding agents run through GitHub — was raised by Saif and Dan but not answered.

---

## Bulk Remediation and Security Campaigns

Saif Gunja and Dan Shanahan described security campaigns and bulk remediation — identifying large swaths of existing vulnerabilities and triaging/remediating them with AI assistance — as an "important story to tell." However, they also flagged this narrative thread as a complication: it introduces tension with the "secure by default" framing, which implies code is pristine and clean from the start. How (and whether) to incorporate the bulk remediation story into content was left unresolved in the conversation.

Tim did not address bulk remediation or security campaigns.

`[NEEDS SOURCE]` The specific mechanics of how security campaigns work — how vulnerabilities are identified at scale and how AI assists in remediation — are not described in the available summaries.

---

## What Is Known and Unknown About AI-Generated Code Security

Saif Gunja and Dan Shanahan addressed the underlying empirical question directly: whether AI-generated code is inherently more or less secure than human-generated code. Their position was that this is genuinely unknown.

> "I don't know the truth of AI generated code being more or less secure than human generated code. And I think like to be like really honest with Kevin, I'm not sure that anybody actually does at this point, right?" — Saif Gunja & Dan Shanahan, `[13:49]` · [2026-01-20-saif-gunja-security-thought-leadership.md](../summaries/2026-01-20-saif-gunja-security-thought-leadership.md)

They noted it would be difficult to establish a baseline by going back three years to compare. The recommended framing they offered: AI code generation is happening regardless, so the productive question is how safe your AI-generated code is — not whether to use AI.

Tim did not address the question of AI-generated code security rates or comparisons to human-generated code.

---

## Source Index

| Interview | Interviewee | Date |
|-----------|-------------|------|
| [2026-01-20-saif-gunja-security-thought-leadership.md](../summaries/2026-01-20-saif-gunja-security-thought-leadership.md) | Saif Gunja, PMM, GitHub; Dan Shanahan, Field Services Director, Security Products, GitHub | 2026-01-20 |
| [2026-02-18-andrea-griffiths-2-18-26.md](../summaries/2026-02-18-andrea-griffiths-2-18-26.md) | Tim (surname and role not stated), GitHub; hosted by Andrea Griffiths, GitHub | 2026-02-18 |
