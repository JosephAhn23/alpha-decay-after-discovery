📘 Alpha Decay vs Tradability
When Surviving Alpha Stops Paying
Overview

This repository extends prior work on alpha decay after discovery by addressing a more practical question:

When does a statistically valid signal stop being economically tradable?

Many signals persist in backtests long after publication, yet fail in live trading. This project studies why, focusing on transaction costs, turnover, slippage, and capacity constraints rather than statistical significance alone.

Motivation

Most quantitative research asks:
Does this signal work?

This project asks:
If it still works statistically, can it still be traded?

The gap between statistical edge and economic viability is a primary reason published strategies fail outside backtests.

Prior Work (Brief)

This project builds on a previous study of alpha decay after discovery, using the same fixed signal definitions and discovery proxies for consistency.

Signals studied:

12–1 Momentum

Short-term Mean Reversion

Volatility Breakouts

Moving Average Crossovers

The earlier work showed that:

Alpha decays gradually after discovery

Hit rates often remain near 50%

Statistical edge can persist long after publication

What This Project Adds

This project measures economic decay, not just statistical decay.

Core question:

At what point do costs and capacity constraints eliminate the remaining alpha?

The analysis explicitly models:

Transaction costs and slippage

Turnover-driven cost drag

Capital scalability and capacity limits

Core Hypothesis

Alpha decays in two stages:

Statistical decay
Edge weakens as information diffuses

Economic decay
Costs and crowding overwhelm residual edge

Most research stops at stage one. This project focuses on stage two.

Key distinction:

Statistical edge ≠ economic edge

Signals can retain hit rates > 50% while producing negative net returns

Methodology (High Level)

Signal definitions are frozen (no tuning or optimization)

Costs are added incrementally:

Commissions

Bid–ask spread

Slippage (volatility and volume scaled)

Turnover is treated as a first-class variable

Capacity is estimated using conservative participation assumptions

Metrics evaluated:

Gross vs net Sharpe

Break-even transaction costs

Capacity thresholds

PnL collapse vs hit rate persistence

Key Findings

High-turnover signals lose economic viability quickly, even when statistical edge persists

Hit rate persistence is largely orthogonal to profitability

Short-horizon mean reversion is untradable under realistic cost assumptions

Gross Sharpe is a poor proxy for tradability
