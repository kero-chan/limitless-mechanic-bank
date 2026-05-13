# limitless-mechanic-bank

> **Public compositional grammar + asset bank of slot game mechanics for Limitless OS.**
> Consumed by **Chris's AI orchestrator** to replicate, recombine, and merge mechanics into novel slots.
> Status: **v1 in progress** (foundations phase) · Owner: d Fun · AI partner: Comet/GPT-5.5

---

## What this is

A catalogue lists parts. A **grammar** lets you build infinite valid sentences.
This repo is the grammar. Each slot mechanic is expressed as a typed node with:

- **Input/output ports** (game state in, state mutations out)
- **Math contract** (RTP/volatility/hit-frequency/max-win envelope)
- **Presentation contract** (anticipation windows, audio cue family, animation timing)
- **Legal envelope** (TM/patent safe parameter ranges)
- **Evidence** (citations + confidence score)
- **Compose rules** (which mechanics snap into which)

Given a target (e.g. *RTP 96.2%, vol 4/5, mobile-first, TM-clean*), Chris's AI orchestrator queries this bank and back-solves a valid mechanic stack for a new game.

---

## Repo map

```
README.md                 — this file
SPEC.md                   — Mechanic Grammar & Asset Bank Spec v1
RUBRIC.md                 — "Best mechanic" scoring rubric (locked)
CONFIDENCE.md             — Wilson lower-bound formula + tier thresholds
LEGAL_MAP.md              — TM/patent avoid list per jurisdiction
schemas/                  — JSON Schemas (machine contracts)
mechanics/                — one JSON file per mechanic (M-*.json)
games/                    — one JSON file per scrubbed game
providers/                — provider registry
exemplars/                — frame-by-frame teardowns
pilots/PILOT_10.md        — the 10 pilot games + team assignments
handoff/CHRIS_INDEX.md    — single entry-point for Chris's AI
.github/workflows/        — JSON schema validation CI
```

---

## For Chris's AI orchestrator

Start at **[`handoff/CHRIS_INDEX.md`](handoff/CHRIS_INDEX.md)** — single entry point.

Machine-readable consumption:
- Raw JSON: `https://raw.githubusercontent.com/kero-chan/limitless-mechanic-bank/main/mechanics/<ID>.json`
- Schema: `schemas/mechanic.schema.json`
- Versioning: semver tags on releases (`v1.0.0`, `v1.1.0`, ...)

---

## Status banner

⚠️ **v1 is in foundations phase.** Confidence is currently ~55%. Do **not** consume for production game generation until v1.0.0 is tagged. Target: 9 weeks. See `SPEC.md` § Execution Phases.

---

## License

MIT — see [`LICENSE`](LICENSE).
Mechanic descriptions use generic functional language. Branded trademarks (Megaways™, xWays™, xBomb™, InfiniReels™, Splitz™, etc.) are property of their respective owners and listed only as cross-references in `LEGAL_MAP.md`.
