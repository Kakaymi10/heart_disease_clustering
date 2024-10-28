# Heart Disease Dataset Analysis

## Overview

This project involves analyzing a dataset of medical records to identify patients at high risk of developing heart disease. By employing unsupervised learning techniques, we aim to cluster patients based on their medical history and identify risk factors associated with heart disease. The dataset, sourced from the UCI Machine Learning Repository, contains 303 instances and 14 attributes, including age, sex, chest pain type, blood pressure, serum cholesterol, and a target variable indicating the presence or absence of heart disease.

## Objectives

1. **Exploratory Data Analysis (EDA)**: Gain insights into the dataset's structure, relationships between features, and detect any patterns or anomalies.
  
2. **Data Preprocessing**: Handle missing values, scale the features, and encode categorical variables to prepare the data for clustering.

3. **Clustering Techniques**:
   - Apply **K-means clustering** and optimize the number of clusters (k).
   - Utilize **Hierarchical clustering** to explore alternative clustering methods.
   - Implement **DBSCAN** for density-based clustering.

4. **Dimensionality Reduction and Visualization**:
   - Use **Principal Component Analysis (PCA)** and **t-SNE** to visualize the clusters and understand the relationships between variables.

5. **Gaussian Mixture Models (GMMs)**: Identify risk factors associated with heart disease using GMMs.

6. **Performance Evaluation**: Assess the clustering performance using metrics such as silhouette score and Davies-Bouldin index.

7. **Comparison of Clustering Algorithms**: Compare the performance of different clustering algorithms and determine the best one based on the evaluation metrics.

## Conclusion

Here’s a refined conclusion section based on your clustering analysis results:

---

## Conclusion

The analysis of the heart disease dataset revealed distinct clustering patterns, dividing the data into four clusters. This finding contrasts with the ground truth, which contains five labels. The discrepancies suggest that categorical variables such as sex, chest pain type (cp), and resting electrocardiogram results (restecg) significantly influence the clustering outcomes, providing separability that does not fully align with the original disease categories.

In health data clustering, these variables are crucial, as they encapsulate important patient characteristics that may lead to identifiable groupings. However, the alignment with ground truth categories is not perfect, indicating the complexity of health data and the interplay of various factors in determining heart disease risk.

### Performance Metrics

- **Silhouette Scores**:
  - KMeans: **0.120**
  - Hierarchical: **0.118**
  - DBSCAN: **N/A** (all points classified as noise)
  - GMM: **0.104**

- **Davies-Bouldin Scores**:
  - KMeans: **2.554**
  - Hierarchical: **2.184**
  - DBSCAN: **N/A** (all points classified as noise)
  - GMM: **2.443**

Based on the performance metrics, KMeans emerged as the best clustering algorithm for this dataset, evidenced by its higher silhouette score and lower Davies-Bouldin score. Despite the clustering not perfectly matching the ground truth labels, KMeans demonstrates its effectiveness in revealing underlying patterns within the health data, highlighting the importance of further exploration and refinement of clustering methodologies in the healthcare domain.
