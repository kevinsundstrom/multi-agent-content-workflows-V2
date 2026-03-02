# Coverage Map: Agent Orchestration Nurture — Email 1 of 3

**Brief:** `briefs/agent-orchestration-nurture-email-1/brief.md`
**Generated:** 2026-03-02T06:08:00Z

## Summary

The Matt Nigh interview summary provides strong, direct coverage for the email's core editorial claim — that agent failure is structural, not random — through his firsthand description of misreading-of-intention and hallucination-on-integration-failure as the two primary failure modes. Coverage for the monitoring philosophy and parallel agent risks (the supporting texture) is also solid. The one genuine gap is the engineering layer the CTA article surfaces (typed schemas, action schemas, MCP enforcement); by the brief's design, that content is intentionally withheld from the email body and reserved for the article click.

---

## Coverage by topic area

### Agent failure modes — misreading intention and hallucination

**Coverage:** strong

Matt Nigh names two distinct failure modes explicitly. First, "misreading of intention" — the agent interprets vague instructions and pursues work not aligned with the manager's intent `[31:15]`. Second, hallucination when an integration point (an MCP server or API) fails — the agent fabricates data rather than flagging the error `[32:11]`. Both are described in behavioral terms a manager-audience reader would recognize from lived experience. This is the email's central editorial claim and is well-sourced.

**Knowledge store sources:**
- [`2026-01-06-matt-nigh-agent-orchestration.md`](../../knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md) — "Real-Time Steering and Governance" section directly covers both failure modes with quotes and timestamps

`[NEEDS SOURCE]` The brief connects these failure modes to structural causes (schemas, MCP enforcement) — that evidence lives in the CTA article, which the draft agent should fetch at draft time for editorial framing only. Do not summarize its content in the email.

---

### Structural vs. prompting — why failures happen

**Coverage:** partial

The Matt Nigh summary establishes that failures are not random — they follow recognizable patterns tied to instruction quality and integration reliability. However, the summary does not articulate the structural engineering layer (typed schemas, action schemas, MCP as an enforcement mechanism) that the CTA article covers. The knowledge store supports the "symptoms" side of this angle but not the "root cause" engineering explanation. This is intentional per the brief: the email names the pattern, the article explains the engineering.

**Knowledge store sources:**
- [`2026-01-06-matt-nigh-agent-orchestration.md`](../../knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md) — "Writing Effective Agent Specs" and "Real-Time Steering and Governance" sections establish the relationship between instruction clarity and agent reliability

`[NEEDS SOURCE]` The engineering-layer explanation (typed schemas, action schemas, MCP enforcement) is not in the knowledge store. The draft agent should use the CTA article URL to inform the angle of the bridge sentence pointing readers to the article — but must not summarize or excerpt the article's content in the email body.

---

### Parallel agent risks

**Coverage:** strong

Matt Nigh gives a concrete, quotable rule: "If it's touching the same files, I automatically just won't run parallel agents." `[23:25]` He identifies merge conflicts as the primary risk when two agents modify overlapping files or shared dependency code. This is usable as supporting texture — it illustrates the "structural" nature of failure risk in multi-agent workflows, showing that the problem compounds at scale.

**Knowledge store sources:**
- [`2026-01-06-matt-nigh-agent-orchestration.md`](../../knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md) — "When Not to Run Parallel Agents" section covers merge conflict risk and single-threading guidance

---

### Monitoring philosophy — the 5-minute kickoff window

**Coverage:** strong

Matt Nigh's monitoring philosophy is specific and quotable: watch the agent for about five minutes at kickoff to verify it understood intent and correctly fetched referenced files, then walk away. His analogy — "It's kind of like you have a kid on a bicycle" `[45:24]` — is vivid and peer-to-peer in tone, consistent with the brief's voice requirement. This section provides credible, practical texture for the email without becoming a how-to list.

**Knowledge store sources:**
- [`2026-01-06-matt-nigh-agent-orchestration.md`](../../knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md) — "Real-Time Steering and Governance" section covers the 5-minute window and monitoring philosophy

---

### Engineering layer underneath multi-agent reliability

**Coverage:** none

The knowledge store has no material on typed schemas for data consistency, action schemas for intent clarity, or MCP as an enforcement layer. This is the central content of the CTA article and is intentionally outside the email body's scope. The email should create curiosity about this layer — not explain it.

**Knowledge store sources:** none

`[NEEDS SOURCE]` Draft agent should fetch the CTA article (`https://github.blog/ai-and-ml/generative-ai/multi-agent-workflows-often-fail-heres-how-to-engineer-ones-that-dont/`) at draft time to understand the engineering angle well enough to write a compelling bridge sentence — but must not reproduce or summarize the article's content in the email.

---

### Ebook-to-article bridge framing (CTA setup)

**Coverage:** partial

The ebook themes (async delegation, fleet management, writing specs, monitoring) are well-covered by the Matt Nigh summary. The brief asks the email to position the CTA as: "You've assigned the work. Here's what's happening underneath." The "assigned the work" side is well-sourced. The "what's happening underneath" side requires the CTA article. The bridge is structurally sound but depends on the draft agent correctly reading the article's angle without over-explaining it.

**Knowledge store sources:**
- [`2026-01-06-matt-nigh-agent-orchestration.md`](../../knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md) — "Managers as Agent Managers," "The Async Mindset Shift," and "Managing a Fleet of Agents" sections establish the ebook reader's mental model

---

## First-party sources to fetch at draft time

The draft agent will fetch these live. Do not fetch them now.

### GitHub Blog
- `https://github.blog/ai-and-ml/generative-ai/multi-agent-workflows-often-fail-heres-how-to-engineer-ones-that-dont/` — The CTA destination. Fetch to understand the engineering angle (schemas, MCP enforcement) well enough to write the bridge sentence. Do not summarize in the email body.

### GitHub Changelog
- Copilot coding agent / GitHub Copilot workspace features — Any recent changelog entries that ground the reader's experience with agent reliability issues would add recency signal if needed, though likely not necessary given the brief's scope.

---

## Recommended approach

The knowledge store supports this brief well for what the email actually needs to do: establish a shared failure-mode vocabulary (misreading of intention, hallucination on integration failure) and create curiosity about the engineering layer that explains it. The draft agent should lean heavily on the Matt Nigh failure-modes material for the email body and use the CTA article only to calibrate the bridge sentence — not to excerpt or preview the article's content. The brief's 300-word constraint is the real editorial discipline here: prioritize the two failure modes and the curiosity hook; cut anything that moves toward explaining the engineering answer the article delivers.
