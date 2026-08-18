# Diabetes Model Evaluation

A focused binary-classification project exploring how different evaluation metrics can lead to different conclusions about model performance.

This analysis extends the core classification workflow with additional evaluation experiments, with particular attention to **ROC curves and ROC-AUC** as threshold-independent measures of class separation.

## Objective

Use a small clinical dataset to compare classification models and understand model performance beyond accuracy alone.

## What I Explored

- Binary target construction
- Train/test splitting and leakage-safe preprocessing
- Logistic Regression and non-linear classifiers
- Accuracy, Precision, Recall, and F1
- Confusion Matrix
- Predicted probabilities
- ROC curves and ROC-AUC
- Model comparison across complementary evaluation metrics

## Why ROC-AUC?

Precision, Recall, and F1 describe model behavior at a selected decision threshold. ROC-AUC provides another perspective by evaluating how well a model separates positive and negative cases across thresholds.

Adding this analysis helped connect predicted probabilities, decision thresholds, and classification metrics rather than evaluating a classifier using accuracy alone.

## Repository Structure

```text
diabetes-model-evaluation/
├── README.md
├── data/
│   └── diabetes.csv
└── notebooks/
    └── diabetes-model-evaluation.ipynb
```

## Run

Open `notebooks/diabetes-model-evaluation.ipynb` and run the cells from top to bottom.
