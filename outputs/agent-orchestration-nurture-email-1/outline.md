# Outline: Agent Orchestration Nurture — Email 1 of 3

**Brief:** `briefs/agent-orchestration-nurture-email-1/brief.md`
**Slug:** `agent-orchestration-nurture-email-1`
**Format:** nurture email (under 300 words, single CTA)
**Generated:** 2026-03-02T05:05:22Z

---

## Subject line

**Coverage:** thin
**Sources:** none — brief provides constraints; knowledge store does not contain prior email examples

Write one subject line that creates curiosity about why agent runs are inconsistent without being clickbait. Do not refer to "unlocking" anything. The subject should feel like something a thoughtful practitioner would send — specific enough to feel earned, not generic enough to feel like marketing. Consider using the structural vs. prompting tension as the curiosity hook: the reader has experienced inconsistency and probably blamed the prompt.

`[NEEDS SOURCE]` No prior emails in this sequence to match subject line style to — draft agent should prioritize peer-to-peer register over promotional register.

---

## Opening — name the experience the reader has had

**Coverage:** strong
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — Real-Time Steering and Governance section (failure modes at `[31:15]` and `[32:11]`)

Open in 2–3 sentences that name the experience the reader already has: they've assigned work to an agent and sometimes it came back exactly right, sometimes it went sideways in ways that felt hard to predict. Do not explain the cause yet. The job of the opening is recognition — the reader should feel that whoever wrote this email has seen what they've seen.

Do not cite Matt Nigh by name or reference the ebook explicitly. Write as if this is the writer's own observation.

---

## The turn — it's not the prompt

**Coverage:** partial
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — failure mode descriptions provide the evidence; the structural argument must be inferred from the MCP hallucination example

This is the email's core move: the reader probably assumes inconsistency is a prompting problem. Name that assumption and redirect it. The failure patterns Matt Nigh describes — agents "misreading intention" when instructions are ambiguous, agents hallucinating when an integration point fails rather than flagging the failure — are the evidence that the failure is structural, not just a matter of writing better prompts.

Use one specific failure mode, not both. The MCP/integration failure → hallucination example is the stronger choice because it is counterintuitive: the agent didn't fail because of the prompt. It failed because the structure allowed it to continue when it should have stopped. Keep this paragraph to 3–4 sentences. Do not explain the fix — that lives in the article.

`[NEEDS SOURCE]` Draft agent should read the CTA article before writing this section to ensure the structural framing here aligns with what the article argues — the email needs to create curiosity about the article's actual argument, not a generic version of it.

---

## The bridge — from the ebook to the engineering layer

**Coverage:** strong
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — Managers as Agent Managers section; When Not to Run Parallel Agents section

One sentence that connects the ebook experience (workflow, delegation, async mindset) to the engineering layer this email is pointing toward. The brief's framing is exact: "You've assigned the work. Here's what's happening underneath." This sentence should feel like the natural next step — not a sales pivot. It earns the CTA by making the reader feel that clicking is their idea.

Do not introduce new concepts here. This is a bridge, not a new section.

---

## CTA

**Coverage:** strong (format constraint from brief; article URL provided)
**Sources:** Brief provides the URL and framing direction

One sentence introducing the link. Follow the brief's guidance: connect the reader's ebook experience (manager workflow) to the engineering insight in the article. Then the link. No secondary links. No additional framing after the link.

Link text should be descriptive of what the reader will get, not generic ("read more," "learn more"). Something that names the engineering-layer argument.

---

## Sections omitted due to coverage gaps

**Parallel agent merge conflict risks** — the knowledge store covers this well (Matt Nigh's rule: "if it's touching the same files, I automatically just won't run parallel agents"), but the email's angle is structural failure modes at the engineering layer, not fleet management tactics. Including parallel agents would dilute the single editorial move this email needs to make. It belongs in email 2 or 3 if the sequence develops that direction.

**Monitoring / 5-minute kickoff window** — strong coverage in the knowledge store and a strong analogy (bicycle), but this is a management behavior tactic, not the structural engineering insight the email is building toward. Including it would shift the email's register from "here's something you didn't know" to "here's another tip." Reserve for a future email.

**Reliability at scale** — the brief names this as a key question, but the email's job is to plant the question, not answer it. The coverage is partial and the answer lives in the CTA article. Do not attempt to address this in the body.

---

## Notes for the draft agent

- **Tone:** Peer-to-peer, not marketing. Write as if from someone who works on this every day. No hedging, no hype. Matt Nigh's voice in the interview — practical, grounded, specific — is a useful register reference.
- **Length:** Under 300 words in the body. This is a hard constraint. Be ruthless about cutting.
- **Prohibited words/constructions:** Do not use "unlock" or "leverage." No numbered lists. No tips-style structure.
- **The structural argument:** Do not over-explain it. The email's job is to name the structural nature of the problem, not to teach the engineering fix. The article does that. Create curiosity; do not satisfy it.
- **Matt Nigh attribution:** Do not name him in the email. The knowledge comes from the ebook experience and the writer's own framing.
- **The CTA article:** Read it before writing — https://github.blog/ai-and-ml/generative-ai/multi-agent-workflows-often-fail-heres-how-to-engineer-ones-that-dont/ — so the turn in the email body points toward the article's actual argument (typed schemas, action schemas, MCP as enforcement) rather than a generic version of it.
- **One CTA only.** No secondary links, no PS with a resource, no "also check out."
- **Subject line:** Write one subject line. Treat it as copy, not a placeholder.
