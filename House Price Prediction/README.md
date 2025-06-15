# 🏠 House Price Prediction

This project focuses on predicting house prices in Bangladesh using various regression models. The dataset includes features such as floor area, number of bedrooms and bathrooms, floor number, and city. The goal is to build a pipeline that preprocesses the data, trains different regression models, evaluates their performance, and identifies the most accurate model.

---

## 📦 Dataset

The dataset contains the following key features:

- **Price_in_taka** *(Target)*: The selling price of the house/apartment in Bangladeshi Taka.
- **Bedrooms**: Number of bedrooms.
- **Bathrooms**: Number of bathrooms.
- **Floor_no**: The floor number of the apartment.
- **Floor_area**: The total floor area in square feet.
- **City**: The city where the property is located (e.g., Dhaka, Chattogram, etc.).

---

## 📊 Exploratory Data Analysis (EDA)

- Removed outliers from the `Price_in_taka` column using the IQR method.
- Verified right-skewed distributions and filtered unrealistic floor areas.
- Ensured clean and balanced numeric and categorical data for modeling.

---

## 🔧 Preprocessing Pipeline

- **Numerical Features**: `Bedrooms`, `Bathrooms`, `Floor_no`, `Floor_area`
  - Missing values imputed using the **mean**.
  - Features scaled using **StandardScaler**.

- **Categorical Features**: `City`
  - Missing values imputed using the **most frequent** value.
  - **OrdinalEncoder** used for encoding cities.

Implemented using `ColumnTransformer` and `Pipeline`.

---

## 🤖 Models Used

The following regression models were trained and evaluated:

- Linear Regression
- Ridge Regression
- Lasso Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- Support Vector Regressor (SVR)
- XGBoost Regressor

---

## 🧪 Model Evaluation

Each model was evaluated using:

- **Mean Absolute Error (MAE)**
- **R² Score**

Example of performance summary:

| Model                   | MAE         | R² Score   |
|------------------------|-------------|------------|
| Linear Regression       | 2.12M       | 0.41       |
| Ridge Regression        | 2.12M       | 0.41       |
| Lasso Regression        | 2.12M       | 0.41       |
| Random Forest           | **1.14M**   | **0.73**   |
| Gradient Boosting       | 1.35M       | 0.70       |
| Support Vector Regressor| 2.70M       | -0.05      |
| XGBoost                 | 1.21M       | 0.70       |

---

## ✅ Best Performing Model

- **Random Forest Regressor** achieved the lowest MAE and highest R² Score.
- Future tuning can be done using **GridSearchCV** with both `neg_mean_absolute_error` and `r2` scoring for further optimization.

---

## 📌 Future Improvements

- Add cross-validation and grid search to fine-tune hyperparameters.
- Try advanced encoding (e.g., OneHot or Target Encoding for `City`).
- Include additional features like location coordinates, property type, etc.
- Deploy as a web app using Flask or Streamlit.

---
## Dataset- https://www.kaggle.com/datasets/durjoychandrapaul/house-price-bangladesh
## 🛠️ Requirements

```bash
pip install pandas numpy scikit-learn matplotlib seaborn xgboost

