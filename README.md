# GL_NLP_Sentiment-Analysis

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

3. **Sentiment Analysis:**
   
    - Used the `nlptown/bert-base-multilingual-uncased-sentiment` model to perform sentiment analysis on each sentence within the weekly news.
    - Identified top 3 positive and top 3 negative sentences based on sentiment predictions.

4. **Methodology:**
   
* Initial Exploration :
   - Investigated different word embedding techniques (Word2Vec, GloVe, and Sentence Transformer) for text representation.
   - Built a simple Logistic Regression model to determine the sentiment of the news articles
   - Used Hyper-parameter tuning to improve the base Logistic Regression model on each of the word embeddings from Word2Vec, GloVe, and Sentence Transformer

* Secondary Exploration:
   - Grouped the data into weeks and for each week, tried to identify the top-3 news articles (both positive and negative) on the company
   - Using 'nlptown/bert-base-multilingual-uncased-sentiment' model from Hugging face, tried to analyze the news articles
   - Instructed the BERT model using Prompts to extract the top-3 articles in each catefory (positive/negative)

4. **Tech Stack:**
   
* Programming Language: Python
* Libraries:
   - pandas: For data manipulation and analysis.   
   - transformers: For loading and utilizing pre-trained Hugging Face models (specifically nlptown/bert-base-multilingual uncased-sentiment).
   - Hugging Face Model: nlptown/bert-base-multilingual-uncased-sentiment

5. **Results**

The project outputs a DataFrame containing the top positive and negative events for each week, along with their respective sentiment labels.
