# Stock Price Simulator Project

## Overview

This project is a stock price simulator that predicts the potential future prices of a stock over a specified period using historical data. It employs Monte Carlo simulations, which rely on random sampling to generate and visualize possible outcomes for the stock's future price. The code focuses on Infosys Limited (INFY.NS), but it can be adapted for other stocks.

## Features

- **Data Collection**: The script fetches historical stock price data for a selected stock over a specified time period using the `yfinance` library.
- **Monte Carlo Simulation**: The simulator generates multiple potential future price paths by running a Monte Carlo simulation.
- **Visualization**: The predicted stock prices are plotted alongside the actual prices for comparison.
- **Historical Return Calculation**: Historical daily returns are computed to understand the stock's past performance.
- **Price Distribution Analysis**: Simulations account for the mean and standard deviation of historical returns, enabling a realistic prediction of future prices.

## Requirements

### Python Packages
- `pandas`: For data manipulation and analysis.
- `matplotlib`: For plotting and visualization.
- `numpy`: For numerical operations.
- `seaborn`: For enhanced visualization (optional).
- `yfinance`: For fetching stock data.
- `ta-lib`: Technical analysis library (installation instructions provided).
- `scipy`: For statistical functions.

### Installation Instructions

1. **Install Required Libraries**:
    ```bash
    pip install pandas matplotlib numpy seaborn yfinance scipy
    ```

2. **Install `ta-lib`**:
    ```bash
    wget http://prdownloads.sourceforge.net/ta-lib/ta-lib-0.4.0-src.tar.gz
    tar -xzvf ta-lib-0.4.0-src.tar.gz
    cd ta-lib
    ./configure --prefix=/usr
    make
    sudo make install
    pip install Ta-Lib
    ```

## Project Structure

- **Data Collection**:
  - Retrieves historical stock price data for the past 30 days.
  - Stores the closing prices in a `price` variable.

- **Monte Carlo Simulation**:
  - Calculates historical returns based on the percentage change in the closing prices.
  - Runs a simulation for the next 30 days by generating random normal values constrained within the percentiles defined by the normal distribution.
  - Applies the calculated returns to predict future stock prices.

- **Visualization**:
  - Plots the simulated stock prices and compares them with the actual prices from the subsequent 30-day period.

## Usage

1. **Run the Script**: Execute the script in a Python environment with the required libraries installed.
2. **Visualization**: View the generated plots that showcase the potential future stock prices and the actual prices for comparison.

## Limitations

- **Prediction Accuracy**: The predictions are based on historical data and assume that future market behavior will follow the same patterns, which might not always hold true.
- **Randomness**: Monte Carlo simulations rely on randomness, so each run may produce slightly different results.

## Conclusion

This stock price simulator provides a basic yet powerful tool for visualizing potential future stock prices. It demonstrates how historical data and statistical methods can be used to predict market trends, offering insights for investors and financial analysts.
