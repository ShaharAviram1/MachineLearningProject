# 🏠 California Housing Price Prediction

## 📌 Project Overview
This project is part of a supervised learning assignment.  
The goal was to predict **median house values** in California using socioeconomic and geographic features.

We applied the full machine learning flow:
1. Data exploration (EDA)
2. Feature engineering
3. Experiments with cross-validation
4. Final training
5. Evaluation on unseen test data

---

## 📊 Dataset
- **Source:** California Housing dataset.  
- **Target variable:** `MedHouseVal` (median house value in $100,000 units).  
- **Cap:** Values are capped at **5.0 (= $500,000)**, so very expensive homes are not represented fully.  
- **Split:** Dataset was provided in two parts:
  - `housing_train.csv` (for training + cross-validation)
  - `housing_test.csv` (for final evaluation)

---

## 🔎 Exploratory Data Analysis (EDA)
Key findings:
- No missing values or duplicate rows.
- **Median income** is the strongest predictor of house prices.
- Location (latitude/longitude) shows clear geographic patterns: coastal areas are more expensive.

Example visualizations:
- Histogram of target variable (house values)
- Scatterplot: Income vs House Value
- Geographic scatterplot: Latitude/Longitude vs House Value
- Feature importances
- Predicted vs True values on test set

---

## ⚙️ Experiments
- **Model:** RandomForestRegressor  
- **Feature engineering variations:** Scaled vs No-Scale  
- **Hyperparameters tuned:**
  - `n_estimators`: {100, 300}
  - `max_depth`: {None, 12}  
- **Validation:** 5-fold cross-validation (R² metric)
  
---

## ✅ Conclusions
- Median income and location are the most important predictors of house prices.  
- RandomForest handled the data well, with scaling providing a small improvement.  
- Fully grown trees (unlimited depth) generalized better than shallow ones — likely due to the dataset size and complexity.  
- The dataset’s $500k cap limits accuracy for high-value homes.  

---
