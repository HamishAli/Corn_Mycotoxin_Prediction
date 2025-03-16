# Corn_Mycotoxin_Prediction

# Project Overview
This project aims to predict the concentration of vomitoxin_ppb (a mycotoxin) in corn samples using spectral data. The dataset contains 450+ spectral features, making feature selection, preprocessing, and model optimization crucial to achieve accurate predictions.

Through this project, I implemented multiple machine learning techniques, including:
 Data Cleaning and Outlier Treatment
 Log Transformation for Skewed Data
 Neural Network as a Baseline Model
 Optimized XGBoost Model using Optuna
 Interpretability Analysis using SHAP

 # Dataset Overview
Input Features: 450+ spectral reflectance values.
Target Variable: vomitoxin_ppb (concentration of DON in corn samples).
Sample Size: Approximately 500 rows.

##Workflow and Key Steps

# Step 1: Data Cleaning and Preprocessing
Outlier Removal: IQR method applied to detect and remove extreme values.
Log Transformation: Applied to features with high skewness for improved data distribution.
Feature Scaling: StandardScaler was applied to ensure consistent feature scaling.

# Step 2: Exploratory Data Analysis (EDA)
Histogram Plots: To visualize data distribution and detect skewness.
Boxplots: Used to identify and address outliers.
Correlation Heatmap: Identified feature relationships for improved feature selection.

# Step 3: Model Development
Baseline Model:

Neural Network (3 Hidden Layers) — Performed poorly with:
MAE: 1.2105
RMSE: 1.5128
R² Score: -0.0761
 
# Improved Model:

XGBoost — Improved results even before tuning:
MAE: 0.9429
RMSE: 1.2273
R² Score: 0.2888
 
# Step 4: Hyperparameter Optimization Using Optuna
To improve model performance, I performed hyperparameter tuning for XGBoost. The following parameters were optimized:
 n_estimators: Number of trees
 max_depth: Tree depth for complexity control
 learning_rate: Step size for weight updates
 subsample: Fraction of data samples per tree
 colsample_bytree: Fraction of features sampled for each tree

# Final XGBoost Results:
MAE: 0.8313
RMSE: 1.1047
R² Score: 0.4238
 
# Step 5: Model Interpretability
To ensure transparency in predictions, I implemented:

# SHAP (SHapley Additive exPlanations):

Highlighted top features driving model predictions.
Provided insights into feature interactions.
