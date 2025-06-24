# Analysis of Bitcoin Market Sentiment and Trader Performance

This repository analyzes the provided "Bitcoin Market Sentiment Dataset" and "Historical Trader Data from Hyperliquid" to explore the relationship between trader performance and market sentiment. The goal is to uncover hidden patterns and deliver insights that can support smarter, sentiment-aware trading strategies.

## Steps Taken and Analysis

1. **Data Loading and Initial Inspection:**

   * Loaded the `fear_greed_index.csv` dataset into a pandas DataFrame.
   * Loaded the `historical_data.csv` dataset into a pandas DataFrame.
   * Displayed the initial rows to understand structure and content.

2. **Data Preprocessing and Merging:**

   * Converted the 'Timestamp IST' column in the historical data to datetime format.
   * Created a new 'Date' column for consistent merging.
   * Converted the sentiment dataset's 'date' column to datetime and renamed it to 'Date'.
   * Merged the two datasets on the 'Date' column using a left join.
   * Dropped unnecessary columns to streamline the dataset.

3. **Initial Exploratory Data Analysis:**

   * Analyzed the distribution of 'Timestamp IST', 'Date', and 'classification'.
   * Generated descriptive statistics of the merged dataset.
   * Created a new column, 'Profit\_Status', to classify trades as 'Profit' or 'Loss'.
   * Counted values in the 'Profit\_Status' column to understand distribution.

4. **Analyzing Sentiment and Trader Behavior:**

   * Calculated average 'Closed PnL' by sentiment classification.
   * Analyzed 'Side' (BUY/SELL) distribution within each sentiment group.
   * Determined the percentage of profitable trades across sentiment types.
   * Calculated average profit or loss grouped by both 'Side' and 'classification'.

## Visualizations

The following visualizations were generated to support and communicate findings:

* **Box Plot:** Profit and loss distribution by sentiment classification.
* **Bar Chart:** Average 'Closed PnL' by sentiment.
* **Count Plot:** Number of BUY and SELL trades by sentiment classification.
* **Count Plot:** Number of profitable and losing trades by sentiment.
* **Bar Chart:** Average number of tokens traded by sentiment.
* **Bar Chart:** Average USD value of trades by sentiment.
* **Bar Chart:** Total number of trades for each sentiment classification.
* **Bar Chart:** Unique active traders by sentiment classification.
* **Scatter Plot:** Closed PnL over time with sentiment coloring.
* **Heatmap:** Correlation matrix between 'Closed PnL', 'Size USD', 'Size Tokens', and 'Execution Price'.

## Conclusion

* This project successfully merged sentiment and trading datasets to analyze emotional impact on trading behavior.
* Average profit tends to increase during Greed phases, while Extreme Fear shows heightened volatility and lower success rates.
* Traders handled larger token volumes on Extreme Greed days, but overall USD value per trade was lower, possibly due to lower token prices or conservative capital use.
* Trade activity and participation were noticeably higher during Greed, hinting at emotionally-driven market engagement (FOMO).
* Correlation analysis showed dependencies between trade metrics and sentiment, supporting the idea that emotional context impacts both decision-making and outcomes.

These insights can help in crafting more intelligent, emotionally-aware trading strategies that anticipate market behavior rather than react to it impulsively.
