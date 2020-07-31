# Song Genre Prediction using NLP techniques

Every year, more than one million songs are released over the world.

These songs are of different genres,different languages and sung by thousands of different artists.

In this project we will make a classifier model which will be able to classify which genre of music a specific line of text is most likely to come from.

In this notebook ,I have collected songs lyrics from songs of 46 american artists from 7 different genres mainly : Pop,Rock,HipHop,Kids,Rap,Folk and R&B.From the 46 artists song's, we were able to get over 150000 lines of text which we used to train a model.

The songs were collected using [LyricsGenius API](https://github.com/johnwmillr/LyricsGenius) and then were manually split across genres.


## [Part 1: Text Mining](https://github.com/ApurvGude/Song-genre-prediction/blob/master/notebooks/Text%20Mining%20with%20Songs.ipynb)

![Image 1](https://github.com/ApurvGude/Song-genre-prediction/blob/master/images/index2.png)

In this part we analysed,the songs from each genre to find out the average number of words per line, the most active words and n-grams in each genre and even created wordclouds for each genre.

From this analysis , we also made some observations to help us in creating our model.

## [Part 2: Creating the model and analyzing the results](https://github.com/ApurvGude/Song-genre-prediction/blob/master/notebooks/Classification%20Model%20Creation%20And%20Analysis.ipynb)

![Image 2](https://github.com/ApurvGude/Song-genre-prediction/blob/master/images/index1.png)

In this part we tried out two different NLP techniques to make our classifier:
1. **TFIDF-Vectorizer** : In the first method, we used TFIDF-Vectorizer from scikit learn toolkit to make our predictions. The TFIDF-Vectorizer creates a matirx of words per genre telling us how active the word is in that specific genre.

2. **Word2Vec** : In the second model ,we used Googles pretrained Word2Vec weights to create word embeddings which we passed through LSTM units to help us predict the genre. 

Out of the two above methods. Word2Vec model gave the better result. We were able to obtain an validation accuracy of 52% with ROC_AUC score of 0.84.

We also made prediction systems and analysed the two models result based on new data given to the prediction system/
         
