# 🚗 Toyota Corolla Price Prediction using Multiple Linear Regression

## 📌 Objective

This project aims to build a multiple linear regression model to predict the price of Toyota Corolla cars using various attributes such as age, mileage, horsepower, and more. It includes data preprocessing, exploratory data analysis (EDA), multicollinearity handling, model training, evaluation, and the use of regularization techniques like Lasso and Ridge regression.

---

## 📂 Dataset

**File:** `ToyotaCorolla - MLR.csv`  
This dataset contains detailed information about various Toyota Corolla cars and their features relevant to price prediction.

### 🔑 Columns Description:

| Feature         | Description                                      |
|-----------------|--------------------------------------------------|
| Price           | Target variable (Price in Euros)                |
| Age_08_04       | Age of car in months (as of Aug 2004)           |
| KM              | Accumulated kilometers                          |
| Fuel_Type       | Petrol, Diesel, or CNG                          |
| HP              | Horse Power                                     |
| Automatic       | Transmission type (1 = Auto, 0 = Manual)         |
| cc              | Cylinder volume in cc                           |
| Doors           | Number of doors                                 |
| Cylinders       | Number of cylinders                             |
| Gears           | Number of gears                                 |
| Weight          | Weight in kilograms                             |
| Quarterly_Tax   | Quarterly road tax (not always shown initially) |

---

## 🧰 Tools & Libraries

- **Python** (Jupyter Notebook)
- **pandas**, **numpy** – Data manipulation
- **matplotlib**, **seaborn** – Visualization
- **scikit-learn** – Model building, regularization, scaling
- **statsmodels** – Multicollinearity check (VIF)
- **openpyxl** – Excel file support (if needed)

---

## 🧪 Project Workflow

### 1. 📊 Data Exploration & Preprocessing
- Loaded dataset and performed basic inspection (`info()`, `describe()`)
- One-hot encoded categorical feature: `Fuel_Type`
- Outlier capping using the 1st and 99th percentiles
- Standardized numerical features with `StandardScaler`

### 2. 🔍 Multicollinearity Check
- Calculated Variance Inflation Factor (VIF)
- Dropped features with high multicollinearity (VIF > 10)

### 3. 🤖 Model Building
- **Linear Regression** (baseline model)
- **Polynomial Regression** for capturing non-linearity
- **K-Nearest Neighbors Regressor** (as alternative)
- **Lasso Regression** (L1 regularization for feature selection)
- **Ridge Regression** (L2 regularization for coefficient shrinkage)
- **GridSearchCV** for tuning `alpha` in Lasso & Ridge

### 4. 📈 Model Evaluation
- **Metrics Used:**
  - Mean Squared Error (MSE)
  - R-squared (R²)

---

## 🧠 Interview Questions Included

### 🔹 Normalization vs. Standardization
- **Normalization** (Min-Max Scaling): Scales between [0, 1]
- **Standardization** (Z-score): Centers data to μ=0, σ=1  
- Improves convergence and ensures fair contribution of all features

### 🔹 Techniques to Handle Multicollinearity
- Dropping correlated features
- Principal Component Analysis (PCA)
- Regularization: Lasso & Ridge
- Increasing sample size
- Using domain knowledge

---

## 🚀 How to Run

1. **Clone the repository:**
Bash
   git clone https://github.com/yourusername/toyota-price-mlr.git

2. Install dependencies:

pip install pandas numpy matplotlib seaborn scikit-learn statsmodels openpyxl

3. Run the notebook:

jupyter notebook
Open MLR 2.ipynb and run all cells.

## 📁 Files in this Repository
File	Description
ToyotaCorolla - MLR.csv	Primary dataset for regression
MLR 2.ipynb	Jupyter Notebook with full code workflow
Multiple Linear Regression.docx	Instructions, description, and interview Q&A

## ✨ Future Improvements
Feature engineering based on domain knowledge

Try advanced regression models (e.g., XGBoost, SVR)

Deploy with a Streamlit or Flask interface

## 📬 Contact
For any queries or collaboration, feel free to reach out
