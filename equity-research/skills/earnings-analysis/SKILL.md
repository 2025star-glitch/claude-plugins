---
name: earnings-analysis
description: "Analyzes post-earnings results for a company, including financial metrics, guidance, and conference call nuances. Use when the user says '실적 분석', 'earnings analysis', 'break down [company] results', 'how did [ticker] do this quarter', 'Q[N] results analysis', or 'conference call analysis'. Produces a Word report covering actuals vs. consensus, segment performance, guidance read-through, and long-term fundamental implications."
---

When the user requests a post-earnings analysis, gather the data and produce the report as follows:

## Required inputs
Ask for any missing items:
- **Company / Ticker** and **reporting quarter** (e.g., Q2 2025)
- **Actual results** (user can paste the press release, earnings table, or key numbers)
- **Consensus estimates** (Bloomberg, FactSet, or user's own estimates)
- **Conference call transcript or key management quotes** (paste or attach)

If actual data is not provided, state clearly that numbers are from public sources and may not be final.

## Earnings analysis structure (Word output)

Produce a Word document (.docx) using the docx skill:

### Section 1: Headline verdict (1 paragraph)
- Beat / Miss / In-line on revenue and EPS
- Quality of the beat: organic vs. one-time, recurring vs. non-recurring
- Market reaction context (stock up/down X% — note if provided)

### Section 2: Actuals vs. consensus table
| Metric | Actual | Consensus | Surprise % | vs. Prior Quarter | vs. Prior Year |
|--------|--------|-----------|-----------|------------------|---------------|
| Revenue | | | | | |
| Gross profit | | | | | |
| EBITDA | | | | | |
| Operating income | | | | | |
| Net income | | | | | |
| EPS | | | | | |
| FCF | | | | | |

### Section 3: Segment deep-dive
- Break down revenue and margin by business segment
- Identify which segments drove the beat/miss
- Volume vs. price/mix analysis where applicable

### Section 4: Guidance read-through
- Company guidance vs. prior guidance vs. consensus
- Implied Q-o-Q and Y-o-Y growth in guidance
- Management confidence level: raised / maintained / cut / withdrawn
- Key swing factors management highlighted

### Section 5: Conference call analysis — tone and nuances
This is critical. Analyze beyond the numbers:
- **Management tone**: confident / cautious / defensive / evasive
- **Key themes repeated**: count how many times certain words/topics appear (e.g., "macro uncertainty," "pricing power," "AI investment")
- **What they emphasized vs. what they avoided**
- **Analyst Q&A**: which questions got direct answers vs. deflections
- **Noteworthy quotes**: pull 3–5 verbatim quotes with significance explained

### Section 6: Long-term fundamental implications
Answer these questions explicitly:
1. Does this quarter change the structural earnings power of the business?
2. Has the competitive position strengthened, weakened, or held?
3. Are margins structurally expanding or compressing?
4. Does management's capital allocation remain value-creating?
5. Revise or maintain prior thesis — and why?

### Section 7: Estimate revisions
- Updated revenue / EBITDA / EPS estimates for next 2 years
- Explain the change drivers
- Revised target price if applicable

## Output
- Produce Word document (.docx) via the docx skill
- Name: `[Ticker]_Earnings_Q[N]YYYY_YYYYMMDD.docx`
- Lead with the verdict — busy PMs read the first paragraph only
- Flag any data that relies on estimates or incomplete information
