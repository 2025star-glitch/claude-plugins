---
name: morning-note
description: "Generates a pre-market morning briefing note for investors. Use when the user says '모닝노트', '오늘 장 준비', 'morning note', 'pre-market briefing', '장 시작 전 정리', or 'today's market prep'. Summarizes overnight macro moves, key news, portfolio-relevant developments, and provides a daily investment action plan."
---

When the user requests a morning note, produce the following structured briefing:

## Required inputs
Ask for any missing items:
- **Date** (default: today)
- **Portfolio holdings** (user can paste tickers or describe positions — optional but recommended)
- **Focus markets** (Korea / US / both / global)
- **News or data** (user can paste overnight news, data releases, or macro moves; otherwise note that Claude will work from knowledge cutoff)

Important: If real-time data is not available, clearly state this and ask the user to paste current data. Do not fabricate prices or market levels.

## Morning note structure

Produce a concise, scannable note — designed to be read in 5 minutes before market open:

---

### 📅 [Date] Morning Note

#### 1. Overnight market snapshot
| Market | Level | Change | Change % |
|--------|-------|--------|---------|
| S&P 500 | | | |
| NASDAQ | | | |
| KOSPI futures | | | |
| USD/KRW | | | |
| US 10Y yield | | | |
| WTI crude | | | |
| Gold | | | |
| VIX | | | |

*If user has not provided data, insert [DATA NEEDED] and ask them to paste current levels.*

#### 2. Key macro events overnight
- List the 3–5 most market-moving developments
- Format: **[Category]** — What happened → Market implication (1 sentence each)
- Categories: Fed/central bank, economic data, geopolitical, currency, commodities

#### 3. Key news by sector
Group relevant overnight news by sector (only include sectors relevant to user's portfolio or specified focus):
- **Tech / Semis**: 
- **Healthcare / Bio**: 
- **Energy**: 
- **Financials**: 
- **Consumer**: 
- **Industrial / Defense**: 

#### 4. Portfolio holdings check
For each holding the user specified:
| Ticker | Overnight move | Driver | Action signal |
|--------|---------------|--------|--------------|
| | | | Watch / Add / Trim / Hold |

#### 5. Today's key events and data releases
| Time (KST) | Event | Consensus | Prior | Significance |
|-----------|-------|-----------|-------|-------------|

#### 6. Daily investment action plan
Provide a clear, prioritized action list for the trading day:

**Must-do today:**
- [Specific action with rationale]

**Watch list — act if triggered:**
- [Condition] → [Action]

**Avoid / sit out:**
- [What to avoid and why]

**Key levels to watch:**
- Support: [level] for [asset]
- Resistance: [level] for [asset]

---

## Output
- Deliver the morning note directly in chat (no file unless user requests one)
- Keep total length to one screen (~500 words) — brevity is the priority
- Use bold for anything requiring action
- Date and timestamp the note
- End with one "conviction call" — the single most important trade or observation for the day
