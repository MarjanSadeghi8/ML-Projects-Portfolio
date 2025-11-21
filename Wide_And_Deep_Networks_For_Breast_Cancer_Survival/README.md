# Breast Cancer Survival Prediction Using Wide-and-Deep Neural Networks

This project predicts breast cancer survival outcomes using the Breast Cancer Dataset from Kaggle
, containing 4,024 patients with demographic, pathological, and receptor-related features. The target variable is survival status (Alive or Dead).

## Dataset

- Features: Age, race, marital status, tumor size, lymph node involvement, stage classifications (T Stage, N Stage, 6th Stage, A Stage), tumor grade, differentiation, hormone receptor status.

- Target: Survival status (Alive/Dead)

## Methodology

- Preprocessing: One-hot encoding for categorical features, scaling for numerical features, cross-product feature creation.

- Model: Wide-and-deep neural network

- Wide branch: memorizes interactions among categorical variables

- Deep branch: captures higher-order nonlinear relationships

- Training: Stratified 5-fold cross-validation and 80/20 train-test split

- Evaluation Metrics: ROC AUC, PR AUC, F1 score

## Results

- Wide-and-deep models achieved:

  - ROC AUC ≈ 0.86–0.87

  - PR AUC ≈ 0.96–0.97

  - F1 score ≈ 0.94

- Deep-only MLP performed similarly; wide branch did not significantly improve metrics

- Embedding analysis (PCA) showed meaningful latent structures aligned with clinical progression

- Models generalized well with no evidence of overfitting

## Conclusion

Wide-and-deep architectures provide a robust framework for structured medical data. In this dataset, moderately deep networks capture most relevant patterns, and the wide branch may not add measurable value when features are dense and informative. The project highlights the interpretability, generalization, and internal feature learning potential of neural networks in healthcare analytics.
