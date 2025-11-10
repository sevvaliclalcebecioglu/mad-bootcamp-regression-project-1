# 🏡 Regression Project - King County House Price Prediction
**Project from the "Mastering Applied Data Science Bootcamp"**

This project focuses on predicting **house prices** in King County, Washington, using regression analysis.  
The goal was to build accurate models to predict prices with **R² > 0.80** and **RMSE < $100K**.

---

## 🔹 Project Overview

The workflow of this project includes:

1. **Data Loading & Inspection**
   - Loaded dataset `kc_house_data.csv`  
   - Explored columns such as `bedrooms`, `bathrooms`, `sqft_living`, `price`, `zipcode`, and others  
   - Checked for missing values and general statistics  

2. **Exploratory Data Analysis (EDA)**
   - Visualized distributions and relationships using:
     - Heatmaps for correlations
     - Boxplots for outlier detection
     - Countplots for categorical variables  
   - Removed extreme outliers based on 97th percentile  

3. **Feature Engineering**
   - Converted categorical features (`zipcode`) to numeric using one-hot encoding  
   - Created new features:
     - `age` of the house (`current year - yr_built`)  
     - Binary flag for renovations (`yr_renovated`)  
   - Applied transformations to numerical features to capture non-linear relationships  

4. **Regression Modeling**
   - Split data into training (80%) and testing (20%) sets  
   - Trained multiple regression models:
     - Linear Regression, Ridge, Lasso, ElasticNet  
     - Decision Tree, Extra Trees, XGBoost  
     - Gradient Boosting, AdaBoost, SVR, MLP Regressor  
   - Evaluated models using:
     - R² Score
     - Root Mean Squared Error (RMSE)
     - Mean Absolute Error (MAE)

5. **Model Evaluation**
   - Checked residuals distribution using **Yellowbrick ResidualsPlot** and **Seaborn KDE plots**  
   - Selected the best-performing model based on R² and RMSE  

---

## 🔹 Key Results

- The **XGBRegressor** achieved the best performance  
- **R² Score:** 0.85  
- **RMSE:** $81,881  
- The model successfully predicts house prices with high reliability  

