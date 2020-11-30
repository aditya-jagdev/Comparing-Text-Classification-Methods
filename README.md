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
|Naive Bayes (Count Vectors)   	| <1 second|
|Naive Bayes (TFIDF Vectors)   	| <1 second|
|Logistic Regression (Count Vectors)  	| 20 seconds|
|Logistic Regression (TFIDF Vectors)  	| 3 minutes|
|CNN   	|47 minutes|
|LSTM based CNN   	|3 hours|

### Accuracy Achieved
|   	|Word Count    	|TFIDF   	|GloVe |
|---	|---	|---	|---	|
|Naive Bayes   	|92.53 %   	|92.34 %   	|X|
|Logistic Regression   	|94.22 %   	|93.46 %   	|X|
|CNN   	|X   	|X   	|88.33 %|
|LSTM based CNN   	|X   	|X   	|89.81 %|

## Key Takeaways

* When working on a project, there are multiple constraints such as time, resources, and the quality of solution, among various other things that have to be kept in mind. Hence, knowing which methods to use will result in quicker development of the solution.
* If classification is to be carried out on words from a known and specific domain wherein it is known that no new words may show up, then traditional ML techniques are better.
* If classification is to be carried out in a scenario where the words in the given domain can vary too much with sentences, and there is no control over the kind of word inputs that one is going to receive, CNNs should be used.
* While LSTM gave marginally better performance, this came at a huge price of much longer training times.
