# Partner Briefing — Consistency Audit

*Internal. April 2026. Pressure-test sweep before the Tlali / Micha / Kim review.*

---

## Scope

Swept the full `partner-briefing/` directory plus `uploads/` for:

- "Brandformance OS" residuals (should only survive as **BFL / Brandformance Live** — the events entity)
- Three-layer tagline drift
- Pricing v7 consistency
- Partner-constellation naming
- Section-04 label ("Operating Model", not "Finance")
- Cross-reference integrity (every download link resolves)
- Numbers consistency across artefacts

---

## Summary

The briefing is substantially consistent. Product naming, tagline system, pricing tiers, partner constellation, section labels, and download links all check out. **Two real inconsistencies and two housekeeping items surfaced — none blocking, all fixable in a pass.**

---

## Findings

### 1. Real inconsistency — 7-year SOM ARR figure

Three numbers in circulation for the same thing (7-year SOM target revenue):

| Location | Figure |
|---|---|
| `index.html` (briefing landing) | **€38.8M ARR** (stated twice) |
| `artefacts/market_size_v1.html` (the sizing artefact itself) | **€32M ARR** · 580 clients · 1% SAM capture |
| `GritFuel_BrandGuide_v2.html` (example quote) | €38.8M ARR · 675 clients |
| Context Doc §11 detailed table | €38.8M revenue at Y7 · 675 clients |
| Context Doc §11 summary line | "€36M ARR · 1.2% SAM capture" |
| Investor Deck v1.1 (headlines) | €36M ARR |
| Investor Deck v1.1 (detail slide) | €38.8M |

The math-consistent number is **€38.8M** (675 clients × €57,450 blended ARR per client as stated in the Business Model Canvas). **€36M is the round-down headline.** The `market_size_v1.html` artefact is the outlier — it caps at 3-year SOM and uses an older 580-client / 1% SAM frame instead of the 675-client / 1.2% SAM frame everything else now uses.

**Recommended fix:** decide on one canonical pair — e.g. "~675 clients · €36M ARR (round)" or "~675 clients · €38.8M ARR (exact)" — and make `market_size_v1.html` match. Keep the Business Model Canvas blended-ARR math aligned to whichever you pick.

### 2. Real inconsistency — capital-burn figure not reconstructed anywhere before this week

The **€15–25B wasted annually** anchor lives in:

- Context Doc §11 (line 212) — as a bullet
- Investor Deck v1.1 (around the market-gap slide) — no derivation

It does **not** appear in the Partner Deck, any of the 6 briefing pages, or any artefact. The new `capital_burn_calculation.html` (re-rendered today with validated inputs) is the first written derivation. It lands on **€9–18B / yr** as the honest range — meaningfully lower than the original claim — and recommends anchoring on the 43% PMF/GTM stat (CB Insights 2024, n=431) instead of the aggregate burn figure.

The memo is internal-only and not linked from the microsite. No action needed unless you want to keep the €15–25B line in the Investor Deck; if so, the memo flags the assumptions it rests on.

### 3. Housekeeping — stale files in `/downloads/`

Two superseded files are still sitting in the downloads folder, not linked from any live page:

- `GritFuel_Brandformance_OS.pdf` (31KB · old name · superseded by `GritFuel_OS_SystemDoc.pdf` at 88KB)
- `GritFuel_Brandformance_OS_SystemDoc.docx` (50,455B · old name · superseded by `GritFuel_OS_SystemDoc.docx` at 50,444B)

**Safe to delete** — the microsite points at the renamed versions. They'll just clutter the repo / GitHub Pages directory listing otherwise. I haven't removed them because permanent deletion needs your say-so.

### 4. Housekeeping — `.bak` files at briefing root

Six backup files from the Brandformance-OS → GritFuel-OS rename survive in `partner-briefing/`:

```
01-strategy.html.bak    02-product.html.bak    03-brand.html.bak
04-finance.html.bak     05-gtm.html.bak        index.html.bak
```

They contain the original "Brandformance OS" text in a handful of places. They won't load via GitHub Pages navigation but will appear in a repo file listing. **Safe to delete** — same ownership flag as above.

---

## Checks that passed

- **Product naming** — "Brandformance OS" no longer appears anywhere in the live microsite or live artefacts. The only surviving "Brandformance" references are (a) `.bak` backups, (b) inside stale PDFs, (c) the correct **BFL (Brandformance Live)** entity reference in the Business Model Canvas.
- **Three-layer tagline** — umbrella "Human thinking. Relentless execution." consistent across index, 03-brand, and BrandGuide. Descriptor "The growth operating system." used 11 places. Companion "Growth that compounds. Visibly." correctly scoped to the brand guide and 03-brand (internal-first, not the loud line).
- **Pricing v7** — €3,500 / €5,250 / €8,000 · 70 / 110 / 180 credits · €25/credit · 75% cost-share to partners. Consistent across 04-finance, `pricing_v7.html`, `GritFuel_Business_Model_Canvas_v1.html`, Brand Guide example, Founder/CEO Deep Dive.
- **Section 04 label** — "Operating Model" (not "Finance") across nav, breadcrumbs, titles, and meta tags. The filename `04-finance.html` is the only Finance residue — intentionally kept to avoid breaking links.
- **Partner constellation** — `.frank` / `Bluegyfu` / `BFL` naming stable across 10 files, 39 occurrences total.
- **Download cross-references** — every `downloads/*.pdf|docx|xlsx` href in the live pages resolves to an actual file in `/downloads/`.
- **Market-sizing sources** — TAM anchors (25,000 EU / 7,500 SSA / 450 EU-Africa · €225M + €225M + €27M SAM) consistent between Context Doc and `market_size_v1.html`.
- **Validated headline claims** — 43% PMF/GTM failure stat (CB Insights 2024) and €118.9B EU digital ad spend (IAB Europe AdEx 2024) both fact-checked ✓.

---

## Recommended ordering if you want to address

1. Pick the canonical 7-year SOM number (€36M vs €38.8M) and update `market_size_v1.html` to match everything else.
2. Decide whether to keep the €15–25B line in the Investor Deck v1.1 or swap it for the 43% stat per the memo.
3. Clean the four stale files (2× `Brandformance_*` in `/downloads/` + 6× `.bak` at root) once you're comfortable.
4. Everything else is already aligned.
