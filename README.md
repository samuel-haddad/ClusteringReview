# Clustering Review
**Keywords:** PCA, Cluster, KMeans, DBSCAN

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![scikit-learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-%233F4F75.svg?style=for-the-badge&logo=plotly&logoColor=white)
![Kaggle](https://img.shields.io/badge/Kaggle-035a7d?style=for-the-badge&logo=kaggle&logoColor=white)
![](https://api.visitorbadge.io/api/VisitorHit?user=samuel-haddad&repo=ClusteringReview&countColor=#40e0d0)

## Introduction
This project is an Unsupervised Machine Learning study with Python (Clustering & PCA). The focus was to further discuss the theories behind these models and present some visualization ideas.

You will see that the Kmeans technique was used, which makes this process iterative. What is the implication of this? That the results of your code might be a little different even with the same settings.

Finally, don't hesitate to send me tweaks and improvement suggestions.
Any collaboration is welcome.

Have fun! :-)

## **Model Theory**
Clustering techniques aim to reduce observations by grouping them according to varied criteria, but generally seeking:

1. Greater internal similarity (within groups)
2. Less external similarity (inter groups - external)

These similarities are verified by looking at the distances between observations. These distances can be calculated in different ways, but before presenting some of them, it is important to emphasize that, as they are distance measurements, we can state that this type of analysis is performed on continuous or discrete metric variables. **Categorical variables should not be used in these clustering models**, but they can help to understand groups of observations after applying them.
<br><br>

### **Distances**
Regarding distances, the two main ones are:
- Euclidean (most used) <br>
![formula](https://render.githubusercontent.com/render/math?math=\color{white}\large\d_E=\sqrt{\sum_{i=1}^k(x_i-w_i)^2})

- Minkowsky <br>
![formula](https://render.githubusercontent.com/render/math?math=\color{white}\large\d_p(x_i,x_j)=(\sum_{k=1}^d|x_i-w_i|^p)^\frac{1}{p})

### **Métodos**

**Hierarchical**<br>
The hierarchical method, also known as **dendogram** (which is actually the method's output), is a method in which groupings are created as distances between observations increase. At each level, a number of groups are created. This method, however, is usually not very efficient for large volumes of data.<br>

**Main techniques:**
- Single Linkage (closest neighbor)
- Complete linkage (farthest neighbor)
- Average linkage
- Centroid method (centroid)
- Ward's method
<br>

**Application Roadmap**
1. Definition of technique.
2. Calculation of distances (from standardized data).
3. Grouping fur shorter distance.
4. Definition of the distance between the first group and the others.
5. Repeat the previous step until you have a single group (top of dendrogram)
6. Draw the dendrogram,
<br>

**Number of clusters**<br>
The choice of the number of clusters can also be done in different ways. Overall, we seek a balance between the incremental gain from increasing the number of clusters and the costs involved (business, processing, marketing, etc). When this increase in the number of clusters no longer produces such distinct groups (closer, with less variability between them), this is usually where the ideal quantity (candidate) to work is.
- R²: the bigger, the better (greater distance between, lesser intra)
- Elbow (cotevel method): a number of clusters is searched for in the graph curve, where the variability between clusters becomes smaller.
- Silhoutte: compares the indoor x outdoor distances - the closer to 1 the better.
- CCC: search for the "fall" point on the graph, where the incremental gain falls.
<br><br>

**Non-hierarchical** <br>
In the non-hierarchical method, the process is performed iteratively from initial seeds, looking for a number of previously defined groups. The goal is still the same, to seek the greatest similarity within the group and the greatest possible between groups. These iterations are repeated until the data converge, that is, the changes cease to occur or become minimal. <br>

The techniques presented above in the topic of hierarchical method can be used to define the number of clusters in some cases of non-hierarchical modeling.

**k-Means**
1. A first centroid is selected.
2. The groups are created (marked)
3. The centroids are updated.
4. The process is repeated until convergence
<br>

**DBscan**
Density-based. In other words, groups are determined based on data density. For this, two parameters are defined:
- Eps: radius for determining the closest points.
- MinPts: minimum number of points within a point's radius (Eps-neighbors).

**Documentação:**
<br>https://scikit-learn.org/stable/modules/clustering.html </br>


<br> > **Bonnus track:** https://machinelearningmastery.com/threshold-moving-for-imbalanced-classification/
<br> > **Kaggle:** https://www.kaggle.com/code/haddads/cc-clustering/data
