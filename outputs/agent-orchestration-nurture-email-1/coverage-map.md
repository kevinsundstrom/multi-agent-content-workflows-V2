# Coverage Map: Agent Orchestration Nurture — Email 1 of 3

**Brief:** `briefs/agent-orchestration-nurture-email-1/brief.md`
**Generated:** 2026-03-02T05:05:22Z

## Summary

The Matt Nigh summary directly supports the core editorial content this email needs: specific failure modes (misreading intention, hallucination on failed integrations) and the monitoring philosophy that connects those failure modes to actionable manager behavior. The structural framing — that failure is an engineering-layer problem, not a model problem — is implied by the evidence in the knowledge store but not stated explicitly; that argument lives in the CTA article, which the email points to rather than summarizes. The app modernization interview is not relevant to this brief.

---

## Coverage by topic area

### Agent failure modes — misreading intention and hallucination

**Coverage:** strong

Matt Nigh names both primary failure modes directly and specifically. "Misreading of intention" occurs when instructions are vague and the agent pursues work not aligned with the manager's intent `[31:15]`. Hallucination occurs specifically when an integration point — an MCP server or API — fails and the agent fabricates data rather than flagging the failure `[32:11]`. These are the exact failure patterns the brief asks the email to name.

**Knowledge store sources:**
- [`2026-01-06-matt-nigh-agent-orchestration.md`](../../knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md) — Real-Time Steering and Governance section provides direct quotes and timestamps for both failure modes

`[NEEDS SOURCE]` The GitHub Blog article at the CTA URL covers the structural explanation (typed schemas, action schemas, MCP as enforcement layer) — draft agent should read this article to understand the engineering-layer argument, but should not summarize it in the email body.

### Structural vs. prompting framing

**Coverage:** partial

The knowledge store establishes that failure modes exist and describes them behaviorally, but does not explicitly frame the distinction between "this is a prompting problem" and "this is a structural problem." The evidence is present — the MCP hallucination example implies structural failure — but the argument that it's architecture, not prompting, is the angle the brief wants the email to plant. That argument is what the CTA article makes, not the knowledge store.

**Knowledge store sources:**
- [`2026-01-06-matt-nigh-agent-orchestration.md`](../../knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md) — failure mode descriptions provide the evidence; the structural framing must be inferred from the hallucination-on-integration-failure example

`[NEEDS SOURCE]` Draft agent should read the CTA article (https://github.blog/ai-and-ml/generative-ai/multi-agent-workflows-often-fail-heres-how-to-engineer-ones-that-dont/) to understand the structural argument before writing — the email's job is to make the reader curious about that article, which requires understanding what it argues.

### Parallel agent risks at scale

**Coverage:** strong

Matt Nigh covers this concisely: the primary risk is merge conflicts when agents touch the same files or shared dependency code `[22:39]`. His rule — "if it's touching the same files, I automatically just won't run parallel agents" `[23:25]` — is specific and quotable. The brief mentions this as a relevant area for the audience of managers running fleets of agents.

**Knowledge store sources:**
- [`2026-01-06-matt-nigh-agent-orchestration.md`](../../knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md) — When Not to Run Parallel Agents section

`[NEEDS SOURCE]` No data on how often parallel agent conflicts actually occur in practice — the email doesn't need this, but a future piece might.

### Monitoring philosophy — the 5-minute kickoff window

**Coverage:** strong

Matt Nigh's bicycle analogy and the 5-minute kickoff recommendation are directly usable editorial material. "It's kind of like you have a kid on a bicycle. And once you get them up on the bike and once you see them moving, they're fine, but you want to stand there and watch them get on that bike." `[45:24]` The recommended window is approximately five minutes at kickoff to verify the agent understood intent and correctly fetched referenced files `[45:55]`.

**Knowledge store sources:**
- [`2026-01-06-matt-nigh-agent-orchestration.md`](../../knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md) — Real-Time Steering and Governance section and Review Workflow section

### Reliability at scale — what managers should care about

**Coverage:** partial

The knowledge store covers the individual failure modes and one mitigation (monitoring window) but does not address reliability at scale systematically. There is useful supporting material: the fleet management section (custom agents per repo, sub-issues) and the use case validation section (monoliths are the weakest use case, scale investment with complexity) provide context, but none of this is framed as a reliability engineering argument. The email needs to gesture at this question without answering it — the CTA article is where the answer lives.

**Knowledge store sources:**
- [`2026-01-06-matt-nigh-agent-orchestration.md`](../../knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md) — Managing a Fleet of Agents section; Use Case Validation section

`[NEEDS SOURCE]` No knowledge store material on what reliability looks like at team scale — percentage of successful runs, tooling patterns, organizational practices. The brief does not require this to be answered in the email, only raised as a question.

### Email format — peer-to-peer tone, under 300 words, one CTA

**Coverage:** none

The knowledge store does not contain email copy, tone guidelines, or format examples. The brief provides all necessary format constraints. The Matt Nigh interview voice — practical, specific, grounded in real use — should inform tone, but the format execution is entirely brief-driven.

**Knowledge store sources:** none

`[NEEDS SOURCE]` Prior email examples in this nurture sequence (emails 2 and 3) would help establish voice consistency — not available yet since this is email 1.

---

## First-party sources to fetch at draft time

The draft agent will fetch these live. Do not fetch them now.

### GitHub Blog
- https://github.blog/ai-and-ml/generative-ai/multi-agent-workflows-often-fail-heres-how-to-engineer-ones-that-dont/ — The CTA destination article; draft agent must read this to understand what structural argument the email is pointing readers toward (without summarizing it)

### GitHub Docs
- GitHub Copilot coding agent documentation — confirm current product name and any specific language around how agents handle integration failures

### GitHub Changelog
- Copilot coding agent — any recent changes to how agents handle MCP server failures or tool call errors would be relevant context for the structural argument

---

## Recommended approach

The knowledge store is well-matched to the email's editorial core: the Matt Nigh interview provides direct, specific, quotable material on both failure modes the brief wants to name. The brief is appropriately scoped — it does not ask the email to explain the structural fix, only to name the structural nature of the problem and point to where the answer lives. The draft agent should read the CTA article before writing to ensure the email's framing creates genuine curiosity about what the article argues, rather than pointing to it generically. No additional interviews are needed for this email; the Matt Nigh material is sufficient for a 300-word piece. The parallel agent section is available but should be used sparingly — the email's angle is failure modes and structure, not fleet management tactics.
