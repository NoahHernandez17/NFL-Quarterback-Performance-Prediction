# NFL Quarterback Performance Prediction

Analyze NFL quarterback statistics collected from ESPN and compare regression models that estimate Total QBR.

## Project Objectives

- Collect and clean quarterback passing statistics
- Explore distributions, outliers, correlations, and player comparisons
- Engineer touchdown and interception percentages
- Train Linear Regression and Ridge Regression models
- Evaluate models with MAE, RMSE, R², and five-fold cross-validation
- Tune Ridge regularization with GridSearchCV and examine residuals

## Models and Results

Results recorded in the notebook on a 20% test split:

| Model | MAE | RMSE | R² |
|---|---:|---:|---:|
| Linear Regression | 6.39 | 8.16 | 0.7801 |
| Ridge Regression | 6.34 | 8.07 | 0.7849 |
| Tuned Ridge Regression | **5.82** | **7.52** | **0.8133** |

GridSearchCV selected **alpha = 10**. The best cross-validation RMSE was **11.24**.

## Tools

Python, pandas, NumPy, Matplotlib, Seaborn, scikit-learn, and Jupyter Notebook.

## Files

- [NFL_2026_Mini_Project.ipynb](NFL_2026_Mini_Project.ipynb) — Complete analysis, visualizations, model training, and saved outputs

## Run the Project

Install the required packages:

```bash
pip install jupyter pandas numpy matplotlib seaborn scikit-learn lxml
```

Open the notebook in Jupyter or VS Code and run the cells in order. Data is collected from ESPN; live statistics and website availability may change, so rerun results can differ from the saved outputs.

## Limitations

The dataset contains 50 quarterbacks, with 10 in the test set. Cross-validation performance was weaker than test performance. Repeated comparisons on the same test set limit confidence in the final estimate. This project estimates existing QBR from passing statistics; it does not forecast future performance.
