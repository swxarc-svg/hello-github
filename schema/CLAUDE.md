# PhD Research Wiki — Schema

## Identity

This is a personal academic knowledge base for a PhD dissertation on **outdoor public space shading systems in high-density cities under humid-hot climates and typhoon conditions**. The research sits at the intersection of design and technical axes, incorporating CFD wind simulation, Ladybug/Honeybee environmental analysis, and Grasshopper parametric design.

The wiki is maintained by an LLM agent (you). The human researcher directs sourcing, exploration, and critical judgment. You handle all summarising, cross-referencing, filing, and maintenance.

---

## Directory structure

```
phd-wiki/
├── raw/                    # Immutable source materials — NEVER modify
│   ├── papers/             # PDF research papers
│   ├── articles/           # Web articles converted to .md (via Obsidian Web Clipper)
│   ├── assets/             # Images, diagrams, downloaded figures
│   └── clips/              # Quick notes, screenshots, conference photos
├── wiki/                   # LLM-maintained knowledge base (Obsidian vault)
│   ├── sources/            # One page per ingested source (paper/article summary)
│   ├── concepts/           # Topic pages (e.g., "CFD wind simulation", "retractable shading")
│   ├── entities/           # People, institutions, projects, standards
│   ├── comparisons/        # Side-by-side analyses (e.g., "fixed vs retractable shading")
│   ├── synthesis/          # Literature review drafts, research gap analyses
│   ├── index.md            # Master catalog of all wiki pages
│   ├── log.md              # Chronological record of all operations
│   └── overview.md         # High-level research landscape summary
└── schema/
    └── CLAUDE.md           # This file — wiki operating instructions
```

---

## Page types and templates

### Source page (`wiki/sources/`)

Filename: `{first-author-lastname}-{year}-{short-title}.md`

```markdown
---
type: source
title: "{Full paper title}"
authors: [Author1, Author2]
year: 2024
journal: "Journal Name"
doi: "10.xxxx/xxxxx"
tags: [shading, CFD, humid-hot, typhoon, parametric, ...]
confidence: high | medium | low
date_ingested: YYYY-MM-DD
raw_path: "raw/papers/filename.pdf"
---

## Summary
2-3 paragraph summary of key contributions.

## Key findings
- Finding 1
- Finding 2

## Methodology
Brief description of research methods, simulation tools, experimental setup.

## Relevance to dissertation
How this connects to the researcher's specific focus.

## Connections
- [[concept-page]] — how this source relates
- Agrees with [[other-source]] on X
- Contradicts [[other-source]] on Y

## Quotes & data
Key statistics, figures, or direct quotes worth citing (with page numbers).
```

### Concept page (`wiki/concepts/`)

Filename: `{concept-name}.md`

```markdown
---
type: concept
title: "{Concept Name}"
tags: [relevant, tags]
source_count: N
last_updated: YYYY-MM-DD
---

## Definition
Clear definition of this concept.

## Current state of research
What the literature collectively says.

## Key debates & contradictions
Where sources disagree.

## Methods & tools
Common research methods for studying this concept.

## Related concepts
- [[other-concept]] — relationship description

## Sources
- [[source-1]] — what it contributes to this topic
- [[source-2]] — what it contributes
```

### Entity page (`wiki/entities/`)

For researchers, labs, institutions, standards, or notable projects.

```markdown
---
type: entity
title: "{Entity Name}"
entity_type: person | institution | project | standard
tags: []
last_updated: YYYY-MM-DD
---

## Overview
Who/what this is and why it matters.

## Key contributions
- Contribution 1 ([[source]])

## Connections
- Collaborates with [[entity]]
- Affiliated with [[entity]]
```

### Comparison page (`wiki/comparisons/`)

```markdown
---
type: comparison
title: "{X vs Y}"
tags: []
last_updated: YYYY-MM-DD
---

## Overview
Why this comparison matters for the dissertation.

## Comparison table
| Dimension | X | Y |
|-----------|---|---|
| ... | ... | ... |

## Analysis
Synthesis of which approach suits what context.

## Sources
```

### Synthesis page (`wiki/synthesis/`)

For literature review drafts, research gap analyses, theoretical framework development.

