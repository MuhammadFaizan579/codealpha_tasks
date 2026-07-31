# 🚗 Car Price Prediction using Machine Learning

A Machine Learning Regression project that predicts the selling price of a used vehicle based on its specifications using **Python** and **Scikit-learn**.

---

# 📌 Project Overview

The objective of this project is to build a machine learning model capable of estimating the selling price of a used vehicle using historical vehicle information.

The project covers the complete machine learning workflow, including:

* Data Exploration
* Data Cleaning
* Feature Engineering
* One-Hot Encoding
* Train-Test Split
* Model Training
* Prediction
* Model Evaluation
* Data Visualization
* Insight Generation

A **Linear Regression** model was trained to predict vehicle selling prices based on multiple numerical and categorical features.

---

# 📂 Dataset

The dataset contains **301 vehicle records** with the following attributes:

| Feature       | Description                     |
| ------------- | ------------------------------- |
| Car_Name      | Vehicle Name                    |
| Year          | Manufacturing Year              |
| Selling_Price | Selling Price (Target Variable) |
| Present_Price | Current Market Price            |
| Driven_kms    | Total Distance Driven           |
| Fuel_Type     | Petrol / Diesel / CNG           |
| Selling_type  | Dealer / Individual             |
| Transmission  | Manual / Automatic              |
| Owner         | Number of Previous Owners       |

---

# 📊 Dataset Information

* Total Records: **301**
* Total Features: **9**
* Numerical Features: **5**
* Categorical Features: **4**
* Missing Values: **None**

The dataset was clean and required no missing value treatment.

---

# 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook / Google Colab

---

# ⚙️ Machine Learning Workflow

```text
Dataset
      │
      ▼
Data Loading
      │
      ▼
Data Exploration
      │
      ▼
Data Cleaning
      │
      ▼
Feature Engineering
      │
      ▼
One-Hot Encoding
      │
      ▼
Train-Test Split
      │
      ▼
Linear Regression Model
      │
      ▼
Prediction
      │
      ▼
Model Evaluation
      │
      ▼
Visualization
      │
      ▼
Insights & Conclusion
```

---

# 🔍 Data Exploration

The dataset was explored using:

```python
df.head()
df.shape
df.info()
df.describe()
df.isnull().sum()
```

This helped identify:

* Dataset dimensions
* Data types
* Statistical summaries
* Missing values
* Feature distributions

---

# 🧹 Data Preprocessing

The following preprocessing steps were performed:

* Checked missing values
* Removed the `Car_Name` column
* Converted categorical variables into numerical form using **One-Hot Encoding**
* Prepared feature matrix (X)
* Selected target variable (y)

Categorical columns encoded:

* Fuel_Type
* Selling_type
* Transmission

---

# ✂️ Train-Test Split

The dataset was divided into:

* **80% Training Data**
* **20% Testing Data**

using:

```python
train_test_split(test_size=0.2, random_state=42)
```

---

# 🤖 Machine Learning Model

The project uses:

## Linear Regression

Linear Regression was trained to learn the relationship between vehicle features and selling price.

Model Training:

```python
model = LinearRegression()

model.fit(X_train, y_train)
```

Predictions:

```python
y_pred = model.predict(X_test)
```

---

# 📈 Model Evaluation

The model was evaluated using multiple regression metrics.

| Metric   | Score      |
| -------- | ---------- |
| R² Score | **0.8489** |
| MAE      | **1.216**  |
| MSE      | **3.481**  |
| RMSE     | **1.866**  |

The model explains approximately **85% of the variation** in vehicle selling prices.

---

# 📊 Data Visualization

The following visualizations were created:

* Correlation Matrix
* Correlation Heatmap
* Actual vs Predicted Selling Price Scatter Plot

These visualizations helped understand feature relationships and evaluate prediction performance.

---

# 💡 Key Insights

* The dataset contained **301 complete vehicle records** with no missing values.
* Present Price showed the strongest positive correlation (**0.88**) with Selling Price.
* Manufacturing Year had a positive impact on resale value.
* Most vehicles in the dataset were Petrol and Manual transmission.
* One-Hot Encoding successfully transformed categorical variables into numerical format.
* Linear Regression produced reliable predictions with an **R² Score of 0.85**.
* The Actual vs Predicted visualization demonstrated that most predictions were close to the actual selling prices.

---

# 📌 Conclusion

This project successfully demonstrates the complete implementation of a Machine Learning Regression model for vehicle price prediction.

After exploring and preprocessing the dataset, categorical variables were encoded using One-Hot Encoding, and a Linear Regression model was trained using Scikit-learn.

The trained model achieved an **R² Score of approximately 85%**, indicating strong predictive performance. Model evaluation metrics and visualizations confirmed that the regression model is capable of estimating used vehicle prices with reasonable accuracy.

This project highlights a real-world application of Machine Learning in automobile price estimation and demonstrates practical skills in data preprocessing, feature engineering, regression modeling, and performance evaluation.

---

# 📁 Project Structure

```text
Car-Price-Prediction/
│
├── Car Price Prediction.ipynb
├── car data.csv
├── README.md
└── images/
    ├── correlation_heatmap.png
    └── actual_vs_predicted.png
```

---

# 🚀 Future Improvements

Possible improvements include:

* Implement Random Forest Regressor
* Train XGBoost Regressor
* Apply Hyperparameter Tuning
* Perform Cross Validation
* Build a Streamlit Web Application
* Deploy the model for real-time price prediction

---

# 👨‍💻 Author

**Muhammad Faizan**

This project was developed as part of my learning journey in **Data Science, Machine Learning, and Predictive Analytics**.
