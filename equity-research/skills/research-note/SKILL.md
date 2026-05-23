---
name: research-note
description: "Generates a professional equity research note for a given stock. Use when the user says 'write a research note', 'draft a report on [company]', 'initiate coverage on', 'analyze [ticker]', or requests a comprehensive company analysis. Produces a Word document (.docx) in institutional analyst style covering thesis, business overview, financials, valuation, risks, and investment recommendation."
---

When the user requests a research note or company analysis, follow these steps:

## Required inputs
Ask for these if not provided:
- **Ticker / Company name** (e.g., 005930.KS for Samsung, AAPL for Apple)
- **Market** (KOSPI, KOSDAQ, NYSE, NASDAQ, or other)
- **Target price** (optional — derive from DCF/Comps if not given)
- **Investment stance** (Buy / Hold / Sell / Not Rated)

## Research note structure

Produce the report in this order:

### 1. Cover page
- Company name, ticker, exchange
- Rating and target price
- Current price and upside/downside %
- Analyst date
- One-sentence investment summary

### 2. Investment thesis (200–300 words)
- Three to five key reasons to own or avoid the stock
- Catalysts: near-term (0–3 months), medium-term (3–12 months), long-term (1–3 years)

### 3. Business overview
- Segment breakdown with revenue contribution %
- Geographic exposure
- Competitive moat assessment (pricing power, switching costs, network effects, scale)
- Key customers and suppliers

### 4. Financial summary table
Include a 3-year historical + 2-year forward table:
| Metric | FY-2 | FY-1 | FY0E | FY+1E | FY+2E |
|--------|------|------|------|-------|-------|
| Revenue | | | | | |
| EBITDA | | | | | |
| Net income | | | | | |
| EPS | | | | | |
| P/E | | | | | |
| EV/EBITDA | | | | | |
| ROE | | | | | |

### 5. Valuation
- Primary method: EV/EBITDA or P/E with peer comparison
- Secondary method: DCF (if applicable)
- Implied target price derivation
- Bull / Base / Bear scenario table

### 6. Risk factors
- Upside risks (at least 3)
- Downside risks (at least 3)
- ESG / regulatory considerations

### 7. Appendix
- Detailed P&L, balance sheet, cash flow (3 years historical + 2 years forecast)
- Key assumptions

## Output format
- Save as a Word document (.docx) using the docx skill
- Use professional institutional formatting: section headers, tables, bold key metrics
- Language: Korean unless user specifies otherwise
- Length: 8–15 pages equivalent

## Style guidelines
- Write in the third person, active voice ("We initiate coverage with a Buy rating...")
- Lead with the most important insight in each section
- Quantify every claim with data (%, KRW/USD, multiples)
- Flag data gaps clearly rather than fabricating numbers
