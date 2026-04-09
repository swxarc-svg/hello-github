---
type: synthesis
title: "Thermal comfort evaluation methods in shading studies"
tags: [thermal-comfort, utci, mrt, envi-met, ladybug, shadow, methodology, query]
sources: [ghoniem-2025-albedo-shading-thermal-comfort, hassan-2025-knitted-textile-canopies-generative-design, lyu-2026-computational-delivery-framework]
query: "What methods have been used to evaluate thermal comfort in shading studies?"
last_updated: 2026-04-09
---

## Query

> What methods have been used to evaluate thermal comfort in shading studies?

_Based on 3 ingested sources as of 2026-04-09._

---

## Simulation-based methods

### ENVI-met + Ladybug hybrid (Ghoniem et al. 2025)

The most complete workflow in the current literature:

- **ENVI-met 5.7.1** handles fine-grain atmospheric simulation — surface temperatures, air temperature, and radiation exchange — at 50×50 m domain, 1.4 m pedestrian height
- **Ladybug v1.8** (Grasshopper) computes MRT and UTCI from those outputs
- Validated against field data: MRT R² = 0.924; Ta R² = 0.984
- Outputs: Ts, Ta, MRT, UTCI at 5 time intervals (09:00–17:00)

### Ladybug shadow casting only (Hassan et al. 2025)

A faster proxy metric used in generative optimization loops:

- Shadow coverage percentage (shadow area / land area) at 09:00, 12:00, 14:00 using Cairo EPW data
- Not full UTCI — wind, humidity, and MRT are not captured
- Allows rapid iteration across hundreds of geometry variants (Biomorpher: 313 solutions in 5 min)
- Explicitly acknowledged as a limitation; full thermal comfort simulation flagged as future work

---

## Field measurement

### Globe thermometer protocol (Ghoniem et al. 2025, ISO 7726)

- **Instruments**: Testo 435-2 (Ta, RH), Testo globe probe (globe temperature), hot-wire anemometer (wind speed), Extech EasyView IAQ
- **MRT** back-calculated from globe temperature, air temperature, and wind speed per ISO 7726
- Measurement intervals: 5 time points on a single peak-summer day (August 15)
- Role: validation of ENVI-met simulation, not primary data collection

---

## Comparison

| Method | Metrics produced | Validation | Strength | Limitation |
|--------|-----------------|------------|----------|------------|
| ENVI-met + Ladybug | MRT, UTCI, Ta, Ts | Field-validated (R²≥0.924) | Full comfort picture; spatially distributed | Neighbourhood scale; not structural loads |
| Ladybug shadow % only | Shadow coverage | None | Fast; embeds in optimization loops | Proxy only; excludes wind, humidity |
| Field measurement | MRT, Ta, RH, wind | Ground truth | Real-world accuracy | Single day/site; resource-intensive |

---

## Key methodological observation

**The ENVI-met + Grasshopper/Ladybug dual-platform workflow** (Ghoniem 2025) is the most complete validated approach and directly applicable to this dissertation's toolchain.

**Critical gap across all three sources**: none include wind-load or CFD analysis. There are no comfort evaluations under typhoon-scale wind conditions in the current literature. The shadow-% proxy used in Hassan 2025 is specifically unsuited to this — it captures solar geometry but ignores the wind component that dominates comfort (and structural safety) under typhoon events.

---

## Related pages

- [[thermal-comfort-outdoor]] — concept page with metric definitions and benchmarks
- [[envi-met-simulation]] — detailed workflow documentation
- [[parametric-design-tools]] — Ladybug/Grasshopper integration for optimization
- [[shading-structures]] — performance outcomes from these methods
- [[cfd-wind-simulation]] — the missing method for typhoon wind comfort
