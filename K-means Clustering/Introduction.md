##K-Means Clustering Algorithm : 
<b>Input : </b>k,  x<sub>1</sub>, x<sub>2</sub>,..........,x<sub>n</sub> <br>
k is the number of clusters that we are trying to obtain and x<sub>1</sub> to x<sub>n</sub> are set of data points whose clustering is to be done.
<br>
<b>Output : </b>k sets of clusters.
####Outlines of algorithm : 
1. Place centroids c<sub>1</sub>, c<sub>2</sub>,.......,c<sub>k</sub> at random locations<br>
2. Repeat unitl convergence : <br>
 * for each point x<sub>i</sub> :<br>
    * find nearest centroid c<sub>j</sub><br>
    * assign x<sub>i</sub> to the cluster j<br>
 * for each cluster j = 1, 2, 3,...., k
    * new centroid c<sub>j</sub> = mean of all points x<sub>i</sub> assigned to that cluster in previous step.<br>
3. Stop when none of the points change there cluster <b> or </b> when the maximum number of iterations have been reached.   
    
####Complexity of the algorithm : O(#iterations * #clusters * #instances * #dimensions) 

####Advantages of this technique : 
1. Fast and efficient in terms of computational cost.
2. Works great if clusters are spherical.
3. k-means becomes a great solution for pre-clustering, reducing the space into disjoint smaller sub-spaces where other clustering algorithms can be applied.
4. Using some variations like careful initial placing of centroids, allowing clusters to be split and merged chances of finding the global optimum can be improved.

####Limitations of this technique : <br>
1. It finds a local optimum but might miss a global optimum.
2. Does not work on categorical data because the mean must be defined on attribute type. Although, a variation of K-means, K-modes does handle categorical data. As the name suggest, instead of using means, it uses modes.
3. Only convex-shaped clusters are found.
4. It does not handle outliners well.

This is from my understanding of K-means algorithm. Please raise an issue if I err somewhere.

