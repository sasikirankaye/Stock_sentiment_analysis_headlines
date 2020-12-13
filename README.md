# Stock_sentiment_analysis_headlines
Identification of trends in the stock prices of a company by performing fundamental analysis of the company. News articles were provided as training data-sets to the model which classified the articles as positive or neutral. Sentiment score was computed by calculating the difference between positive and negative words present in the news article. Comparisons were made between the actual stock prices and the sentiment scores. Naive Bayes, OneR and Random Forest algorithms were used to observe the results of the model using Weka

Stock Prices are considered to be very dynamic and susceptible to quick changes because of the underlying nature of the financial domain and in part because of the mix of known parameters (Previous Days Closing Price, P/E Ratio etc.) and unknown factors (like Election Results, Rumors etc.) An intelligent trader would predict the stock price and buy a stock before the price rises, or sell it before its value declines. Though it is very hard to replace the expertise that an experienced trader has gained, an accurate prediction algorithm can directly result into high profits for investment firms, indicating a direct relationship between the accuracy of the prediction algorithm and the profit made from using the algorithm. In practice, there are 2 Stock Prediction Methodologies: Fundamental Analysis: Performed by the Fundamental Analysts, this method is concerned more with the company rather than the actual stock. The analysts make their decisions based on the past performance of the company, the earnings forecast etc. Technical Analysis: Performed by the Technical Analysts, this method deals with the determination of the stock price based on the past patterns of the stock (using time-series analysis.) When applying Machine Learning to Stock Data, we are more interested in doing a Technical Analysis to see if our algorithm can accurately learn the underlying patterns in the stock time series. This said, Machine Learning can also play a major role in evaluating and forecasting the performance of the company and other similar parameters helpful in Fundamental Analysis. In fact, the most successful automated stock prediction and recommendation systems use some sort of a hybrid analysis model involving both Fundamental and Technical Analysis.

In practice, there are 2 Stock Prediction Methodologies:

Fundamental Analysis:
Performed by the Fundamental Analysts, this method is concerned more with the company rather than the actual stock. The analysts make their decisions based on the past performance of the company, the earnings forecast etc.

Technical Analysis:
Performed by the Technical Analysts, this method deals with the determination of the stock price based on the past patterns of the stock (using time-series analysis.

Pre Processing
Text data is unstructured data. So, we cannot provide raw test data to classifier as an input. Firstly, we need to tokenize the document into words to operate on word level. Text data contains more noisy words which are not contributing towards classification. So, we need to drop those words. In addition, text data may contain numbers, more white spaces, tabs, punctuation characters, stop words etc. We also need to clean data by removing all those words. 2.3 Sentiment Detection Algorithm For automatic sentiment detection of news articles, we are following Dictionary based approach which uses Bag of Word technique for text mining. This method is based on the research of J. Bean in his implementation of Twitter sentiment analysis for airline companies. To build the polarity dictionary, we need two types of words collection; i.e. positive words and negative words. Then we can match the article’s words against both these words list and count numbers of words appears in both the dictionaries and calculate the score of that document. We created the polarity words dictionary using general words with positive and negative polarity.

Algorithm:
Tokenize the document into word vector.
Prepare the dictionary which contains words with its polarity (positive or negative)
Check against each word weather it matches with one of the word from positive word dictionary or negative words dictionary.
Count number of words belongs to positive and negative polarity.
If the Score is 0 or more, we consider the document is positive or else, negative.
 

Classifier Learning
As most of the research shows that  Random Forest and Naïve Bayes classification algorithms performs good in text classification. So, we are considering all three algorithms to classify the text and check each algorithm’s accuracy. We can compare all the results such as accuracy, precision, recall and other model evaluation methods. All three classification algorithms are implemented and tested using Weka tool.
