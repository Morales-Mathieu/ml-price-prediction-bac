# Machine Learning and the Limits of Daily Return Prediction  
A Rigorous Out-of-Sample Study on Bank of America (BAC)

This project examines whether non-linear machine learning models can extract economically meaningful predictive information from daily equity returns under strict out-of-sample evaluation.

Let \( P_t \) denote the closing price at time \( t \), and \( r_t = \log(P_t / P_{t-1}) \) the corresponding daily log-return. The objective is to estimate the conditional expectation \( \mathbb{E}[r_{t+1} \mid \mathcal{F}_t] \) using information available at time \( t \), and to assess whether any stable predictive structure can be identified once proper temporal validation constraints are imposed.

The dataset spans 2000–2024 and combines price-based technical features with market and macroeconomic variables, including the S&P 500 index, VIX, and US 10-year Treasury yield. The empirical design enforces strict temporal splits to eliminate data leakage and implements walk-forward retraining to replicate realistic forecasting conditions.

The modeling framework includes regularized decision trees, Random Forest, and Gradient Boosting. Performance is evaluated out-of-sample using mean squared error, directional accuracy, cumulative strategy returns, annualized Sharpe ratio, and bootstrap-based statistical inference. All results are benchmarked against a naive forecast to ensure that any apparent improvement reflects genuine predictive content rather than persistence or structural bias.

The empirical findings indicate that although ensemble methods reduce variance relative to single trees, improvements over naive benchmarks remain limited. Out-of-sample trading performance does not consistently outperform a passive buy-and-hold strategy. These results align with the well-documented low signal-to-noise ratio of daily stock returns and highlight the structural difficulty of short-horizon return prediction.

This study prioritizes methodological rigor, statistical discipline, and financial realism over in-sample performance. It illustrates both the capabilities and the inherent limits of machine learning when applied to short-term equity return forecasting under realistic research constraints.

Full notebook available at:  
https://morales-mathieu.github.io/ml-price-prediction-bac/01_ml_price_prediction_bac.html

This work is intended for research and educational purposes only and does not constitute investment advice.
