# IPL Player Price Prediction

Predicting IPL auction prices for batsmen, bowlers, and all-rounders using domestic and international cricket statistics.

---

## Overview

IPL auction prices depend on a complex mix of domestic performance, international experience, age, and team demand. This project builds separate ML models for each player type to predict their auction price, giving franchises a data-driven way to evaluate players before bidding.

---

## Dataset

**Sources:**
- IPL batting and bowling stats (2016–2022) from Kaggle
- International player stats manually collected from Cricbuzz

**Player categories:** Batsmen · Bowlers · All-rounders

**Key features used:**
- Batting: Average (Avg), Strike Rate (SR)
- Bowling: Economy Rate (Econ), Bowling Strike Rate
- Non-cricket: Age, Country, Team
- Target: `SOLD_PRICE` (auction price in INR)

---

## Approach

**Preprocessing:**
- Label encoding for `Country` and `Team` columns
- Derived missing batting/bowling metrics from existing features
- Feature selection using correlation matrix
- Missing value handling with forward fill (`ffill`)

**Modeling strategy:**
- Trained separate models for batsmen, bowlers, and all-rounders
- Compared three input combinations: IPL stats only · International stats only · Both combined

**Models evaluated:**
- Linear Regression
- Ridge Regression
- Lasso Regression
- Decision Tree Regressor
- Random Forest Regressor

**Evaluation metrics:** MSE · MAE · R²

---

## Results

| Player Type | Best Model |
|---|---|
| Batsmen | Random Forest Regressor |
| Bowlers | Linear Regression |
| All-rounders | Random Forest Regressor |

---

## Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- Jupyter Notebook
- Matplotlib / Seaborn

---

## Files

```
├── player price prediction.ipynb   # Main notebook with full analysis
├── Dataset/                        # IPL + International stats CSVs
└── README.md
```

---

## Goal

To help IPL franchises make smarter, data-backed decisions during auctions — identifying undervalued players and avoiding overpaying based on historical performance data.
