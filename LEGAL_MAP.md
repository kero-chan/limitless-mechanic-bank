# Legal Map — TM / Patent Avoid List (v1 DRAFT)

> ⚠️ **DRAFT.** Not yet reviewed by IP counsel. Treat as working hypothesis until lawyer consult is logged in `meta/legal_review_log.md`.

## Principle
Slot mechanics as functional rules are generally **not copyrightable**. What IS protected: branded names (trademarks), specific code (copyright), and a small number of jurisdiction-specific patents. We catalogue mechanics by **functional description + parameter envelope**, never by branded name.

## Naming policy
- ✅ `M-CASCADE-AVALANCHE-001` (our canonical ID)
- ✅ "symbol-removal cascade with growing global multiplier" (generic functional)
- ❌ "Megaways-style" (TM reference)
- ❌ "xBomb-like" (TM reference)

## Trademark avoid list (do NOT use these terms in mechanic IDs, names, marketing)

| Branded Term | Holder | Jurisdictions (known) | Generic equivalent in our bank |
|---|---|---|---|
| Megaways™ | Big Time Gaming | UK, EU, US | M-GRID-VARIABLE-REELS-001 |
| InfiniReels™ | NetEnt | EU | M-GRID-INFINITE-EXTEND-001 |
| xWays™ | Nolimit City | UK, EU | M-SYMBOL-SPLIT-MULTIWIN-001 |
| xNudge™ | Nolimit City | UK, EU | M-WILD-NUDGE-MULTIPLIER-001 |
| xBomb™ | Nolimit City | UK, EU | M-MULT-EXPLOSIVE-001 |
| xSplit™ | Nolimit City | UK, EU | M-SYMBOL-LATERAL-SPLIT-001 |
| Splitz™ | Yggdrasil | EU | M-SYMBOL-VERTICAL-SPLIT-001 |
| Cluster Pays™ | NetEnt (filed; status varies) | EU | M-WIN-CLUSTER-ADJACENT-001 |
| Hold & Win (variants) | multiple holders | varies | M-RESPIN-LOCK-COIN-001 |
| Lightning Link™ | Aristocrat | AU, US | M-GRID-LIGHTNING-RESPIN-001 |
| Hyperhold™ | Reel Play | EU | M-RESPIN-PERSISTENT-COIN-001 |
| Power Stacks™ | Hacksaw | UK, EU | M-SYMBOL-STACK-EXPAND-001 |

## Patent watch (live patents to verify before Phase 2)
- **Aristocrat:** several active US patents on Hold & Spin variants and Lightning Link mechanics. Check USPTO before any payline-respin module enters Tier S.
- **IGT:** historic patents on cascading reels (mostly expired or limited). Verify expiry dates per mechanic.
- **Scientific Games / Light & Wonder:** active patents on certain bonus-buy structures.

## Process gate
No mechanic enters Tier S (top 10%) without:
1. Generic functional description (no branded terms)
2. Parameter envelope confirmed outside known TM scope
3. Patent search log entry (USPTO / EPO / WIPO)
4. IP counsel sign-off recorded in `meta/legal_review_log.md`

*Last updated: 2026-05-13. DRAFT pending counsel review.*
