# Monte Carlo Value at Risk (VaR) Simulation in Python

This project demonstrates how to compute **Value at Risk (VaR)** using a Monte Carlo simulation. It models the uncertainty in stock prices to estimate the potential loss in a portfolio over a specified time horizon at a given confidence level.

## 📌 What is Monte Carlo VaR?

Monte Carlo VaR uses simulated future prices based on statistical properties (mean and volatility) of historical returns. It generates thousands of possible scenarios for a portfolio’s value and estimates risk from the worst outcomes.

---

## 🚀 Features

- Downloads historical stock data via Yahoo Finance using `yfinance`
- Estimates mean and standard deviation of daily returns
- Runs Monte Carlo simulations of stock price evolution
- Calculates 1-day VaR at a user-defined confidence level (e.g., 99%)
- Easy to customize stock, horizon, confidence, and number of iterations

---

## 🧾 File Overview

- `VaR_using_Monte_Carlo.py`: Core script that performs:
  - Historical data retrieval
  - Statistical parameter estimation
  - Monte Carlo simulations
  - VaR calculation and display

---

## 🛠️ Requirements

Install dependencies with:

```bash
pip install numpy pandas yfinance

📈 How It Works

    Download Data: Historical closing prices of Citigroup Inc. (C) from Yahoo Finance.

    Calculate Returns: Computes daily percentage returns from price data.

    Parameter Estimation: Uses mean (mu) and standard deviation (sigma) of returns.

    Monte Carlo Simulation: Simulates 100,000 potential future price paths using:
    St=S0⋅exp⁡((μ−0.5σ2)t+σtZ)
    St​=S0​⋅exp((μ−0.5σ2)t+σt

    ​Z)

    VaR Calculation: The (1 - confidence) percentile of simulated outcomes is used to compute potential loss.

💻 Usage

Run the script with:

python VaR_using_Monte_Carlo.py

Example Output

Value at risk with Monte-Carlo simulation: $25713.45

🧮 Adjustable Parameters

Inside the script:

S = 1e6                 # Investment amount ($1,000,000)
c = 0.99                # Confidence level (e.g. 99%)
n = 1                   # Time horizon in days
iterations = 100000     # Number of simulations

📎 Notes

    The model assumes normally distributed returns.

    You can replace 'C' with any valid stock ticker.

    Higher iterations yield more accurate estimates but increase runtime.