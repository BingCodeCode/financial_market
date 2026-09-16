# AI Boom vs. Dot-Com Bust: A Statistical Autopsy of Two Market Manias

*Part 1 of a series on market bubbles and long-term investing.*

Notebook: [AI_bubble.ipynb](AI_bubble.ipynb)

## Goal

Compare the S&P 500's current AI-driven rally (2023-present) to the dot-com bubble (1997-2002) using data rather than opinion, to get a sense of what to expect as a long-term S&P 500 investor.

## What the notebook covers

1. **Shape & volatility comparison** - normalize both eras to a common start value and compare annualized volatility.
2. **Curve alignment & correlation** - find the trading-day shift that maximizes correlation between the two smoothed price curves.
3. **Log returns: day-to-day dynamics** - compare price-level correlation vs. daily log-return correlation at the best-fit shift.
4. **Return distribution & volatility dynamics** - skewness, kurtosis, and rolling volatility, limited to dot-com's pre-crash run-up for a fair comparison.
5. **Drawdowns & recovery** - worst peak-to-trough decline during each era's run-up and how long it took to recover.
6. **12-month holding period returns** - best/worst/median rolling 12-month returns for each era.

## Key findings

- **Similar shape, different mechanics:** shifted ~132 trading days, price trajectories correlate 0.985, but daily log returns barely correlate (-0.029) - the two booms move for different reasons day-to-day.
- **Calmer overall, but fatter tails:** the AI era has lower daily volatility than dot-com's run-up, but far more extreme outlier days (kurtosis 13.3 vs 3.5).
- **Similar drawdowns and recovery speed:** despite different tail behavior, worst pullback-while-climbing and recovery time are nearly identical.
- **Every 12-month holding period in the AI era so far has stayed positive**; dot-com's eventually didn't once its crash entered the rolling window.

## Data source

S&P 500 (`^GSPC`) daily price data via `yfinance`.

## Requirements

`matplotlib`, `numpy`, `pandas`, `yfinance`, `scipy`
