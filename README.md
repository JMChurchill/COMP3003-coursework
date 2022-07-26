# COMP3003-coursework
Machine Learning Coursework. 
## Contents
* Set Exercise - K-means Clustering
* Report - Pattern Recognition
## Report 
Implemented a supervised learning neural network model to detect and classify intrusions on a network based on various network parameters.
### Neural Network
![Neural Network View](https://user-images.githubusercontent.com/57601700/181074335-c55f347a-18d6-4645-8cc0-54eee30061c8.png)
### Epochs VS Cross Entropy
![Epochs vs Cross Entropy](https://user-images.githubusercontent.com/57601700/181074449-f6e3f961-6596-4286-912c-a05615b9eefa.png)
### Performance Metrics
![CrossEntropyVsIterations](https://user-images.githubusercontent.com/57601700/181075022-dd11e574-22d0-457c-aaa6-7b733df0afd9.png)
![AccuracyVsIterations](https://user-images.githubusercontent.com/57601700/181075044-7c56b152-fcfc-4353-bdd1-646a8137239b.png)
![RecallRateVsIterations](https://user-images.githubusercontent.com/57601700/181075064-c837a287-d265-4c9d-94a1-3c97883917e0.png)
![PrecisionVsIterations](https://user-images.githubusercontent.com/57601700/181075103-bc7e108c-31fe-45e4-9d6e-081e4f8f847b.png)
#### Averate Performance Metrics Based on 10 models
![AveragePerformance](https://user-images.githubusercontent.com/57601700/181075392-38f56d3f-8d24-4fc7-837f-a3de06ba0559.png)
#### Confusion Matrix
![ConfusionMatrix](https://user-images.githubusercontent.com/57601700/181075495-342f4da4-b2bf-409f-868a-045b0052c96b.png)
### Performance VS Neurons
Exploring the effect changing neural network parameters had on the model’s classifier performance.
#### Adjusting the number of Neurons
![PerformanceVsNeurons](https://user-images.githubusercontent.com/57601700/181076252-b5fb77d8-328a-49a8-8a02-a925f3348571.png)


#### Adjusting the Learning Rate
![PerformanceVsLearningRate](https://user-images.githubusercontent.com/57601700/181076262-2c552d30-59dd-45aa-9515-bfdecc5b2033.png)



## Set Exercise 
Implemented K-Means Clustering Algorithm on to categories a dataset.
### Process
![KmeansClusteringFlowChart](https://user-images.githubusercontent.com/57601700/181076787-f5df646f-4b02-419f-9568-b0430f0fa143.png)
### Implementation
To implement the K-means clustering algorithm, I started off by generating my original gaussian distributed dataset. I did this by first generating three distinct but partially overlapping clusters of 250 samples each. I then plotted each dataset on a single graph for a point of reference later.
#### Original Dataset
![OriginalDataset](https://user-images.githubusercontent.com/57601700/181077079-8a9b8460-0bc8-4661-8785-4f9978ced9d0.png)
#### Merged Dataset
![MergedDataset](https://user-images.githubusercontent.com/57601700/181077189-0beb6ac5-a11a-4cda-bb9a-6a8d0a61f113.png)
#### K-means clustering graph
![KmeansClusteringGraph](https://user-images.githubusercontent.com/57601700/181077425-b3975f8f-9a0f-419c-83c0-500a6f44fb58.png)

#### Overall distance vs number of iterations
![OveralDistanceVsNumberOfIterations](https://user-images.githubusercontent.com/57601700/181077600-cc01d294-3ce4-4d14-9ee4-76b8cb5ff289.png)

#### ElboPlot
![ElbowPlot](https://user-images.githubusercontent.com/57601700/181077685-59b5a9a2-b3a2-4553-aaa3-d03065d1ff8d.png)

### Conclusion
K-means clustering yields good results for an algorithm that is relatively simple, however when implementing the algorithm from first principles I noticed many implementations that were not initially apparent. Predominantly there being no theoretical solution to finding the optimal value of k before running the algorithm. There exist methods including Elbow and Average silhouette. These take a more brute force approach needing the k means algorithm to be run several times with different values of k then determining the optimal value after the fact, for large datasets this can take a lot of time. 

Another issue with the algorithm is it is very sensitive to its initial centroid selection; certain initial centroids can produce much less optimal clusters than others. This is due to the algorithm getting caught in a local optimum. This can be mitigated by repeating the algorithm multiple times with different starting centroids and comparing the variance or within-cluster sum of squares, this is this extension to k-means is known as k-means++.

A smaller drawback of k-means is it can be sensitive to outliers in a dataset. If an outlier is far from the general trend of the data, it can skew the centroids towards that direction. This can be avoided by removing outliers from a dataset.


