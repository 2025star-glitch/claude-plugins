---
name: sector-analysis
description: "Produces a comprehensive sector or industry analysis report. Use when the user says '섹터 분석', 'industry analysis', 'sector overview for [industry]', 'breakdown of the [sector] sector', 'supply chain analysis', or 'competitive landscape of [industry]'. Produces a Word report covering industry dynamics, supply chain, competitive structure, valuation benchmarks, and top picks."
---

When the user requests a sector analysis, produce the following:

## Required inputs
Ask for any missing items:
- **Sector / Industry** (e.g., Korean battery, US semiconductors, global luxury goods)
- **Scope** (domestic only, global, or specific region)
- **Focus area** (supply chain / competitive dynamics / valuation / all)

## Sector analysis structure (Word output)

Produce a Word document (.docx) using the docx skill:

### Section 1: Sector snapshot
- Definition and scope of the sector
- Total addressable market (TAM) size and growth rate
- Key macro drivers (interest rates, commodity prices, regulation, technology shifts)
- Cycle position: early expansion / mid-cycle / late cycle / downturn

### Section 2: Industry structure and competitive dynamics
- **Porter's Five Forces** assessment (brief — 1–2 sentences per force)
- Market concentration: HHI index or top-3 share
- Key competitive dimensions: price, technology, brand, distribution, scale
- Recent M&A activity and implications

### Section 3: Supply chain map
- Upstream → Midstream → Downstream breakdown
- Key raw materials and sourcing risks
- Critical chokepoints (geopolitical, logistics, single-source dependencies)
- Winners and losers from supply chain shifts

### Section 4: Sector valuation benchmarks
| Metric | Sector Average | Range (low–high) | vs. Historical Avg | vs. Market |
|--------|---------------|------------------|--------------------|-----------|
| EV/EBITDA | | | | |
| P/E | | | | |
| EV/Revenue | | | | |
| P/B | | | | |
| Dividend yield | | | | |

### Section 5: Key sector KPIs
List the 5–8 most important operating KPIs for this sector and explain what they signal:
- Example for semiconductors: book-to-bill ratio, DRAM spot price, fab utilization rate
- Example for retail: same-store sales growth, inventory turns, gross margin
- Example for pharma: R&D pipeline stage, patent cliff exposure, reimbursement rates

### Section 6: Company positioning matrix
- 2x2 matrix: Growth vs. Quality (or relevant axes for the sector)
- Place major sector players
- Identify leaders, challengers, niche players, laggards

### Section 7: Themes and catalysts (12-month horizon)
- Top 3 structural themes driving the sector
- Key catalysts: regulatory changes, technology inflections, demand shifts
- Risk factors to monitor

### Section 8: Top picks and avoid list
| Stance | Ticker | Rationale | Key risk |
|--------|--------|-----------|----------|
| Top pick | | | |
| Top pick | | | |
| Avoid | | | |

## Output
- Produce Word document (.docx) via the docx skill
- Name: `[Sector]_SectorAnalysis_YYYYMMDD.docx`
- Length: 12–20 pages equivalent
- Include data sources for all key statistics
