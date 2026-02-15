# Machine Learning and the Limits of Daily Return Prediction  
### A Rigorous Out-of-Sample Study on Bank of America (BAC)

---

This project investigates whether non-linear machine learning models can extract economically meaningful predictive information from daily equity returns under strict out-of-sample evaluation.

The objective is to estimate next-day log-returns using only information available at time t, and to determine whether any stable predictive structure survives proper temporal validation constraints.

---

### Data

The dataset spans 2000–2024 and combines:

- Price-based technical features  
- Market information (S&P 500)  
- Volatility index (VIX)  
- US 10-year Treasury yield  

All experiments enforce strict temporal splits to eliminate data leakage and implement walk-forward retraining to replicate realistic forecasting conditions.

---

### Modeling Framework

The study evaluates:

- Regularized Decision Trees  
- Random Forest  
- Gradient Boosting  

Performance is assessed strictly out-of-sample using:

- Mean Squared Error  
- Directional Accuracy  
- Cumulative Strategy Returns  
- Annualized Sharpe Ratio  
- Bootstrap Confidence Intervals  

All results are benchmarked against a naive forecast to ensure that any improvement reflects genuine predictive content rather than simple persistence.

---

### Findings

Ensemble methods reduce variance relative to single trees, but improvements over naive benchmarks remain limited.  
Out-of-sample trading performance does not consistently outperform a passive buy-and-hold strategy.

These results align with the well-documented low signal-to-noise ratio of daily stock returns and highlight the structural difficulty of short-horizon return prediction.

---

Full notebook:  
https://morales-mathieu.github.io/ml-price-prediction-bac/01_ml_price_prediction_bac.html

---

This project prioritizes methodological rigor, statistical discipline, and financial realism over in-sample performance.
