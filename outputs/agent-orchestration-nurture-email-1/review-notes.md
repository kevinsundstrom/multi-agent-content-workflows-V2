# Review Notes: Agent Orchestration Nurture — Email 1 of 3

**Draft:** `outputs/agent-orchestration-nurture-email-1/draft.md`
**Outline:** `outputs/agent-orchestration-nurture-email-1/outline.md`
**Generated:** 2026-03-03T00:05:48Z

---

## Outline alignment

| Section | Status |
|---------|--------|
| 1. Subject line | ✅ Developed both options (declarative and question); declarative selected — "Your coding agent's failures aren't random" — passes peer-to-peer tone test and prohibited-phrase check |
| 2. Preheader | ✅ "Most teams assume it's a prompting problem. It isn't." — names structural nature of problem without naming the solution |
| 3. Headline | ✅ "Agent failures follow a pattern. Here's what it looks like." — advances past subject line with a direct claim |
| 4. Hero quote | ✅ Fetched from CTA article: "Most multi-agent workflow failures come down to missing structure, not model capability." — the article's lead claim, not from the Matt Nigh interview |
| 5. Primary CTA | ✅ `[Read the engineering breakdown]` — selected after reading the article's engineering focus (schemas, action schemas, MCP) |
| 6. The bridge | ✅ "You've assigned the work. This piece covers the layer underneath — what's actually happening when an agent quietly goes sideways." — connects ebook reader's experience to engineering layer without explaining it |
| 7. The value triad (prose adaptation) | ✅ Two failure modes (misreading of intention, hallucination on integration failure) named in behavioral terms in flowing prose; no bullet points; points toward structural explanation without delivering it |
| 8. The closer | ✅ "The engineering explanation for why they happen is in the article." — forward motion, not a summary |
| 9. Final link | ✅ Omitted per brief override: "One CTA only. No secondary links." |

---

## Sources used

### Knowledge store

| Source | Contribution |
|--------|-------------|
| `knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md` — "Real-Time Steering and Governance" | Primary source for the two failure modes: misreading of intention `[31:15]` and hallucination on integration failure `[32:11]`. Established failure-mode vocabulary used in the value triad prose. |
| `knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md` — "Managers as Agent Managers," "The Async Mindset Shift" | Established the ebook reader's mental model (async delegation, assigning work) — used to calibrate the bridge's "you've assigned the work" framing |
| `knowledge-store/summaries/2026-01-06-matt-nigh-agent-orchestration.md` — "Real-Time Steering and Governance" (bicycle analogy `[45:24]`) | Used as emotional register reference for the closer — "those first five minutes after kickoff" reflects the monitoring anxiety without citing the source or using the analogy directly |

**Note:** Matt Nigh is not named in the draft. No interview quotes appear in the draft. Knowledge store material was used as editorial framing only, per brief instruction.

### First-party sources fetched

| URL | Relevance | Status |
|-----|-----------|--------|
| `https://github.blog/ai-and-ml/generative-ai/multi-agent-workflows-often-fail-heres-how-to-engineer-ones-that-dont/` | CTA destination — hero quote extracted; engineering angle (typed schemas, action schemas, MCP enforcement) used to calibrate bridge and CTA text without excerpting in email body | Fetched ✅ |

---

## Gap inventory

No `[NEEDS SOURCE]` markers appear in the final draft. All outline-flagged gaps were resolved as follows:

| Location | Gap in outline | Resolution |
|----------|---------------|------------|
| Section 4 — Hero quote | Required fetching CTA article | Fetched; selected "Most multi-agent workflow failures come down to missing structure, not model capability." as the article's lead claim |
| Section 5 — Primary CTA text | Required fetching article to match engineering focus | Selected `[Read the engineering breakdown]` after confirming article covers schemas, action schemas, and MCP enforcement |
| Section 6 — Bridge | Required fetching article to write accurately about engineering angle | Wrote bridge to create curiosity about the engineering layer (structural vs. prompting) without explaining or excerpting the article's content |

---

## Editorial flags

**Word count:** Body text (bridge + value triad + closer) is approximately 68 words. Total email copy including headline and hero quote is approximately 115 words. Well within the brief's 300-word limit. If the editor wants to add texture, the value triad prose section has the most room — but each addition should be tested against the 300-word ceiling and the "would a colleague send this" tone check.

**Subject line choice:** Two options were developed per the outline. The declarative form ("Your coding agent's failures aren't random") was selected over the question form ("Why does your coding agent go sideways?") because the body makes a specific behavioral claim about failure patterns, which the declarative subject line sets up more precisely. The editor may prefer the question form — either works for the peer-to-peer tone requirement.

**Hero quote attribution:** The quote "Most multi-agent workflow failures come down to missing structure, not model capability." is the article's lead/lede claim and appears in the article's deck copy (the summary line beneath the headline). It is unattributed in the email body per the skill file's convention for hero quotes; attribution is carried by the CTA link.

**Bridge framing:** The brief's suggested language ("You've assigned the work. Here's what's happening underneath.") was adapted slightly — "Here's what's happening underneath" was replaced with "This piece covers the layer underneath — what's actually happening when an agent quietly goes sideways." This keeps the brief's framing intent while pointing more specifically to the article's subject (why agents go sideways) and avoiding the slightly promotional register of "here's what's happening underneath" as a standalone sentence.

**Failure-mode vocabulary:** The draft uses "misread the intent of the instructions and pursued work you didn't mean" and "hit a failed integration point and made up data rather than stopping to flag the problem" — these are behavioral paraphrases of the misreading-of-intention and hallucination-on-integration-failure patterns from the Matt Nigh interview, translated into reader-experience terms. They do not attribute or cite the interview.

**Closer:** "The engineering explanation for why they happen is in the article." is intentionally minimal — it's an on-ramp, not a second argument. If it feels too abrupt, the editor could lengthen the value triad prose to give the closer more runway.
