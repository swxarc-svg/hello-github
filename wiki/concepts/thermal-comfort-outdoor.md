---
type: concept
title: "Outdoor thermal comfort"
tags: [thermal-comfort, utci, pet, humid-hot, shading, ventilation, mrt]
source_count: 2
last_updated: 2026-04-09
---

## Definition

Outdoor thermal comfort describes the subjective satisfaction with the thermal environment in open-air spaces. In humid-hot climates, it is primarily governed by solar radiation (mean radiant temperature), air temperature, humidity, and wind speed. Shading directly reduces mean radiant temperature; ventilation increases convective heat loss. Both are critical for making public spaces usable in subtropical and tropical cities.

## Current state of research

Key metrics:
- **UTCI** (Universal Thermal Climate Index) — widely adopted, accounts for clothing adaptation
- **PET** (Physiological Equivalent Temperature) — common in European and Asian studies
- **SET*** (Standard Effective Temperature) — used in ASHRAE contexts
- **MRT** (Mean Radiant Temperature) — the most shading-sensitive variable

**Quantitative benchmarks from literature**:
- Canopy shading reduces UTCI by **5–6.6 °C** in hot-arid conditions (Ghoniem et al. 2025)
- Shaded areas in Cairo are ~10 °C cooler than unshaded (Hassan et al. 2025)
- Tree canopies reduce temperature by 3.5–7.7 °C from generated shadow (Hassan et al. 2025)
- Unshaded UTCI at peak can exceed 46 °C ("extreme" stress) in hot-arid conditions (Ghoniem et al. 2025)

**Key finding — albedo–MRT trade-off**: Higher surface albedo reduces air temperature but *raises* MRT through shortwave reflection toward pedestrians in unshaded conditions. Shading is the dominant lever over material selection (Ghoniem et al. 2025).

## Key debates & contradictions

- **Albedo vs. shading priority**: Cool pavements improve Ts and Ta but elevate MRT if not paired with shade — net effect on UTCI can be negative without canopy
- **Climate transferability**: Findings from hot-arid contexts (Cairo) may not directly transfer to humid-hot contexts (Macau) due to differing humidity regimes and cloud cover
- **Shadow % vs. UTCI**: Shadow coverage percentage (Hassan et al.) is a proxy metric; full UTCI calculation requires wind, humidity, and MRT integration (Ghoniem et al.)

## Methods & tools

- **Ladybug** (Grasshopper) — solar radiation, sky view factor, UTCI/MRT calculation; used in both Ghoniem et al. and Hassan et al.
- **Honeybee** (Grasshopper) — energy and daylight simulation, EnergyPlus/Radiance
- **ENVI-met** — microclimate simulation with surface and vegetation interaction; validated in Ghoniem et al. (MRT R² = 0.924; Ta R² = 0.984)
- **RayMan** — simple MRT/PET calculator
- **Field measurement** — globe thermometer, anemometer, datalogger surveys (ISO 7726 method used in Ghoniem et al.)

## Related concepts

- [[cfd-wind-simulation]] — provides wind data for comfort calculation
- [[retractable-shading-systems]] — design strategy to improve comfort
- [[shading-structures]] — primary intervention for UTCI reduction
- [[envi-met-simulation]] — validated dual-platform workflow
- [[surface-albedo]] — interacts with shading in complex ways (MRT trade-off)

## Sources

- [[ghoniem-2025-albedo-shading-thermal-comfort]] — UTCI benchmarks, albedo–MRT trade-off, ENVI-met + Ladybug validation
- [[hassan-2025-knitted-textile-canopies-generative-design]] — shadow % as comfort proxy; Cairo temperature differentials
