
# Survivor Options Strategy Backtest

A Python-based backtesting framework for a NIFTY options strategy with configurable entry gaps, strike selection logic, stop loss, target, position controls, and performance analytics.

## Overview

This project tests a rule-based options selling strategy on NIFTY spot and options data.  
The strategy is designed to:

- Monitor spot price movement
- Trigger PE/CE entries based on configurable gap thresholds
- Select option contracts using strike distance rules
- Apply risk management using stop loss and target
- Limit open positions
- Generate performance analysis and visual summaries

## Key Features

- User-configurable strategy inputs
- PE and CE side logic
- Risk controls (stop loss / target / max open positions)
- Backtest on historical spot and options data
- Tradebook generation
- P&L analysis
- Visual performance charts

## Project Structure

```text
survivor-options-strategy/
│
├── survivor_strategy_backtest.ipynb
├── README.md
├── requirements.txt
├── .gitignore
└── data/
