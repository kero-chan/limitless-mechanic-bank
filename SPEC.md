# Mechanic Grammar & Asset Bank — SPEC v1

**Status:** IN PROGRESS (target lock: 2026-05-20)
**Owner:** d Fun (Xtekcal@gmail.com)
**AI partner:** Comet/GPT-5.5
**Replaces:** Knowledge Bank v1 (Google Doc) as source-of-truth contract for Chris's AI orchestrator.

---

## 1. Purpose

Give Chris's AI orchestrator a **compositional grammar** (not a catalogue) of slot mechanics so it can replicate, recombine, and merge mechanics into novel, mathematically valid, legally safe, dopamine-tuned slots.

**Core insight:** a catalogue lists parts; a grammar lets you build infinite valid sentences. We are building the grammar.

---

## 2. The 7 Pillars

### Pillar 1 — Mechanic Grammar (type system)
Each mechanic is a typed node with:
- **Input ports:** grid_state, symbol_set, win_event, multiplier_stack, free_spin_counter, bonus_state, rng_seed
- **Output ports:** symbol_mutation, multiplier_delta, trigger_event, state_mutation, presentation_cue
- **Side effects:** rtp_delta, vol_delta, hit_freq_delta, session_length_delta, max_win_cap_interaction
- **Compose rules:** port-type matching, dependency graph, incompatibility list

### Pillar 2 — Math Layer (formal contracts)
- rtp_contribution(params) → [min, max]
- volatility_class_shift ∈ [-2, +2]
- hit_frequency_delta (multiplicative)
- max_win_cap_interaction (additive | multiplicative | replacing)
- distribution_shape (long_tail | clumped | uniform | bimodal)

Enables Chris's AI to target an RTP/vol envelope and back-solve mechanic combinations.

### Pillar 3 — Presentation / Dopamine Layer
- anticipation_window_ms: [min, max]
- audio_cue_family: rising_tension | win_release | near_miss_pause | bonus_summon
- animation_timing per state-transition
- Frame-by-frame teardowns in `exemplars/`

### Pillar 4 — Evidence Layer (immutable citations)
Every claim ties to provider_source, video_evidence, confidence_score (Wilson), reviewer_id + review_date.

### Pillar 5 — Legal Layer (TM/patent map)
- TM avoid list per jurisdiction (Megaways™, xWays™, xNudge™, xBomb™, InfiniReels™, Splitz™, etc.)
- Active patent search per mechanic (Aristocrat / IGT / Scientific Games)
- Generic safe-naming: M-CASCADE-AVALANCHE-001, never "Megaways-style"
- **Gate:** 30-min IP lawyer consult before Phase 2.

### Pillar 6 — Chris's AI Interface Contract
- JSON schema co-designed with Chris (not guessed)
- Read path: raw GitHub URLs against `mechanics/`, `games/`, `providers/`
- Query patterns: "give me 5 mechanics composing into RTP 96.2, vol 4, mobile-first, TM-clean"
- **Gate:** 45-min Chris sync before Phase 1 lock.

### Pillar 7 — Continuous Ingestion Loop
Weekly cron: new releases from top 20 providers. LLM first-pass → human QA. Confidence scores auto-update.

---

## 3. Execution Phases & Confidence Targets

| Phase | Window | Target Conf | Output |
|---|---|---|---|
| 0 — Foundations | D1–D5 | 75% | Grammar v1, Math Contract v1, Legal Map v1, Chris sync done |
| 1 — Pilot 10 games | Week 2 | 82% | Full pipeline. Gate: test-slot math ±2% RTP |
| 2 — Scale corpus | Weeks 3–8 | 88% | 20 Tier-1 fan-outs + 60 scrubs + math/presentation extraction |
| 3 — Integration + loop | Week 9 | 90%+ | handoff/CHRIS_INDEX.md live, continuous ingestion on |

---

## 4. Open Blockers

1. Chris orchestrator input contract — awaiting sync.
2. IP lawyer engagement — not booked.
3. Math designer consultant — not sourced.
4. Data source ToS audit — SlotsLaunch, BigWinBoard, SlotCatalog.

---

*Last updated: 2026-05-13 (Amsterdam, CEST)*
