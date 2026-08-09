# PC Build & Min-Max Plan

## Goal
Min-max the budget for a wood-accented build across a trusted trio of
Sim Lim Square shops, buying from as few stores as possible.

## Extracted Data (persisted in `price-data/`)
- `bizgram.txt` + `dynacore.txt` — the two shop PDFs (user copied into this folder too).
- `pcthemes.txt` / `pcthemes.pdf` / `pcthemes-png/` — PC Themes scanned list, OCR + per-page TSVs.
- `tier1.csv` — SPL PSU Tier List.
- Working copies live in `/tmp/opencode`; `price-data/` is the durable snapshot.

## Preferred Build (current)
| Part | Pick | Note |
|---|---|---|
| CPU + Mobo | Ryzen 7 9800X3D + MSI B850M Mortar WIFI (bundle) | **$1023 PCT** / $969 Biz / $898 Dyna |
| GPU | Asus ProArt RTX 5070 Ti 16GB | $1,819 Dyna / $1,999 Biz — haggle toward $1,700; alternates below |
| Cooler | DeepCool AK620 G2 (wood accent) | $80 Biz |
| RAM | **Team T-Create Expert 6000 CL30 32GB (non-RGB)** | **$639 Dyna** — low-profile (~36mm), fits under AK620 43mm default, no fan mod, has EXPO profile |
| SSD | Crucial T500 2TB (DRAM, Gen4) | $569 Dyna |
| PSU | Seasonic Focus GX-850W V4 (ATX 3.1) | $209 Dyna, SPL Tier A |
| **Fans** | **Arctic P12 Pro A-RGB ×9** — 5 reverse (bottom 3 + front 2) intake, 4 normal (top 3 + rear 1) exhaust | **$25 ea × 9 = $225 Biz** |
| Case | Jonsbo D33 Black Wood | not on list (~$135, ask) |
| **Baseline total (old fans)** | | **~$4,402** |
| **New total (T-Create + Arctic 9-fan, all-ARGB)** | | **~$4,574** |
| Mixed fans (5 ARGB + 4 PST) | | **~$4,542** |

## Price Comparison Matrix (Aug 2026 lists)
| Part | Bizgram | Dynacore | PC Themes | Winner |
|---|---|---|---|---|
| 9800X3D + MSI Mortar (bundle) | $969 | **$898** | $1,023 | Dyna (−$71) |
| 9800X3D + MSI Mortar (split) | — | — | board 364 + CPU (see matrix) | |
| Asus ProArt 5070 Ti 16G | $1,999 | **$1,819** | ProArt not listed (cheapest 5070 Ti: GALAX EX Gamer $1370, Windforce $1499; Prime Ti 1699) | Dyna |
| GPU save-alternates (fit wood look) | — | Prime 5070 Ti **PROMO** (ask) | Palit Gaming Pro S 16G **$1,629** · TUF $1,989 · Prime $1,899 | Biz (Palit) |
| DeepCool AK620 G2 | **$80** | not listed | — | Biz |
| Team T-Force Delta RGB 6000 CL30 (old pick) | — | $679 | — | dropped — 46.1mm needs fan mod |
| **Team T-Create Expert 6000 CL30 (non-RGB)** | $679 | **$639** | — | Dyna — low-profile, EXPO |
| Corsair Vengeance RGB 6000 CL30 | — | $789 | — | Dyna |
| Crucial T500 2TB | $349 (T500/MP441 row, ambiguous) | **$569 (T500 Pro)** | — | Dyna |
| Seasonic Focus GX-850W V4 (v4 Black) | — | $209 | **$207** | PCT (−$2) |
| MSI MAG A850GL 850W | — | $132 | — | C (drop — low tier) |
| DeepCool CF120+ 3-pack (OLD) | **$53** | — | — | Biz (replaced) |
| **Arctic P12 Pro A-RGB ×9** | **$25 ea** | — | — | Biz — 5 reverse + 4 normal |
| Jonsbo D33 Black Wood | not listed | not listed | — | ask at counter |

