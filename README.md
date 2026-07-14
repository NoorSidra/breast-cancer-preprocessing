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

## How to Run

### Option A — Google Colab (recommended)
1. Upload `Breast_Cancer_Wisconsin_Preprocessing.ipynb` to Google Colab, or open it directly from this repo via **File → Open notebook → GitHub**.
2. Run all cells (`Runtime → Run all`). The first cell installs `imbalanced-learn`; everything else uses built-in Colab libraries.
3. Output CSVs (`breast_cancer_train_preprocessed.csv`, `breast_cancer_test_preprocessed.csv`) will be saved in the Colab session storage.

### Option B — Local (Jupyter Notebook / VS Code)
```bash
git clone <this-repo-url>
cd <this-repo>
pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn jupyter
jupyter notebook Breast_Cancer_Wisconsin_Preprocessing.ipynb
```

## What the Notebook Does

1. **Data Understanding** — shape, feature names/types, target classes, statistical summary, missing values, duplicate check, class distribution.
2. **Preprocessing:**
   - Missing value check (none found)
   - Duplicate removal
   - Outlier detection & capping (IQR method)
   - Target encoding confirmation (LabelEncoder)
   - Feature scaling (StandardScaler), with justification
   - Class imbalance analysis
   - Class balancing on the training set using **SMOTE-Tomek**
3. **Output** — clean, scaled, balanced train/test CSVs ready for model training.

## Tools & Libraries

Python · Pandas · NumPy · Scikit-learn · Imbalanced-learn (SMOTE-Tomek) · Matplotlib/Seaborn · Jupyter/Google Colab · Git & GitHub

## Report

See [`Breast_Cancer_Wisconsin_Report.pdf`](./Breast_Cancer_Wisconsin_Report.pdf) for the one-page project summary (problem statement, dataset overview, preprocessing steps, and challenges).
