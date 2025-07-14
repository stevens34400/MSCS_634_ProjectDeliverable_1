
# MSCS 634 Project Deliverable 1 – California Housing Dataset

---

## Dataset Summary

- **Name**: California Housing Dataset  
- **Records**: 20,640  
- **Attributes**: 9 (8 predictive features + 1 target: `MedHouseVal`)  
- **Source**: UCI Machine Learning Repository (via Scikit-learn)  
- **Domain**: Socioeconomic factors, housing valuation, urban and regional planning

The dataset contains aggregated housing data for California districts based on the 1990 U.S. Census. It includes information on income, housing age, occupancy, population, and geographic factors.

---

## Justification for Dataset Choice

This dataset was selected because:
- It satisfies the minimum criteria with over 20,000 records and 8 numeric attributes.
- It comes from a reliable, publicly available source suitable for educational purposes.
- The features allow for real-world regression modeling and socioeconomic insights.
- It offers opportunities for preprocessing, visualization, and downstream machine learning tasks.

> **Note:** I initially considered the Boston Housing Dataset, but due to ethical concerns and its removal from scikit-learn (v1.2+), I opted for the California Housing dataset as a more appropriate alternative.

---

## Data Cleaning Overview

**Steps Performed**:
- Verified no missing values using `isnull().sum()`.
- Confirmed the dataset has no duplicate rows.
- Used descriptive statistics and visualizations to detect noisy data.
- Detected outliers and right-skewed distributions in:
  - `AveRooms` (average number of rooms)
  - `AveOccup` (average occupancy)
  - `Population` (area population)
- Noted distributions for possible transformation (e.g., log scaling) in future phases.

---

## Exploratory Data Analysis (EDA)

**Key Techniques Used**:
- Correlation heatmap to assess linear relationships.
- Histogram and KDE plots to understand feature distributions.
- Boxplots to detect outliers and spread.

**Insights**:
- `MedInc` (median income) shows a strong positive correlation with `MedHouseVal` (target).
- `AveRooms` and `AveOccup` have long right tails — possible transformation candidates.
- `Latitude` and `Longitude` give spatial context, useful for geospatial modeling.
- Findings suggest feature scaling and transformation will improve model accuracy in later phases.

---

## Challenges and How They Were Addressed

| Challenge | Response |
|----------|----------|
| Original dataset (Boston Housing) removed due to ethical concerns | Switched to California Housing, which meets both ethical and technical standards |
| High variance in numeric features like `Population` and `AveOccup` | Identified through EDA; transformation planned for regression modeling |
| Data distributions not normalized | Skewed features noted for normalization in Deliverable 2 |

---

## Conclusion

This deliverable achieved:
- Careful dataset selection and validation
- Complete structural inspection and cleanliness verification
- Outlier and noise identification through robust visualizations
- Foundational insights to inform future regression, classification, and feature engineering steps
