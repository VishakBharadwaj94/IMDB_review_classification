## IMDB dataset and the sentiment classification task

The [large movie review dataset](http://ai.stanford.edu/~amaas/data/sentiment/) contains a collection of 50,000 reviews from IMDB. The dataset contains an even number of positive and negative reviews. The authors considered only highly polarized reviews. A negative review has a score ≤ 4 out of 10, and a positive review has a score ≥ 7 out of 10. Neutral reviews are not included in the dataset. The dataset is divided into training and test sets. The training set is the same 25,000 labeled reviews.

The kaggle dataset link is here - https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews

The **sentiment classification task** consists of predicting the polarity (positive or negative) of a given text.

Our next model is a version of logistic regression with Naive Bayes features.

For every document we compute binarized features as described above, but this time we use bigrams and trigrams too. Each feature is a log-count ratio. A logistic regression model is then trained to predict sentiment.

The approach is insired by the paper Baselines and Bigrams: Simple, Good Sentiment and Topic Classification. Sida Wang and Christopher D. Manning.

The model created here achieves an accuracy over 92% compared to the 91.22% achieved in the paper.
