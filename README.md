# IPL Player Price Prediction

Predicting IPL auction prices for batsmen, bowlers, and all-rounders using IPL and international cricket statistics.

---

## Overview

IPL auction prices are influenced by a complex mix of batting, bowling, and non-cricketing factors like age and nationality. This project trains separate ML models for each player type to predict their auction price, and compares performance across different combinations of domestic vs. international stats.

---

## Dataset

**Curated and published on Kaggle:** [IPL Player Stats Dataset](https://www.kaggle.com/datasets/saivarunreddy1904/ipl-player-stats-dataset) — 7,900+ views, 1,500+ downloads

The dataset combines:
- **IPL stats** (2016–2022) — batting average, strike rate, economy rate, bowling SR
- **International stats** — manually collected from Cricbuzz

**Player types covered:** Batsmen, Bowlers, All-rounders

**Key features:** Avg, SR (batting), Economy, SR (bowling), Age, Country, Team, SOLD_PRICE

---

## Approach

**Preprocessing:**
- Label encoding for `Country` and `Team` columns
- `SOLD_PRICE` column converted to numeric
- Missing values handled with forward fill (`ffill`)
- Feature selection based on correlation matrix
- Derived features: Batting Avg, SR, Economy filled from existing columns

**Modeling strategy:**
Three separate models trained per player type — one using only IPL stats, one using only international stats, and one using both combined. Best model selected per category based on evaluation metrics.

**Models evaluated:**
- Linear Regression
- Lasso Regression
- Ridge Regression
- Decision Tree Regressor
- Random Forest Regressor

**Evaluation metrics:** MSE, MAE, R²

---

## Results

| Player Type | Best Model |
|---|---|
| Batsmen | Random Forest Regressor |
| All-rounders | Random Forest Regressor |
| Bowlers | Linear Regression |

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
├── player price prediction.ipynb   # Full analysis notebook
├── Dataset/                        # IPL + International stats CSVs
└── README.md
```

---

## Use Case

IPL franchises can use this model to make data-driven bidding decisions during auctions, identifying undervalued players and optimizing team composition within budget constraints.
