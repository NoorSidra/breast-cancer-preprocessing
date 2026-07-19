# Breast Cancer Wisconsin — ML Project

Machine learning classification project on the Breast Cancer Wisconsin (Diagnostic) dataset — predicting malignant vs benign tumors from cell nucleus measurements.

## Project Structure

```
.
├── Breast_Cancer_Wisconsin_Preprocessing.ipynb   # Milestone 1: Dataset selection & preprocessing
├── Breast_Cancer_Wisconsin_Report.pdf            # Milestone 1: One-page project report
├── Feature_Engineering_and_EDA.ipynb             # Milestone 2: Feature engineering & EDA visualizations
├── breast_cancer_train_preprocessed.csv          # Output of Milestone 1: balanced, scaled training set
├── breast_cancer_test_preprocessed.csv           # Output of Milestone 1: scaled test set
├── breast_cancer_feature_engineered.csv          # Output of Milestone 2: engineered feature set
└── README.md
```

## Dataset

- **Name:** Breast Cancer Wisconsin (Diagnostic) Data Set
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/17/breast+cancer+wisconsin+diagnostic) / [Kaggle](https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data)
- Both notebooks load the dataset directly via `sklearn.datasets.load_breast_cancer()`, so **no manual download is required** — they work out of the box in Google Colab.
- 569 samples, 30 numeric features (cell nucleus measurements), binary target (Malignant / Benign).

## How to Run

### Option A — Google Colab (recommended)
1. Open either notebook directly from this repo via **File → Open notebook → GitHub**, or upload it manually to Colab.
2. Run all cells (`Runtime → Run all`).
   - `Breast_Cancer_Wisconsin_Preprocessing.ipynb` installs `imbalanced-learn` in its first cell; everything else uses Colab's built-in libraries.
   - `Feature_Engineering_and_EDA.ipynb` only needs libraries already available in Colab (pandas, numpy, matplotlib, seaborn, scikit-learn).
3. Output CSVs will be saved in the Colab session storage.

### Option B — Local (Jupyter Notebook / VS Code)
```bash
git clone <this-repo-url>
cd <this-repo>
pip install pandas numpy scikit-learn matplotlib seaborn imbalanced-learn jupyter
jupyter notebook
```
Then open either notebook and run all cells.

## Milestone 1 — Dataset Selection & Preprocessing
`Breast_Cancer_Wisconsin_Preprocessing.ipynb`

- Data understanding: shape, feature names/types, target classes, statistical summary, missing values, duplicate check, class distribution
- Missing value & duplicate handling
- Outlier detection & capping (IQR method)
- Target encoding confirmation
- Feature scaling (StandardScaler), with justification
- Class imbalance analysis
- Class balancing on the training set using **SMOTE-Tomek**
- Output: clean, scaled, balanced train/test CSVs

See [`Breast_Cancer_Wisconsin_Report.pdf`](./Breast_Cancer_Wisconsin_Report.pdf) for the one-page summary of this milestone.

## Milestone 2 — Feature Engineering & Exploratory Data Analysis
`Feature_Engineering_and_EDA.ipynb`

**Feature Engineering:**
- New ratio/interaction features (e.g. worst-to-mean size ratios)
- Log transformation of skewed features
- Feature selection: Variance Threshold, Correlation, SelectKBest (ANOVA F-test), Mutual Information
- Removal of highly redundant (correlated) features
- Feature importance analysis via Random Forest

**Exploratory Data Analysis & Visualizations** (each with title, axis labels, and written interpretation):
- Histograms / KDE plots for numerical features
- Count plot for the diagnosis (categorical) variable
- Box plots for outlier analysis
- Correlation heatmap
- Pair plot of top predictive features by diagnosis
- Scatter plot of feature relationships
- Target variable distribution (pie chart)
- Class-wise comparison plots (violin plots)
- Feature importance bar chart

## Tools & Libraries

Python · Pandas · NumPy · Scikit-learn · Imbalanced-learn (SMOTE-Tomek) · Matplotlib · Seaborn · Jupyter/Google Colab · Git & GitHub
