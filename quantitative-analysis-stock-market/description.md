# Project Title: Quantitative Analysis of Stock Market prices

## Overview:
This project involves a quantitative analysis of the stock prices of four major technology companies: Netflix, Apple, Microsoft, and Google. The aim of this project is to explore the historical stock performance, analyse risk and return, and identify key trends and correlations among these companies.

## Motivation:
The technology sector is a significant driver of the global economy, and understanding the stock performance of leading companies within this sector can provide valuable insights for investors and financial analysts. This project aims to apply data science techniques to extract actionable insights from stock market data, helping to better understand the dynamics of stock prices in this high-impact industry.

## Data:
The dataset includes daily stock prices and trading volumes for Netflix, Apple, Microsoft, and Google over a specific period. The data was sourced from a reliable financial database, and it includes the following variables:
- **Ticker:** Stock symbol (e.g., NFLX for Netflix)
- **Date:** The trading date
- **Open:** Opening price of the stock on that day
- **High:** Highest price of the stock during the trading day
- **Low:** Lowest price of the stock during the trading day
- **Close:** Closing price of the stock on that day
- **Adj Close:** Adjusted closing price, considering corporate actions like dividends and stock splits
- **Volume:** Number of shares traded

### Preprocessing Steps:
- **Date Formatting:** The 'Date' column was converted to a datetime format for easier time series analysis.
- **Handling Missing Values:** Any missing data points were handled by removing the rows.

## Methodology
The project follows a structured approach, starting with data exploration and ending with a detailed analysis of stock performance:

1. **Exploratory Data Analysis (EDA):** 
   - Performed descriptive statistics to summarise the data using .describe() function. 
  ```python
.describe()
# in this context where we just look at Closing price of the stock:
descriptive_stats = stocksdf.groupby('Ticker')['Close'].describe() 
print(descriptive_stats)
```
   - Conducted visualisations (such as bar, line graph, heatmap) to understand the trend and volatility of each stock.

2. **Data Visualisation:**
   - **Time Series Analysis:** Plotted the historical closing prices to observe trends and compare performance using line graph.
   - **Volatility Analysis:** Calculated and visualised the standard deviation of stock prices to assess risk using bar graph.
   - **Correlation Analysis:** Generated a correlation matrix using heatmap to understand the relationships between the stock prices of the four companies.
   - **Risk/Return Trade-off Analysis:** Analysed the balance between the risk (volatility) and return (average daily return) for each stock, using scatter plots to visualise the trade-offs.

## Results
The analysis provided several insights:

- **Apple (AAPL):** Exhibited low volatility and consistent growth, indicating a stable investment with moderate returns.
- **Google (GOOG):** Displayed the least volatility but had a marginally negative return over the analysis period, suggesting a low-risk, low-reward scenario.
- **Microsoft (MSFT):** Showed a significant positive return with moderate volatility, making it a potentially rewarding investment.
- **Netflix (NFLX):** Had the highest volatility and a notable negative return, indicating high risk.

The visualisations, including time series plots, bar charts for volatility, and correlation heatmaps, clearly illustrate these findings.

## Conclusion
This project demonstrated the importance of quantitative analysis in evaluating stock performance, particularly in understanding risk and return. The analysis highlighted how different companies within the same sector can have vastly different stock market behaviors, which is critical for making informed investment decisions. 
