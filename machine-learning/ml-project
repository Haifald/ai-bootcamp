# Diabetes Diagnosis Prediction — Machine Learning Capstone

An end-to-end machine learning project for predicting whether an individual is diagnosed with diabetes using demographic, lifestyle, cardiovascular, and metabolic features.

## Research Question

Can we predict `diagnosed_diabetes` from available demographic, lifestyle, cardiovascular, and metabolic measurements while avoiding data leakage and prioritizing clinically important errors?

## Dataset

The supplied dataset contains **100,000 observations** and a binary target:

- `diagnosed_diabetes = 1` → diagnosed with diabetes
- `diagnosed_diabetes = 0` → not diagnosed

The project deliberately excludes `diabetes_stage` from the predictors because it leaks information about the target.

## Project Workflow

The notebook follows the required machine-learning workflow:

1. Problem and dataset understanding
2. Initial data exploration
3. Data-quality assessment
4. Missing-value and duplicate checks
5. Invalid-value detection
6. Exploratory Data Analysis
7. Target relationships and correlations
8. Train/test split
9. Leakage-safe preprocessing
10. Baseline model
11. Multiple model comparison
12. Cross-validation
13. Overfitting/underfitting analysis
14. Hyperparameter experiments
15. Final model selection
16. Final test evaluation
17. Threshold analysis
18. Error analysis
19. Feature importance
20. Unsupervised learning
21. Cluster profiling
22. PCA / dimensionality reduction analysis
23. Final conclusions and limitations

## Models

The supervised-learning comparison includes:

- Logistic Regression
- K-Nearest Neighbors
- Decision Tree
- Random Forest
- Gradient Boosting

The final model is selected using validation performance, recall/F1, generalization behavior, interpretability, and practical considerations rather than accuracy alone.

## Data Leakage Prevention

The workflow keeps the test set isolated during model development.

Preprocessing is performed through scikit-learn transformers/pipelines so that learned preprocessing parameters are obtained from the training data rather than from the full dataset.

`diabetes_stage` is excluded from `X` because it can reveal the target almost directly.

## Error Analysis

The project explicitly analyzes:

- False Positives
- False Negatives
- Misclassified observations
- Threshold trade-offs

Because missing a true diabetes case can be more costly than sending a non-diabetic case for additional confirmation, recall is treated as an important decision metric.

## Unsupervised Learning

Clustering is performed without using `diagnosed_diabetes` or `diabetes_stage` to construct the clusters.

The analysis investigates hidden patient profiles using clinical and lifestyle measurements, then uses the target only afterward to interpret the discovered groups.

## PCA

PCA is evaluated as a dimensionality-reduction technique.

The project compares the original feature representation with PCA-transformed data and bases the decision on the observed validation performance rather than assuming PCA must improve the model.

## Important Limitations

- The supplied dataset should not automatically be treated as clinical validation data.
- Predictive performance does not prove clinical usefulness.
- The model depends partly on laboratory measurements such as HbA1c and glucose.
- External validation on an independent population is required before any real clinical deployment.
- This project is educational and is not a medical diagnostic system.

## Repository Structure

```text
diabetes-diagnosis-ml/
├── README.md
├── requirements.txt
├── .gitignore
├── notebooks/
│   └── Diabetes_Diagnosis_ML_Capstone.ipynb
├── data/
│   ├── diabetes_dataset.csv
│   └── README.md
├── figures/
│   ├── error_analysis.png
│   └── clustering_pca.png
├── presentation/
│   └── README.md
├── docs/
│   └── PROJECT_SUMMARY.md
└── src/
    └── README.md
```

## How to Run

```bash
pip install -r requirements.txt
```

Then open:

```text
notebooks/Diabetes_Diagnosis_ML_Capstone.ipynb
```

and run the notebook from top to bottom.

## Team Project

This repository was developed as a machine-learning capstone group project. Each team member should be able to explain the complete workflow, model choices, evaluation, error analysis, clustering, and PCA results.
