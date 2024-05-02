# Tutorial-on-word2vec-embedding

This is a tutorial on word2vec embedding as a part of DA_623, with the subtopic: `Analyze word2vec embedding by demonstrating clustering on a subtitle file of a movie of your choice`.

I have chosen the movie `Titanic` and have used 'Titanic.1997.720p.BluRay.X264-AMIABLE.srt' as it's subtitle file (downloaded from [here](https://www.opensubtitles.com/en/subtitles/4682747-titanic-1997-720p-bluray-x264-amiable)).

To run the tutorial:
1. Clone the repository.
2. Run the Jupyter Notebook (word2vec_embedding.ipynb)

## Overview
This repository presents an analysis of Word2Vec embedding applied to `Titanic` film's subtitle. The analysis encompasses various stages, including preprocessing, model selection, parameter estimation, clustering, and visualization.

## Analysis Steps

### Understanding Word2Vec Embeddings
We delve into the concept of Word2Vec embeddings and take an overview of two primary methods: Continuous Bag of Words (CBOW) and Skip-gram.

### Data Preprocessing
We preprocess the subtitles file by tokenizing sentences, removing punctuations, converting text to lowercase, and eliminating stopwords.

### Data Statistics
We provide statistics on the preprocessed data, including the total number of sentences, words, and unique words.

### Model Selection and Parameter Estimation
We utilize the Word2Vec module from the `gensim` library and experiment with different vector sizes. Through experimentation, we determine an optimal vector size of 70 for our dataset.

### Clustering
We apply k-means clustering to the Word2Vec embeddings with various values of k. After experimentation, we find that k = 10 yields the most interpretable clusters.

### Cluster Interpretation
We analyze the resulting clusters to interpret their meanings and observe similarities among words within each cluster.

### Visualizations
We generate wordclouds to visually represent the contents of each cluster, providing insight into the semantic relationships among clustered words.

## Future Directions

### Character vs. Dialogue Analysis
More analysis could have been possible if the character vs dialogue was present in a subtitles file. It could help us figure out if any character dominates any specific cluster providing **character specific attributes**.

### Temporal Analysis
One could also try to plot clusters as the plot progresses, to notice how the clusters change throughout the film's runtime. This could help us to link clusters to specific stages of the movie moments.

## References
https://towardsdatascience.com/introduction-to-word-embedding-and-word2vec-652d0c2060fa

https://medium.com/@zafaralibagh6/simple-tutorial-on-word-embedding-and-word2vec-43d477624b6d

https://radimrehurek.com/gensim/models/word2vec.html

https://radimrehurek.com/gensim/models/keyedvectors.html
