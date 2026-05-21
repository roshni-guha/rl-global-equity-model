# Capital Fund — Quantitative Research

Two quantitative trading models built on a proprietary backtesting and simulation engine.

---

## RL Global Equity Allocator

A PPO reinforcement learning agent that rotates across six global equity ETFs and cash using a macro-momentum state vector.

- **Training period:** 2004–2013
- **Out-of-sample (2014–2025):** 13.3% annualised return, Sharpe 0.75 — matching SPY with reduced drawdown
- **Hybrid overlay:** drawdown-differential rule cuts max drawdown from −34.6% to −30.0% (Calmar 0.38 → 0.41)
- **Portfolio integration:** integrates positively into a mean-variance portfolio alongside AMMA sector models

**Files:** [RLGlobalEquity_clean.ipynb](RLGlobalEquity_clean.ipynb) · [RLGlobalEquity.pdf](RLGlobalEquity.pdf) · [slides.pdf](slides.pdf)

---

## AMMA Momentum Model

A multi-lookback SPY momentum strategy (10/20/60/120/240-day) optimised via mean-variance portfolio construction with Ledoit-Wolf covariance shrinkage.

- **Universe:** 25 ETFs across global equity, fixed income, commodities, and crypto
- **Best individual model:** 60-day lookback — Sharpe 0.76, 8.4% annualised return (2004–2025)
- **Ensemble (mean-variance optimised):** Sharpe 0.76, with reduced correlation to SPY

**Files:** [AMMASPY.ipynb](AMMASPY.ipynb)

---

## Repository Structure

```
RLGlobalEquity_clean.ipynb   # RL model: training, backtesting, hybrid overlay, portfolio integration
AMMASPY.ipynb                # AMMA momentum model: signals, ensemble, mean-variance optimisation
main.tex                     # Research paper source (LaTeX)
slides.tex                   # Presentation source (Beamer)
RLGlobalEquity.pdf           # Compiled research paper
slides.pdf                   # Compiled presentation slides
*.png                        # Result charts
```
