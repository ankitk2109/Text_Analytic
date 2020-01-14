# Clustering: k-Means

**Task1. Use the init_board fn to randomly generate 15 points; store this output and set the data variable to it. Now running this set 10 times and notice the clusters found by k-means. Checking the results of these runs and the extent to which the same clusters are found.**

Ans. 
Kmeans clustering: It is a simple unsupervised learning algorithm that is used to solve clustering problems. It follows a simple procedure of classifying a given data set into a number of clusters, defined by the letter "k," which is fixed beforehand. The clusters are then positioned as points and all observations or data points are associated with the nearest cluster, computed, adjusted and then the process starts over using the new adjustments until a desired result is reached[1].
The init_board function is used to generate 15 random points. These random points are then grouped into 3 clusters as k value is set to 3.
Below are the 15 generated random points.

![image](https://user-images.githubusercontent.com/26432753/72312706-d249ff00-3680-11ea-930f-74c49593f923.png)

Running through the data 10 times, generates 4 different formations. The different categories are shown below.

![image](https://user-images.githubusercontent.com/26432753/72312717-de35c100-3680-11ea-9c1f-97641301b4dd.png)

Out of 10 runs 6 times similar cluster are formed and 4 times different categories are identified. The reason for different cluster formation is because, in each run random centroids are selected and based on distance the data points are categorized into a cluster. However selecting random points cause the cluster to take noise into consideration as well. Hence whenever the centroids are changed data points in each cluster also change.

**Task2. Now, creating another set of data, again with 15 points. We should construct this data-set to have very clear clusters (a bit like the simple 6-point example shown in Code).**
**Now running this set 20 times and notice the clusters found by k-means. Checking the results of these runs and the extent to which the same clusters are found.**

Ans: Following data set is created with 15 different points.

![image](https://user-images.githubusercontent.com/26432753/72312810-281ea700-3681-11ea-83ee-485eb47e9933.png)


Running through the data 20 times, generates 4 different formations. These different clusters are shown below.

![image](https://user-images.githubusercontent.com/26432753/72312822-379df000-3681-11ea-9a57-6758b27341bc.png)

Out of 20 runs, 4 different clusters are formed. Remaining 16 clusters are repeated to one of the category shown above. The variations in this set is less than the previous set because the selected data points are such that their intra-cluster distance is less and the inter cluster distance is large hence clear clusters boundaries are defined and only few variation is noticed.

**Task3. We need to find why k-means produces different answers on different runs.**

Ans:
Following are the issues with kMeans due which different answers are produced on different runs:
a)KMeans may not find the global optimum value (random initial points).

b)KMeans clustering algorithm places the initial seeds (cluster centers) randomly. So each run of the algorithm will have a different initial set of seed locations, and as such (slightly) different outcomes. The algorithm is often executed multiple times and there is an error measurement calculated as the mean square distance of each point to the cluster centroid to which it belongs

c)The algorithm contains a certain random element that repeatedly uses the same starting points to find the global solution. But each time, owing to the algorithm's pseudo-random nature, slightly different clusters are obtained[2].

d)Starting with predefined initial seeds instead of randomly selected seeds for the centroids will ensure a consistent answer.

e)As the location of the initial centroids is random, results may not be comparable and show lack of consistency. Also, K-means produces clusters with almost equal number of data points in it, although the data might be different completely and it’s very sensitive to outliers and noisy data[3].

Two Techniques to handle above problems:
a)K-means++: It is a randomized variant of the furthest point heuristic. It chooses the first centroid randomly and the next ones using a weighted probability pi = costi/SUM(costi), where costi is the squared distance of the data point xi to its nearest centroids. This algorithm is an O(log k)- approximation to the problem[4].
Algorithm :
i.Take one center c1, chosen uniformly at random from X.
ii.Take a new center ci, choosing x ∈ X with probability 
iii.Repeat Step (i) until we have taken k centers altogether.
iv.Proceed as with the standard k-means algorithm.
K-means++ clustering chooses its first center randomly but afterwards it takes next points from Data-set with some probability hence this algorithm converges way early than simple kmeans. So we can use kmeans++ to have better results than kmeans.

b)Furthest point heuristic (Maxmin): It selects an arbitrary point as the first centroid and then adds new centroids one by one. At each step, the next centroid is the point that is furthest (max) from its nearest (min) existing centroid. This is also known as Maxmin[5].

Algorithm[7]:
i.The farthest-point heuristic starts with an arbitrary point s1. 
ii.Pick a point s2 that is as far from s1 as possible. 
iii.Pick si to maximize the distance to the nearest of all centroids picked so far. That is, maximize the min {dist (si, s1), dist (si, s2), ...}. 
iv.After all k representatives are chosen we can define the partition of D: cluster Cj consists of all points closer to sj than to any other representative.

Obviously, farthest-point heuristic based method has the time complexity O (nk), where n is number of objects in the dataset and k is number of desired clusters. Furthermore, one can implement farthest-point heuristic based method in constant dimension in O (nlogk) time[6].
                
References:
[1]Krishni, “K-Means Clustering ”, 2019 [Online]. Available: https://www.techopedia.com/definition/32057/k-means-clustering [Accessed Nov. 3, 2019]
[2]R. Oldenhuis, “Matlab: Kmeans gives different results each time”, 27, Aug 2012 [Online]. Available: https://stackoverflow.com/questions/12137282/matlab-kmeans-gives-different-results-each-time [Accessed Nov. 3, 2019]
[3]D. L. Yse, “The Anatomy of K-means”, 22, Feb 2019 [Online]. Available: https://towardsdatascience.com/the-anatomy-of-k-means-c22340543397 [Accessed Nov. 3, 2019]
[4]D. Arthur,S. Vassilvitskii, “k-means++: The Advantages of Careful Seeding”, 2006-13 [Online]. Available: http://ilpubs.stanford.edu:8090/778/1/2006-13.pdf [Accessed Nov. 3, 2019]
[5]P.Fränti,S. Sieranoja, “How much can k-means be improved by using better initialization and repeats?”, 15, Apr 2019 [Online]. Available: https://www.sciencedirect.com/science/article/pii/S0031320319301608 [Accessed Nov. 3, 2019]
[6]Z. He, “Farthest-Point Heuristic based Initialization Methods for K-Modes Clustering”, 9, Nov 2006 [Online]. Available: https://www.researchgate.net/publication/1960044_Farthest-Point_Heuristic_based_Initialization_Methods_for_K-Modes_Clustering  [Accessed Nov. 3, 2019]

