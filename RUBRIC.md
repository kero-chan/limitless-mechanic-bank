# "Best Mechanic" Scoring Rubric — v1 (LOCKED 2026-05-13)

Defines how every mechanic in this bank is scored. Score determines tier-A/B/C inclusion priority and surfaces top candidates for Chris's AI orchestrator composition queries.

## Weighted composite (0–1.0)

| Axis | Weight | What it measures |
|---|---|---|
| Composability | 30% | How many other mechanics this one cleanly snaps into (graph degree on compose-rules) |
| Player engagement | 25% | Retention signal from review aggregates + scrub session-length data |
| Math flexibility | 20% | Width of RTP/vol envelope achievable while keeping mechanic intact |
| Dopamine yield | 15% | Anticipation strength × release satisfaction (from `exemplars/`) |
| TM/patent safety | 10% | Availability of generic parameter envelope provably outside active TM/patent claims |

## Formula
score = 0.30*C + 0.25*E + 0.20*M + 0.15*D + 0.10*L
where each axis is normalized to [0, 1].

## Tier thresholds
- **Tier S (top 10%):** score ≥ 0.85 — default candidates for Chris's AI compositions
- **Tier A (next 25%):** 0.70 ≤ score < 0.85
- **Tier B (next 35%):** 0.55 ≤ score < 0.70
- **Tier C (rest):** score < 0.55 — catalogued, not recommended

## Review cadence
Re-score quarterly or when evidence count increases by ≥50%.

*Locked 2026-05-13. Changes require version bump + changelog entry.*
