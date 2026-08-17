# Project record

## Stage 1
- Decision: PIVOT from generic calculator site to purchase-oriented DIY buying planner.
- First MVP: Patio Buying Planner.
- Core differentiation: real pack inputs, pack rounding, mixed-pack cost optimisation, surplus visibility and shopping-list output.
- Budget: £0.
- Architecture: static HTML/CSS/JavaScript, client-side calculations, no backend or paid API.

## Calculation specification v0.1
- Area = length x width.
- Paving target = area x (1 + user waste percentage).
- Compacted sub-base volume = area x user-selected compacted sub-base depth.
- Theoretical mortar volume = area x user-selected mortar-bed depth.
- Mortar component split is shown by volume using a user-selected sand:cement ratio.
- No automatic conversion from aggregate/sand/cement volume to package weight unless the user supplies product coverage/yield. This avoids unsupported density assumptions.
- Paving optimiser searches integer combinations of up to six user-entered packs; objective order: lowest cost, then lowest surplus, then fewest packs.

## Construction guidance used for defaults
- Marshalls general patio guidance: 100 mm compacted sub-base; about 40 mm concrete/mortar layer; 3:1 sand:cement example.
- Bradstone concrete/natural stone guidance: 100 mm sub-base; around 30 mm mortar bed; 4:1 sharp sand:cement; installation system details vary by product.
- Defaults are editable and described as planning assumptions rather than universal recommendations.

## Tests completed
- JavaScript syntax check.
- HTML parser check.
- Single-pack rounding: 43 m2 at 2.4 m2/pack -> 18 packs / 43.2 m2.
- Exact coverage case.
- Mixed-pack cheapest-combination case.
- Cost tie broken by lower surplus.
- Zero target logic.
- Invalid pack ignored.
- Area, waste, sub-base and mortar volume calculations.

## Known limitations / next work
- Rectangle only in MVP v0.1.
- Jointing coverage is supplier-entered rather than geometrically calculated because product coverage varies with joint dimensions and paving format.
- No domain/analytics/Search Console yet; these require external setup after deployment.
- No retailer scraping or live prices.
- No affiliate links until programmes are verified and demand is demonstrated.

## 17 Aug 2026 — Growth cycle 1
- Live GitHub Pages MVP confirmed.
- Google Search Console ownership verified.
- Homepage submitted for indexing.
- Sitemap publicly accessible; Search Console fetch status pending.
- Competitor/search review: MOT Type 1 and conventional flooring calculators are crowded with multiple active/new entrants.
- Decision: second indexable tool will be a standalone Pack Optimiser, reusing the existing cheapest-valid-basket engine.
- Purpose: create a broader purchase-optimisation entry point without adding construction assumptions or density guesses.
- New page: `pack-optimiser.html`.
- Existing patio page updated with internal navigation to Pack Optimiser.
- Sitemap expanded to include both pages.
## Growth cycle 2 — 17 August 2026
- Verified Pack Optimiser exists on `main` and is listed in the sitemap.
- Researched the third search entry-point. Generic tile and paving calculator SERPs remain crowded; flooring calculators commonly calculate packs for a single pack size.
- Built `flooring-pack-calculator.html` to combine multiple rooms, waste allowance, multiple actual pack options and cheapest-valid-basket optimisation.
- Updated internal navigation on the patio calculator and general Pack Optimiser.
- Expanded sitemap to three URLs.
- Budget remains £0.

