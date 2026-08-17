# Project Summary

## Problem
Predict `diagnosed_diabetes` as a binary classification problem.

## Key methodological decisions

- Exclude `diabetes_stage` because of target leakage.
- Remove the 154 rows where `systolic_bp <= diastolic_bp` because the relationship is physiologically invalid.
- Keep preprocessing inside the machine-learning workflow to avoid leakage.
- Use validation/CV for model selection and reserve the final test set for the final unbiased evaluation.
- Evaluate more than accuracy: ROC-AUC, precision, recall, F1, and confusion matrix.
- Analyze false negatives and false positives separately.
- Perform clustering without using the target.
- Use PCA experimentally and keep or reject it based on measured performance.

## Interpretation principle

The model predicts the target; clustering discovers groups based on similarity. The target can be used after clustering to describe the groups, but not to create them.

## Deployment position

The model should be presented as an educational/research prototype, not as a standalone medical diagnostic tool.
