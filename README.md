# finrisk-analytics

Machine learning project on financial data: predict loan default, estimate bank balance and segment customers.

## Objective
Using a customer's financial profile (employment status, bank balance, annual salary), the project answers three questions:
1. **Classification**: will the customer default?
2. **Regression**: what is the customer's bank balance?
3. **Clustering**: which customer segment does the customer belong to?

## Data
- **Dataset:** `Default_Fin.csv` from Kaggle: [PUT THE KAGGLE LINK HERE]
- Synthetic data generated from real anonymized financial data
- 10,000 rows, columns: `Employed`, `Bank Balance`, `Annual Salary`, `Defaulted?`
- The dataset is **imbalanced**: 333 defaults (3.3%) vs 9,667 non-defaults
- The CSV file is not included in this repository. Download it from Kaggle and place it next to the notebook.

## Method
1. Exploratory data analysis
2. Stratified 80/20 train/test split
3. Scaling (StandardScaler) fitted on the training set only
4. SMOTE applied on the training set only, to handle class imbalance
5. Model comparison with metrics suited to imbalanced data

## Results

### Classification
Models compared: Logistic Regression, Random Forest, SVM, XGBoost.

| Model | AUC | Precision | Recall | F1 |
|---|---|---|---|---|
| Logistic Regression | 0.95 | [ ] | [ ] | [ ] |
| Random Forest | 0.92 | [ ] | [ ] | [ ] |
| SVM | 0.92 | [ ] | [ ] | [ ] |
| XGBoost | 0.92 | [ ] | [ ] | [ ] |

Logistic Regression gave the best AUC. On this small synthetic dataset, a simple linear model is enough.

### Regression
Target: `Bank Balance`. Models: Linear Regression, Ridge, Lasso, Random Forest, XGBoost.
Best model: [NAME], MAE = [ ], R² = [ ].

### Clustering
KMeans with [K] clusters, chosen with the elbow method and silhouette score ([ ]).
- Cluster 0: [describe]
- Cluster 1: [describe]
- Cluster 2: [describe]

## Limitations
- Synthetic dataset with only 3 explanatory variables
- Very few defaults in the test set (about 67), so differences between models should be read with caution
- Regression on `Bank Balance` is mainly an exercise on the ML pipeline
- Not intended for real credit decisions

## How to run
```bash
git clone https://github.com/ghofranebenhaj/finrisk-analytics.git
cd finrisk-analytics
pip install -r requirements.txt
```
Then open the notebook in Jupyter or Google Colab and run all cells.

## Tech stack
Python, pandas, scikit-learn, XGBoost, imbalanced-learn, matplotlib, seaborn.

## Author
Ghofrane Toukebri, Software & Data Engineering student at ESPRIT.
