# 🏡 House Price Prediction – Ames Housing Dataset  

## 📌 Overview  
This project predicts house prices using the **Ames Housing dataset** (79 features, ~2,900 records).  
I explored data cleaning, feature engineering, visualization, and applied multiple machine learning models to understand what drives house prices.  

The project demonstrates an **end-to-end Data Science workflow**: from raw data to insights and predictive modeling.  

---

## 🎯 Objectives  
- Clean and preprocess the dataset (handle nulls, outliers, categorical encoding).  
- Perform **exploratory data analysis (EDA)** to identify key factors affecting SalePrice.  
- Build regression models to predict **log-transformed SalePrice**.  
- Compare Linear Regression with Ridge, Lasso, Random Forest, and Gradient Boosting.  
- Evaluate performance using **R², RMSE, and cross-validation**.  

---

## 🛠 Tools & Libraries  
- **Python** (pandas, numpy, matplotlib, seaborn, scikit-learn)  
- **Machine Learning Models:** Linear Regression, Ridge, Lasso, RandomForest, Gradient Boosting  
- **Visualization:** Matplotlib, Seaborn  
- **Other:** Cross-validation, GridSearchCV for hyperparameter tuning  

---

## 📊 Workflow  

### 1. Data Preprocessing  
- Dropped high-null columns (`PoolQC`, `MiscFeature`, `Alley`, `Fence`).  
- Imputed missing values (mean for numeric, mode for categorical).  
- Removed outliers (`GrLivArea > 4000` with low SalePrice).  
- Applied **log transformation** to SalePrice and skewed features.  
- One-hot encoded categorical variables.  

### 2. Exploratory Data Analysis (EDA)  
- Correlation heatmaps → **OverallQual, GrLivArea, GarageCars, TotalBsmtSF** were top predictors.  
- Scatter plots & boxplots to visualize relationships.  
- Identified redundancy between features (e.g., `GarageCars` vs `GarageArea`).  

### 3. Modeling  
- **Baseline Linear Regression:** R² = 0.90, RMSE ≈ 0.127  
- **Ridge Regression:** R² = 0.917, RMSE ≈ 0.115 (Best performance)  
- **Lasso Regression:** R² = 0.913, RMSE ≈ 0.118  
- **Gradient Boosting:** R² = 0.903, RMSE ≈ 0.124  
- **RandomForest:** R² = 0.876, RMSE ≈ 0.140  

### 4. Evaluation  
- Used **cross-validation (5-fold)** to confirm robustness.  
- Visualized **Predicted vs Actual** and **residual plots** for diagnostics.  

---

## 📈 Results  
- **Ridge Regression** provided the best balance between accuracy and stability.  
- Cross-validation confirmed Ridge (R² ≈ 0.92, RMSE ≈ 11.5%) was the most reliable model.  
- Top predictors: **OverallQual, GrLivArea, GarageCars, YearBuilt, TotalBsmtSF**.  

---

## 🚀 Key Learnings  
- Feature engineering (log transforms, encoding) can significantly improve model accuracy.  
- Regularization (Ridge/Lasso) helps combat multicollinearity in high-dimensional datasets.  
- Even simple models can outperform complex ones if the data is well-prepared.  


