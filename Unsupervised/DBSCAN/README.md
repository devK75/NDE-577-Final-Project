# Customer Segmentation with DBSCAN Clustering

This project analyzes customer behavior by segmenting a dataset using the DBSCAN clustering algorithm. The dataset includes demographic and spending information, allowing for insights into customer groups based on annual income and spending scores.

## Project Overview

The dataset contains 200 customer entries with the following features:
- **Genre:** Customer's gender.
- **Age:** Customer's age.
- **Annual_Income (k$):** Annual income in thousands of dollars.
- **Spending_Score:** Score assigned based on spending behavior.

The goal is to:
1. Visualize the distribution of customer demographics.
2. Segment customers into clusters using DBSCAN to identify patterns in income and spending.
3. Use clustering insights for targeted marketing strategies.

## Key Steps and Insights

### 1. Data Preprocessing
- Dropped unnecessary features (e.g., `CustomerID`).
- Checked for missing values and feature correlations.
- Saved relevant features (Annual Income and Spending Score) for clustering.

### 2. Exploratory Data Analysis (EDA)
- Created pie charts for gender distribution.
- Heatmap revealed strong correlations between some features, highlighting potential redundancies.
- Imbalanced gender distribution (more females than males) observed.

### 3. Clustering with DBSCAN
- DBSCAN clustering applied with `eps=3` and `min_samples=4`.
- Generated multiple clusters and noise points, reflecting customer segments.
- Sensitivity to DBSCAN parameters led to fragmented clusters and significant noise.

### 4. Visualization
- Scatter plots illustrated clusters with unique spending and income profiles.
- Clear separations between clusters highlighted potential customer segmentation opportunities.

### Insights
- **Clusters:** Distinct customer groups were identified, each with specific income and spending patterns.
- **Noise Points:** Customers outside clusters indicate unique or outlier behavior, requiring tailored strategies.
- **Correlations:** Spending Score strongly correlated with Annual Income, suggesting potential multicollinearity.

### Challenges
- DBSCAN's sensitivity to parameters (`eps`, `min_samples`) required careful tuning.
- Imbalanced gender representation and fragmented clusters necessitate further analysis and alternative algorithms.

## Technologies Used

- **Python Libraries:**
  - `numpy` and `pandas` for data manipulation.
  - `matplotlib` and `seaborn` for visualizations.
  - `sklearn` for DBSCAN clustering.
- **Clustering Algorithm:**
  - DBSCAN (Density-Based Spatial Clustering of Applications with Noise)


