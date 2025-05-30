# Olfactory Mixture Similarity Prediction (Ensemble Model)

## Project Overview
This project aims to predict perceptual similarity between pairs of molecular mixtures. It reimplements two state-of-the-art 2024 models: **UMich CASI** and **belfaction**, then ensembles them to improve predictive performance.

## Models Implemented
- **UMich CASI**: Focuses on weighted GNN-based molecular embeddings and mixture-level representations using exponential scaling.
- **belfaction**: Uses a rich set of statistical and molecular features with an ExtraTrees ensemble model.

## Ensemble Strategy
Three ensemble approaches were explored:
- Simple 50-50 averaging
- Optimized scalar-weighted combination
- Linear stacking (meta-learner: Linear Regression)


## How to Run
1. Unzip the file.
2. Run in this order:
   ```
   python code/extract_umich_features.ipynb
   python code/train_umich_catboost.ipynb
   python code/extract_belfaction_features_train_ExtraTree.ipynb
   python code/ensemble.ipynb
   ```
