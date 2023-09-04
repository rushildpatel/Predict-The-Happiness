Hackathon Link:
https://www.hackerearth.com/challenge/competitive/predict-the-happiness/problems/

This was a contest to predict whether costumers were happy or not about a hotel and their service from their reviews.

## TOOLS USED:

Python 3.6, Numpy, Pandas, NLTK, ,Gensim, SKLearn, Keras. 

## DATA PRE-PROCESSING:

Basic preprocessing on text such as converting to lowercase, removing punctuation, removing stop words is performed.

The preprocessed text is then tokenized and Word2Vec model is built on the entire preprocessed training corpus.

Using Word2Vec a dense representation is obtained for each word. So, each preprocessed review is converted to a dense representation.

Target is 0 - not happy or 1 - happy.

## MODEL BUILDING:

A keras model is built such that it takes Word2vec representation of each word of the review as input.

The input is then passed through LSTM layer.

The output representation from LSTM layer is then passed through the Dense layer.

Finally a sigmoid layer is added which outputs the probability of the review beloging to class 1.

It is trained with ADAM optimizer and loss being Binary crossentropy.

## Performance:

Metric is Accuracy.

Accuracy of on test data is 89.35%

