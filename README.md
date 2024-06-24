 >"If stock trading was as easy as our models make it look, we'd all be sipping cocktails on our private islands by now."

# HMMvsML

# Comparative Analysis of HMM and Machine Learning Trading Strategies for NVIDIA Stock

This repository contains the code and data used in the study of trading strategies for NVIDIA stock using Hidden Markov Models (HMM) and Machine Learning models (Random Forest, XGBoost). The primary goal of this study is to compare the performance of traditional statistical models with advanced machine learning techniques in predicting stock market trends.

## Table of Contents
1. [Introduction](#introduction)
2. [Data](#data)
3. [Models](#models)
   - [HMM-Based Strategy](#hmm-based-strategy)
   - [Machine Learning Models](#machine-learning-models)
4. [Results](#results)
5. [Conclusion](#conclusion)
6. [References](#references)

## Introduction
Stock market trend prediction is crucial for trading strategies, risk management, and financial decision-making. This project implements and evaluates two types of models for trading strategies: Hidden Markov Models (HMM) and Machine Learning models (Random Forest and XGBoost). The performance of these models is compared using metrics such as Sharpe Ratio, Total Return, and the number of trades executed.

## Data
The dataset used in this study consists of daily stock prices of NVIDIA Corporation (Ticker: NVDA). The data spans from January 2018 to January 2024 and includes features such as:
- Open, Close, High, Low prices
- Volume
- Returns
- Rolling volatility

## Models

### HMM-Based Strategy
Hidden Markov Models (HMM) are used for modeling probabilistic market states and generating trading signals. The following steps are implemented:
- **Data Preparation**: Calculate returns and rolling volatility.
- **HMM Training**: Gaussian HMM with 2 hidden states trained on returns data.
- **Trading Signals**: Identify "good" regime based on returns and generate buy/sell signals.
- **Backtesting**: Implement a strategy with initial capital of $100,000 and a stop-loss mechanism.

### Machine Learning Models
Machine Learning models, particularly Random Forest and XGBoost, are used for predicting stock market trends. The following steps are implemented:
- **Feature Engineering**: SMA, EMA, Momentum, RSI, Bollinger Bands, MACD, ADX, Stochastic, ATR.
- **Models**: Random Forest and XGBoost.
- **Implementation**: Python's `sklearn` and `xgboost` libraries.
- **Training and Validation**: Cross-validation and grid search for hyperparameter tuning.

## Results
The models' performance is evaluated using out-of-sample predictions. Key findings include:

| Metric                | HMM                        | Random Forest    | XGBoost           |
|-----------------------|----------------------------|------------------|-------------------|
| **Sharpe Ratio**      | 1.88                       | 2.17             | 1.99              |
| **Total Return**      | 111.66%                    | 183%             | 161%              |
| **Number of Trades**  | 7                          | 14               | 14                |

## Conclusion
The study concludes that while HMM strategies are effective for generating adaptive trading signals and managing risk, Machine Learning models, particularly Random Forest and XGBoost, offer superior performance in terms of risk-adjusted returns and overall profitability. These findings have significant implications for developing robust trading strategies.


## References
- Hamilton, J. D. (1989). A new approach to the economic analysis of nonstationary time series and the business cycle. *Econometrica*, 57(2), 357-384.
- Elliott, R. J., Aggoun, L., & Moore, J. B. (2008). *Hidden Markov Models: Estimation and Control*. Springer.
- Prado, M. L. (2018). *Advances in Financial Machine Learning*. Wiley.
- Patel, J., Shah, S., Thakkar, P., & Kotecha, K. (2015). Predicting stock and stock price index movement using Trend Deterministic Data Preparation and machine learning techniques. *Expert Systems with Applications*, 259-268.
- Zhang, Y., & Wang, J. (2017). Integrating EMA indicators into machine learning models to enhance stock price prediction. *International Journal of Economics and Finance*, 183-194.
- [Full list of references in the report]
