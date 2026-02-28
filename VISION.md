Agentic Content Development System

## What This Is

Most content teams operate on a 1:1 knowledge model: one SME interview produces one piece of content, and then that knowledge disappears. The insight, the context, the specific way that person framed a problem — it lives in a notes doc somewhere, or it's gone entirely.

This system is built on a different premise: that SME knowledge is a durable asset, not a perishable input. Every interview, every conversation, every internal expert perspective gets captured, structured, and made available to every piece of content that follows. The knowledge compounds. The more you feed it, the more powerful it becomes.

At the same time, not everything a writer needs comes from interviews. GitHub produces a continuous stream of first-party content — blog posts, documentation, changelog entries — that is authoritative, public, and almost never systematically incorporated into content research. This system fetches that live at draft time, closing the gap between what GitHub has published and what writers actually know when they sit down to write.

The result is a knowledge store built from human expertise, that serves writers at whatever level of autonomy makes sense for them.

## Two Modes, One System

### Mode 1: Research Assistant

A writer arrives with a topic or a brief. The system surfaces everything the knowledge store knows about that topic — sourced, attributed, organized by coverage strength. It identifies what's well-supported, what's thin, and what's missing entirely. The writer gets a coverage map and a proposed outline, then takes it from there. Their voice, their structure, their judgment — supported by everything the system has aggregated.

This mode fits into any existing editorial workflow. Writers don't have to change how they work. They just start better-informed.

### Mode 2: First Draft Generation

When knowledge store coverage is sufficient, the system goes end to end. Coverage map, outline, draft, review notes — in one automated pass. The writer enters at the editing stage rather than the blank page stage. The draft is grounded in real sources, audited for accuracy before it reaches them, and marked clearly where coverage was thin or gaps remain.

The same pipeline serves both modes. The difference is where the human takes the wheel. Writers can start with Mode 1 and graduate to Mode 2 as the knowledge store matures and their confidence in the system grows.

## The Principles That Make This Work

### 1. Human knowledge and voice are irreplaceable — preserve them exactly

SME interviews are the highest-value input in this system. The way an expert frames a problem, the specific language they use, the nuance in how they describe a tradeoff — that is the raw material that makes content credible and distinctive. The system's job is to preserve that fidelity across every layer of processing.

This means: every key point traces back to a specific timestamp in a specific transcript. Every quote is verbatim. Nothing is paraphrased into a summary and presented as what the person said. If a claim cannot be attributed to a source, it does not enter the knowledge store.

### 2. First-party sources augment — they don't replace — human perspective

GitHub Blog posts, documentation, and changelog entries provide factual grounding, product accuracy, and breadth. They are fetched live at draft time to enrich context. But they are a different kind of source than an interview — they represent what GitHub has published, not what a human expert actually thinks. The system treats them accordingly: useful for facts and context, not for voice or perspective.

### 3. Living knowledge documents are unbiased by design

The knowledge store's living documents represent what sources say — not what any particular content piece wants them to say. If two sources contradict each other, that contradiction is surfaced explicitly, not smoothed over. If coverage is thin, it is marked as thin. If a claim cannot be supported, it is not made.

This is not a limitation — it is the system's primary quality guarantee. A knowledge store that angles toward conclusions is not a knowledge store; it is a bias amplifier. The living documents exist to give writers the real picture, including where that picture is incomplete.

### 4. Gaps are surfaced, never fabricated

When the knowledge store cannot support a section of a draft, that section is marked with a clear gap indicator rather than filled with inference or generalization. Writers see exactly where the sourcing is strong and where it is weak. They decide how to handle it — gather more source material, write around the gap, or acknowledge the limitation. The system never makes that decision for them.

### 5. Human checkpoints are hard stops

The pipeline has two mandatory review gates that cannot be bypassed:

- **Checkpoint 1:** The coverage map and outline require human approval before drafting begins. A human must merge this PR to authorize the draft agent to proceed.
- **Checkpoint 2:** The draft and review notes require human editing before publication. The merged version of the draft is the publication-ready version.

These gates exist because the most important editorial decisions — whether the angle is right, whether the sourcing is sufficient, whether the draft reflects the intended voice — require human judgment. The system handles research and structure; humans handle meaning.

### 6. The system gets smarter over time

Every interview ingested makes the next piece of content easier and better. Coverage that was thin becomes strong. Topics that required human research become automatically supportable. Briefs that previously required gathering new source material can be fulfilled from existing knowledge.

This compounding is the system's long-term value proposition. In the short term, it saves research time. Over time, it creates an organizational knowledge asset that no individual writer or team could build alone.

## The Agent Roster

| Agent | Trigger | What it does |
|-------|---------|--------------|
| Ingestion Agent | New transcript committed | Generates a hierarchical summary with timestamp references, opens a PR for human review |
| State Agent | Summary or living doc committed to main | Reads the full knowledge store, updates STATE.md, manages living document lifecycle |
| Living Document Agent | STATE.md updated | Creates or updates topic-level knowledge documents for topics at threshold |
| Orchestrator | Brief committed | Validates knowledge store, produces coverage map and outline, opens Checkpoint 1 PR |
| Draft Agent | Checkpoint 1 PR merged | Writes draft against approved outline, fetches first-party sources live, opens Checkpoint 2 PR |

## The Knowledge Store

```
knowledge-store/
  transcripts/    # Raw interview transcripts (YYYY-MM-DD-source-name.md)
  summaries/      # AI-generated summaries with timestamp references
  living-docs/    # Topic-level synthesis documents (the primary knowledge asset)
  STATE.md        # System state — maintained by state agent, never edited manually

briefs/           # Human-authored content briefs
outputs/          # Coverage maps, outlines, drafts
```

## What Humans Always Decide

- Whether a summary accurately represents what the source said
- Whether a coverage map correctly assesses knowledge store depth
- Whether an outline reflects the angle and argument they want to make
- Whether a draft is ready for publication
- Whether two living documents should be consolidated into one
- Whether a knowledge gap should be filled before drafting proceeds
