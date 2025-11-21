# Child Poverty Classification Using MLP

This project predicts child poverty levels across U.S. census tracts using ACS 2017 tract-level socioeconomic data. Child poverty rates were categorized into four meaningful groups using data-driven quartiles aligned with social policy.

## Dataset

- Features: Income, education, employment, housing, demographics

- Target: Child poverty rate split into four categories (low to very high poverty)

## Methodology

- Data preprocessing: normalization and one-hot encoding

- Models: Multilayer Perceptrons (3 to 5 layers) with sigmoid activations

- Optimizers: SGD, RMSProp, Adam

- Training with mini-batches and cross-entropy loss

## Results

- 3-layer MLP with SGD achieved ~60% accuracy

- Increasing depth with SGD led to vanishing gradients and lower accuracy

- Adaptive optimizers (RMSProp, Adam) significantly improved accuracy (~74%)

- Gradient analysis confirmed adaptive methods prevent vanishing gradients

- RMSProp and Adam performed similarly

## Conclusion

Adaptive optimizers are essential for training deeper MLPs on complex socioeconomic data. Proper feature scaling and meaningful class definitions enable effective modeling of child poverty levels.

## Usage

- Normalize and encode data.

- Train MLP with selected architecture and optimizer.

- Evaluate accuracy and training dynamics.
