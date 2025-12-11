# Markowitz-Portfolio-Risk-Analyzer
Portfolio Analysis Tool

This project is a simple Python script that downloads historical stock data from Yahoo Finance, calculates daily returns, and computes basic portfolio metrics such as expected return and risk. All input settings are managed through a config.json file.

Features:
-Reads tickers, date range, and portfolio weights from config.json
-Supports any number of assets (multiple tickers and matching weights)
-Validates tickers, weights, and date inputs
-Downloads closing price data and saves it to prices.csv
-Computes daily returns and saves them to daily_returns.csv
-Calculates expected portfolio return, covariance matrix, and portfolio risk (standard deviation)

Installation:
pip install yfinance pandas numpy

Example config.json:
{
"tickers": ["KGH.WA", "PKN.WA"],
"start_date": "2024-01-01",
"end_date": "2024-12-31",
"weights": [0.5, 0.5]
}

Key configuration notes:
-tickers: stock symbols in Yahoo Finance format
-start_date / end_date: must be formatted YYYY-MM-DD (end_date must be earlier than today)
-weights: must sum to 1


The script will download data, generate CSV files with prices and daily returns, and print portfolio return and risk values.
