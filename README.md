# Portfolio Optimization: Dhaka Stock Exchange (DSE) vs. Global Equities

## Executive Summary
This project evaluates investment strategies comparing domestic equities listed on the **Dhaka Stock Exchange (DSE)** against 
a globally diversified portfolio of **US Multinationals (NYSE/NASDAQ)**. 

Using historical return distributions, multi-stage Dividend Discount Models (DDM), Capital Asset Pricing Model (CAPM) 
estimations, variance-covariance matrices, and algorithmic trade execution scripts, the project demonstrates how global asset 
allocation significantly mitigates localized macroeconomic and systematic risks.

---

## 📊 Portfolio Performance & Quantitative Backtest Results

A total initial balance of **$1,000 USD** was allocated across optimized US multi-asset portfolios to test model execution, 
short-selling constraints, and algorithmic trade signals.

| Metric | Portfolio A (LLY, WMT, JPM, V) | Portfolio B (KO, MA, COST, XOM) |
|---|---|---|
| **Capital Executed** | $818.54 | $532.05 |
| **Cash Held** | $181.46 | $467.95 |
| **Final Portfolio Balance** | **$820.30** | **$534.42** |
| **1-Day Net Return** | **+0.2144%** | **+0.4464%** |
| **Annualized Return (ROI)** | **71.57%** | **207.19%** |
| **Core Traded Assets** | WMT (Long), JPM (Short) | KO (Long) |

---

## 🤖 Algorithmic Trade Execution Log

### Portfolio A Execution
* **Walmart (WMT) - Long:** Purchased 1 share at **$107.48** $\rightarrow$ Sold at **$108.66** (Net Gain: **+$1.18**).
* **JPMorgan Chase (JPM) - Short:** Short-sold 2 shares at **$355.53** $\rightarrow$ Repurchased at **$355.24** (Net Gain: **+$0.58**).
* **Supporting Assets (LLY & V):** Validated signal directional movements without triggering sub-portfolio rebalancing threshold.

### Portfolio B Execution
* **Coca-Cola (KO) - Long:** Purchased 6 shares at **$88.67** $\rightarrow$ Sold at **$89.07** (Net Gain: **+$2.37**).
* **Empty Sell Side:** No assets met short-selling conditions, leaving cash unallocated to preserve capital.

---

## 🇧🇩 Domestic DSE Market Analysis & CAPM Estimation

The study analyzed four representative domestic assets: **Kohinoor Chemicals (KHCH)**, 
**Orion Infusion (ORION)**, **IPDC Finance (IPDC)**, and **Envoy Textiles (ENVOY)**.

* **Risk-Free Rate ($R_f$):** 10.43% (20-Year Bangladesh Treasury Bond yield).
* **Expected Market Return ($R_m$):** 12.00% (Normalized historical DSE return).
* **Market Risk Premium ($R_m - R_f$):** 1.57%.

| Stock | Beta ($\beta$) | CAPM Expected Return | Actual 1-Year Return | Valuation & Risk Note |
|---|---|---|---|---|
| **Kohinoor Chemicals (KHCH)** | -0.60 | 9.49% | +5.50% | Powerful defensive shock absorber; low leverage ($D/E = 0.12$). |
| **Orion Infusion (ORION)** | -1.75 | 7.68% | -35.31% | Idiosyncratic risk failure despite low systematic beta; current ratio < 1.0. |
| **IPDC Finance (IPDC)** | 0.01 | 10.45% | +48.91% | Zero-beta market independence; rally driven by firm-specific catalysts. |
| **Envoy Textiles (ENVOY)** | 0.15 | 10.67% | +14.42% | Low P/E (8.49x); strong dollar-denominated cash flows from denim exports. |

---

## 📁 Repository Structure

* `Fin435 REPORT.pdf` — Full academic research paper and literature review.
* `Fin435 DSE PART FINAL..xlsx` — DSE stock time-series, variance-covariance matrix, Sharpe ratio optimization, and DDM valuations.
* `portfolio_output A..csv` — Algorithmic execution log for Portfolio A (WMT, JPM, LLY, V).
* `portfolio_output B.csv` — Algorithmic execution log for Portfolio B (KO, MA, COST, XOM).

---
**Authors:** Rahik Rahman, Faiyaj Rafiq, Nafis Rahman, Kazi Sanjida Yasmin, Safayet Ahmed Rohan  
**Instructor:** Hasan Mohammed Sami (HAS), Department of Accounting & Finance, North South University
