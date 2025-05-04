# 📉 Drawdown-Triggered Capital Boost Strategy (2019–2024)

A **personally developed**, long-only tactical allocation strategy that deploys extra capital when others panic — transforming deep drawdowns into calculated opportunities. 
This project was independently conceived and built from scratch using Python and vectorized logic to simulate disciplined, risk-aware re-entry.

---

## 📌 Strategy Overview

This project explores a contrarian allocation philosophy: **exit** when a stock suffers a steep drawdown, and **re-enter with more capital** when the price shows signs of recovery. 
The approach mimics a disciplined value investor who avoids catching falling knives but strikes when the crowd realizes the world isn’t ending.

| **Parameter**       | **Setting**                                  | **Purpose**                                           |
|---------------------|-----------------------------------------------|--------------------------------------------------------|
| Initial Capital     | $100 per stock                                | Easy-to-track sizing across 12 names                  |
| Drawdown Threshold  | ‑50% from 252-day high                        | Filters routine noise; captures true capitulation     |
| Re-entry Rule       | Price recovers to 50% below peak              | Avoids early re-entry into downtrends                 |
| Capital Boost       | +10% of original capital on re-entry          | Simulates value investor with spare cash              |
| Weighting           | Daily equal-weight portfolio                  | Prevents single stock domination                      |
| Benchmark           | SPY, with $100 initial stake                  | Apples-to-apples comparison                           |

---

## 🧠 Strategy Logic

- 💰 **Start**: Allocate $100 per stock across 12 tickers.
- 📉 **Drawdown Exit**: If a stock falls more than 50% below its 1-year peak → exit to cash.
- 🔄 **Re-entry & Boost**: If the price rebounds to the drawdown threshold → re-enter with +10% more capital.
- ⚖️ **Portfolio Logic**: All equities are daily rebalanced for equal weighting across positions.

This strategy is **fully vectorized** for speed and transparency — no black-box backtest libraries were used.

---

## 🛠️ Tech Stack

- `pandas` – time-series processing
- `numpy` – mathematical calculations
- `matplotlib` – performance plotting
- `yfinance` – historical market data
- 🧠 **No black-box backtest packages** — all custom logic

---

## 🧪 Backtest Details

- **Tickers**: `["AMZN", "WMT", "NVDA", "F", "CVX", "GOOGL", "JNJ", "JPM", "COST", "TSM", "BLK", "GLD"]`
- **Benchmark**: `SPY`
- **Date Range**: Jan 2019 – Dec 2024
- **Capital Deployed**: $1,470 (initial + re-entry boosts)

---

## 📈 Results Summary

| **Metric**        | **Strategy Portfolio** | **SPY Benchmark** |
|-------------------|------------------------|-------------------|
| Final Value       | USD 6,710.76           | USD 3,798.51      |
| CAGR              | 29%                    | 17%               |
| Sharpe Ratio      | 1.32                   | 0.90              |
| Max Drawdown      | 33%                    | 34%               |
| ROI               | **4.57×**              | **2.58×**         |
| T-value           | 3.23                   | 2.20              |
| p-value           | 0.0016                 | 0.03              |

---

## 📊 Visuals

### Equity Curve vs SPY

![Strategy Equity Curve](Drawdown%20Strategy%20Returns.jpg)

### Summary Table

![Returns Table](Portfolio%20returns%20table.jpg)

---

## 🧠 Interpretation

Despite a comparable drawdown to SPY, this strategy generated **+12 percentage points in annual CAGR** and a **Sharpe Ratio 46% higher**. The p-value indicates the excess return is statistically significant, not a fluke.

It shows that **structured, behaviorally-aware capital boosting** can materially outperform passive buy-and-hold — without excessive complexity.

---

## 🎯 Why This Matters (for Recruiters & Practitioners)

| Signal | Value |
|--------|-------|
| ✅ Tactical portfolio construction | Understands allocation beyond naive buy-hold |
| ✅ Risk-aware alpha generation     | Combines Sharpe, Drawdown, CAGR with real triggers |
| ✅ Original strategy design        | No templated logic or copied models |
| ✅ Market intuition meets code     | Human behavioral insights → executable logic |
| ✅ Recruiter-friendly keywords     | `Sharpe`, `CAGR`, `T-stat`, `backtesting`, `alpha`, `dynamic allocation` |

---

## 🧭 How to Run This Notebook

1. Clone this repo:
   ```bash
   git clone https://github.com/your-username/Drawdown-Capital-Boost.git

---
🧠 Author’s Note
This strategy was not copied from an academic paper or forum post — it was conceptualized, built, and refined independently to test a simple question:

Can disciplined re-entry sizing beat passive investing?

The answer, at least here, is yes.

---
⚠️ Disclaimer
This project is for educational and research purposes only.
It is not investment advice, and no results are guaranteed in real-world conditions.
Use at your own risk.

---
