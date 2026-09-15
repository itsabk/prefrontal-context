# DECISIONS.md — decisions that currently stand

Consequential decisions whose rationale a future agent needs: architecture, key dependencies, things we don't do and why. Owner-stated direction and non-goals themselves live in `MEMORY.md`'s Direction section; record here the decisions that follow from them. Not a log — record only what matters now.

- Record what a future agent needs: what was decided, the reasoning and evidence that made it decisive, and when it would be worth revisiting — e.g., "2026-09-07 — Use sqlite, not flat files: single-writer simplicity (load-test notes); revisit if concurrent access is ever needed."
- When a decision is superseded, replace or remove the old entry in the same change, carrying forward any rationale that still matters. Git retains the old text.
- One decision, one entry; reference `MEMORY.md` or `WORK.md` rather than restating content.
- Don't record small implementation or product choices here — if the rationale matters, it belongs in `MEMORY.md`; if it's just history, git has it.
- If an owner remark reads like a decision but was casual or ambiguous, confirm before recording it as standing.

_No decisions recorded yet._
