---
name: comps-analysis
description: "Runs a trading comparables (Comps) analysis for a stock against its peer group. Use when the user says 'Comps 분석', 'peer comparison', 'trading multiples', 'how does [company] compare to peers', 'relative valuation', or 'comp sheet'. Produces an Excel comp sheet with peer multiples, implied valuation range, and a positioning chart."
---

When the user requests a Comps analysis, proceed as follows:

## Required inputs
Ask for any missing items:
- **Target company / Ticker**
- **Peer group** (ask user to confirm or suggest sector-appropriate peers — typically 5–10 companies)
- **Multiples to use** (defaults: EV/EBITDA, EV/Revenue, P/E, P/B, EV/EBIT)
- **Year(s)** (NTM = next twelve months preferred; also include LTM = last twelve months)

## Comp sheet structure (Excel output)

Build one Excel workbook with these tabs using the xlsx skill:

### Tab 1: Trading Comps Table
Columns per company:
| Company | Ticker | Mkt Cap | EV | EV/Revenue | EV/EBITDA | EV/EBIT | P/E | P/B | Net Debt/EBITDA | EBITDA Margin | Revenue Growth |
|---------|--------|---------|----|-----------|-----------|---------|----|-----|----------------|--------------|---------------|

- Highlight the target company row in a distinct color
- Show mean, median, 25th percentile, 75th percentile at the bottom
- Shade outliers (> 2 standard deviations from mean)

### Tab 2: Implied Valuation
- Apply median and mean multiples to the target's metrics
- Show implied EV and implied share price for each multiple
- Football field chart showing valuation range across methods

### Tab 3: Scatter Charts
- Plot EV/EBITDA vs. EBITDA margin growth (bubble = market cap)
- Plot P/E vs. EPS growth (PEG visualization)
- Label each bubble with ticker

### Tab 4: Premium / Discount Analysis
- Target's current multiple vs. peer median: premium or discount %
- Historical premium/discount trend if data is available
- Commentary on whether premium/discount is justified

## Output
- Produce Excel file (.xlsx) via the xlsx skill
- Name the file: `[Ticker]_Comps_YYYYMMDD.xlsx`
- Summarize key takeaways in chat: "Target trades at X% premium/discount to peers on EV/EBITDA; implied price range is KRW/USD X–Y"
- Flag any peers that distort the median (e.g., loss-making companies inflating P/E)
