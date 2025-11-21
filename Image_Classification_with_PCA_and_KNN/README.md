# Snake Breed Classification
The dataset used for this project is "Identifying Different Breeds of Snakes – Snake Breed Classification" from Kaggle. It contains 13,000+ JPEG images across 35 snake species. Our goal is to build a model that can classify a snake species from an input image.

## Dataset Description

- More than 13,000 raw images

- 35 species, each stored in its own folder

- Each folder = one species → clear supervised classification task

- Image data consists of diverse shapes, textures, and patterns

- JPEG format, varied lighting/background conditions

## Prediction Goal

- Given an image of a snake, predict its species (one of 35 classes)

- Aim for > 80% accuracy for meaningful real-world use

- Serve as a foundation for a more advanced classifier (CNN, ViT, etc.)

## Methods Used

- Principal Component Analysis (PCA)  
- Randomized Principal Component Analysis (Randomized PCA)  
- Histogram of Oriented Gradients (HOG) feature extraction  
- DAISY feature descriptor  
- k-Nearest Neighbors (kNN) classifier  
- Stratified K-Fold cross-validation  

## 🌍 Why This Dataset Matters

Species recognition is useful for:

🧪 Ecologists tracking biodiversity

🐍 Wildlife researchers identifying species in the field

🎓 Educators teaching herpetology

🚶 Hikers / nature enthusiasts identifying snakes for safety and education

Automated recognition connects machine learning with ecology and public engagement

## Business Value

- Supports research, education, and wildlife monitoring

- Provides a starting point for building a mobile snake-identifier tool

- Even moderate accuracy (>80%) helps with:

- Quick ecological surveys

- Field identification support

- Reducing human–snake conflict by improving awareness
