# Comparing-Text-Classification-Methods

This is a multi-class classification problem wherein using previous years' news headlines and their categories, a classifier is created to deal with unseen headlines. Both machine learning and deep learning techniques were used to achieve it and a comparison based on preprocessing required, training time, and validation metrics is presented. The data used can be found [<u>here (UCI News Aggregator)</u>](https://archive.ics.uci.edu/ml/datasets/News+Aggregator).

### Preprocessing Required

|Method|    	| 
|---	|---	|
|Word Count, TFIDF   	|Scikit-Learn provides `CountVectorizer` and `TfidfVectorizer` which are used to create usable vectors to act as input to the algorithm. Stop words were removed using `NLTK`'s stopwords.	|
|GloVe   	|GloVe embeddings were used to preprocess input for the neural network models. A maximum length of 20 words was used to create the vectors.	|

### Training Times
|Model|Time Taken    	|
|---	|---	|
|Naive Bayes   	||
|Logistic Regression   	||
|ANN   	||
|LSTM based ANN   	||

### Accuracy Achieved
|   	|Word Count    	|TFIDF   	|GloVe |
|---	|---	|---	|---	|
|Naive Bayes   	|92.53 %   	|92.34 %   	|X|
|Logistic Regression   	|94.22 %   	|93.46 %   	|X|
|ANN   	|X   	|X   	|88.33 %|
|LSTM based ANN   	|X   	|X   	| %|

