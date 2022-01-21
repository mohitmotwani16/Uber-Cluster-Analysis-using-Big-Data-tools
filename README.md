# Uber-Cluster-Analysis-using-Big-Data-tools
## Introduction
The Project Uber Cluster Analysis aims at:
- To help Uber serve the customer faster as vehicles are placed closer to potential customers.
- Make Uber booking faster and seamless for customers.
- To help drivers know about peak time and hotspot locations for maximum profit.
- Deciding optimal pricing by analysing which cluster deals with maximum requests, peak times etc.

## Problem Description
The Uber pickup data is analyzed to determine ride pickup clusters as zones and their centroids as hubs so that maximum cars can be made available around these hubs. This would help ensure minimum distance and time to cover to reach to the assigned customer trip request. 

## Dataset
The Uber trip dataset, which contains data generated by Uber from New York City.
The data from New York City which has five boroughs: Brooklyn, Queens, Manhattan, Bronx, and Staten Island. 

![image](https://user-images.githubusercontent.com/52165191/150493048-881edf53-066b-4b73-ad40-38c8643e4068.png)

## Solution Approach
This is a business case of Clustering – Unsupervised learning problem. Clustering algorithm like K-means, Bisecting K-means are used to solve this business problem. 

## KMeans clustering
We use elbow curve to find optimal number of clusters at for our dataset the optimal number of clusters turn out to be 8.
KMeans Cluster Centers: 
- [ 40.7301, -73.9982]
- [ 40.7655, -73.9734]
- [ 40.7817, -73.2536]
- [ 40.6579, -73.7866]
- [ 40.6997, -74.2012]
- [ 40.7917, -73.8882]
- [ 40.6863, -73.9629]
- [ 40.8554, -73.6578] 

![image](https://user-images.githubusercontent.com/52165191/150493212-4e1f1598-da59-4452-9bc5-1f401fb8cc18.png)

## Location of centroids over map

![image](https://user-images.githubusercontent.com/52165191/150493760-a6491949-84ed-41e7-8081-6bd3f6f2f2f9.png)


## Data Exploration
We can use Spark SQL to explore the dataset. Here are some example queries using the Spark
SQL. We will also replicate the same results that we get using Spark SQL by calling the Spark
Dataframe APIs directly.
1. Which hours of the day and which cluster had the highest number of pickups?
![image](https://user-images.githubusercontent.com/52165191/150493832-650e92ec-97c0-45f3-8ee3-c097a08dccfc.png)

2. How many pickups occurred in each cluster?

![image](https://user-images.githubusercontent.com/52165191/150494125-a053075a-5eb7-41f4-96a7-b76e6b3223a1.png)

3. How many pickups occurred in each hour?

![image](https://user-images.githubusercontent.com/52165191/150494285-88755901-ae36-4b5d-8c26-fbf57f078733.png)

## Management Actions
- Uber can use these centroids as their hubs. Drivers should be instructed to reach nearest to the cluster-centroid(hub) while waiting for the incoming trip demand.
- More cars should be made available during peak demands.
- If trip demand is more than available cars, then surge pricing should be applied. 
- Effective taxi dispatching will facilitate each driver and passenger to reduce the wait time to seek out one another. The model is employed to predict the demand on points of the city.

## Conclusion
- Machine learning Clustering algorithms are applied to big data specifically Uber trips pickups as a case study.
- In this project we show how clustering helps Uber in optimal pricing, the optimal position of cars in order to serve their customer faster and grow their business.
- The merit of the project is that it explains the functioning of how cabs are assigned to passengers based on an unsupervised algorithm and explains the key concepts of machine learning.






