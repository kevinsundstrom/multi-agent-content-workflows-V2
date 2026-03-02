# Outline: Agent Orchestration Nurture — Email 1 of 3

**Brief:** `briefs/agent-orchestration-nurture-email-1/brief.md`
**Slug:** `agent-orchestration-nurture-email-1`
**Format:** nurture email (single, under 300 words)
**Generated:** 2026-03-02T06:08:00Z

---

## Subject line

**Coverage:** partial
**Sources:** brief constraints only — no knowledge store source applies

The subject line must create curiosity without clickbait. It should name the problem space (agent inconsistency) without revealing the answer (structural causes). Options to explore: a question that the reader has silently asked themselves, or a declarative that names the pattern without explaining it.

`[NEEDS SOURCE]` Draft agent should test subject line options against the brief's prohibition on clickbait and the peer-to-peer tone requirement. Avoid: "5 reasons," superlatives, urgency language.

---

## Opening — name the reader's lived experience

**Coverage:** strong
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — "Real-Time Steering and Governance" section

One to two sentences. The reader has used Copilot's coding agent. They've seen it work well — and they've seen it go sideways. The opening doesn't explain why yet; it mirrors the experience back to them accurately enough that they feel recognized. The tone is peer-to-peer, as if written by someone who has run agents themselves.

Draw on the failure pattern Matt Nigh describes — agents that "misread intention" or that fabricate results when an integration fails — as the experiential reference point. Do not cite Matt Nigh or the interview. Write from the pattern, not the source.

---

## The pivot — it's structural, not the model

**Coverage:** partial
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — "Real-Time Steering and Governance," "When Not to Run Parallel Agents"

Two to three sentences. This is the email's central editorial move: the reader's inconsistency isn't random, and it isn't a model quality problem. The failure is predictable once you understand the structure underneath. This section plants the question — "what structure?" — without answering it. That's the article's job.

Use Matt Nigh's failure-mode vocabulary (misreading of intention, hallucination on integration failure, merge conflict risk in parallel agents) to make the claim feel grounded and specific, not abstract. Do not use jargon from the CTA article (no mention of typed schemas, action schemas, or MCP enforcement).

`[NEEDS SOURCE]` The draft agent should fetch the CTA article to internalize the engineering angle, then deliberately withhold it from this section — the withholding is the editorial strategy.

---

## The bridge — from ebook to engineering layer

**Coverage:** partial
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — "Managers as Agent Managers," "The Async Mindset Shift"; CTA article (fetch at draft time)

One to two sentences. The ebook gave the reader the manager workflow: how to assign work, write specs, monitor at kickoff, review outputs. This sentence connects that workflow to the engineering layer underneath it — without explaining what that layer is. The CTA article frames it for engineers; this sentence tells the manager-audience reader why it's worth their time.

The brief's suggested framing: "You've assigned the work. Here's what's happening underneath." The draft agent should adapt this to match the tone established in the opening — it should not feel like a gear-shift from editorial to promotional.

---

## CTA

**Coverage:** strong (by brief design)
**Sources:** brief; CTA article URL

One sentence plus a link. The CTA should feel like a natural next step, not an advertisement. It should point the reader toward the article without summarizing it — the email's job is to make them curious enough to click, not to pre-answer the question.

Brief constraint: one CTA only. No secondary links.

`[NEEDS SOURCE]` Draft agent fetches: `https://github.blog/ai-and-ml/generative-ai/multi-agent-workflows-often-fail-heres-how-to-engineer-ones-that-dont/` — the anchor text and framing sentence should match the article's actual engineering focus (don't promise what the article doesn't deliver).

---

## Sections omitted due to coverage gaps

**Engineering layer explanation (typed schemas, action schemas, MCP enforcement):** The knowledge store has no material on this. The brief explicitly designates this as the CTA article's territory. Omitting from the email body is correct — not a gap in execution.

**Review workflow and self-correction mechanics:** Matt Nigh covers this in the summary (session log, PR comments, playwright tests), but it is out of scope for this email. The brief's angle is failure causes, not the review process. Omitted to maintain word-count discipline.

**Ebook recap:** No recap of ebook content. The reader has already received it. The email should advance past it, not re-summarize it.

---

## Notes for the draft agent

- **Word count is the constraint.** Under 300 words for the body means approximately: 2-sentence opening, 3-sentence pivot, 2-sentence bridge, 1-sentence CTA. Every word must earn its place.
- **Tone check:** Read every sentence aloud. If it sounds like a marketing email, rewrite it. The brief asks for peer-to-peer — as if from someone who works on this every day, not someone selling it.
- **Do not name Matt Nigh or reference the interview.** The failure-mode vocabulary is editorial input, not a citation to include in the email.
- **Do not use "unlock" or "leverage."** Per brief constraints. Also avoid: "game-changing," "powerful," "exciting," "seamless."
- **No numbered list.** The brief prohibits a listicle format. The pivot section may describe failure modes in prose but must not itemize them as a list.
- **Fetch the CTA article before drafting.** Read it enough to write the bridge sentence accurately — then deliberately leave the engineering content out of the email body.
- **Subject line:** Draft at least two options. One question form, one declarative form. Both should pass the "would a peer send this?" test.
- **Key quote to internalize (but not use verbatim):** Matt Nigh — "It's kind of like you have a kid on a bicycle. And once you get them up on the bike and once you see them moving, they're fine, but you want to stand there and watch them get on that bike." `[45:24]` — This captures the manager's monitoring anxiety that the email should speak to without over-explaining.
