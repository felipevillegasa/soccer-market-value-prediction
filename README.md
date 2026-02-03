# Predicting Soccer Player Market Value Changes Using Performance Metrics

This project builds and evaluates machine learning models to predict season-over-season market value changes for professional soccer players using structured performance metrics.

---

## Overview
- **Goal:** Predict market value change using quantitative performance data.
- **Data:** Public player statistics and market values scraped from FBRef and soFIFA.
- **Approach:** End-to-end pipeline including scraping, preprocessing, EDA, feature engineering, and model evaluation.
- **Key finding:** Model performance varies by position; predictions are stronger for forwards than for midfielders and defenders.

---

## Data Collection (Key Engineering Work)
Data was collected using automated web scraping and required handling:
- CAPTCHA interruptions (manual intervention + random delays)
- profile URL redirections across timepoints

Final dataset includes **2,000+ players** across top European leagues.

---

## Modeling
Models evaluated include:
- Linear Regression (baseline)
- Random Forest (best-performing overall)
- Support Vector Machines (SVM)
- Neural Networks

In addition to a global model, **position-specific models** (FW/MF/DF) were trained to account for role-dependent performance metrics.

---

## Results (High-Level)
- Overall predictive power is moderate (R² ~ 0.3–0.4 for most models).
- Best performance is observed for **forwards** (Random Forest R² ≈ 0.64).
- Results highlight the limitations of quantitative-only valuation and the impact of external factors (media, injuries, international play).

---

## Tech Stack
Python · Pandas · Scikit-learn · Selenium · Matplotlib/Seaborn

---

## Notes / Future Improvements
- Incorporate contextual signals (injuries, international competitions, media exposure).
- Improve evaluation with additional seasons and broader leagues.
- Explore models that better capture non-linear interactions and uncertainty.
