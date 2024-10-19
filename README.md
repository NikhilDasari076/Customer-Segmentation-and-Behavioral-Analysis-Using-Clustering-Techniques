# Customer-Segmentation-and-Behavioral-Analysis-Using-Clustering-Techniques

**Project Overview**
This project aims to perform customer segmentation on a dataset of credit card users using various clustering techniques. The goal is to identify distinct customer groups based on their behavior, which can help businesses create personalized marketing strategies, improve customer retention, and optimize product offerings.

**Key Techniques Used:**
K-Means Clustering
DBSCAN (Density-Based Spatial Clustering)
PCA (Principal Component Analysis) for dimensionality reduction
Evaluation Metrics: Silhouette Score, Davies-Bouldin Index, and Calinski-Harabasz Index

**Dataset**
The dataset used in this project is a Credit Card Customer Data obtained from Kaggle. It contains customer information such as balance, purchases, cash advances, and credit limit. The dataset is used to segment customers based on these financial behaviors.

**Steps Involved in the Project**


**1. Exploratory Data Analysis (EDA)**
We begin by performing exploratory data analysis to understand the distribution of features and identify patterns and anomalies in the data. This includes:
Correlation Matrix: Visualizing correlations between features.
Outlier Detection: Identifying outliers using box plots and capping them to prevent model distortion.


**2. Feature Engineering**
Log Transformations: Applying log transformations to skewed features such as balance, purchases, and cash advances.
Interaction Features: Creating new features such as Purchase-to-Balance Ratio and Payments-to-Credit Limit Ratio to enrich the dataset.


**3. Clustering Analysis**


**K-Means Clustering**
Elbow Method: Used to determine the optimal number of clusters.
K-Means Clustering: Applied to both the original data and PCA-reduced data to segment customers into distinct groups.
Evaluation: Metrics such as Silhouette Score, Davies-Bouldin Index, and Calinski-Harabasz Index are used to evaluate the quality of clustering.


**DBSCAN (Density-Based Clustering)**
Hyperparameter Tuning: Grid search to find the optimal eps and min_samples values.
DBSCAN Clustering: Applied to both original data and PCA-reduced data.
Noise Detection: DBSCAN's ability to detect outliers and noise points in the dataset.
Evaluation: Using the same clustering evaluation metrics as K-Means.

**4. Dimensionality Reduction (PCA)**
PCA is applied to reduce the dataset to two principal components, making it easier to visualize clusters in 2D space.
Clustering on PCA-Reduced Data: Both K-Means and DBSCAN are applied to the reduced dataset for comparison with the original feature space.

**5. Cluster Evaluation**
After applying both clustering algorithms, the clusters are evaluated using three key metrics:
Silhouette Score: Measures how well each point fits within its cluster.
Davies-Bouldin Index: Measures the average similarity ratio between clusters.
Calinski-Harabasz Index: Measures cluster dispersion and separation.

**6. Business Insights**
K-Means tends to form tightly packed, well-defined clusters, making it ideal for businesses seeking precision in customer segmentation.
DBSCAN is better suited for detecting distinct customer groups and outliers, allowing businesses to identify niche or outlier customers who may need specialized marketing strategies.
Actionable Insights: Each cluster is analyzed to derive business insights that can guide personalized marketing, loyalty programs, and product recommendations.


**7. Visualizations**
Cluster Visualizations: Clusters are visualized in 2D using PCA to make it easier to understand the customer segments.
Feature Importance: Important features for segmentation are highlighted based on feature analysis and PCA.


**Key Findings**
DBSCAN provided better-defined clusters with higher Silhouette Scores and lower Davies-Bouldin Index values, indicating well-separated customer groups.
K-Means had more tightly packed clusters with high Calinski-Harabasz scores, which may be useful for precise marketing campaigns targeting homogeneous customer groups.

**Technologies Used**
Python
Pandas for data manipulation
Seaborn/Matplotlib for data visualization
Scikit-learn for clustering algorithms, PCA, and evaluation metrics


**Conclusion**
This project demonstrates the application of unsupervised learning techniques to perform customer segmentation. By using clustering algorithms like K-Means and DBSCAN, businesses can better understand customer behavior, identify distinct segments, and tailor marketing strategies to each group. The analysis also highlights the importance of using dimensionality reduction techniques like PCA and feature engineering to improve model performance and provide actionable insights.
