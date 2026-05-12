# Acteck Method — Forecasting Reversals in Forex Currency Pairs

**Author:** Evgeniy Acteck  
**Repository:** `Acteck_Method_Scientific_Paper`  
**Scientific Paper:** [docs/Acteck_Method_Scientific_Paper.pdf](docs/Acteck_Method_Scientific_Paper.pdf)

---

## Project Description

This repository contains a scientific paper dedicated to the method of forecasting reversals in Forex currency pair movements, along with the mathematical apparatus and algorithmic description of the Acteck QA5 method.

### Scientific Paper

The full version of the scientific paper is available at:  
`docs/Acteck_Method_Scientific_Paper.pdf`

The paper describes:
- Mathematical foundation of the reversal forecasting method
- Algorithmic implementation of trend wave analysis
- Statistical probability estimation based on empirical distribution function
- Practical recommendations for applying the method in trading

---

## Method Overview

The Acteck QA5 method is a **non-parametric approach** for estimating the probability of trend exhaustion (reversal) on financial markets.

### Key Principles

1. **No parametric assumptions** — The method does not require assumptions about the distribution form of price movements
2. **Empirical CDF-based** — Probability is calculated as the value of the empirical cumulative distribution function of historical trend segment sizes
3. **Robust to outliers** — Rank-based nature ensures stability against extreme values
4. **Transparent interpretation** — Results have clear frequency-based probabilistic meaning

### Governing Equation

The core equation of the method:

**P(D) = (100/n) · Σᵢ₌₁ⁿ 1{ pipsᵢ × pt ≤ D } [%]**

Where:
- **P(D)** — Probability of trend exhaustion (reversal probability)
- **n** — Number of historical trend segments in the sample
- **pipsᵢ** — Size of i-th historical segment in pips
- **pt** — Point value for the financial instrument
- **D** — Current traversed distance from the last extremum
- **1{·}** — Indicator function (1 if condition is true, 0 otherwise)

**Interpretation:** The probability of trend reversal equals the percentage of historical trend movements that ended before reaching the distance already traversed by the current trend.

---

## Structure

```
.
├── README.md
├── LICENSE
└── docs/
    ├── Acteck_Method_Scientific_Paper.pdf  # Main scientific paper
    ├── generate_paper.py                    # Paper generation script
    └── paper_images/                        # Figures for reproducibility
        ├── page1_img0.png
        ├── page2_img0.png
        ├── ...
        └── page10_img0.png
```

---

## Method Features

### Three Analysis Modes

1. **Probability Mode** — Estimates reversal probability based on current distance
2. **Duration Mode** — Analyzes trend duration relative to historical averages
3. **Speed Mode** — Evaluates current wave speed (points per minute)

### Signal Quality Filtering

The method includes multi-factor filtering:
- Maximum correction thresholds (80% of trend, 60% from last extremum)
- Current deviation limits (40% of filter)
- Probability thresholds (71% for major pairs, 86% for cross-courses)

### Dynamic Target Estimation

Based on historical statistics of subsequent movements after reversals at similar probability levels.

---

## Statistical Foundation

The method is based on:
- **Glivenko-Cantelli Theorem** — Uniform convergence of empirical CDF
- **Dvoretzky-Kiefer-Wolfowitz Inequality** — Bounds on CDF estimation error
- **Extreme Value Theory (EVT)** — Analysis of tail probabilities
- **Survival Analysis** — Function of survival approach
- **Rank-based Nonparametric Methods** — Robust statistical procedures

---

## Applications

While developed for Forex trading, the method has potential applications in:
- Supply chain management
- Energy consumption forecasting
- Predictive maintenance of industrial equipment
- Medical diagnostics
- Climatology

---

## License

This project is licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0 International (CC BY-NC-ND 4.0)**.

This means you may:
- **Share** — Copy and redistribute the material in any medium or format

Under the following terms:
- **Attribution** — You must give appropriate credit to the author
- **NonCommercial** — You may not use the material for commercial purposes
- **NoDerivatives** — If you remix, transform, or build upon the material, you may not distribute the modified material

Full license text: [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/)

---

## Citation

If you use this method in your research, please cite:

```
Acteck, E. (2025). Method of Non-Parametric Estimation of Trend Exhaustion Probability 
Based on Empirical Distribution Function: Mathematical Apparatus, Software Implementation 
and Interdisciplinary Applications. Scientific Paper, Version 2.0.
```

---

## Copyright

- **Method Author:** Evgeniy Acteck
- **Scientific Paper:** Acteck Method — Forecasting Reversals in Forex Currency Pairs
- **Repository:** `Acteck_Method_Scientific_Paper`
- **License:** CC BY-NC-ND 4.0

---

## Contact

Email: makdak23@mail.ru
