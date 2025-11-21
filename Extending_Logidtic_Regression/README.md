# ME/CFS vs Depression Classification

This project focuses on building a multi-class classification model to differentiate between Myalgic Encephalomyelitis / Chronic Fatigue Syndrome (ME/CFS), Depression, and their comorbid condition ("Both"). Using a rich clinical and demographic dataset from Kaggle, we explore interpretable logistic regression models implemented from scratch and analyze their performance in a clinically relevant context.
Patients suffering from ME/CFS and Depression often exhibit overlapping symptoms such as fatigue, cognitive impairment, and sleep disturbances, which complicates accurate diagnosis. Our goal is to develop a transparent and interpretable classification model that supports clinicians by providing data-driven insights and helps identify key differentiating features to improve diagnosis and treatment decisions.

## Dataset

The dataset is sourced from [Kaggle: ME/CFS vs Depression Classification Dataset](https://www.kaggle.com/datasets/storytellerman/mecfs-vs-depression-classification-dataset) and contains detailed physiological, psychological, and lifestyle information for 1,000 individuals diagnosed with ME/CFS, Depression, or Both. Features include fatigue severity scores, PHQ-9 depression scores, sleep quality indices, stress levels, and more.

## Methods Used

- Logistic Regression (implemented from scratch) with multiple solvers:  
  - Gradient Descent  
  - Stochastic Gradient Descent  
  - Newton Method  
  - BFGS (custom and SciPy implementation)  
- One-vs-All (OvA) framework for multi-class classification  
- Regularization: L1, L2, and Elastic Net  
- Feature selection and interpretability analysis  
- Dimensionality reduction (PCA and Randomized PCA)  
- Feature extraction techniques: Histogram of Oriented Gradients (HOG), DAISY descriptor  
- k-Nearest Neighbors (k-NN) classifier for feature evaluation  

## Results & Evaluation

- The best model used SGD with L1 regularization (C=10), achieving a test accuracy of **79.5%** and a macro-F1 score of **0.764**, matching scikit-learn’s implementation.  
- Newton’s method was fastest, BFGS (SciPy) most efficient among quasi-Newton solvers; all solvers achieved nearly identical accuracy.  
- Per-class performance:  
  - ME/CFS: Near-perfect recall (0.987)  
  - Depression: Balanced F1 score (0.741)  
  - Both: Moderate F1 score (0.589) due to symptom overlap.  
- Feature importance analysis highlighted fatigue severity, PHQ-9 depression score, sleep quality, and stress level as critical predictors.  
- Collapsing “Both” into one of the single diagnoses increased accuracy but reduced clinical interpretability and diagnostic precision.  
- Multi-label classification showed promise for handling comorbidity more realistically, with macro-F1 ~0.94.
