---
name: investment-memo
description: "Writes an investment memo with Bull, Base, and Bear case scenarios for a stock. Use when the user says '투자 메모', 'investment memo', 'bull bear case', 'thesis for [company]', 'write up on [ticker]', or 'make the case for/against [stock]'. Produces a concise Word document structured as a hedge-fund style investment memo."
---

When the user requests an investment memo, produce the following:

## Required inputs
Ask for any missing items:
- **Company / Ticker**
- **Investment horizon** (short: <6 months, medium: 6–18 months, long: 18+ months)
- **Starting position** (long / short / initiating)

## Investment memo structure (Word output)

Produce a Word document (.docx) with these sections using the docx skill:

### Section 1: Headline (1 paragraph)
- One punchy sentence: what is the trade, why now, what is the return potential
- Example: "[Company] is a misunderstood compounder trading at a 40% discount to intrinsic value; the catalyst is [event] in [timeframe]."

### Section 2: Situation summary (bullet points)
- What the company does (2–3 sentences max)
- Why the market has mis-priced it (the "edge")
- Key catalyst(s) that will close the gap

### Section 3: Scenario analysis
| | Bull | Base | Bear |
|-|------|------|------|
| Probability | % | % | % |
| Key assumption | | | |
| Revenue (FY+2) | | | |
| EBITDA margin | | | |
| EV/EBITDA | | | |
| Implied price | | | |
| Return | % | % | % |

- Weight scenarios by probability → expected value
- Time-weighted IRR for each scenario

### Section 4: The bull case (200–300 words)
- Strongest arguments for owning the stock
- Specific evidence: data points, industry trends, management track record

### Section 5: The bear case (200–300 words)
- Most credible counterarguments
- What would make this thesis wrong
- Mitigants to each bear argument

### Section 6: Catalysts and timeline
| Catalyst | Expected date | Magnitude | Probability |
|----------|--------------|-----------|-------------|

### Section 7: Position sizing and exit
- Recommended position size rationale
- Stop-loss level and conditions
- Profit-taking plan

## Output
- Produce Word document (.docx) via the docx skill
- Name: `[Ticker]_InvestmentMemo_YYYYMMDD.docx`
- Keep total length to 2–4 pages — institutional memos are dense, not long
- Use tables and bullet points over prose wherever possible
