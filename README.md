# Machine Learning and the Limits of Daily Return Prediction  
A Rigorous Out-of-Sample Study on Bank of America (BAC)

This project investigates whether non-linear machine learning models can improve next-day return prediction for Bank of America (BAC) under strict out-of-sample evaluation.

Rather than assuming predictability, the study adopts a disciplined quantitative framework. Let $ P_t $ denote the closing price at time $ t $, and $ r_t = \log(P_t / P_{t-1}) $ the daily log-return. The objective is to estimate the conditional expectation $ \mathbb{E}[r_{t+1} \mid \mathcal{F}_t] $ using observable features at time $ t $, and assess whether any economically meaningful predictive structure exists.

The dataset spans 2000–2024 and includes daily market and macroeconomic variables such as the S&P 500 index, VIX, and US 10-year Treasury yield, along with engineered technical features. All models are evaluated using strict temporal splits to prevent data leakage, with walk-forward retraining and out-of-sample testing.

The modeling framework includes regularized decision trees, Random Forest, and Gradient Boosting. Performance is assessed using mean squared error, directional accuracy, cumulative strategy returns, annualized Sharpe ratio, and bootstrap confidence intervals. A naive benchmark is included to ensure proper performance comparison.

Empirical results indicate that while ensemble methods reduce variance relative to single decision trees, predictive improvements remain limited. Out-of-sample trading performance does not consistently outperform buy-and-hold. These findings are consistent with the well-documented low signal-to-noise ratio of daily equity returns.

This project emphasizes methodological rigor, financial realism, and careful evaluation over artificial in-sample performance. It illustrates the practical limits of machine learning in short-horizon equity return prediction under realistic research constraints.

The full notebook is available here:  
./notebooks/01_ml_price_prediction_bac.ipynb

This work is for research and educational purposes only and does not constitute investment advice.
