---
type: concept
title: "ENVI-met simulation"
tags: [envi-met, microclimate, simulation, mrt, utci, validation, hot-arid, urban]
source_count: 1
last_updated: 2026-04-09
---

## Definition

ENVI-met is a microclimate simulation software for modelling urban airflow, heat transfer, vegetation interaction, and surface energy exchange at fine spatial resolution. It is widely used in outdoor thermal comfort research as an alternative or complement to CFD. Unlike pure CFD tools, ENVI-met integrates radiation, convection, and moisture exchange in a single solver.

## Current state of research

**Validated workflow** (Ghoniem et al. 2025): ENVI-met 5.7.1 + Grasshopper/Ladybug v1.8 hybrid:
- ENVI-met handles atmospheric simulation at fine grain (50×50 m domain, 2 m horizontal / 0.5 m vertical resolution)
- Ladybug computes MRT and UTCI at larger urban scales from ENVI-met outputs
- Validation against field measurements: MRT R² = 0.924; Ta R² = 0.984
- This dual-platform approach is robust and transferable

**Key parameters** (Ghoniem 2025):
- Domain: 50×50 m, 1.4 m pedestrian height analysis level
- Albedo scenarios tested: 0.12 / 0.20 / 0.30
- Surface temperatures, air temperature, MRT, UTCI extracted at 5 intervals (09:00–17:00)

## Key debates & contradictions

- **ENVI-met vs. CFD**: ENVI-met is faster and better for surface–vegetation–radiation interactions; CFD (OpenFOAM) is more accurate for turbulent wind flow and structural pressure loads
- **Scale limitation**: ENVI-met is suited for neighbourhood/block scale; not for structural wind load analysis
- **Vegetation baseline**: Ghoniem 2025 notes that excluding vegetation from baseline simulations may overstate MRT penalties

## Methods & tools

- Pre-processing: site modelling in Rhinoceros 3D, exported to ENVI-met format
- Solver: ENVI-met 5.7.1 (albedo, material properties, atmospheric boundary conditions)
- Post-processing: ENVI-met results → Grasshopper/Ladybug v1.8 for MRT and UTCI computation
- Validation: ISO 7726 globe thermometer, Testo 435-2, hot-wire anemometer (field measurement protocol)

## Related concepts

- [[thermal-comfort-outdoor]] — primary output metric (UTCI, MRT, Ta)
- [[parametric-design-tools]] — Grasshopper/Ladybug integration
- [[cfd-wind-simulation]] — complementary tool for wind-focused analysis
- [[surface-albedo]] — key input variable in ENVI-met scenarios

## Sources

- [[ghoniem-2025-albedo-shading-thermal-comfort]] — validated dual-platform workflow; albedo scenarios; quantitative R² figures
