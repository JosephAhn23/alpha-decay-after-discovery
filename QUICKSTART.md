# Quick Start Guide

## Installation

```bash
# Install dependencies
pip install -r requirements.txt
```

## Run the Analysis

```bash
# Launch Jupyter
jupyter notebook alpha_decay_research.ipynb
```

Or:

```bash
jupyter lab alpha_decay_research.ipynb
```

## What You'll Get

1. **Signal Definitions**: 4 simple signals (momentum, mean reversion, volatility breakout, MA crossover)

2. **Discovery Proxies**: Conservative dates for when signals became "known"

3. **Decay Analysis**: Pre vs post-discovery performance metrics:
  : Sharpe Ratio
  : Hit Rate
  : Maximum Drawdown
  : Statistical significance tests

4. **Control Analysis**: Tests whether decay correlates with:
  : Volatility regimes
  : Liquidity
  : Transaction costs
  : Crowding

5. **Visualizations**: Charts showing signal decay patterns

## Customization

### Change the Asset

Edit the notebook cell:

```python
ticker = 'QQQ'  # Or any ticker symbol
```

### Change Signals

```python
selected_signals = ['momentum_12_1', 'mean_reversion']  # Pick your signals
```

### Change Discovery Proxy

```python
proxy_name = 'academic'  # Options: 'academic', 'book', 'blog', 'conservative', 'aggressive'
```

## Expected Results

- Most signals will show some decay after discovery
- Not all decay will be statistically significant
- Decay patterns may vary by market regime

**This is correct and expected.** Negative or boring results are the right outcome.

## Next Steps

1. Run the full notebook end-to-end
2. Review the results and interpretations
3. Try different signals or proxies
4. Extend with multi-asset analysis
5. Write up your conclusions

---

Remember: This project is about **understanding why you cannot win**, not how to win.

