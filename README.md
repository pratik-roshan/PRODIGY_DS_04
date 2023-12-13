# Twitter Sentiment Analysis

This Jupyter notebook analyzes sentiment data from a Twitter dataset using Python with Pandas, NumPy, and Matplotlib.

## Dataset

The dataset used is stored in a CSV file named `twitter_datasets.csv`. The columns are initially unnamed and are later renamed to 'ID', 'Entity', 'Sentiments', and 'Remarks'.

## Data Exploration

### Basic Statistics
- Descriptive statistics of the dataset are obtained using `df_new.describe()`.
- Data types of each column are examined using `df_new.dtypes`.
- Missing values in the dataset are identified and handled with `df_new.dropna()`.

### Sentiment Distribution
- Sentiment counts are calculated and visualized using a pie chart to show the distribution of sentiments across different entities.

```python
# Visualizing Distribution of sentiments towards different entities in a pie chart
plt.figure(figsize=(10, 10))
plt.pie(df_sentiment, labels=df_sentiment.index, autopct='%1.1f%%', startangle=90)
plt.title('Distribution of Sentiments')
plt.show()
