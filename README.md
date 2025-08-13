# Stock-Market-Index-Volatility-Prediction-Linear-Regression-SVR-

This project applies Linear Regression, Support Vector Regression (SVR), and Support Vector Machines (SVM) with a Linear kernel to predict the main stock market indices of Greece, Ireland, Italy, Portugal, and Spain using historical technical and economic indicators.
The datasets include features such as moving averages, RSI, MACD, GDP, inflation, and interest rates, all closely related to the countries’ general stock market indices. The goal is to build accurate predictive models for individual markets and to explore whether combining multi-country data improves performance and generalization.

📚 Dataset Description
The datasets contain historical technical and economic indicators that are directly related to the main stock market indices of five countries:

-Greece
-Ireland
-Italy
-Portugal
-Spain

Example feature categories:

Technical indicators: Moving Averages, RSI, MACD, Bollinger Bands, etc.

Economic indicators: Inflation, GDP, interest rates, unemployment.

Stock market indicators: Historical values of the main index (closing prices, returns, volatility).

Each .xlsx file contains time-series data of these indicators for the respective country. In the SVM_ALL_DATA_1 notebook, the datasets from all countries are merged into one combined dataset to enable cross-country learning.

🧪 Code Description
1. Linear Regression (per country)
Load and clean each country’s dataset.

Train a linear regression model to predict the main stock market index based on the technical and economic indicators.

Evaluate performance using R², MAE, and RMSE.

2. SVR (Support Vector Regression) with Linear kernel (per country)
Perform preprocessing and feature scaling.

Use SVR(kernel='linear') so predictions are based on linear hyperplanes in feature space.

Evaluate performance and compare with Linear Regression.

3. SVM_ALL_DATA_1 (merged multi-country dataset)
Merge datasets from all five countries.

Perform feature engineering (e.g., country indicator variables, time-based features).

Scale features and train an SVM with a Linear kernel on the entire dataset.

Goal: Assess whether combining information from multiple markets improves predictive accuracy.

🎯 Prediction Goal
The primary objective is to predict the future value or change in each country’s main stock market index using a set of technical and economic indicators.

Individual training: Models trained separately on each country’s dataset.

Combined training: A model trained on the merged multi-country dataset to test generalization across markets.

Performance is evaluated by measuring how close the model’s predictions are to the actual index values, aiming for low error and high explanatory power.

🛠 Requirements
bash
Copy
Edit
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
