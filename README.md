

# Survivor Options Strategy Backtest

A Python-based backtesting framework for a **NIFTY options selling strategy** with configurable entry gaps, strike selection logic, stop loss, target, position controls, and performance analytics.

---

# Strategy Highlight

🚀 **Backtested Return (2024)**
**265.93% annual return on NIFTY options strategy**

This result was generated using the historical **2024 NIFTY spot and options dataset** with predefined risk controls.

The strategy focuses on:

* systematic options selling
* rule-based entries
* strict risk management
* controlled position sizing

⚠️ Results are based on **historical backtesting** and are **not guaranteed future performance**.

---

# Overview

This project tests a **rule-based options selling strategy on NIFTY spot and options data**.

The strategy is designed to:

* Monitor **spot price movement**
* Trigger **PE / CE entries based on configurable gap thresholds**
* Select **option contracts using strike distance rules**
* Apply **risk management using stop loss and target**
* Limit **maximum open positions**
* Generate **performance analysis and visual summaries**

---

# Key Features

* User-configurable strategy inputs
* PE and CE side execution logic
* Risk controls (stop loss / target / max open positions)
* Backtesting on historical **NIFTY spot and options data**
* Tradebook generation
* P&L analysis
* Visual performance charts
* Monthly performance heatmaps

---

# Performance Result

Backtest summary for **2024**

| Metric         | Value           |
| -------------- | --------------- |
| Total Return   | **265.93%**     |
| Strategy Type  | Options Selling |
| Underlying     | NIFTY 50        |
| Data Frequency | 1-minute        |
| Year Tested    | 2024            |

This strategy captures **premium decay and directional movements using systematic entry triggers**.

---

# Data

Due to GitHub file size limitations, the **full options dataset (~900MB)** is **not included in this repository**.

Instead, the repository includes:

```
data/NIFTY_OPTIONS_SAMPLE.parquet
```

This is a **small sample dataset** provided only to:

* Understand the **data schema**
* Test the **code structure**
* Verify that the notebook runs correctly

For full backtesting, the **complete dataset must be generated locally**.

---

# How to Generate Full Dataset

### Step 1 — Download raw dataset

Download the historical NIFTY options dataset from Kaggle:

[https://www.kaggle.com/datasets/senthilkumarvaithi/historical-nifty-options-2024-all-expiries](https://www.kaggle.com/datasets/senthilkumarvaithi/historical-nifty-options-2024-all-expiries)

---

### Step 2 — Run the data consolidation notebook

Execute the notebook:

```
FNO 2024 Nifty50 Data Consolidator.ipynb
```

This notebook processes the downloaded expiry-wise files and generates a **single consolidated dataset required by the strategy**.

It will produce:

```
NIFTY_OPTIONS_2024_CONSOLIDATED.parquet
```

---

### Step 3 — Place file inside the data folder

Move the generated file into:

```
data/NIFTY_OPTIONS_2024_CONSOLIDATED.parquet
```

Once this file is present, the **backtest notebook will run using the full dataset**.

---

# Project Structure

```
survivor-options-strategy/
│
├── survivor_strategy_backtest.ipynb
├── README.md
├── requirements.txt
├── .gitignore
│
└── data/
    ├── README.md
    ├── NIFTY_OPTIONS_SAMPLE.parquet
    └── NIFTY_OPTIONS_2024_CONSOLIDATED.parquet
```

---

# Strategy Inputs

The notebook allows users to configure:

* PE gap trigger
* CE gap trigger
* Stop loss %
* Target %
* Lot size
* Strike step
* Square-off time
* Max open positions
* Backtest date range

---

# Outputs

The framework generates:

* Tradebook
* Strategy P&L
* Performance charts
* Monthly P&L heatmaps
* Risk metrics

---

# Requirements

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# Disclaimer

This project is intended **for research and educational purposes only**.

The reported **265.93% return is based on historical backtesting using 2024 data** and does not account for:

* transaction costs
* slippage
* liquidity constraints
* execution delays

Real trading performance may differ significantly.

