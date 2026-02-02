# Project 2 – Factor-Based Portfolio Construction

## Objective
Design, evaluate, and improve a momentum-based factor portfolio across
major asset classes, with explicit consideration of transaction costs
and risk management.

## Asset Universe
- SPY (US equities)
- IWM (US small caps)
- EFA (Developed ex-US)
- EEM (Emerging markets)
- TLT (Long-duration bonds)
- IEF (Intermediate bonds)
- GLD (Gold)

## Methodology
- Daily returns computed from adjusted prices
- 12-month momentum signal (252 trading days), skipping the most recent 21 days
- Monthly rebalancing
- Top-3 assets selected by momentum each month
- Equal-weight allocation among selected assets
- Benchmark: equal-weight portfolio of all assets

## Transaction Costs
- Monthly turnover explicitly modeled
- Transaction cost assumption: 10 bps per unit turnover
- Net-of-cost performance evaluated

## Strategy Improvements
- Volatility targeting applied with a 10% annualized volatility target
- Exposure scaled using rolling 63-day realized volatility
- Volatility scaling improved Sharpe ratio and reduced drawdowns

## Results (Net of Costs)
- Annual Return: ~8.4%
- Annual Volatility: ~10.4%
- Sharpe Ratio: ~0.81
- Maximum Drawdown: ~-15%

## Key Takeaways
- Factor performance is highly sensitive to implementation details
- Transaction costs materially reduce raw factor returns
- Risk management techniques can meaningfully improve risk-adjusted performance

## Tools
Python, pandas, numpy, matplotlib, yfinance
