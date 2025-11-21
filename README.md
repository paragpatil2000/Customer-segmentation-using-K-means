
# Customer Segmentation Using K-Means Clustering

This project groups customers into different segments based on:
- Age
- Annual Income (k$)
- Spending Score (1–100)

The goal is to help businesses understand different types of customers and target them better.

## Dataset Columns
- CustomerID
- Gender
- Age
- Annual Income (k$)
- Spending Score (1–100)

## Steps in the Project
1. Loaded the dataset
2. Selected features (Age, Annual Income, Spending Score)
3. Scaled the data
4. Used the Elbow Method to find the best number of clusters
5. Applied K-Means clustering
6. Visualized the clusters

## Elbow Method
Used WCSS (Within Cluster Sum of Squares) to find the best value of K.
The elbow point gave the optimal number of clusters.

## Visualization Code
```python
plt.figure(figsize=(10,6))
plt.scatter(X[y_kmeans==0,0],X[y_kmeans==0,1],s=100,c='red',label='Cluster 1')
plt.scatter(X[y_kmeans==1,0],X[y_kmeans==1,1],s=100,c='blue',label='Cluster 2')
plt.scatter(X[y_kmeans==2,0],X[y_kmeans==2,1],s=100,c='green',label='Cluster 3')
plt.scatter(X[y_kmeans==3,0],X[y_kmeans==3,1],s=100,c='cyan',label='Cluster 4')
plt.scatter(X[y_kmeans==4,0],X[y_kmeans==4,1],s=100,c='magenta',label='Cluster 5')

plt.scatter(kmeans.cluster_centers_[:,0],kmeans.cluster_centers_[:,1],
            s=300,c='yellow',label='Centroids')

plt.title('Clusters of Customers')
plt.xlabel('Annual Income (k$)')
plt.ylabel('Spending Score')
plt.legend()
plt.show()
Interpretation
Cluster 1: Low income, low spending

Cluster 2: High income, high spending

Cluster 3: High income, low spending

Cluster 4: Average customers

Cluster 5: Low income, high spending

Conclusion
K-Means successfully grouped customers into different segments.
Businesses can use this information to target each customer group with better marketing strategies.
