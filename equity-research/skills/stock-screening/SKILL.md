---
name: stock-screening
description: "Screens for undervalued or thematic investment opportunities within a sector or market. Use when the user says '종목 발굴', 'stock screening', 'find undervalued stocks', '저평가 종목 찾기', 'screening for [theme]', 'which stocks benefit from [trend]', 'hidden gems in [sector]', or 'idea generation'. Produces a ranked list of investment candidates with thesis and screening criteria."
---

When the user requests stock screening or idea generation, proceed as follows:

## Required inputs
Ask for any missing items:
- **Universe** (KOSPI, KOSDAQ, S&P 500, NASDAQ, global, or specific sector)
- **Screening theme** — choose one or more:
  - Valuation: undervalued vs. peers / vs. history
  - Growth: high growth at reasonable price (GARP)
  - Quality: high ROIC, strong balance sheet, durable moat
  - Thematic: beneficiaries of a specific trend (AI, aging population, energy transition, etc.)
  - Event-driven: upcoming catalysts (FDA, contract, product launch)
  - Contrarian: out-of-favor stocks with improving fundamentals
- **Market cap preference** (large cap, mid cap, small cap, or all)
- **Risk tolerance** (conservative / moderate / aggressive)

## Screening framework

### Step 1: Define the opportunity
Clearly articulate the investment thesis driving this screen:
- What is the market getting wrong?
- Why should this opportunity exist now?
- What is the expected timeline for re-rating?

### Step 2: Screening criteria
Build a multi-factor screen based on the stated theme:

**For undervaluation screens:**
| Criterion | Threshold | Rationale |
|-----------|-----------|-----------|
| EV/EBITDA | < sector median | Cheaper than peers |
| P/B | < historical 25th percentile | Historically cheap |
| FCF yield | > 5% | Cash generative |
| Net debt/EBITDA | < 2x | Balance sheet strength |

**For thematic screens:**
| Criterion | Definition | How to measure |
|-----------|-----------|---------------|
| Revenue exposure to theme | >30% of revenue | Segment disclosure |
| Beneficiary type | Direct / Indirect | Value chain position |
| Competitive position in theme | Leader / Challenger | Market share data |

**For quality screens:**
| Criterion | Threshold |
|-----------|-----------|
| ROIC | > cost of capital (WACC) |
| Gross margin trend | Expanding or stable |
| Net debt | Net cash preferred |
| Earnings quality | FCF/Net income > 80% |

### Step 3: Candidate list
Present the top 5–10 stocks passing the screen:

| Rank | Ticker | Company | Market | Mkt Cap | Key metric 1 | Key metric 2 | Thesis (1 sentence) | Upside potential |
|------|--------|---------|--------|---------|-------------|-------------|--------------------|--------------------|

### Step 4: Deep dive on top 3 candidates
For each of the top 3 stocks, provide:

**[Company name] — [Ticker]**
- **Why it screens well**: specific data points
- **The edge**: what the market is missing
- **Key catalyst**: what will close the valuation gap / re-rate the stock
- **Main risk**: what could make this wrong
- **Recommended action**: buy now / wait for dip to [level] / watch for [trigger]

### Step 5: Portfolio fit assessment
- How do these ideas diversify the existing portfolio?
- Correlation risks (do they all move on the same macro factor?)
- Suggested position sizing framework (higher conviction = larger size, subject to risk limits)

## Output
- Deliver results directly in chat for quick scanning
- Offer to generate a Word or Excel file if user wants the detailed version
- Clearly label all screening criteria as a starting point for further diligence, not a final buy list
- Recommend priority order for further research

## Important disclaimer
Present these as research starting points, not final recommendations. Flag data quality, recency of financials, and the need for the user to verify current market conditions.
