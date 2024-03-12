# Topic-Modelling


This project demonstrates how to perform clustering and topic modeling on text data using K-means and LDA algorithms. It provides insights into how to preprocess text data, set up vectorization, perform clustering, and extract meaningful topics. By following this walkthrough, users can understand the code and apply similar techniques to their own text data analysis tasks.


Step-by-Step Explanation:

1.Importing Libraries:

  NumPy and pandas for data manipulation.
  NLTK for natural language processing tasks such as tokenization and stemming.
  Seaborn and Matplotlib for data visualization.
  Scikit-learn for implementing machine learning algorithms.
  
2.Data Preprocessing:

  We read the dataset Review_data.csv containing review data.
  Preprocessing involves text cleaning, tokenization, stemming, and removing stop words. We define a function tokenization_and_stemming() for this purpose.
  We set up TF-IDF vectorization using TfidfVectorizer, specifying parameters like maximum document frequency (max_df), maximum number of features (max_features), minimum document 
  frequency (min_df), use of inverse document frequency (use_idf), tokenizer, and n-gram range.
  
3.K-means Clustering:

  We fit the TF-IDF matrix to a K-means clustering model with different numbers of clusters (2, 3, and 5).
  To assess clustering quality, we visualize the clustering using Silhouette scores via the Yellowbrick library.
  We assign cluster labels to each review and count the number of reviews in each cluster.
  Dimensionality reduction using Kernel PCA is performed to visualize clusters in a 2D space.
  
4.Latent Dirichlet Allocation (LDA):

  Another vectorization using CountVectorizer is set up for LDA.
  We fit the TF matrix to an LDA model with 3 components (topics) and extract the document-topic matrix.
  For each document, we identify the dominant topic and count the number of documents in each topic.
  We extract the topic-word matrix and print the top keywords for each topic.

5.Printing Results:

  We print the document-topic matrix, the count of documents in each topic, and the topic-word matrix to understand the clustering and topic extraction results.


Conclusion

  In this project, I tried out both K-means and LDA as examples of clustering and topic modeling.

  K-means has some limitations. It is very sensitive to outliers. As you may have already seen, it can produce very small clusters corresponding to outliers. And K-means also has 
  difficulties with clusters of different sizes and densities. That is why I randomly select equal size subsets of different star ratings reviews from the whole dataset.

  Latent Dirichlet allocation (LDA) is a generative statistical model that allows sets of observations to be explained by unobserved groups that explain why some parts of the data 
  are similar. The LDA model is highly modular and can, therefore, be easily extended. The main field of interest is modeling relations between topics. In this task, LDA did a 
  better job of clustering the reviews.