```markdown
---
type: synthesis
title: "{Topic}"
status: draft | in-progress | review-ready
tags: []
last_updated: YYYY-MM-DD
---

## Thesis / argument

## Section content

## Evidence map
Which sources support which claims.

## Gaps identified

## Next steps
```

---

## Operations

### Ingest

When the researcher adds a new source to `raw/`:

1. Read the source thoroughly.
2. Discuss key takeaways with the researcher if in interactive mode.
3. Create a source page in `wiki/sources/`.
4. Update `wiki/index.md` with the new entry.
5. Update or create relevant concept pages in `wiki/concepts/`.
6. Update or create relevant entity pages in `wiki/entities/`.
7. Check for contradictions with existing sources — flag them on both pages.
8. Append an entry to `wiki/log.md`.

A single source typically touches 5-15 wiki pages. Always preserve existing content — append and update, never overwrite.

### Query

When the researcher asks a question:

1. Read `wiki/index.md` to find relevant pages.
2. Read those pages.
3. Synthesize an answer with `[[wikilink]]` citations to wiki pages.
4. If the answer is substantial and reusable, offer to file it as a new page (comparison, synthesis, or concept expansion).

### Lint

Periodic health check. Look for:

- Orphan pages (no inbound links from other wiki pages)
- Stale claims superseded by newer sources
- Concept pages mentioned in text but not yet created (red links)
- Missing cross-references between related sources
- Inconsistent tags or metadata
- Sources with low confidence that need verification
- Research gaps — important subtopics with few or no sources

### File back

When a query produces valuable synthesis:

1. Ask the researcher if they want it filed.
2. Create an appropriate page type (usually synthesis or comparison).
3. Update index.md and relevant concept pages.
4. Log the operation.

---

## Conventions

### Wiki links
Use Obsidian-style `[[page-name]]` links. When referencing a specific section, use `[[page-name#section]]`.

### Tags
Use lowercase, hyphenated tags. Core tag taxonomy:
- **Climate**: `humid-hot`, `subtropical`, `tropical`, `typhoon`, `monsoon`
- **Design**: `shading`, `canopy`, `retractable`, `parametric`, `tensile`, `kinetic`
- **Technical**: `cfd`, `wind-simulation`, `ladybug`, `honeybee`, `grasshopper`, `fea`
- **Performance**: `thermal-comfort`, `wind-resistance`, `ventilation`, `utci`, `pet`
- **Context**: `high-density`, `public-space`, `urban`, `macau`, `hong-kong`, `southeast-asia`
- **Method**: `case-study`, `simulation`, `experiment`, `survey`, `review`

### Language
Write wiki content in **English** for academic compatibility. The researcher may communicate in Chinese; respond in whatever language they use, but wiki pages are always in English.

### Confidence scoring
- **high**: Peer-reviewed, well-cited, methodology is sound
- **medium**: Conference paper, preprint, or limited sample size
- **low**: Blog post, news article, anecdotal, or methodology concerns

### Citation format
In wiki prose, cite as `(Author, Year)` with a `[[wikilink]]` to the source page.

---

## Research context

### Core dissertation question
How can outdoor public space shading systems in high-density humid-hot cities be designed to provide effective everyday shading and ventilation while resisting or adapting to typhoon conditions?

### Key tensions
- Everyday performance (shade + airflow) vs. extreme weather resilience
- Fixed robust structures vs. retractable/kinetic systems
- Parametric optimisation vs. constructability
- Climatic responsiveness vs. structural simplicity

### Methodological toolkit
- CFD (computational fluid dynamics) for wind simulation
- Ladybug/Honeybee for environmental performance analysis
- Grasshopper for parametric design exploration
- Potentially physical wind tunnel testing for validation

---

## Notes for the LLM

- Always check `index.md` before creating a new page — it might already exist.
- When in doubt about categorisation, prefer concept pages over entity pages.
- Flag contradictions explicitly — they are research opportunities, not errors.
- Keep source summaries focused on what's relevant to the dissertation topic.
- When the wiki grows beyond ~50 sources, suggest building a search tool.
- Periodically remind the researcher to back up the wiki (it's just a git repo).
