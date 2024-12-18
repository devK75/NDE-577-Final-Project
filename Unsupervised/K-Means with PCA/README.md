# Wholesale Customers Clustering Analysis

This project involves analyzing and clustering the Wholesale Customers dataset to extract meaningful insights about customer behavior and spending patterns. The analysis employs dimensionality reduction techniques like Principal Component Analysis (PCA) and clustering algorithms such as K-Means and Agglomerative Clustering.

## Project Overview

The dataset contains information on wholesale spending across various product categories, including:
- Fresh
- Milk
- Grocery
- Frozen
- Detergents_Paper
- Delicassen

The goal is to:
1. Understand the relationships between features through exploratory data analysis.
2. Reduce dimensionality for easier visualization and interpretation.
3. Identify customer segments using clustering techniques.

## Key Steps and Insights

1. **Exploratory Data Analysis (EDA):**
   - Distribution plots and heatmaps revealed skewed data distributions and feature correlations (e.g., Grocery vs. Detergents_Paper).
   - Features like Fresh, Grocery, and Frozen exhibited strong right-skewed distributions.

2. **Dimensionality Reduction:**
   - PCA reduced the dataset to two principal components (PC1 and PC2), explaining the majority of variance.
   - PCA provided a foundation for clustering and visualization.

3. **Clustering Analysis:**
   - **K-Means Clustering:**
     - The Elbow Method identified two optimal clusters.
     - Clusters were visualized and showed distinct spending patterns:
       - Cluster 0: Customers with low PC1 and high PC2 values.
       - Cluster 1: Customers with high PC1 and low PC2 values.
     - Alignment of clusters with the `Channel` feature (Horeca vs. Retail) highlighted a partial relationship.

   - **Hierarchical Clustering:**
     - A dendrogram validated the two-cluster structure.
     - Consistency with K-Means clustering reinforced the reliability of results.

4. **Insights and Recommendations:**
   - **Cluster 0:** Likely represents smaller retailers with focused spending needs. Strategies include:
     - Bulk discounts on specific product categories.
   - **Cluster 1:** Includes larger clients or Horeca businesses with diverse purchases. Recommendations:
     - Offer premium services and broader inventory options.

## Files Included

- **Wholesale customers data.csv:** Dataset used for analysis.
- **Analysis notebook (.ipynb):** Contains code for EDA, PCA, clustering, and visualization.
- **Plots and Visualizations:** Output images showcasing data distributions, PCA results, and clustering.

## Technologies Used

- **Python Libraries:**
  - `pandas` and `numpy` for data manipulation.
  - `matplotlib` and `seaborn` for visualization.
  - `sklearn` for PCA and clustering algorithms.
- **Clustering Techniques:**
  - K-Means Clustering
  - Agglomerative Clustering





