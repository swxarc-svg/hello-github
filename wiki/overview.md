# Overview

## Research landscape: Outdoor public space shading in humid-hot, typhoon-prone cities

_This page is progressively enriched as sources are ingested. It provides a bird's-eye view of the dissertation's research territory._

### Core question

How can outdoor public space shading systems in high-density humid-hot cities be designed to provide effective everyday shading and ventilation while resisting or adapting to typhoon conditions?

### Research territory map

The dissertation spans three overlapping domains:

1. **Climate-responsive design** — Shading, ventilation, and thermal comfort in humid-hot urban environments. Key metrics include UTCI, PET, and mean radiant temperature (MRT).

2. **Structural resilience** — Wind-resistant design for typhoon conditions. The tension between lightweight shade structures and the extreme wind loads of typhoon events (sustained winds >118 km/h, gusts >200 km/h).

3. **Parametric and kinetic design** — Computational approaches to optimising shading geometry, including retractable and transformable systems that can adapt between everyday and extreme weather states.

---

### Key findings so far (3 sources ingested)

**Shading performance**:
- Canopy shading reduces UTCI by 5–6.6 °C in hot-arid conditions (Ghoniem 2025)
- Doubly curved (saddle-form) textile canopy achieves 94–98% shadow coverage across peak hours (Hassan 2025)
- Shading is the dominant lever on pedestrian comfort — surface albedo improvements are secondary and can backfire (raise MRT) without paired shade (Ghoniem 2025)

**Generative design**:
- Biomorpher (Grasshopper) outperforms Galapagos and Octopus for multi-objective shading geometry optimization: 313 solutions in 5 min; all 4 goals achieved simultaneously (Hassan 2025)
- MOO tools produce Pareto-optimal sets but mask cultural/institutional biases and cannot capture qualitative values (atmosphere, ritual) — epistemological limitation (Lyu 2026)

**Fabrication and accountability**:
- The Computational Delivery Framework (CDF) identifies three systemic tensions: geometric freedom vs. fabrication feasibility; speculative prototypes vs. warrantable delivery; simulation optimism vs. institutional accountability (Lyu 2026)
- Architecture must be evaluated by whether it is certifiable, maintainable, and insurable — not by novelty alone

**Methodology**:
- ENVI-met + Grasshopper/Ladybug dual-platform workflow is validated (MRT R² = 0.924; Ta R² = 0.984) and directly applicable to this dissertation

---

### Key gaps (emerging from literature)

1. **No wind/structural analysis on shading canopies**: Hassan 2025 explicitly acknowledges the FEA and wind load gap — this is a direct dissertation research opportunity
2. **No typhoon context**: No literature yet identified on shading structures designed simultaneously for typhoon wind loads and everyday thermal performance
3. **Hot-arid only**: All thermal comfort + shading benchmarks so far are from Cairo (hot-arid); no humid-hot / monsoon / typhoon climate studies yet
4. **No retractability studies**: No sources yet address kinetic/retractable mechanisms for storm adaptation
5. **Institutional accountability gap**: No studies embed insurability or regulatory compliance in the parametric design workflow (flagged by Lyu 2026 as future agenda)

---

### Dominant methodologies in the field

- CFD wind simulation (ANSYS Fluent, OpenFOAM, Butterfly/Grasshopper)
- Environmental performance modelling (Ladybug/Honeybee, ENVI-met)
- Parametric design optimisation (Grasshopper: Galapagos, Octopus, **Biomorpher**)
- Physical wind tunnel testing
- Post-occupancy field measurements (thermal comfort surveys)

### Geographic focus

Primary: Macau, Hong Kong, Shenzhen, Guangzhou (Pearl River Delta)
Secondary: Singapore, Taipei, Bangkok, and other humid-hot high-density Asian cities

_Current literature: Cairo-focused. Gap to be addressed._

---

_Last updated: 2026-04-09 — after ingesting 3 sources (Ghoniem 2025, Hassan 2025, Lyu 2026)_
