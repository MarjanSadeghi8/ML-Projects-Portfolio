# Breast Cancer Survival Analysis – Summary

This project analyzes the Breast Cancer dataset from Kaggle to understand which clinical and demographic factors influence patient survival status (Alive vs. Dead).

# Dataset Overview

4,023 unique patient records

Features include: age, tumor size, grade, lymph node status, hormone receptor status, and survival months

No missing values

One duplicate removed

Highly imbalanced race distribution → Race feature dropped

Key Cleaning Steps

Removed redundant or highly correlated features:

T Stage (overlaps with Tumor Size)

Progesterone Status (overlaps with Estrogen Status)

differentiate (overlaps with Grade)

Encoded categorical variables

Standardized numeric features

# Main Insights

Tumor size and tumor grade strongly relate to survival—larger or higher-grade tumors show worse outcomes.

Age also affects survival; deceased patients tend to be older.

Lymph node features (N Stage, Regional Node Positive) show moderate correlation with survival and reflect disease severity.

Correlation heatmap shows no single dominant predictor, indicating survival depends on multiple interacting factors.

# UMAP Visualization

Both unsupervised and supervised UMAP projections show overlapping clusters between Alive and Dead patients.

This suggests survival outcomes cannot be easily separated in low-dimensional space and require more complex modeling.

# Conclusion

The dataset is clean, clinically rich, and suitable for prediction tasks. Survival is influenced by a combination of tumor characteristics, age, and staging features. These insights prepare the data for the next phase: feature engineering and model development.
