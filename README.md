# GL_NL_Sentiment-Analysis

# Stock Sentiment Analysis

This project analyzes stock-related news articles to identify key positive and negative events that might impact stock prices.

**1. Introduction**

This project utilizes a pre-trained sentiment analysis model (nlptown/bert-base-multilingual-uncased-sentiment) to analyze news articles related to stock movements. The goal is to identify the top 3 most positive and negative events within each week of news.

**2. Data**

* **Source:** refer: Dataset - stock_news.csv
* **Fields:**
    * Date
    * News 
    * Open
    * High
    * Low
    * Close
    * Volume

**3. Methodology**

1. **Data Preparation:**
    - Grouped news articles by week.
    - Concatenated news articles within each week using "#" as a separator.

2. **Sentiment Analysis:**
    - Used the `nlptown/bert-base-multilingual-uncased-sentiment` model to perform sentiment analysis on each sentence within the weekly news.
    - Identified top 3 positive and top 3 negative sentences based on sentiment predictions.

**4. Results**

The project outputs a DataFrame containing the identified top positive and negative events for each week, along with their respective sentiment labels.
