# Outline: Agent Orchestration Nurture — Email 1 of 3

**Brief:** `briefs/agent-orchestration-nurture-email-1/brief.md`
**Slug:** `agent-orchestration-nurture-email-1`
**Format:** nurture email (single, under 300 words)
**Generated:** 2026-03-02T22:53:18Z

---

## 1. Subject line

**Coverage:** partial
**Sources:** Brief constraints; `2026-01-06-matt-nigh-agent-orchestration.md` for failure-mode vocabulary

Sentence case. Creates curiosity about agent inconsistency without being clickbait. The reader has experienced an agent going sideways — the subject line names that experience without explaining it. Must pass the "would a peer send this?" test.

Two options for the draft agent to develop:
- Declarative: "Your coding agent's failures aren't random"
- Question: "Why does your coding agent go sideways?"

`[NEEDS SOURCE]` Draft agent tests both forms against the brief's peer-to-peer tone requirement and prohibited phrases (no urgency language, no superlatives).

---

## 2. Preheader

**Coverage:** partial
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — "Real-Time Steering and Governance"

One sentence. Expands the subject line — adds the editorial angle that agent inconsistency is structural rather than random. Appears alongside the subject line in email clients; write it knowing both will be read together.

Direction: the preheader names the structural nature of the problem without naming the solution. Example register: "Most teams assume it's a prompting problem. It isn't."

---

## 3. Headline

**Coverage:** strong
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — "Real-Time Steering and Governance"

Sentence case. Advances past the subject line — makes a direct claim, not a teaser. The Matt Nigh failure-mode vocabulary (misreading of intention, hallucination on integration failure) is the raw material. The headline names the pattern without citing the source or explaining its cause.

---

## 4. Hero quote

**Coverage:** none (must come from CTA destination)
**Sources:** CTA article — fetch at draft time

A single, high-impact quote from the CTA article. Must come from the article (`https://github.blog/ai-and-ml/generative-ai/multi-agent-workflows-often-fail-heres-how-to-engineer-ones-that-dont/`), not from the Matt Nigh interview. No attribution required in the email body.

`[NEEDS SOURCE]` Draft agent fetches the CTA article to identify the one line that best captures the article's central claim about structural failure. This quote is the emotional and intellectual peak of the email — the payoff for the subject line's promise.

---

## 5. Primary CTA

**Coverage:** strong (by brief design)
**Sources:** Brief (CTA URL provided)

Short action in brackets. No punctuation inside. Appears above the body copy as the above-the-fold action for readers who don't scroll.

CTA framing connects the ebook reader's experience (assigned the work) to the engineering insight in the article (what's happening underneath). Must not summarize the article.

`[NEEDS SOURCE]` Draft agent selects CTA text after fetching the article — text should match the article's actual engineering focus. Options: `[Read the analysis]`, `[Read the engineering breakdown]`.

---

## 6. The bridge

**Coverage:** partial
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — "Managers as Agent Managers," "The Async Mindset Shift"; CTA article (fetch at draft time)

One to two sentences. Connects the headline and hero quote to why this article matters to this specific reader. The ebook gave them the manager workflow; this article gives them the engineering layer underneath. The bridge does not explain the engineering — it creates the gap the article fills.

The brief's suggested framing: "You've assigned the work. Here's what's happening underneath." Adapt to match the established tone — peer-to-peer, not promotional.

`[NEEDS SOURCE]` Draft agent fetches the CTA article to understand the engineering angle (typed schemas, action schemas, MCP enforcement) well enough to write this sentence accurately — then deliberately withholds it from the email body.

---

## 7. The value triad — prose adaptation

**Coverage:** partial
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — "Real-Time Steering and Governance," "When Not to Run Parallel Agents," "Writing Effective Agent Specs"

**Brief override:** The brief prohibits numbered lists and listicle format ("No numbered list of tips. This is a short editorial email, not a listicle."). The three ideas from the value triad should be expressed in flowing prose rather than bullet points, while still covering: (1) what the reader will understand, (2) the problem it names, and (3) the outcome or strategy.

In prose form: name the failure patterns (misreading of intention, hallucination on integration failure) in behavioral terms the reader recognizes from lived experience. Two to three sentences. Point toward the structural explanation without delivering it.

**Word count note:** Brief specifies under 300 words for the full body — overriding the skill file's 150-word limit. The additional headroom belongs here and in the bridge, not in any single section.

---

## 8. The closer

**Coverage:** strong
**Sources:** `2026-01-06-matt-nigh-agent-orchestration.md` — "Real-Time Steering and Governance"

One short sentence. Forward motion — not a summary. Transitions from the named failure patterns to the action (reading the article).

Matt Nigh's monitoring philosophy — the 5-minute kickoff window, the bicycle analogy `[45:24]` — establishes the emotional register: the manager's anxiety when an agent starts. The closer should speak to that tension without over-explaining it. It is the on-ramp to the CTA, not a second argument.

---

## 9. Final link

**Coverage:** N/A

**Brief override:** Brief specifies "One CTA only. No secondary links." Element 9 (final link) is omitted. The primary CTA button (element 5) is the sole link in this email.

---

## Sections omitted due to coverage gaps

**Engineering layer (typed schemas, action schemas, MCP enforcement):** The knowledge store has no material on this. Per the brief's design, this content belongs to the CTA article, not the email body. Intentionally omitted.

**Ebook recap:** No recap of ebook content. The reader already received the ebook. The email advances past it.

**Parallel agent merge conflict detail:** Matt Nigh's specific single-threading guidance (`[23:25]`) is relevant supporting texture but too granular for a sub-300-word email. The two primary failure modes (misreading of intention, hallucination on integration failure) are sufficient without this detail.

---

## Notes for the draft agent

- **Word count:** Under 300 words for the full body — brief override of the skill file's 150-word limit. Allocate approximately 1–2 sentences per section; every sentence must earn its place.
- **No bullet points or numbered lists.** The brief prohibits listicle format. Element 7 (the value triad) must be expressed in prose.
- **One CTA only.** No secondary links. Element 9 (final link) is omitted per brief constraint.
- **Hero quote must come from the CTA article**, not the Matt Nigh interview. Fetch the article before drafting.
- **Do not name Matt Nigh or reference the interview.** Failure-mode vocabulary is editorial input for the writer, not a citation to include in the email.
- **Banned words:** unlock, leverage, game-changing, powerful, exciting, seamless (skill file). Also per brief: no urgency language, no superlatives, no numbered list of tips.
- **Tone check:** Every sentence should pass — "Would a colleague working on this every day send this?" If it sounds promotional, rewrite it.
- **Key internalize-but-don't-use:** Matt Nigh's bicycle analogy `[45:24]` — captures the monitoring anxiety without explaining it. Use as emotional register reference, not as a verbatim quote.
- **Draft the subject line last.** After the body is written, return to the subject line to ensure it matches the specific claim the email makes rather than a generic version of the topic.
