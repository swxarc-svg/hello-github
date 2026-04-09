---
type: concept
title: "CFD wind simulation"
tags: [cfd, wind-simulation, methodology, openfoam, butterfly]
source_count: 0
last_updated: 2026-04-09
---

## Definition

Computational Fluid Dynamics (CFD) wind simulation is a numerical method for predicting airflow patterns, wind pressure distribution, and ventilation performance around and through urban structures. In outdoor shading research, CFD is used to evaluate both pedestrian-level wind comfort under normal conditions and structural wind loads during typhoon events.

## Current state of research

_To be populated as sources are ingested._

Key tools in use:
- **ANSYS Fluent** — commercial, widely used in engineering
- **OpenFOAM** — open-source, increasingly popular in research
- **Butterfly** (Grasshopper plugin) — wraps OpenFOAM for parametric workflows
- **ENVI-met** — focused on microclimate, less precise for structural loads

## Key debates & contradictions

_To be populated._

Expected debates:
- RANS vs LES turbulence models for urban wind prediction
- Validation requirements: wind tunnel vs field measurement
- Computational cost vs accuracy trade-offs for parametric studies
- Appropriate boundary conditions for typhoon-scale wind events

## Methods & tools

- Pre-processing: meshing strategies for complex shading geometries
- Solver: steady-state RANS for comfort, transient LES for extreme events
- Post-processing: wind speed maps, pressure coefficients, turbulence intensity
- Integration: coupling CFD results with thermal comfort models (UTCI, PET)

## Related concepts

- [[thermal-comfort-outdoor]] — CFD provides wind input for comfort models
- [[typhoon-wind-loads]] — extreme scenario simulation
- [[grasshopper-parametric-design]] — Butterfly enables parametric CFD
- [[retractable-shading-systems]] — CFD evaluates deployed vs stowed performance
- [[wind-tunnel-testing]] — physical validation method

## Sources

_No sources ingested yet for this concept._
