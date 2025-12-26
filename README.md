# Alpha Decay & the Limits of Discovery

**Level-7 Meta-Quant Research Project**

---

## Research Question

> **Do simple technical signals lose effectiveness after they become widely known?**

This is **not** about finding alpha. It's about **measuring how alpha dies**.

---

## What This Project Tests

We are studying:

- **The limits of empirical discovery**: How quickly does knowledge diffuse?
- **The economics of attention**: What happens when signals become "common knowledge"?
- **Researcher selection bias**: Why do retrospective studies find so much alpha?
- **How humans mistake noise for opportunity**: The psychology of pattern recognition

**Level-7 quant work is about understanding why you *cannot* win, not how to win.**

---

## Project Structure

### Core Modules

- **`signals.py`**: Simple, well-known signal definitions (momentum, mean reversion, volatility breakout, MA crossover, value)
- **`discovery_proxies.py`**: Proxies for when signals became "known" (academic papers, books, blogs)
- **`decay_analysis.py`**: Performance metrics and decay measurement (Sharpe, hit rate, drawdown)
- **`controls.py`**: Alternative explanations (volatility regimes, liquidity, transaction costs, crowding)
- **`data_utils.py`**: Data loading and preparation utilities

### Main Notebook

- **`alpha_decay_research.ipynb`**: Complete research workflow from signal computation to conclusions

---

## Methodology

### Step 1: Choose Simple Signals

We select 3-5 well-known signals. No fancy ML. If it feels "too basic," we're doing it right.

**Selected signals:**
- 12-1 Month Momentum (Jegadeesh-Titman style)
- Short-Term Mean Reversion
- Volatility Breakout (Bollinger Bands style)
- Moving Average Crossover (Golden/Death Cross)
- Value Factor (Book-to-Market proxy)

### Step 2: Define Discovery Proxies

This is the hardest and most interesting part. We are not claiming *the exact* discovery moment: only a **reasonable proxy**.

**Proxy types:**
- **Academic Paper**: First major academic publication
- **Popular Book**: First appearance in widely-read practitioner books
- **Blog Mentions**: Widespread mentions in quant blogs
- **Conservative**: Earliest date (most conservative)
- **Aggressive**: Latest date (assumes decay starts later)

### Step 3: Split Time Pre- vs Post-Discovery

For each signal:
- Measure performance **before** discovery proxy
- Measure performance **after** discovery

**Metrics:**
- Sharpe Ratio
- Hit Rate
- Maximum Drawdown
- Mean Return
- Stability across regimes

**Important:** We do **not** optimize parameters separately. That would contaminate the test.

### Step 4: Control for Alternative Explanations

This is what makes this Level-7. We test whether decay correlates with:

- Market efficiency (liquidity, volume)
- Volatility regime
- Transaction costs
- Crowding proxies

We're not just saying "it died": we're asking **why**.

### Step 5: Accept the Likely Conclusion

The result will probably be:

> "Most simple signals exhibit measurable decay after discovery, but the rate varies by market structure and cost sensitivity."

That is an **excellent** result. Negative or boring conclusions are **the correct outcome**.

---

## Installation

```bash
# Install dependencies
pip install -r requirements.txt
```

### Required Packages

- pandas, numpy, scipy, statsmodels: Data analysis and statistics
- yfinance: Financial data
- matplotlib, seaborn: Visualization
- scikit-learn: Machine learning utilities
- jupyter, notebook: Interactive analysis

---

## Usage

### Run the Research Notebook

```bash
jupyter notebook alpha_decay_research.ipynb
```

Or:

```bash
jupyter lab alpha_decay_research.ipynb
```

### Customize Analysis

**Change signals:**
```python
selected_signals = ['momentum_12_1', 'mean_reversion', 'volatility_breakout']
```

**Change discovery proxy:**
```python
proxy_name = 'academic'  # or 'book', 'blog', 'conservative', 'aggressive'
```

**Change data source:**
```python
ticker = 'QQQ'  # Or use multiple assets for portfolio analysis
```

---

## What Makes This Project Impressive (Even If It Fails)

✓ **We study the research process itself**: Meta-analysis of discovery

✓ **We explicitly acknowledge:**
 : Data-snooping
 : Survivorship bias
 : Hindsight bias

✓ **We are not claiming tradability**: This is research, not a trading system

✓ **Most quants never attempt this**: It requires intellectual honesty

---

## Expected Write-Up Style

A strong conclusion should sound like:

> "Our results suggest that the discovery of simple signals is constrained not by creativity but by structural limits imposed by competition, liquidity, and cost. The apparent abundance of alpha in retrospective studies likely reflects selection bias rather than persistent inefficiency."

This sentence alone signals maturity.

---

## Why This Is NOT a Student Flex Project

❌ No leaderboard  
❌ No PnL screenshot  
❌ No "I beat the market"  
✅ Mostly negative results

That's exactly why it works.

---

## Key Insights

1. **Discovery proxies are imperfect**: We acknowledge uncertainty in when signals became "known"

2. **Decay is multi-dimensional**: Not just Sharpe, but hit rate, drawdown, stability

3. **Controls matter**: Decay might be explained by structural factors, not just discovery

4. **Negative results are valid**: If signals don't decay, that's also interesting

5. **The process is the product**: Understanding *why* we can't find alpha is more valuable than finding alpha

---

## Limitations and Future Work

### Current Limitations

- Discovery dates are proxies, not exact moments
- Single asset analysis (SPY): could extend to portfolios
- Simplified transaction costs
- Limited crowding proxies

### Future Extensions

- Multi-asset portfolio analysis
- Alternative discovery proxies (citation analysis, patent filings)
- Machine learning signals (test if ML signals decay faster)
- Cross-asset class analysis (equities vs bonds vs commodities)
- Real-time decay monitoring (signals discovered in last 5 years)

---

## References and Inspiration

### Academic Papers

- Jegadeesh & Titman (1993): Momentum
- Fama & French (1992): Value factor
- Lo & MacKinlay (1990): Mean reversion
- Harvey et al. (2016): "The Challenge of Replicating Factor Returns"

### Books

- "Advances in Financial Machine Learning": López de Prado (2018)
- "The Quants": Patterson (2010)
- "A Man for All Markets": Thorp (2017)

### Blogs and Resources

- QuantStart
- Alpha Architect
- SSRN Finance Papers

---

## License

This is a research project. Use it for learning and research purposes.

---

## Author Notes

This project asks the **right impossible question**. It doesn't try to make money: it **earns respect** by acknowledging the limits of what we can know.

Anyone who finds this boring is not ready for it.

---

**One sentence truth:**

> **Level-7 quant work is about understanding why you *cannot* win, not how to win.**

