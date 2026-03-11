# DA TASK 9
# 🏠 House Price Prediction using Machine Learning

A machine learning project that predicts house prices based on property features such as area, number of bedrooms, location, property type, and age of the property.

This project demonstrates a **complete end-to-end machine learning workflow**, including data exploration, preprocessing, model training, evaluation, and visualization.

---

# 📌 Project Overview

Real estate price prediction is a common regression problem in data science. The goal of this project is to build a predictive model that estimates housing prices based on property characteristics.

The project implements multiple regression algorithms and compares their performance to determine the most accurate model.

The final model uses **Random Forest Regression**, which achieved the best performance among all tested models.

---

# ⚙️ Technologies Used

The project is implemented using the following tools and libraries:

- **Python**
- **Pandas** – data manipulation
- **NumPy** – numerical computations
- **Matplotlib** – visualization
- **Seaborn** – data visualization
- **Scikit-learn** – machine learning models
- **Jupyter Notebook** – development environment

---

# 📊 Dataset Description

The dataset contains **300 property records** with the following features:

| Feature | Description |
|------|------|
| Property_ID | Unique identifier for each property |
| Area | Total property area |
| Bedrooms | Number of bedrooms |
| Bathrooms | Number of bathrooms |
| Age | Age of the property |
| Location | Property location |
| Property_Type | Type of property |
| Price | Target variable (house price) |

The objective is to **predict the price of a house** based on these attributes.

---

# 🔎 Machine Learning Workflow

The project follows a structured machine learning pipeline.

### 1️⃣ Data Exploration
- Load dataset
- Inspect data types
- Identify missing values
- Visualize relationships between features

### 2️⃣ Data Preprocessing
- Remove irrelevant columns
- Encode categorical variables
- Standardize numerical features
- Split dataset into training and testing sets

### 3️⃣ Model Training
The following regression models were implemented:

- Linear Regression
- Polynomial Regression
- Decision Tree Regressor
- Random Forest Regressor

### 4️⃣ Model Evaluation

The models were evaluated using multiple regression metrics:

- **MAE (Mean Absolute Error)**
- **MSE (Mean Squared Error)**
- **RMSE (Root Mean Squared Error)**
- **R² Score**

---

# 📈 Model Performance

Best performing model:
Random Forest Regressor

Performance metrics:
MAE: $2,188,736
MSE: 8.45e+12
R² Score: 0.94

Important features influencing house price:
num__Area
cat__Location_City Center
cat__Location_Rural

# 📊 Visualization

The model predictions were visualized using a **Predicted vs Actual Prices plot**.

This plot helps assess how closely the model predictions match real values.

Output file:
predictions_vs_actual.png

Points near the diagonal line represent accurate predictions.

---

# 📂 Project Structure


house-price-prediction
│
├── house_price_prediction.ipynb
├── house_data.csv
├── predictions_vs_actual.png
├── requirements.txt
├── model_evaluation_report.md
└── README.md

# 🚀 How to Run the Project

### 1️⃣ Clone the repository

git clone https://github.com/your-username/house-price-prediction.git

### 2️⃣ Navigate to the project folder
cd house-price-prediction

### 3️⃣ Install dependencies
pip install -r requirements.txt

### 4️⃣ Run the notebook
jupyter notebook

Open:

house_price_prediction.ipynb

Run the cells sequentially to train and evaluate the model.

# 📚 Key Learnings

This project demonstrates:

Building regression models using scikit-learn

Creating preprocessing pipelines

Handling categorical and numerical features

Evaluating models using multiple metrics

Visualizing predictions vs actual results

Comparing machine learning algorithms

# 🔮 Future Improvements

Potential improvements include:

Hyperparameter tuning using GridSearchCV

Using advanced models like XGBoost or Gradient Boosting

Adding more housing market features

Deploying the model as a web application using Flask or FastAPI

Creating an interactive house price prediction dashboard