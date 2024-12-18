# Bike Rental Analysis with Linear Regression

This project analyzes factors influencing bike rentals using a dataset of hourly bike rental counts. A Linear Regression model is employed to predict rental counts based on weather, temporal, and categorical features.

## Project Overview

The dataset contains information on bike rentals with the following key features:
- **datetime**: Timestamp for the observation.
- **season**: Categorical feature representing the season.
- **holiday**: Whether the day is a holiday (binary).
- **workingday**: Whether the day is a working day (binary).
- **weather**: Weather condition (categorical).
- **temp**: Actual temperature in Celsius.
- **atemp**: Perceived temperature in Celsius.
- **humidity**: Relative humidity.
- **windspeed**: Wind speed.
- **casual**: Number of casual bike rentals (train data only).
- **registered**: Number of registered bike rentals (train data only).
- **count**: Total bike rentals (target variable in train data).

### Objectives
- Explore data trends and relationships among features.
- Train a Linear Regression model to predict rental counts.
- Analyze model performance and identify key predictors.

---

## Key Steps and Insights

### 1. Data Preprocessing
- **Combined Datasets**: Merged training and test datasets with placeholder columns to align structure.
- **Feature Engineering**:
  - Extracted the hour from the `datetime` column for temporal analysis.
- **Data Distribution**:
  - `humidity`, `temp`, and `atemp` followed normal distributions.
  - `windspeed`, `casual`, `registered`, and `count` were skewed.

### 2. Exploratory Data Analysis
- **Seasonal and Hourly Trends**:
  - Better weather conditions were observed during fall (lower weather scores).
  - Rental activity peaked during early hours for registered users.
- **Feature Relationships**:
  - Bar plots and histograms highlighted variations in key features by time and weather.

### 3. Model Training
- **Model**: Linear Regression.
- **Data Split**:
  - Training and test datasets split with 70-30 proportion.
  - `count` used as the target variable.
- **R-squared Score**:
  - Model explained approximately **33% of the variance** in rental counts (R² = 0.33).

### 4. Feature Importance
The model's coefficients highlighted the following:
- **Positive Predictors**:
  - `season`, `hour`, and `atemp` increased rental counts.
- **Negative Predictors**:
  - `holiday` had the largest negative impact, reducing rentals on holidays.
  - `humidity` also negatively affected rentals.

---

## Insights and Recommendations
- The model successfully identified trends in bike rentals but showed a low R² score, indicating:
  - Non-linear relationships may exist between features and the target variable.
  - Noise or missing interactions in the data may limit model performance.
- Future enhancements:
  - Explore non-linear regression techniques.
  - Add features such as traffic conditions or special events.
  - Use advanced models like Random Forests or Gradient Boosting.

---

## Technologies Used
- **Python Libraries**:
  - `pandas` and `numpy` for data manipulation.
  - `matplotlib` and `seaborn` for visualizations.
  - `scikit-learn` for Linear Regression and evaluation metrics.
- **Linear Regression**:
  - Explained feature impacts through coefficients.
  - Evaluated performance with R² score.

## Conclusion
This project provides a foundation for understanding bike rental dynamics and predicting rental counts. While Linear Regression captured basic trends, future iterations will explore more robust models to improve prediction accuracy and insights.

