---
name: earnings-preview
description: "Generates a pre-earnings preview report analyzing consensus estimates, company guidance, and earnings surprise/shock probability. Use when the user says '실적 프리뷰', 'earnings preview', 'before earnings', '실적 발표 전 분석', 'what to expect from [company] earnings', 'will [ticker] beat?', or 'consensus check before results'. Produces a Word report with expectation framework, surprise probability, and trading setup."
---

When the user requests an earnings preview, produce the following:

## Required inputs
Ask for any missing items:
- **Company / Ticker** and **upcoming reporting quarter** (e.g., Q2 2025)
- **Earnings date** (if known)
- **Consensus estimates** (user can paste; otherwise use available knowledge and flag as approximate)
- **Company guidance** (from most recent quarter's management commentary)
- **Recent channel checks or data points** (optional — user can share)

## Earnings preview structure (Word output)

Produce a Word document (.docx) using the docx skill:

### Section 1: Earnings snapshot
| Item | Detail |
|------|--------|
| Company | |
| Ticker | |
| Reporting date | |
| Time (pre/post market) | |
| Consensus EPS | |
| Consensus Revenue | |
| Company guidance | |
| Last quarter's actual | |
| Stock reaction last quarter | |

### Section 2: Consensus vs. guidance gap analysis
- Where does consensus sit relative to management's guidance?
- Is consensus above, in-line, or below the guidance midpoint?
- Has consensus been rising or falling over the past 30/60/90 days? (estimate revision trend)
- Conclusion: Is the bar set high or low going into the print?

### Section 3: Key metrics to watch
Identify the 3–5 metrics the market will focus on most this quarter:
| Metric | Consensus | Management guidance | Whisper number | Why it matters |
|--------|-----------|--------------------|----|----------------|

*"Whisper number" = the real market expectation beyond official consensus — often higher than consensus for momentum stocks*

### Section 4: Earnings surprise / shock probability assessment
Assess the probability of three outcomes:

**Earnings Surprise (beat + raise):**
- Supporting evidence: [list specific data points, channel checks, industry trends]
- Probability: X%

**In-line:**
- Scenario: Meets consensus but guidance unchanged
- Probability: X%

**Earnings Shock (miss or cut):**
- Risk factors: [list specific warning signs]
- Probability: X%

Key signal framework — check each:
- [ ] Order data / booking trends positive or negative?
- [ ] Recent competitor results as read-through?
- [ ] Supply chain / input cost dynamics changed?
- [ ] FX tailwind or headwind vs. prior guide?
- [ ] Macro environment better or worse than assumed in guidance?
- [ ] Management credibility: do they typically guide conservatively?

### Section 5: Historical earnings track record
| Quarter | EPS actual | EPS consensus | Surprise % | Stock reaction (1-day) |
|---------|------------|--------------|------------|----------------------|

- Pattern: consistent beater / mixed / frequent misser?
- Average 1-day stock move on earnings day (absolute %)
- Options-implied move going into this quarter (if user can provide)

### Section 6: Pre-earnings trading setup
Recommend a clear pre-earnings framework:

**If bullish:**
- Entry point and rationale
- Position size (consider binary risk around earnings)
- What to do if stock gaps up before the announcement

**If bearish / cautious:**
- Case for reducing exposure before the print
- Hedge options (e.g., put spreads if implied vol is reasonable)

**Regardless of direction:**
- Earnings date reminder
- Key levels to watch on the day

## Output
- Produce Word document (.docx) via the docx skill
- Name: `[Ticker]_EarningsPreview_Q[N]YYYY.docx`
- Lead with the verdict: "We expect a beat / in-line / miss based on..."
- Keep to 3–5 pages — this is an actionable note, not a full research report
- Flag all estimates as approximate if real-time data is unavailable
