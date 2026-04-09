# Log

Chronological record of all wiki operations. Each entry is tagged by type.

Format: `## [YYYY-MM-DD] type | description`

Types: `ingest` | `query` | `lint` | `file-back` | `maintenance`

---

## [2026-04-09] file-back | literature-review-report-draft

整理文獻梳理報告（第一階段），含文獻信息表（3篇）＋4個關鍵表：遮陽做法類型總表、空間類型×遮陽做法對照表、性能目標分類表、落地難點表。
頁面：[[literature-review-report-draft]]

## [2026-04-09] query | thermal comfort evaluation methods

Query: "What methods have been used to evaluate thermal comfort in shading studies?"
Sources consulted: Ghoniem 2025, Hassan 2025, Lyu 2026
Synthesis saved: [[thermal-comfort-methods]]

Key finding: ENVI-met + Ladybug is the only validated full-comfort workflow; Hassan uses shadow % as a fast proxy; no source includes wind-load comfort analysis — critical gap for typhoon context.

---

## [2026-04-09] ingest | ghoniem-2025-albedo-shading-thermal-comfort

Ingested: Ghoniem, Fahmy, Kamel (2025) — "Evaluating Urban Surface Materials: Albedo Optimization and Shading for Pedestrian Thermal Comfort in Hot-Arid Environments." *Civil Engineering and Architecture* 13(6): 4331–4352.

Key contributions to wiki:
- Quantitative benchmark: canopy shading reduces UTCI by 5–6.6 °C
- Albedo–MRT trade-off: higher albedo raises MRT up to 6 °C in unshaded conditions — cautionary finding
- Validated ENVI-met + Grasshopper/Ladybug dual-platform workflow (MRT R² = 0.924; Ta R² = 0.984)
- Updated: [[thermal-comfort-outdoor]], [[envi-met-simulation]], [[shading-structures]], [[surface-albedo]], [[parametric-design-tools]]

## [2026-04-09] ingest | hassan-2025-knitted-textile-canopies-generative-design

Ingested: Hassan, Torky, El-Mahdy (2025) — "Knitted Textile Canopies: A Rapid Generative Design Optimization Tool for Enhanced Shading Performance." *Nexus Network Journal* 27: 875–904.

Key contributions to wiki:
- Biomorpher outperforms Galapagos and Octopus for multi-objective shading optimization: 313 solutions in 5 min; all 4 goals achieved; optimal shape No. 301 = ~95–98% shadow coverage
- GFRP + knitted membrane hybrid structure capable of 3–200 m spans
- Explicit FEA gap acknowledged — direct research opportunity for typhoon wind analysis
- Updated: [[shading-structures]], [[parametric-design-tools]], [[thermal-comfort-outdoor]]

## [2026-04-09] ingest | lyu-2026-computational-delivery-framework

Ingested: Lyu, Zhao, Chen (2026) — "From Algorithmic Intent to Accountable Assembly: A Computational Delivery Framework for Digital Architecture." *E3S Web of Conferences* 683: 01012.

Key contributions to wiki:
- Proposes the Computational Delivery Framework (CDF): Encoding → Materializing → Validating intent
- Three systemic tensions: geometric freedom vs. fabrication feasibility; speculative prototypes vs. warrantable delivery; simulation optimism vs. institutional accountability
- Critique of MOO tools (Octopus, Wallacei): mask cultural biases; cannot capture qualitative values
- Updated: [[parametric-design-tools]], [[shading-structures]]

## [2026-04-09] maintenance | concept and index scaffolding

Created initial concept pages (retractable-shading-systems, cfd-wind-simulation, thermal-comfort-outdoor) and stub pages for envi-met-simulation, parametric-design-tools, shading-structures, surface-albedo. Updated index.md with all 3 ingested sources.
