# Credit Card Customer Analysis Project 

<p align="center">
  <img src=images/credit_card.jpg /width=500>
</p>

 ### Project Overview:
 
This project consisted of evaluating characteristics of credit card customers. The given data consisted of features such as average credit limit, total credit cards, visits to the bank and online, and calls made to the bank. 

Evaluating the characteristics of the clusters consisted of implementing the well known clustering methods KMeans and Hierarchical.  

## Code and Resources Used 
**Python Version:** 3.9  
**Packages:** pandas, numpy, sklearn, matplotlib, seaborn

**Books Used**: 
- Grus, Joel. Data science from scratch: first principles with python. O'Reilly Media, 2019.
- Bruce, Peter, Andrew Bruce, and Peter Gedeck. Practical Statistics for Data Scientists: 50+ Essential Concepts Using R and Python. O'Reilly Media, 2020.
- McKinney, Wes. Python for data analysis: Data wrangling with Pandas, NumPy, and IPython. " O'Reilly Media, Inc.", 2012.

**URLs Used**: 
- https://towardsdatascience.com/understanding-the-concept-of-hierarchical-clustering-technique-c6e8243758ec
- https://towardsdatascience.com/a-deep-dive-into-k-means-f9a1ef2490f8


## Data Cleaning: 
The data itself was very clean as given with no missing values. The only cleaning that was done was to engineer features that I thought would be important for the clustering process. The features that were created were 'interactions', 'avg_credit_per_card', and 'avg_credit_per_interactions'. 


## EDA
The following images are highlights of the exploratory data analysis performed on this data set. A quick summary of each image is given. 

### KMeans Clustering
* Scatter plot giving the potential clusters along with their centroids.  

![](images/cluster_image.jpg )

* This elbow plot shows that the ideal number of clusters could potentially be three for KMeans clustering. 

![](images/elbow_plot.jpg)

* The following silhouette plot shows the average silhouette score for the data as well as how large each cluster is relative to the other clusters. Further analysis was done on other cluster sizes and this graph gave the best silhouette score. 

![](images/silhouette_plot.jpg)

### Hierarchical Clustering
* Dendrogram for the hierarchical clustering technique. This dendrogram was graphed using the 'Max' metric. The graph shows that three clusters could be optimal but the branches also have a long length, indicating large dissimilarity between the clusters. 

![](images/max_metric_dendrogram.jpg)

* Dendrogram for the hierarchical clustering technique. This dendrogram was graphed using the 'Ward' metric. The graph shows that again three clusters and the branches are relatively long indicating nice cluster dissimilarity. We will use this metric in the agglomerative clustering method as well as three clusters. 

![](images/ward_metric_dendrogram.jpg)

## Model Building: 

For this problem, we used two different clustering techniques: KMeans and Agglomerative Hierarchical Clustering. Analysis was done to find the best number of clusters for each technique. Various metrics were used for the hierarchical technique including: 'Complete (Max)', 'Weighted', 'Average', and 'Ward'. 

## Models Used: 
*	**KMeans Clustering** – Interpretable model and a baseline for seeing what could occur with clustering. 
*	**Hierarchical Clustering** – Given the amount of data, the Hierarchical technique was used for further analysis to contrast against KMeans. 


## Model performance

* KMeans Clustering: 
  * Silhouette score with three clusters: 0.1541

* Hierarchical Clustering: 
  *  * Silhouette score with three clusters: 0.1796

