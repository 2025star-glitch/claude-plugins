---
name: dcf-valuation
description: "Builds a DCF (Discounted Cash Flow) valuation model for any stock. Use when the user says 'DCF 해줘', 'intrinsic value of [company]', 'discounted cash flow model', 'what is [ticker] worth', or 'valuation model'. Produces an Excel workbook with FCF projections, WACC calculation, terminal value, sensitivity table, and implied share price."
---

When the user requests a DCF valuation, gather inputs and build the model as follows:

## Required inputs
Ask for any missing items:
- **Company / Ticker**
- **Revenue growth assumptions** (near-term 3–5 years, terminal growth rate)
- **EBIT margin trajectory**
- **Tax rate**
- **CapEx as % of revenue**
- **Working capital assumptions**
- **WACC** (or component inputs: risk-free rate, beta, equity risk premium, debt cost, capital structure)
- **Projection horizon** (default: 5 years explicit + terminal value)

If the user says "use reasonable assumptions," apply sector-appropriate defaults and state them explicitly.

## Model structure (Excel output)

Build an Excel workbook with these tabs using the xlsx skill:

### Tab 1: Assumptions
| Parameter | Value | Notes |
|-----------|-------|-------|
| Risk-free rate | % | |
| Equity risk premium | % | |
| Beta | | |
| Cost of equity | % | |
| Pre-tax cost of debt | % | |
| Tax rate | % | |
| WACC | % | |
| Terminal growth rate | % | |

### Tab 2: FCF Projection
- Revenue → EBIT → NOPAT → FCF for each projection year
- Show all line items: D&A, CapEx, change in working capital
- Format: color-coded (blue for inputs, black for formulas)

### Tab 3: Valuation Bridge
- PV of FCFs (sum of discounted free cash flows)
- Terminal value (Gordon Growth or EV/EBITDA exit multiple)
- PV of terminal value
- Enterprise value
- Net debt bridge → Equity value → Implied share price
- Current price vs. implied price → upside/downside %

### Tab 4: Sensitivity Analysis
- 2D sensitivity table: WACC (x-axis) vs. terminal growth rate (y-axis)
- Second table: WACC vs. exit EV/EBITDA multiple
- Color gradient: green (upside) → red (downside) vs. current price

### Tab 5: Scenario Analysis
| Scenario | Revenue CAGR | EBIT Margin | WACC | TV Growth | Implied Price | Upside |
|----------|-------------|-------------|------|-----------|--------------|--------|
| Bull | | | | | | |
| Base | | | | | | |
| Bear | | | | | | |

## Output
- Produce Excel file (.xlsx) via the xlsx skill
- Name the file: `[Ticker]_DCF_YYYYMMDD.xlsx`
- State all key assumptions explicitly in the chat summary
- Flag which assumptions are most sensitive to the valuation
- Note data quality (e.g., "Revenue growth based on analyst consensus — verify against latest guidance")
