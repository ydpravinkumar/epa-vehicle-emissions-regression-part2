# 📊 EPA Vehicle Emissions Regression Analysis – Part 2

## 📌 Project Overview

This project builds upon exploratory analysis (Part 1) to apply a diverse range of **machine learning regression algorithms** on EPA vehicle testing data. The objective is to accurately **predict two continuous target variables**—mileage per gallon (`RND_ADJ_FE`) and **carbon monoxide (CO) emissions**—using a variety of model architectures. Performance is benchmarked across six algorithms using standard regression metrics and feature importance analysis.

## 📂 Contents

* Jupyter Notebook: `EPA_Regression_Modeling.ipynb`
* Model Performance Report: `model_results_summary.csv`
* Feature Importance Charts: `/visualizations/feature_importance/`
* Final Models (Pickle/Joblib): `/models/`
* Summary Report: `regression_summary.md` (this file)

## 📈 Data Source

The data is sourced from the **U.S. Environmental Protection Agency (EPA)**, including:

* Vehicle engine and emissions test results
* Year-wise datasets (2015–2024)
* Processed dataset from Part 1 used as input

## 📁 Folder Structure

```
/epa-vehicle-regression/
│
├── data/
│   └── 
│
├── EPA_Vehicle_Emissions_EDA_Part2.ipynb
├── regression_summary.md
└── README.md
```

## 🎯 Objectives

* Predict **RND\_ADJ\_FE (adjusted fuel economy)** and **CO emissions** using ML algorithms.
* Compare **six different regression models** and assess their performance.
* Identify and interpret **top features** influencing predictions.

## 🛠️ Tasks

### Step 1: Data Preprocessing

* Handle missing values and apply multiple imputations.
* Standardize column names and continuous variables.
* Remove outliers based on statistical thresholds.
* Split data into training and testing subsets for both targets.

### Step 2: Model Building

Train the following **six algorithms** for both `RND_ADJ_FE` and `CO emissions`:

1. **Multiple Linear Regression (MLR)**
2. **K-Nearest Neighbors (KNN)**
3. **Random Forest Regressor**
4. **Gradient Boosted Trees**
5. **XGBoost Regressor**
6. **CatBoost Regressor**

> 🔁 Total Models: 12 (6 algorithms × 2 target variables)

### Step 3: Model Evaluation

Each model is evaluated using:

* **R-squared** (explained variance)
* **Mean Absolute Error (MAE)**
* **Root Mean Squared Error (RMSE)**

### Step 4: Feature Importance

For models supporting interpretability (RF, GBT, XGBoost, CatBoost):

* Extract top 10 features based on importance scores.
* Visualize and compare feature influence across models.

### Step 5: Results Comparison

* Compare all models side-by-side based on metrics.
* Discuss trends in feature importance.
* Identify best-performing models for each target.
* Analyze model behavior and assumptions.

## 🧠 Key Learnings

* Ensemble models (like **XGBoost** and **CatBoost**) typically outperformed simpler models for both targets.
* Certain engine parameters and emission coefficients consistently appeared as **top predictors**.
* Algorithms differ significantly in **feature weighting and sensitivity**.

## ⚠️ Limitations

* Some features had to be imputed, potentially introducing bias.
* Models were trained on historical EPA test data only; real-world generalization may vary.
* KNN performance can degrade with high dimensionality and uneven feature scaling.

## 📄 License

This project is licensed under the **MIT License**. The EPA data used is public and covered under the **Open Government License**.

