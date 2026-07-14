# Breast Cancer Wisconsin — Data Preprocessing & Class Balancing

**Milestone 1:** Dataset Selection & Data Preprocessing

## Project Structure

```
.
├── Breast_Cancer_Wisconsin_Preprocessing.ipynb   # Main preprocessing notebook (Colab-ready)
├── Breast_Cancer_Wisconsin_Report.pdf            # One-page project report
├── breast_cancer_train_preprocessed.csv          # Output: balanced, scaled training set
├── breast_cancer_test_preprocessed.csv           # Output: scaled test set
└── README.md
```
## Dataset

- **Name:** Breast Cancer Wisconsin (Diagnostic) Data Set
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic) / [Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)
- The notebook loads the dataset directly via `sklearn.datasets.load_breast_cancer()`, so **no manual download is required** — it works out of the box in Google Colab.
- 569 samples, 30 numeric features (cell nucleus measurements), binary target (Malignant / Benign).

er_Wisconsin_Report.pdf`](./Breast_Cancer_Wisconsin_Report.pdf) for the one-page project summary (problem statement, dataset overview, preprocessing steps, and challenges).


LINK:https://www.kaggle.com/code/mragpavank/breast-cancer-wisconsin
