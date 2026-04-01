# 📊 PortfolioIQ — HackNova 1.0 (2026)
### *Advanced Quantitative Analysis & Risk-Adjusted Portfolio Construction*

**Venue:** HBTU Kanpur  
**Track:** Financial Analytics / Data Science  
**Core Objective:** To outperform the Nifty 50 benchmark through data-driven stock selection and risk-weighted allocation.

---

## 🚀 Project Overview
PortfolioIQ is an end-to-end financial pipeline that transforms raw NSE market data into an optimized investment strategy. The project evaluates 15 blue-chip stocks across **Banking, IT, and Pharma** sectors, utilizing 2 years of historical data (2023–2024) to build a high-alpha portfolio.

## 🛠️ Methodology & Pipeline

### **Task 1: Data Engineering**
* **Extraction:** Automated retrieval of OHLCV data via `yfinance`.
* **Quality Audit:** 8-point validation suite (TC1-TC8) ensuring no negative prices, extreme jumps (>50%), or excessive missing trading days.
* **Cleaning:** Implemented a `ffill(limit=5)` and `bfill(limit=2)` strategy to handle NSE holidays and data gaps.

### **Task 2: Quantitative Analysis**
* **Risk-Return Modeling:** Calculation of Annualized Returns, Volatility, and Max Drawdown.
* **Sharpe Ratio:** Performance benchmarking against a **6.5% Risk-Free Rate**.
* **Technical Indicators:** Tracking **Golden Cross** and **Death Cross** signals using SMA-50 and SMA-200.

### **Task 3: Correlation & Diversification**
* **Heatmap Analysis:** Visualizing sector dependencies. 
* **Diversification:** Reducing portfolio variance by pairing low-correlation assets (e.g., Banking vs. Pharma).

### **Task 4: Strategic Portfolio Construction**
* **Portfolio A (Baseline):** Equal-weight allocation (₹66,667 per stock).
* **Portfolio B (Strategic):** High-conviction allocation (₹10,00,000 total) excluding underperformers and overweighting high-Sharpe stocks like **SUNPHARMA** and **HCLTECH**.

---

## 📈 Key Performance Results (2023-2024)

| Metric | Portfolio A | **Portfolio B (Strategic)** | NIFTY 50 |
| :--- | :--- | :--- | :--- |
| **Annualised Return** | 24.94% | **34.56%** | 15.26% |
| **Sharpe Ratio** | 1.62 | **2.28** | 0.72 |
| **Max Drawdown** | -8.27% | **-8.23%** | -10.93% |

---

## 📂 Project Structure
* `HackNova1_0.ipynb`: Main analysis notebook.
* `task1_master_ohlcv.csv`: Cleaned historical price data.
* `task2_metrics_summary.csv`: Computed financial ratios.
* `task2_signals_summary.csv`: Technical trend signals.
* `portfolio_metrics_comparison.png`: Visual performance audit.

## 🧠 Conclusion
Portfolio B achieved a **Sharpe Ratio of 2.28**, significantly outperforming the Nifty 50 (0.72). This proves that active sector-tilting and rigorous risk-