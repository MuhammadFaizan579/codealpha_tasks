# Iris Flower Classification using Machine Learning

A machine learning classification project that predicts the species of Iris flowers based on their physical measurements using Python and Scikit-learn.

## Project Overview

This project implements a complete machine learning workflow to classify Iris flowers into three different species:

* Iris-setosa
* Iris-versicolor
* Iris-virginica

The classification is performed using four flower measurements:

* Sepal Length
* Sepal Width
* Petal Length
* Petal Width

Two machine learning algorithms were trained and compared:

1. Logistic Regression
2. K-Nearest Neighbors (KNN)

---

## Dataset

The dataset contains **150 Iris flower samples** and includes the following features:

| Feature       | Description                        |
| ------------- | ---------------------------------- |
| SepalLengthCm | Length of the sepal in centimeters |
| SepalWidthCm  | Width of the sepal in centimeters  |
| PetalLengthCm | Length of the petal in centimeters |
| PetalWidthCm  | Width of the petal in centimeters  |
| Species       | Target flower species              |

The dataset contains:

* 150 total samples
* 4 input features
* 3 target classes
* 50 samples per species
* No missing values

The `Id` column was removed because it only represented the record identifier and did not provide meaningful information for classification.

---

## Technologies and Libraries Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook / Google Colab

---

## Machine Learning Workflow

The project follows a complete machine learning pipeline:

```text
Dataset
    ↓
Data Loading
    ↓
Data Exploration
    ↓
Data Cleaning
    ↓
Feature Selection
    ↓
Train-Test Split
    ↓
Model Training
    ↓
Prediction
    ↓
Model Evaluation
    ↓
Visualization
    ↓
Model Comparison
```

---

## Data Exploration and Preprocessing

The dataset was explored using:

* `df.head()`
* `df.shape`
* `df.info()`
* `df.isnull().sum()`
* `value_counts()`
* `unique()`

The dataset was checked for missing values and data quality issues. Since no missing values were found, no missing-value treatment was required.

The `Id` column was removed because it was not a meaningful predictive feature.

The dataset was then divided into:

* **Features (X):** Flower measurements
* **Target (y):** Flower species

---

## Train-Test Split

The dataset was divided using an 80/20 split:

* 80% Training Data: 120 samples
* 20% Testing Data: 30 samples

The `stratify=y` parameter was used to maintain a balanced distribution of all three flower species in the training and testing sets.

---

## Models Implemented

### 1. Logistic Regression

Logistic Regression was used as a classification algorithm to predict the species of an Iris flower based on its measurements.

**Accuracy: 96.67%**

The model correctly classified 29 out of 30 test samples.

---

### 2. K-Nearest Neighbors (KNN)

KNN classifies a new data point based on the classes of its nearest neighboring data points.

The model was implemented using:

```python
KNeighborsClassifier(n_neighbors=5)
```

**Accuracy: 100%**

The model correctly classified all 30 test samples in the selected test set.

---

## Model Performance Comparison

| Model               | Accuracy |
| ------------------- | -------: |
| Logistic Regression |   96.67% |
| K-Nearest Neighbors |     100% |

Based on the selected train-test split, KNN achieved the highest accuracy.

> Note: Model performance may vary depending on the train-test split and dataset characteristics.

---

## Model Evaluation

The models were evaluated using:

* Accuracy Score
* Classification Report
* Confusion Matrix
* Confusion Matrix Heatmap

The classification report included:

* Precision
* Recall
* F1-Score
* Support

The confusion matrix helped identify the correct and incorrect predictions for each Iris species.

---

## Feature Visualization

Feature relationships were explored using:

### Pairplot

A pairplot was used to visualize relationships between different flower measurements and identify patterns among the three species.

### Boxplots

Boxplots were used to compare feature distributions across different Iris species.

The visualizations showed that:

* Iris-setosa was relatively easy to distinguish.
* Iris-versicolor and Iris-virginica showed some overlapping characteristics.
* Petal Length and Petal Width were particularly useful features for separating the species.

---

## Key Insights

* The dataset was balanced, with 50 samples for each species.
* No missing values were found in the dataset.
* Petal measurements were highly useful for distinguishing different Iris species.
* Iris-setosa was relatively easy to classify due to its distinct measurements.
* Some overlap existed between Iris-versicolor and Iris-virginica.
* Logistic Regression achieved 96.67% accuracy.
* KNN achieved 100% accuracy on the selected test set.
* Comparing multiple machine learning algorithms helped identify the better-performing model for this dataset.

---

## Conclusion

This project demonstrates a complete machine learning classification workflow using Python and Scikit-learn.

The project covered:

* Dataset loading
* Data exploration
* Data preprocessing
* Feature selection
* Train-test splitting
* Model training
* Predictions
* Model evaluation
* Data visualization
* Algorithm comparison

Two classification algorithms were implemented: Logistic Regression and K-Nearest Neighbors. Based on the selected train-test split, KNN achieved better performance with an accuracy of 100%, while Logistic Regression achieved 96.67%.

This project provided practical experience in solving a real classification problem and understanding the complete machine learning pipeline from raw data to model evaluation.

---

## Project Structure

```text
Iris-Flower-Classification/
│
├── Iris Flower Classification.ipynb
├── Iris.csv
└── README.md
```

---

## Future Improvements

Possible future improvements include:

* Testing additional classification algorithms such as Decision Tree and Random Forest
* Performing cross-validation
* Applying hyperparameter tuning
* Creating an interactive prediction interface
* Deploying the model as a web application using Streamlit or Flask

---

## Author

**Muhammad Faizan**

This project was developed as part of my learning journey in **Data Science and Machine Learning**.
