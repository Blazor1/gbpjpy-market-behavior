 Modeling GBP/JPY Market Behavior (2019–2025)
 Project Overview

This project focuses on modeling and analyzing the GBP/JPY foreign exchange market between 2019 and 2025, a period characterized by extreme volatility and structural market changes.

The goal is not to predict exact prices, but to understand and model market behavior by transforming raw price data into structured signals that capture direction, risk, and regime dynamics under modern FX conditions.

 Business Understanding (Problem Statement)

The GBP/JPY currency pair is known for its high volatility and sensitivity to global macroeconomic events. Between 2019 and 2025, the FX market experienced:

COVID-19–driven market shocks

Aggressive global interest rate hikes

Prolonged Japanese yen weakness

Modern algorithmic and high-frequency trading regimes

These conditions make raw price data noisy, unstable, and difficult to interpret.

 Problem

How can we transform noisy GBP/JPY price data into interpretable, risk-aware signals that reflect real market behavior and support better trading and risk management decisions?

 Project Goal

Model GBP/JPY market behavior during modern FX regimes

Capture directional movement, volatility, and regime shifts

Engineer features suitable for classification and risk analysis

Provide a decision-support framework, not an automated trading system

 Data Understanding

Dataset: Historical GBP/JPY time-series data

Period: 2019–2025

Core Features: Open, High, Low, Close, Volume

Frequency: Daily

To ensure temporal consistency and avoid data leakage, the dataset was filtered to a fixed date range:

df = df[
    (df["date"] >= "2019-01-01") &
    (df["date"] <= "2025-12-31")
].reset_index(drop=True)


This period captures modern market regimes while excluding outdated structural behaviors.

 Data Preparation

The following preprocessing steps were applied:

Renamed columns for clarity and consistency

Converted date column to datetime format

Sorted data chronologically

Filtered dataset to the 2019–2025 window

These steps ensured the data was properly structured for time-series analysis and feature engineering.

🛠 Feature Engineering

Feature engineering was central to this project and focused on extracting meaningful market signals from raw price data.

Key Engineered Features

 Daily Returns – measure directional movement and momentum

 Volatility Indicators – assess market risk levels

 Breakout Context – identify regime shifts

 Technical Indicators – RSI, MACD, moving averages

 Volume-Based Metrics – confirm price movements

Daily returns form the foundation for:

Direction classification (Up vs Down)

Risk assessment (High vs Low volatility)

Breakout and regime detection

Data Analysis – Key Insights

GBP/JPY exhibits strong volatility clustering, especially during macroeconomic events

Large price movements are often followed by continued instability

Market behavior differs significantly across volatility regimes

Directional trends are more reliable than exact price prediction

These findings confirm that behavioral modeling is more effective than price-level forecasting in highly volatile FX markets.

 Modeling Approach

The model learns patterns from engineered features rather than raw prices.

What the Model Does

Learns relationships between returns, volatility, and technical indicators

Identifies directional movement and risk regimes

Supports classification-based decision-making

 The model is designed as a decision-support tool, not a price prediction engine.

 Recommendations

Use engineered features instead of raw price levels

Apply volatility filters to manage risk exposure

Focus on directional and regime-based strategies

Avoid using the model during extreme market shocks without additional safeguards

 Next Steps

Add advanced volatility measures (ATR, rolling standard deviation)

Implement breakout and regime detection features

Train and evaluate classification models

Build an interactive dashboard (Tableau / Power BI / Streamlit)

 Limitations

External macroeconomic news is not directly modeled

Performance may degrade during extreme, unexpected events

FX markets are inherently stochastic and non-stationary



Ashono Bravian
Phase Three Data Science Project
