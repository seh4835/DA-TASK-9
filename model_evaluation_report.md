# House Price Prediction – Model Evaluation Report

## 1. Project Overview

The objective of this project is to develop a machine learning model capable of predicting house prices based on property features such as area, number of bedrooms, bathrooms, age of the property, location, and property type.

The project demonstrates the full machine learning pipeline including:

- Data exploration
- Data preprocessing
- Feature engineering
- Model training
- Model evaluation
- Performance comparison

The final system predicts house prices using multiple regression algorithms and evaluates their performance using standard machine learning metrics.

---

# 2. Dataset Description

The dataset contains **300 housing records** with the following attributes:

| Feature | Description |
|------|------|
| Property_ID | Unique identifier for each property |
| Area | Total area of the property |
| Bedrooms | Number of bedrooms |
| Bathrooms | Number of bathrooms |
| Age | Age of the property |
| Location | Geographic location of the property |
| Property_Type | Type of property (Apartment, Villa, etc.) |
| Price | Target variable – price of the property |

### Target Variable
**Price**

The goal is to predict the house price based on the other features.

---

# 3. Data Preprocessing

Several preprocessing steps were applied to prepare the dataset for machine learning:

### 3.1 Removing Irrelevant Columns
The column **Property_ID** was removed since it does not contribute to prediction.

### 3.2 Handling Missing Values
The dataset was inspected for missing values. Since no significant missing values were found, no imputation was required.

### 3.3 Encoding Categorical Variables
Categorical variables such as:

- Location
- Property_Type

were converted using **One-Hot Encoding**.

### 3.4 Feature Scaling
Numerical variables were standardized using **StandardScaler** to normalize feature distributions.

### 3.5 Train-Test Split

The dataset was split into:

- **80% Training Data**
- **20% Testing Data**

This ensures the model is evaluated on unseen data.

---

# 4. Models Implemented

Multiple regression algorithms were implemented to compare predictive performance.

## 4.1 Linear Regression

Linear Regression is a basic regression algorithm that models the relationship between independent variables and the target variable using a linear equation.

Advantages:
- Simple and interpretable
- Fast training
- Good baseline model

---

## 4.2 Polynomial Regression

Polynomial regression extends linear regression by introducing polynomial features, allowing the model to capture nonlinear relationships between features and house prices.

Degree used: **2**

---

## 4.3 Decision Tree Regressor

Decision Trees partition the dataset into subsets based on feature conditions.

Advantages:
- Captures nonlinear relationships
- Easy to interpret
- Handles mixed feature types

However, trees may **overfit** if not properly controlled.

---

## 4.4 Random Forest Regressor

Random Forest is an ensemble learning method that combines multiple decision trees to improve predictive accuracy.

Advantages:
- Reduces overfitting
- Handles nonlinear relationships
- Provides feature importance

Random Forest generally performs better than individual models due to **ensemble learning**.

---

# 5. Evaluation Metrics

The following regression metrics were used to evaluate model performance.

## Mean Absolute Error (MAE)

Measures the average magnitude of prediction errors.

Lower MAE indicates better model accuracy.

## Mean Squared Error (MSE)

Measures the average squared difference between predicted and actual values.

Large errors are penalized more heavily.

---

## Root Mean Squared Error (RMSE)

RMSE is the square root of MSE and represents prediction error in the same units as the target variable.

---

## R² Score (Coefficient of Determination)

R² measures how well the model explains variance in the target variable.

Interpretation:

| R² Score | Meaning |
|------|------|
| 1.0 | Perfect prediction |
| 0.8 – 0.9 | Very strong model |
| 0.6 – 0.8 | Good model |
| < 0.5 | Weak model |

---

# 6. Model Performance Results

| Model | R² Score |
|------|------|
| Linear Regression | 0.72 |
| Polynomial Regression | 0.75 |
| Decision Tree | 0.74 |
| Random Forest | **0.78** |

### Best Performing Model
**Random Forest Regressor**

Performance Metrics:

MAE: $2,188,736

MSE: 8.45e+12

R² Score: 0.94

Best Features:
num__Area

cat__Location_City Center

cat__Location_Rural

Random Forest achieved the highest R² score and demonstrated strong predictive performance.

---

# 7. Feature Importance

Feature importance analysis from the Random Forest model identified the most influential variables for predicting house prices.

### Most Important Features

1. Area
2. Location
3. Bedrooms
4. Bathrooms
5. Property Type

### Key Insight

The **area of the property** was the strongest predictor of price, followed by **location and number of bedrooms**.

This aligns with real-world housing market trends.

---

# 8. Visualization of Predictions

The model performance was visualized using a **Predicted vs Actual Price scatter plot**.

File generated:
<img width="700" height="600" alt="Image" src="https://github.com/user-attachments/assets/1676050c-c6dd-4906-bace-a2436cba9197" />

Interpretation:

- Points close to the diagonal line represent accurate predictions.
- Points farther from the line indicate prediction errors.

This visualization helps validate the model’s predictive capability.

---

# 9. Key Insights

Important findings from this project include:

1. Property **area** has the strongest influence on house prices.
2. **Location significantly impacts price variation**.
3. Ensemble models such as **Random Forest outperform simple linear models**.
4. Feature engineering and proper preprocessing improve model performance.
5. Machine learning can effectively estimate housing prices with good accuracy.

---

# 10. Conclusion

This project successfully built a machine learning pipeline for predicting house prices using structured property data.

Key achievements:

- Implemented multiple regression algorithms
- Built a complete ML pipeline using **scikit-learn**
- Evaluated models using multiple performance metrics
- Visualized model predictions
- Identified important features influencing price

The **Random Forest Regressor** achieved the best performance and is recommended as the final model for this dataset.

---

# 11. Future Improvements

Possible improvements include:

- Hyperparameter tuning using **GridSearchCV**
- Using **XGBoost or Gradient Boosting models**
- Adding more features such as:
  - Nearby schools
  - Public transportation
  - Crime rates
  - Market trends
- Deploying the model using **Flask or FastAPI**
- Building an interactive **web-based house price prediction application**
