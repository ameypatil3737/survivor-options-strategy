# Survivor Options Strategy Backtest

A Python-based backtesting framework for a systematic **NIFTY options selling strategy** with configurable entry gaps, strike selection logic, stop loss, target, position controls, and performance analytics.

The strategy generated **₹6,27,822 backtested profit in 2024**, equivalent to **313.91% return on assumed capital** and **139.52% return on estimated deployed capital**, using historical NIFTY spot and options data.

---

# Strategy Highlight

🚀 **Backtested Performance (2024)**

**₹6,27,822 total backtested profit**
**313.91% return on assumed capital**
**139.52% return on estimated minimum deployed capital**

The strategy is designed around:

* systematic options selling
* rule-based entries
* strict risk management
* controlled position sizing

Results are produced using **historical 2024 NIFTY spot and options data**.

⚠️ Results are based on **historical backtesting** and do **not guarantee future performance**.

---

# Overview

This project implements a **rule-based options selling strategy on NIFTY spot and options data**.

The framework:

* monitors **NIFTY spot price movement**
* triggers **PE / CE option selling based on gap thresholds**
* selects option contracts using **strike distance rules**
* manages risk using **stop loss and target levels**
* limits **maximum simultaneous open positions**
* generates **tradebook and performance analytics**

Signals are generated using **5-minute candles derived from 1-minute raw data**.

---

# Key Features

* User-configurable strategy inputs
* Systematic PE and CE execution logic
* Risk controls

  * stop loss
  * target
  * max open positions
* Backtesting on historical **NIFTY spot and options data**
* Automated tradebook generation
* Strategy P&L calculation
* Performance charts
* Monthly P&L heatmaps
* Risk metrics

---

# Performance Result

Backtest summary for **2024**

| Metric                              | Value           |
| ----------------------------------- | --------------- |
| Total Profit                        | **₹6,27,822**   |
| Return on Assumed Capital           | **313.91%**     |
| Return on Estimated Minimum Capital | **139.52%**     |
| Total Trades                        | **863**         |
| Win Rate                            | **56.43%**      |
| Average Profit per Trade            | **₹727.49**     |
| Max Drawdown                        | **-₹2,61,683**  |
| Strategy Type                       | Options Selling |
| Underlying                          | NIFTY 50        |
| Raw Data Frequency                  | **1-minute**    |
| Strategy Execution Frequency        | **5-minute**    |
| Year Tested                         | **2024**        |

This strategy captures **option premium decay and directional movements using systematic entry triggers**.

---

# Best Parameter Setup Found

| Parameter          | Value    |
| ------------------ | -------- |
| PE Gap             | **30**   |
| CE Gap             | **20**   |
| PE Symbol Gap      | **100**  |
| CE Symbol Gap      | **100**  |
| Target %           | **0.70** |
| Stop Loss %        | **0.50** |
| Max Open Positions | **3**    |

---

# Capital Interpretation

Based on the backtest:

* **Total backtested profit:** ₹6,27,822
* **Assumed capital:** ₹2,00,000
* **Estimated minimum investment capital:** ₹4,50,000

Returns:

* **Return on assumed capital:** 313.91%
* **Return on estimated minimum capital:** 139.52%

The strategy generated **₹6.27 lakh profit during 2024** with controlled risk parameters and position limits.

---

# Data

Due to GitHub file size limitations, the **full options dataset (~900MB)** is not included in the repository.

Instead, a **sample dataset** is provided:

```
data/NIFTY_OPTIONS_SAMPLE.parquet
```

This sample dataset allows users to:

* understand the **data schema**
* verify that the **notebook runs correctly**
* test the **strategy logic**

To run a full backtest, the complete dataset must be generated locally.

---

# How to Generate Full Dataset

### Step 1 — Download Raw Dataset

Download the historical NIFTY options dataset from Kaggle:

[https://www.kaggle.com/datasets/senthilkumarvaithi/historical-nifty-options-2024-all-expiries](https://www.kaggle.com/datasets/senthilkumarvaithi/historical-nifty-options-2024-all-expiries)

---

### Step 2 — Run Data Consolidation Notebook

Execute the notebook:

```
FNO 2024 Nifty50 Data Consolidator.ipynb
```

This notebook processes expiry-wise files and produces a **single consolidated dataset** required by the strategy.

The output file will be:

```
NIFTY_OPTIONS_2024_CONSOLIDATED.parquet
```

---

### Step 3 — Place File in Data Folder

Move the generated file into:

```
data/NIFTY_OPTIONS_2024_CONSOLIDATED.parquet
```

Once this file is available, the **backtest notebook can run using the full dataset**.

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

Users can configure the following parameters:

* PE gap trigger
* CE gap trigger
* stop loss percentage
* target percentage
* lot size
* strike step
* square-off time
* maximum open positions
* backtest date range

These inputs allow testing multiple parameter combinations and optimizing strategy performance.

---

# Outputs

The framework produces:

* Tradebook
* Strategy P&L
* Equity curve
* Performance charts
* Monthly P&L heatmaps
* Risk statistics

---

# Requirements

Install required Python dependencies:

```
pip install -r requirements.txt
```

---

# Disclaimer

This project is intended **for research and educational purposes only**.

The reported performance of:

* **₹6,27,822 profit**
* **313.91% return on assumed capital**
* **139.52% return on estimated deployed capital**

is based on **historical backtesting using 2024 data** and does not account for:

* transaction costs
* slippage
* liquidity constraints
* execution delays

Actual trading results may differ significantly.
