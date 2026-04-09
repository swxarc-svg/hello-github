---
type: source
title: "Knitted Textile Canopies: A Rapid Generative Design Optimization Tool for Enhanced Shading Performance"
authors: [Mahmmoud Hassan, Esraa Torky, Deena El-Mahdy]
year: 2025
journal: "Nexus Network Journal"
volume: "27"
pages: "875–904"
doi: "10.1007/s00004-025-00839-7"
tags: [canopy, shading, generative-design, parametric, grasshopper, ladybug, tensile, textile, membrane, simulation, hot-arid, urban, fabrication, parametric]
confidence: high
date_ingested: 2026-04-09
raw_path: "raw/papers/Hassan 等 - 2025 - Knitted Textile Canopies A Rapid Generative Design Optimization Tool for Enhanced Shading Performan.pdf"
---

## Summary

This study develops and tests a rapid generative design workflow for knitted textile shading canopies, focusing on maximizing shadow coverage while minimizing footprint and material usage. Using a 10×5 m rectangular baseline surface (2.5–4.2 m height) deconstructed into parametric UV control points in Grasshopper/Rhino, three evolutionary optimization plugins — **Galapagos** (single-objective), **Octopus** (multi-objective), and **Biomorpher** (multi-objective) — were benchmarked against four goals: maximum shadow at 9:00, 12:00, and 14:00 on August 21 (hottest day, Cairo EPW data via Ladybug), plus minimum anchor/footprint area.

**Biomorpher** decisively outperformed the others: it generated 313 solutions in 5 minutes (vs. 142 in 15 min for Galapagos, 1073 in 15 min for Octopus), was the only tool to achieve all four goals simultaneously, and produced an optimal shape (No. 301) with ~95–98% shadow coverage at all three times and an area of 27.05 m². Octopus generated the most solutions but failed to meet the top-10% threshold on any goal. The optimized geometry — a doubly curved saddle shell — was then adapted for a real site at the British University in Egypt (BUE) campus using a hybrid construction system: GFRP bent rods + CNC-knit PTFE-coated membrane + cable net.

The study establishes a transferable workflow roadmap: train a generative tool on site-specific solar/shadow parameters, benchmark tools, select optimal geometry, adapt for structural feasibility. Future work explicitly flags the need for FEA structural analysis (Kangaroo, SOFiSTiK), wind load assessment, and full thermal comfort simulation.

## Key findings

- Biomorpher: 313 solutions in 5 min; achieved all 4 goals; optimal shape No. 301 = 98.36% / 95.80% / 94.73% shadow at 9/12/14h; area = 27.05 m²
- Galapagos: 142 solutions in 15 min; single objective only (14:00); optimal shape No. 32 = 98.34% shadow; area = 31.58 m²
- Octopus: 1073 solutions in 15 min; multi-objective but could not achieve top-10% on any combined goal
- Biomorpher ~200% more efficient than Galapagos, ~20% more efficient than Octopus
- Saddle-form doubly curved geometry achieved shadow percentages >100% at 14:00 (shadow extends beyond canopy footprint due to sun angle)
- Tree canopies reduce temperatures by 3.5–7.7 °C; shaded areas in Cairo ~10 °C cooler than unshaded (cited)
- Textile hybrid structure: GFRP rods (tension) + cable net (waffle pattern) + PTFE-coated CNC-knit membrane — spans 3–200 m possible
- Study explicitly excludes structural load analysis and thermal comfort assessment — acknowledged limitations

## Methodology

Three-phase:
1. **Basic modelling**: 10×5 m rectangular surface parametrized with 33 UV control sliders (X, Y, Z values) in Grasshopper/Rhino. Corner points vary Z only (2.5–4.2 m); body points vary X, Y, Z — producing a patch-based freeform surface.
2. **Goal definition**: Shadow cast area at 09:00, 12:00, 14:00 (Ladybug, Cairo EPW, August 21) vs. built-up area. Shadow % = shadow area / land area (can exceed 100%). Anchor area = minimum convex hull of projected support points.
3. **Comparative analysis**: Galapagos (single-objective, simulated annealing, fitness = shadow at 14:00), Octopus (multi-objective, minimizing only — negative values required), Biomorpher (multi-objective, genome + geometry + perform inputs). Each run 15 min (Galapagos, Octopus) or 5 min / 5 generations (Biomorpher). Results exported to Excel; top 10% filtered.

Tested on 12 GB RAM / Intel Core i5 8th gen laptop — hardware constraint acknowledged.

Key limitation: structural stability unassessed. Current shapes "may not fully capture structural realities of tensioned fabric canopies." Thermal comfort beyond shadow % not evaluated.

## Relevance to dissertation

**Highly relevant** on two fronts:

1. **Generative design workflow**: Directly demonstrates how Grasshopper plugins (Galapagos, Octopus, Biomorpher) can optimize shading canopy geometry for shadow performance — precisely the type of parametric optimization the dissertation may employ. The Biomorpher finding is practically actionable.

2. **Textile/lightweight canopy construction**: The GFRP + knitted membrane hybrid structure is a compelling lightweight, potentially retractable-adjacent system. Its wide-span capability (3–200 m) and low mass are relevant for typhoon-context design, though wind resistance is not addressed here.

**Gap for dissertation**: No wind resistance analysis — critical for typhoon conditions. No thermal comfort beyond shadow %. Hot-arid context, not humid-hot. No retractability or adaptability mechanism. The structural FEA gap is explicitly acknowledged and represents a direct research opportunity.

## Connections

- [[shading-structures]] — primary source for generative design of shading canopies; saddle-form tensile geometry
- [[parametric-design-tools]] — Biomorpher vs. Octopus vs. Galapagos comparison; shadow optimization workflow in Grasshopper
- [[thermal-comfort]] — shadow coverage as proxy for comfort; cites Cairo 10 °C shaded/unshaded differential
- Complements [[ghoniem-2025-albedo-shading-thermal-comfort]] — both study canopy shading in Cairo but from different angles: Ghoniem quantifies UTCI reduction, Hassan optimizes canopy geometry
- [[lyu-2026-computational-delivery-framework]] — Hassan's generative workflow (Phase 1: encoding intent) maps onto Lyu's CDF encoding phase; Hassan's FEA gap maps onto Lyu's "validating intent" phase

## Quotes & data

- "Biomorpher outperformed other plugins, achieving the highest shadow coverage in the shortest time." (abstract)
- "Shape No. 301 emerged as the best solution, with shadow percentage coverage of 98.36%, 95.80%, and 94.73% at 9 a.m., 12 p.m., and 2 p.m. respectively along with a total area of 27.05 m²." (p. 893–894)
- "Biomorpher demonstrated a performance that was 200% better than Galapagos and 20% more efficient than Octopus." (p. 901)
- "In Cairo, summer temperatures reach up to 50 °C, while shaded areas typically experience around 10 degrees lower." (p. 876)
- "Tree canopies can reduce the temperature from the generated shadows by 3.5–7.7 °C." (p. 876)
- Membrane spans: "3 to 200 m" (Kamal 2020, cited p. 877)
