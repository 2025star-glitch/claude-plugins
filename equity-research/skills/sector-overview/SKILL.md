---
name: sector-overview
description: "Generates a quick-reference sector overview covering industry trends, supply chain, competitive structure, and average valuation multiples. Use when the user says '섹터 개요', 'sector overview', 'industry snapshot', '[sector] 산업 요약', 'give me the lay of the land for [industry]', 'sector primer', or 'help me understand the [industry] space'. Produces a concise briefing — shorter than a full sector analysis."
---

When the user requests a sector overview, produce the following concise briefing:

## Required inputs
Ask for any missing items:
- **Sector / Industry** (e.g., 2차전지, K-beauty, US defense, global shipping)
- **Depth** (quick primer = 1 page / standard overview = 3–5 pages)
- **Audience** (new to the sector / familiar with basics)

## Sector overview structure

Produce a clean, scannable overview — this is a primer, not a deep dive:

---

### 🏭 [Sector name] — Sector Overview

#### 1. Industry definition and size
- What the sector does in 2–3 sentences
- Global / Korean market size (USD or KRW)
- Growth rate: CAGR over last 3 years and next 3 years (estimated)
- Maturity stage: nascent / growth / mature / declining

#### 2. Macro drivers (top 3–5)
For each driver:
- **[Driver name]**: How it affects the sector → current direction (tailwind / headwind / neutral)

Example format:
- **금리 인상**: 자본집약적 기업의 WACC 상승 → 밸류에이션 압박 (현재: 헤드윈드)
- **AI 수요 확대**: 데이터센터 전력 수요 급증 → 전력장비 업체 수혜 (현재: 테일윈드)

#### 3. Supply chain overview
Draw the value chain in text format:
```
[원재료] → [중간재 / 부품] → [완제품 제조] → [유통] → [최종 소비자]
```
- List 2–3 key companies at each stage
- Flag bottlenecks or concentration risks (e.g., "NAND flash: Samsung + SK하이닉스 = 70% share")

#### 4. Competitive landscape
- Number of major players globally / in Korea
- Market structure: monopoly / oligopoly / fragmented
- Basis of competition: price / technology / brand / scale / relationships
- Korean players' global position (leader / follower / niche)

Top players quick table:
| Company | Ticker | Country | Market share | Competitive edge |
|---------|--------|---------|-------------|-----------------|

#### 5. Sector average valuation multiples
| Multiple | Current | 3Y average | 5Y average | vs. KOSPI / S&P 500 |
|---------|---------|-----------|-----------|----------------------|
| EV/EBITDA | | | | |
| P/E | | | | |
| EV/Revenue | | | | |
| P/B | | | | |
| Dividend yield | | | | |

Note: Are current multiples above or below history? Why?

#### 6. Key sector KPIs to monitor
List 5–8 leading indicators specific to this sector:
| KPI | What it measures | Where to find it | Bullish signal | Bearish signal |
|-----|-----------------|-----------------|--------------|---------------|

#### 7. Recent sector news and trends (last 3 months)
- 3–5 most significant developments
- Format: **[Date approx]** — What happened → Implication for sector

#### 8. Quick investment framework
- **Best time to buy**: when in the cycle / at what valuations
- **Best stocks to own** in bull vs. bear cycle (different characteristics)
- **Red flags to watch**: what signals sector deterioration

---

## Output
- Deliver overview directly in chat for quick reading
- Keep to 1–2 screens for a "quick primer" request
- Offer to expand into full sector-analysis if user wants depth
- Flag that all market data should be verified against current sources
