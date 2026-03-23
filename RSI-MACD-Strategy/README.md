# TradingView RSI & MACD Strategy Indicator

A custom TradingView strategy script combining the Relative Strength Index (RSI) and Moving Average Convergence Divergence (MACD) indicators to generate buy and sell signals.

## Features
- **RSI Confirmation**: Filters trades by ensuring the RSI is in an oversold (buy) or overbought (sell) territory.
- **MACD Crosses**: Uses the MACD signal line crossovers as the primary trigger for entries and exits.
- **Visual Shapes**: Plots "BUY" and "SELL" labels directly on the chart to visualize historical entries.
- **Configurable Settings**: All lengths and thresholds can be adjusted in the TradingView settings dialog.

## How to use
1. Open [TradingView](https://www.tradingview.com/).
2. Open a chart for your preferred asset.
3. Click on the **Pine Editor** tab at the bottom of the screen.
4. Replace any existing code with the contents of `strategy.pine`.
5. Click **Add to Chart**.
6. Adjust parameters via the indicator settings wheel to backtest it on different timeframes and assets.

## Logic Overview
- **Go Long (Buy)**: Triggers when the MACD line crosses above the MACD signal line, AND the RSI is at or below the Oversold threshold (default 30).
- **Close Long (Sell)**: Triggers when the MACD line crosses below the MACD signal line, AND the RSI is at or above the Overbought threshold (default 70).
