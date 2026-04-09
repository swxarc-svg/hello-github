---
type: source
title: "Evaluating Urban Surface Materials: Albedo Optimization and Shading for Pedestrian Thermal Comfort in Hot-Arid Environments"
authors: [Mayar Ghoniem, Amgad Fahmy, Tarek M. Kamel]
year: 2025
journal: "Civil Engineering and Architecture"
volume: "13(6)"
pages: "4331–4352"
doi: "10.13189/cea.2025.130616"
tags: [thermal-comfort, utci, mrt, albedo, shading, canopy, envi-met, ladybug, grasshopper, parametric, simulation, hot-arid, urban, public-space, method]
confidence: high
date_ingested: 2026-04-09
raw_path: "raw/papers/Ghoniem 等 - 2025 - Evaluating Urban Surface Materials Albedo Optimization and Shading for Pedestrian Thermal Comfort i.pdf"
---

## Summary

This study evaluates the thermal effects of varying surface albedo (0.12, 0.20, 0.30) on a commercial pedestrian strip in New Cairo, Egypt — a hot-arid environment. Using a hybrid workflow combining ENVI-met 5.7.1 microclimate simulation with Grasshopper/Ladybug Tools v1.8 parametric modelling, and validated against field measurements, the study isolates the independent effect of surface reflectivity on Ts (surface temperature), Ta (air temperature), MRT (mean radiant temperature), and UTCI.

The central finding is a critical trade-off: higher albedo reduces Ts (up to 7 °C) and Ta (up to 1.5 °C) but simultaneously *raises* MRT (up to 6 °C) through shortwave reflection toward pedestrian bodies in unshaded conditions, pushing UTCI above 46 °C — "extreme" heat stress. When modular circular canopy shading was introduced, UTCI declined 5–6.6 °C, effectively neutralizing the radiant penalties of high albedo. The study concludes that shading is the dominant lever on pedestrian comfort, not material selection alone.

The hybrid ENVI-met + Grasshopper/Ladybug workflow was validated against field measurements (MRT: R² = 0.924; Ta: R² = 0.984), demonstrating the robustness of this dual-platform approach. ENVI-met handled fine-grain atmospheric simulation (50×50 m domain, 1.4 m pedestrian height) while Ladybug computed MRT and UTCI at larger urban scales.

## Key findings

- Albedo 0.30 vs 0.12: Ts reduced by 7 °C at 13:00; Ta reduced by 1.5 °C at 15:00
- Higher albedo *raised* MRT by up to 6 °C (from 51 °C to 56 °C at 9:00; from 70 °C to 72 °C at 13:00) due to shortwave repulsion
- Unshaded UTCI at 15:00: 45.8 °C (albedo 0.12) → 46.9 °C (albedo 0.30) — "very strong" to "extreme" heat stress
- Post-shading UTCI: declined 5–6.6 °C regardless of albedo, converging across all surface scenarios
- Canopy design: clustered circular modules, 2.65–2.87 m height, 7.35 m spacing, white-coated wood
- Validation: MRT R² = 0.924; Ta R² = 0.984 (field measurements vs simulation, August 15, peak summer)
- Reflective pavements show albedo degradation over time (dust, wear) — maintenance protocols required

## Methodology

Three-phase hybrid workflow:
1. **Field data acquisition**: Ta, Ts, globe temperature, RH, wind speed at 5 time intervals (09:00–17:00), August 15. MRT calculated from ISO 7726 black globe thermometer. Instruments: Testo 435-2, Extech EasyView IAQ, hot-wire anemometer, Testo globe probe.
2. **Digital modelling**: Full site in Rhinoceros 3D; 50×50 m subdomain in ENVI-met 5.7.1 (2 m horizontal, 0.5 m vertical resolution). Three albedo scenarios (0.12/0.20/0.30) with all other variables held constant.
3. **Thermal analysis**: MRT and UTCI computed in Grasshopper using Ladybug Tools v1.8 (Outdoor Solar MRT module; UTCI-Fiala model). Ts from solar radiation + material properties. Analysis at 09:00, 11:00, 13:00, 15:00, 17:00.

Key limitation: single urban typology (low-rise commercial strip), single summer day, no vegetation in baseline simulations — MRT penalties may be overstated compared to vegetated real-world settings.

## Relevance to dissertation

**Directly relevant** on methods and comfort metrics. The ENVI-met + Grasshopper/Ladybug hybrid workflow is the same toolchain used in this dissertation. The findings on shading vs. albedo have direct implications for Macau's humid-hot context: while the climate differs (arid vs. humid-subtropical), the dominance of shading over material selection as a comfort lever is likely transferable. The UTCI and MRT frameworks are core dissertation metrics.

The canopy shading result — 5–6.6 °C UTCI reduction — provides a benchmark for what outdoor shading structures can achieve in extreme conditions. The albedo trade-off (cool pavements raising MRT) is a cautionary finding for any design guidance recommending reflective surfaces without paired shading.

**Gap for dissertation**: This study is hot-arid, not humid-hot/typhoon. No wind resistance or structural considerations. No monsoon or typhoon context. Provides the thermal comfort simulation baseline but not the resilience dimension.

## Connections

- [[thermal-comfort]] — provides quantitative benchmarks for UTCI and MRT in a shaded vs. unshaded pedestrian strip
- [[shading-structures]] — modular circular canopy with white-coated wood; 5–6.6 °C UTCI reduction
- [[surface-albedo]] — key source for albedo–MRT trade-off; pairs with [[envi-met-simulation]]
- [[envi-met-simulation]] — validated dual-platform workflow (ENVI-met + Ladybug); R² figures cited here
- [[parametric-design-tools]] — Grasshopper/Ladybug workflow for outdoor thermal comfort
- Builds on [[kamel-2021-workflow]] (cited as [21]) — Egypt-focused outdoor thermal comfort modelling workflow

## Quotes & data

- "The canopy shading intervention proved far more decisive, reducing UTCI by 5–6.6 °C and neutralizing albedo-driven MRT increases." (p. 4348)
- "Increasing albedo reduced Ts by up to 7 °C and Ta at pedestrian height by 1.5 °C... higher reflectivity elevated MRT by as much as 6 °C, which in turn raised UTCI values beyond 46 °C in unshaded conditions." (abstract)
- MRT validation table (Table 1): field 9:00 = 52.01 °C, simulated = 50.2 °C; field 15:00 = 69.8 °C, simulated = 71.6 °C
- Ts at peak (13:00): 58.2 °C (albedo 0.12) → 51.25 °C (albedo 0.30) — 7 °C reduction
- UTCI shading intervention, albedo 0.20: 11:00 declined from 41.4 °C → 35.3 °C (−6.1 °C); 15:00 from 46.2 °C → 40.95 °C
