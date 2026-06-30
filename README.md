# Task 2: Exploratory Data Analysis (EDA) — Titanic Dataset

**AI & ML Internship — Elevate Labs**

## Objective
Understand the Titanic dataset using descriptive statistics and visualizations, and draw feature-level inferences about what influenced passenger survival.

## Tools Used
- Pandas — data loading, cleaning, summary statistics
- NumPy — numeric operations
- Matplotlib & Seaborn — static visualizations (histograms, boxplots, heatmaps, pairplots)

## Files in this Repository
| File | Description |
|---|---|
| `task2_EDA.ipynb` | Full EDA notebook with code, plots, and written observations |
| `Titanic-Dataset.csv` | Dataset used for analysis (standard Titanic passenger data, 891 rows) |
| `README.md` | This file |

## What Was Done
1. Loaded the dataset and inspected its structure (`shape`, `dtypes`, missing values).
2. Generated summary statistics (mean, median, std, quartiles) for all numeric and categorical columns.
3. Visualized distributions of `Age`, `Fare`, `SibSp`, and `Parch` using histograms with KDE overlays.
4. Used boxplots to detect outliers in `Age` and `Fare`, including a class-wise breakdown.
5. Built a correlation matrix and pairplot to study relationships between numeric features and `Survived`.
6. Compared survival rate across `Sex`, `Pclass`, and `Embarked` using bar charts.
7. Compared age distributions of survivors vs. non-survivors with KDE plots.
8. Summarized key feature-level inferences and a missing-data handling strategy.

## Key Findings
- **Sex** is the strongest single predictor of survival — female passengers survived at a much higher rate than male passengers.
- **Passenger class** matters: survival rate drops steadily from 1st → 2nd → 3rd class.
- **Fare** correlates positively with survival, largely because it's tied to class (`Pclass` and `Fare` are correlated at ≈ -0.66).
- **Fare, SibSp, and Parch** are right-skewed and would benefit from transformation before modeling.
- **Cabin** is ~77% missing and needs special handling (e.g., a "has_cabin" flag) rather than direct imputation.
- No problematic multicollinearity exists between independent predictors.

## How to Run
```bash
pip install pandas numpy matplotlib seaborn
jupyter notebook task2_EDA.ipynb
```

## Interview Questions Covered
The notebook's final section answers all 8 interview questions from the task brief: purpose of EDA, boxplots, correlation, skewness detection, multicollinearity, EDA tools, a real example of EDA catching a problem, and the role of visualization in ML.

---
*Submitted as part of the AI & ML Internship program (Elevate Labs).*
