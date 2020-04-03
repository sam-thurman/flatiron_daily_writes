# Clustering (k-means, hierarchical agglomerative)

### K-Means
</br>
The algorithm starts with points as centroids, analyzes all of it's nearest points' distances, and then moves to the new center of these points. The algorithm then analyzes nieghbor linkage at the new centroid, and again, encompassing new data points at this new centroid. This keeps happening until the groups are as defined as possible according to the algorithm. Over time, the centroids navigate themselves to the center of most similar data.
</br>

### Hierarchical Agglomerative
</br>
In hierarchical agglomerative clustering, the algorithm starts by treating every data point as a centroid, it then combines like points using some linkage metric that you assign. Each new group continues to accumulate data points until all points are members of one master group. You can stop the process at any given point to get the number of groups that you want. You can use a dendrogram to help determine this number of groups if you are unsure. A dendrogram shows each clustering step, and the distance between clusters when they were combined. The greater the distance between combining clusters, the less alike they are, and therefor, it is less likely that those data points have the same properties and same classifcation.