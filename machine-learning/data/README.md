# Dataset

Place the supplied `diabetes_dataset.csv` in this folder.

The notebook expects the following relative path:

```python
pd.read_csv("../data/diabetes_dataset.csv")
```

If the dataset is not included in a public GitHub repository, keep the CSV out of Git and provide the approved dataset source/link in the main README instead.

The target variable is `diagnosed_diabetes`.

`diabetes_stage` is excluded from the model features because it introduces target leakage.
