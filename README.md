
# Bengaluru House Price Prediction – Data Analysis & ML Model

## 📌 Overview

This project predicts house prices in Bengaluru using a real estate dataset.
It focuses on data cleaning, exploratory analysis, feature engineering, and regression model building to estimate property prices accurately.

---

## 📂 Dataset Information

* Dataset: Bengaluru House Price CSV
* Original dataset size: ~13,320 rows
* Final cleaned dataset size: ~7,251 rows
* Target variable: **price** (in Lakhs ₹)

### Main features used:

* total_sqft
* bath
* bhk
* location (one-hot encoded)

---

## 🧹 Data Cleaning & Preprocessing

The following steps were performed:

* Removed irrelevant columns (area_type, availability, society, balcony)
* Handled missing values in key fields
* Converted total_sqft ranges into numeric values
* Extracted BHK values from size
* Created price_per_sqft
* Grouped rare locations into “other”
* Removed duplicates
* Removed outliers based on:

  * price per sqft distributions
  * sqft per BHK threshold
  * bathroom > bhk + 2
* Applied one-hot encoding on location
* Train–test split: 80% train / 20% test

---

## 📊 Exploratory Data Analysis

Visualizations include:

* price distribution
* BHK and bathroom counts
* sqft vs price scatter plots
* correlation heatmap

Key insights:

* total_sqft shows strong positive correlation with price (~0.84)
* majority homes are 2BHK or 3BHK
* outlier removal improved consistency between sizes and prices

---

## 🤖 Machine Learning Models

Two regression models were trained and compared:

| Model             | R² Score |
| ----------------- | -------- |
| Linear Regression | ~0.847   |
| Decision Tree     | ~0.649   |

Linear Regression performed the best and was chosen as the final model.

---

## 🚀 Final Output

The model predicts house price based on:

* location
* total_sqft
* number of bathrooms
* number of bedrooms

Model performance demonstrates strong predictive capability.




