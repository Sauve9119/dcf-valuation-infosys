# DCF Valuation Model — Infosys (INFY)

A Python-based **Discounted Cash Flow (DCF) valuation model** to estimate the intrinsic value of Infosys (INFY) using real financial data from Yahoo Finance, with sensitivity analysis and visualizations.

📈 **Result: Intrinsic Value = $15.59 | Market Price = $12.09 | 29% Upside → BUY Signal**

---

## What is DCF?

DCF (Discounted Cash Flow) is a valuation method that estimates a company's intrinsic value based on its future cash flows, discounted back to today's value using WACC (Weighted Average Cost of Capital).

> Money today is worth more than money tomorrow — DCF accounts for this via discounting.

---

## Methodology

```
Historical Financials (yfinance)
        ↓
Free Cash Flow Calculation (OCF - CapEx)
        ↓
5-Year FCF Projection (8% growth rate)
        ↓
WACC Calculation (10.5%)
        ↓
Terminal Value (Gordon Growth Model, 3% g)
        ↓
Enterprise Value → Intrinsic Value per Share
        ↓
Sensitivity Analysis (25 WACC × Growth combinations)
```

---

## Key Assumptions

| Parameter | Value | Justification |
|---|---|---|
| FCF Projection Growth | 8% | Conservative — between revenue growth (3.45%) and historical FCF growth (15.63%) |
| WACC | 10.5% | Risk-Free Rate 7% + Beta 0.7 × ERP 5% |
| Terminal Growth Rate | 3% | Approx. India long-term GDP growth |
| Projection Period | 5 years | Standard DCF horizon |

---

## Results

| Metric | Value |
|---|---|
| Current Market Price | $12.09 |
| Intrinsic Value | $15.59 |
| Upside Potential | 29% |
| Enterprise Value | $63.16B |
| PV of 5-yr FCFs | $17.44B |
| PV of Terminal Value | $45.72B |

**Verdict: UNDERVALUED — Potential BUY Signal**

---

## Sensitivity Analysis

Intrinsic value across 25 combinations of WACC (8.5%–12.5%) and Terminal Growth Rate (2%–4%):

| | 8.5% WACC | 9.5% WACC | 10.5% WACC | 11.5% WACC | 12.5% WACC |
|---|---|---|---|---|---|
| 2.0% g | $18.68 | $16.12 | $14.17 | $12.63 | $11.38 |
| 2.5% g | $19.93 | $17.02 | $14.84 | $13.14 | $11.79 |
| 3.0% g | $21.41 | $18.05 | $15.59 | $13.71 | $12.23 |
| 3.5% g | $23.19 | $19.26 | $16.46 | $14.36 | $12.73 |
| 4.0% g | $25.36 | $20.69 | $17.46 | $15.09 | $13.28 |

> Even at conservative WACC (11.5%) and low terminal growth (2%), intrinsic value ($12.63) exceeds market price ($12.09) — BUY signal is robust.

---

## Tech Stack

| Category | Tools |
|---|---|
| Language | Python |
| Data Source | yfinance (Yahoo Finance API) |
| Data Handling | Pandas, NumPy |
| Visualization | Matplotlib |
| Environment | Google Colab |

---

## Project Structure

```
├── DCF_Valuation_Infosys.ipynb   # Full model notebook
├── dcf_fcf_projection.png         # FCF historical vs projected chart
├── dcf_sensitivity_heatmap.png    # Sensitivity analysis heatmap
└── README.md
```

---

## Run It Yourself

```bash
git clone https://github.com/Sauve9119/dcf-valuation-infosys.git
```

Open `DCF_Valuation_Infosys.ipynb` in Google Colab and run all cells.

**Requirements:**
```
yfinance
pandas
numpy
matplotlib
```

---

## Author

**Rachit Gupta**
B.Tech Mechanical Engineering | MNIT Jaipur
[LinkedIn](https://www.linkedin.com/in/rachit-gupta-4ba904321/) | [GitHub](https://github.com/Sauve9119)
