# Changelog

## 2026-02-27 — Clean build

Started fresh. The initial prototype established the right concepts but accumulated too much complexity and inconsistency. This build starts from a clean architectural brief with all principles reconciled upfront.

Core decisions carried forward:
- Interviews are the only permanent knowledge store input
- First-party sources (GitHub Blog, Docs, Changelog) fetched live at draft time — never stored
- Living documents created only when 2+ interview transcripts cover the same topic
- State agent is the source of truth; idempotent by manifest hash
- Two hard human checkpoints: outline approval, draft editing
