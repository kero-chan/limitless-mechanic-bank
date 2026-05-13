# Confidence Scoring — v1 (LOCKED 2026-05-13)

Every mechanic carries a `confidence` field in [0, 1]. Computed via Wilson lower-bound on weighted evidence.

## Formula
```
confidence = wilson_lower_bound(
    successes = sum(evidence_quality_weights),
    n = sum(possible_evidence_slots),
    z = 1.96   # 95% CI
)
```

## Evidence quality weights
| Source | Weight |
|---|---|
| Provider paytable PDF | 1.0 |
| Provider math whitepaper | 1.0 |
| Regulator filing (UKGC, MGA, etc.) | 1.0 |
| Video scrub ≥100 spins | 0.7 |
| Video scrub <100 spins | 0.3 |
| Review aggregate (3+ sources) | 0.4 |
| Secondary blog/wiki | 0.2 |

## Tier thresholds
- **Tier A primitives** (grid, payline, scatter): require ≥0.85
- **Tier B/C** (modifiers, triggers): require ≥0.70
- **Tier D/E** (math envelope, presentation): require ≥0.60

Mechanics below threshold are catalogued but flagged `do_not_recommend: true` in their JSON and excluded from Chris's AI default composition queries.

## Refresh policy
Confidence recomputes on every new evidence commit affecting that mechanic. CI runs the recompute via `.github/workflows/validate.yml`.
