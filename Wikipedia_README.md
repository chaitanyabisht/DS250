
## NLP feature extraction
We used tf-idf feature vector. TF-IDF (term frequency-inverse document frequency) is a statistical measure that evaluates how relevant a word is to a document in a collection of documents. This is done by multiplying two metrics: how many times a word appears in a document, and the inverse document frequency of the word across a set of documents. <br>
pic <br>

First we had the cleaned text, on that text stemming was applied i.e. keywords were extracted and stopwords were removed. For 3984 articles, feature vector of length 24,596 was obtained. Prebuilt library was used to obtain the feature vector. <br>
After this to shorten the feature vector, SVD was applied. The Singular Value Decomposition (SVD) of a matrix is a factorization of that matrix into three matrices. Also for this a prebuilt library was used and feature vector of length 1000 was obtained. <br>
Then cosine similarity was taken to find the similarity between 2 vectors, i.e. 2 articles. if similarity > 0.5, edge was drawn between nodes  as they show high similarity, belonging  to the same community. <br>
We used networkx library to draw the graph and calculate centrality metrics and clustering coefficient. <br>

