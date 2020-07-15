# Sentiment-Analysis-of-Yelp-Reviews
This is a course project for ERG3020 by three students from CUHK(SZ). The dataset used in this project is revised from the original Kaggle dataset, which can be found from the link here: https://www.kaggle.com/omkarsabnis/sentiment-analysis-on-the-yelp-reviews-dataset

## Project Organization
* Data preprocessing
* Algorithms Implement
1. Multinominal Naive Bayes
2. Support Vector Machine
3. K-Nearest Neighbors
4. Random Forest
5. Multilayer Perceptron

## Project Conclusion & Reflection
This project conducts sentiment analysis of Yelp Reviews dataset with Naive Bayes, SVM, k-NN, MLP, and Random Forest algorithms. All algorithms are applied using tools from sklearn. Our sentiment analysis indicates Naive Bayes algorithm has nearly the best performance.

**Reflection:Why CounterVectorizer better than TFIDF Vectorizer?**
TfFIDF Vectorizer would be better able to differentiate rare words and commonly occurring words while Countvectorizer would still give equal weight to all words which is undesirable. So, TfidfVectorizer will give you better performance than CountVectorizer as the size of the vocabulary increases.
Therefore, to further investigate the performance of these text vectorizers, we need to collect much more data and increase the size of the dataset.

**Insights**
After the comparison of the various models above, we find that the accuracy of Naive Bayes is the highest among the five models. Even after we complete the cross validation, Naive Bayes algorithm still performs best. Then we start to think about why Naive Bayes is the most suitable model for our case.
Multinomial Naive Bayes often involves the concept of frequency or discrete variables, which means the feature matrix is often sparse, while the famous TF-IDF vectorization and the common count-word vectorization generate exactly discrete sparse matrices. Moreover, this data set is relatively simple. Even if the correlation between words is ignored, as long as some words such as ’excellent’, ’good’, and ’nasty’ appear, the text can be classified correctly.