Notes:
- Crucial T500 row in Biz mixes T500/MP441 — the `349` is likely the 1TB; 2TB column ambiguous, so default to Dyna
  T500 Pro `$569` (clean in the `500/1TB/2TB/4TB` header).
- CPU+mobo **bundle beats separating** at both shops. On the PC Themes scanned list, the MSI B850M Mortar
  row reads **$1,023 with the 9800X3D** and $389 board-only (from TSV column alignment).
- PC Themes bundle is *more expensive* than both shops → PC Themes doesn't undercut for the bundle.
- ProArt haggle: Bizgram lists ProArt 5070 Ti at **$1,999** → Dyna's $1,819 is already −$180. Point at the Dyna Prime/TUF **PROMO** rows and the Palit $1,629 (Biz) quote → ask for ~$1,700.
- Wood-look GPU save-alternates (if ProArt won't budge): ASUS Prime 5070 Ti (PROMO Dyna / $1,699 PCT / $1,899 Biz), Palit Gaming Pro S $1,629 Biz, ASUS TUF (PROMO Dyna / $1,989 Biz), MSI Ventus 3X $1,809 Dyna, ZOTAC SOLID $1,799 Biz. Avoid white/gamer-RGB cards (GALAX EX Gamer $1,370, Gaming Trio White, Aero, Aorus).

## Decision Rules
- Importunity threshold: ANY saving counts (verbal haggling at counter).
- Stores: minimize store count to build rapport (target 1-2 shops).
- Preferred-but-swappable parts: ProArt 5070 Ti, Jonsbo D33, AK620 wood
  cap. Reconsider only if a clearly cheaper equivalent appears.

## Scope / Steps
1. Data: have Bizgram + Dynacore PDFs locally; fetch PC Themes list, extract.
2. Build per-part price matrix across the trio.
3. Compare bundle-vs-separate CPU+mobo at each shop.
4. Identify cheapest store per part + anchor store; suggest 2-3 shop split.
5. Report: comparison table, one-trip shopping order, negotiation notes,
   final total vs baseline.

## Core Parts to Compare (each shop)
- 9800X3D + MSI B850M Mortar (bundle + split)
- Asus ProArt 5070 Ti (+ cheaper 5070 Ti variants)
- Team T-Force Delta 6000 CL30 (+ cheaper CL30 RGB kits)
- Crucial T500 2TB (+ cheaper Gen4 DRAM 2TB)
- Corsair RM850e (+ MSI A850GL $132 — dropped, Tier C)
- DeepCool AK620 G2 (wood) / standard AK620
- Jonsbo D33 Black Wood (vs alternatives)
- CF120+ 3-pack fans

## Deliverables
- Per-part comparison matrix.  (DONE above)
- One-trip store-by-store shopping order.  (next)
- Negotiation + discount call-outs.
- Final estimated total vs $4,442 baseline.

---

## As-Built Addendum — 09 Aug 2026 (planned vs bought)

Supersedes the totals above. On-site swaps + what they saved:

| Change | Plan | Built | Δ |
|---|---|---|---|
| PSU | Seasonic Focus GX-850W V4 (Tier A) | **ASUS TUF 850W Gold EVO** (Tier A, ATX 3.1) | −70 |
| SSD | Crucial T500 2TB | **2× WD Black SN850X 1TB** | −31 |
| Fans | 9-fan | **7-fan**: 5× A-RGB Reverse + 2× P12 Pro PST | −66* |
| Cooler | AK620 G2 | **AK620 G2 Digital NYX** | +15 |
| Paste | — | Arctic **MX-7** | +10 |
| Case | D33 (~135 counter) | **online order** (no SG distributor stock) | TBD |

\* Fans paid 144 actual (5×22 + 2×17); −66 vs the 9× A-RGB 225, −15 more vs the planned 7-fan 159.

- **Dynacore (bundle, no per-item):** planned 4,033 → **paid 4,021** (incl GST) = −12
- **Bizgram:** planned 239 → **paid 249** (cooler 95, fans 110, PST 34, MX-7 10) = +10
- **On-site total: 4,270** (excl case) vs planned 4,407 → **~137 saved**
- vs original all-ARGB 4,574 → **~304 saved**; final incl online case ~4,405 ≈ plan