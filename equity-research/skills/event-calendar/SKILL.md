---
name: event-calendar
description: "Builds a structured investment event calendar for stocks or a portfolio. Use when the user says '이벤트 캘린더', 'event calendar', 'upcoming catalysts', '주요 일정 정리', 'catalyst timeline', 'what events are coming for [ticker]', or 'key dates for my portfolio'. Produces a visual timeline of market-moving events organized by date with impact assessment."
---

When the user requests an event calendar, produce the following:

## Required inputs
Ask for any missing items:
- **Tickers / companies** (one stock, a basket, or portfolio)
- **Time horizon** (default: next 3 months; can extend to 12 months)
- **Event types to include** (default: all — see list below)
- **Focus**: high-impact only, or comprehensive

## Event types to track

Organize events into these categories:

### Corporate events
- Earnings announcements (date, time pre/post market)
- Analyst days / investor days
- AGM / shareholder meetings
- Dividend ex-dates and payment dates
- Lock-up expiration dates (for recent IPOs)
- Share buyback program milestones
- M&A closing dates / regulatory deadlines

### Clinical / regulatory (for biotech/pharma)
- FDA PDUFA dates
- Phase 2 / Phase 3 trial readouts
- Advisory committee meetings
- NDA/BLA submission deadlines
- IND filings

### Macro / policy events
- Central bank meetings (Fed, BOK, ECB, BOJ)
- Key economic data releases (CPI, NFP, GDP, PMI)
- Government policy announcements
- Tariff / trade decision deadlines

### Industry / sector events
- Product launches and unveilings
- Trade shows and conferences (CES, MWC, ASCO, etc.)
- Contract award announcements
- Regulatory approval deadlines for new products

## Event calendar output format

Produce an Excel workbook using the xlsx skill:

### Tab 1: Master calendar (chronological)
| Date | Day | Ticker | Event type | Event description | Expected impact | Probability | Bullish / Bearish | Action |
|------|-----|--------|-----------|------------------|----------------|-------------|------------------|--------|

- Sort by date ascending
- Color-code by event type (earnings = blue, regulatory = orange, macro = gray, corporate = green)
- Impact rating: High / Medium / Low
- Action column: Buy ahead / Sell ahead / Hold / Watch / Hedge

### Tab 2: By company
- Group events by ticker
- Show all events for each holding in one view

### Tab 3: Impact heat map
- Month × Company matrix
- Cell color intensity = number of high-impact events that month
- Quickly shows which months are "event heavy"

### Tab 4: Action checklist
For each high-impact event:
| Event | Date | Pre-event action (T-5 days) | Day-of action | Post-event action |
|-------|------|-----------------------------|--------------|------------------|

## In-chat summary
After producing the file, also provide in chat:
- Top 5 most important upcoming events (next 30 days)
- "Red zone" months where event density is highest
- Any events with binary outcomes (pass/fail, approval/rejection) requiring position management

## Output
- Produce Excel file (.xlsx) via the xlsx skill
- Name: `EventCalendar_YYYYMMDD.xlsx`
- Note clearly which events are confirmed vs. estimated dates
- If real-time data unavailable, mark estimated dates and ask user to verify
