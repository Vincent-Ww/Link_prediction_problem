python version: python3

The library we use:
numpy
pandas
sklearn
tensorflow
keras
networkx


Our submission includes 4 notebooks: 
1. sampling.ipynb
2. feature_engineering.ipynb
3. ML.ipynb
4. DL.ipynb


sampling.ipynb
1. convert the training set to that at least one paper exists which includes the two incident authors as co-authors. 
2. construct an undirected graph from the new training set
    Now every instance in training set has just two feautures: source and sink.
2.  choose the positive samples and negative samples as training set
	positive samples: all the edges in the graph
	positive samples: randomly sample pair of nodes that don't construct an edge in the graph
3. save the positive samples and negative samples in "data/pos_samples.npy" and "data/neg_samples.npy" respectively.


feature_engineering.ipynb
1. generate 22 features for each edge in the training set and test set
	edge-based features: Jaccard Coefficient, Resource Allocation Index, Adamic-Adar Index, Preferential Attachment, 
			  Within Inter Cluster, Common neighbour Soundarajan Hopcroft, Resource Index Soundarajan Hopcroft, Shortest Path Distance 

	node-based features: Degree Centrality, Eigenvector Centrality, Load Centrality, Closeness Centrality, Clustering, K-Core Number, Average Neighbour Degree 

2. save the new training set and test set in "model" folder




ML.ipynb
1. standandrize the training set and test set
2. train the SVR model
3. use the trained model to make prediction on test set
4. save the result(csv file)




DL.ipynb
1. standandrize the training set and test set
2. set the hyperparameters
3. construct the feed-forward neural network
4. train the FFNN
5. use the FFNN model to make prediction on test set
6. save the result(csv file)