# Kaggle — Spaceship Titanic

My take on Kaggle's "Spaceship Titanic" binary classification competition.

Best public scores: **0.79003** (CatBoost) · **0.77554** (PyTorch MLP)

## Approach

- Feature engineering: group/family extraction from PassengerId,
  cabin split (deck/num/side), missingness indicators
- Encoding strategy by cardinality (one-hot ≤ 10 categories, ordinal
  otherwise), robust to unseen values at inference
- Model comparison: gradient boosting (CatBoost) vs. a PyTorch MLP
- 5-fold cross-validation with fold ensembling for the MLP

The notebook is narrated step by step (markdown sections) — it was written
as a learning exercise and reads like one.

## Context

Built in 2023-2024 while teaching myself machine learning. Repo kept as-is, no longer maintained —
it documents the learning process more than it showcases production code.
