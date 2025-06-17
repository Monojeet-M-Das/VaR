# Value at Risk (VaR) Implementation in Python

This project demonstrates a simple implementation of the **Value at Risk (VaR)** model using historical stock data. It estimates potential losses in investment portfolios under normal market conditions, using both 1-day and multi-day VaR calculations based on the assumption that returns are normally distributed.

## 📈 What is Value at Risk?

**Value at Risk (VaR)** is a statistical technique used to measure the risk of loss on a portfolio. For a given confidence level (e.g., 95%), it estimates the maximum expected loss over a specified time period.

## 🧠 Features

- Downloads historical stock data using `yfinance`
- Calculates daily logarithmic returns
- Computes 1-day and N-day VaR using parametric (normal distribution) method
- Easily customizable for other stocks, periods, or portfolio sizes

## 📂 Files

- `VaR_implementation.py`: Main script that downloads data, calculates returns, and computes VaR.

## 🛠️ Requirements

Make sure you have the following Python libraries installed:

```bash
pip install numpy pandas yfinance scipy

🚀 Usage

    Clone the repository or download the script.

    Run the script using Python:

python VaR_implementation.py

🔍 Example Output

Value at risk is: $17983.55
Value at risk is: $56846.88

This means, with 95% confidence, you can expect that:

    You won’t lose more than ~$17,983 in one day.

    You won’t lose more than ~$56,847 in ten days.

⚙️ How It Works

    Data Download: Historical stock data for Citigroup Inc. (ticker C) is downloaded from Yahoo Finance.

    Returns Calculation: Log returns are computed from the stock price data.

    VaR Calculation:

        1-Day VaR: Based on standard deviation and mean of returns.

        N-Day VaR: Scales the daily risk according to the square root of time.

📌 Notes

    The script assumes normally distributed returns, which may not hold in real-world scenarios.

    You can replace the stock symbol 'C' with any other ticker for analysis.