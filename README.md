# Zijin Mining — Geostrategy Deck

Interactive presentation for the KEDGE *International Business & Geostrategy* group report on **Zijin Mining Group (紫金矿业)**.

Built in the **Dragon Vein · Crystal** visual style (`concepts/concept2c-dragon-crystal.html`) with five interactive D3 regional maps covering China, Eurasia, South America, Africa, and Europe + Oceania.

## Live deck

**→ [`index.html`](./index.html)** — full 12-slide deck with integrated maps.

Scroll to navigate. Hover a marker to highlight the host country; click for a full asset panel (stake, commodity, status, narrative).

## Structure

```
.
├── index.html              — full integrated presentation (12 slides)
├── regional-maps/          — standalone single-region maps
│   ├── 01-china.html
│   ├── 02-eurasia.html
│   ├── 03-south-america.html
│   ├── 04-africa.html
│   ├── 05-europe-oceania.html
│   └── _styles.css
└── concepts/               — six early style explorations
    ├── concept1-golden-mountain.html
    ├── concept2-dragon-vein.html
    ├── concept2a-dragon-gold.html
    ├── concept2b-dragon-ink.html
    ├── concept2c-dragon-crystal.html   ← selected style
    └── concept3-ore-future.html
```

## Map projections

Each regional map uses a projection chosen for its footprint:

| Region | Projection | Parameters |
|---|---|---|
| China | Lambert Conformal Conic | parallels 25° / 47°, λ₀ = 105°E |
| Eurasia (Central Asia + Tuva + Mongolia) | Lambert Conformal Conic | parallels 35° / 55°, λ₀ = 80°E |
| South America | Albers Equal-Area Conic | parallels −8° / −32°, λ₀ = 62°W |
| Africa | Mercator | centre 20°E / 2°N |
| Europe + Oceania | Split: LCC Europe + Mercator Oceania | — |

## Operations covered

**China** — Zijinshan · Julong · Ashele · Wulatehouqi · Duobaoshan · Shuiyindong · Luoning
**Eurasia** — Taldybulak Levoberezhny (KG) · Zeravshan (TJ) · Kyzyl-Tashtyg (RU–Tuva) · Raygorodok (KZ) · Mongolia exploration
**South America** — Buriticá (CO) · Rosebel (SR) · Guyana exploration · Río Blanco (PE) · Tres Quebradas 3Q (AR)
**Africa** — Kamoa-Kakula (CD) · Akyem (GH) · Bisha (ER) · South Africa office
**Europe + Oceania** — Timok / Bor (RS) · Norton Gold Fields (AU) · Porgera JV (PG)

## Tech

- Pure HTML / CSS / vanilla JS
- [D3 v7](https://d3js.org/) + [topojson-client](https://github.com/topojson/topojson-client)
- [world-atlas](https://github.com/topojson/world-atlas) `countries-110m`
- Fonts: Space Grotesk, Noto Serif SC, Outfit (Google Fonts)

All dependencies load from CDN — no build step.

## Run locally

```bash
python3 -m http.server 8000
# then open http://localhost:8000/
```

## Course context

- **Course:** International Business & Geostrategy (KEDGE, 2026)
- **Evaluator:** Juliette Thiolas-Hittos
- **Rubric weighting:** Geographic analysis 25%, Conceptual accuracy 20%, Evidence 20%, Strategic reasoning 20%, Presentation 15%
