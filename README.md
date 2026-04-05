# Customer Churn Prediction Project

This project builds a **customer churn prediction system** using the uploaded `telecom_churn_data.csv` dataset and a **Colab-ready Jupyter notebook**.

## Project Objective

The goal of this project is to predict whether a customer is likely to **churn** (`Yes`) or **not churn** (`No`) using machine learning models. The workflow includes:

* data loading
* data cleaning
* missing-value handling
* duplicate removal
* exploratory data analysis (EDA)
* outlier handling
* encoding and scaling
* class imbalance handling using **SMOTE**
* model training and evaluation
* hyperparameter tuning
* final model comparison

## Files Included

* `customer_churn_prediction_colab.ipynb` - Main Colab notebook for the project
* `telecom_churn_data.csv` - Dataset used for model building
* `README.md` - Project documentation

## Dataset Overview

The dataset contains customer details related to telecom services and churn status.

Important observations from the uploaded dataset:

* **7043 rows**
* **21 columns**
* target column: **Churn**
* identifier column: **customerID**
* some missing values in columns like `gender`, `PaperlessBilling`, `MonthlyCharges`, and `TotalCharges`
* `TotalCharges` needs conversion to numeric format before modeling
* class imbalance exists, so **SMOTE** is used

## Notebook Workflow

### 1. Library Installation

Installs required packages such as:

* `imbalanced-learn`
* `xgboost`

### 2. Import Libraries

Imports all required Python libraries for:

* data analysis
* preprocessing
* visualization
* machine learning
* model evaluation

### 3. Upload and Load Dataset

The dataset is uploaded in Colab and loaded into a pandas DataFrame.

### 4. Data Cleaning

This step includes:

* checking dataset shape
* checking missing values
* removing duplicate rows
* converting `TotalCharges` to numeric
* dropping `customerID`

### 5. Exploratory Data Analysis (EDA)

The notebook analyzes:

* churn distribution
* numerical features vs churn
* categorical trends
* data patterns useful for business understanding

### 6. Outlier Handling

Outliers in important continuous columns are handled using **IQR capping**.

### 7. Feature Engineering and Preprocessing

* target column `Churn` is converted to binary
* numerical columns are imputed and scaled
* categorical columns are imputed and one-hot encoded
* preprocessing is done using `ColumnTransformer`

### 8. Train-Test Split

The dataset is split into training and testing sets using stratification.

### 9. Handle Imbalanced Data

Since churn data is imbalanced, **SMOTE** is applied only on the training pipeline.

### 10. Model Training

The following models are trained:

* Logistic Regression
* KNN
* Decision Tree
* Random Forest
* SVC
* Gradient Boosting
* XGBoost

### 11. Model Evaluation

Each model is evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Classification Report
* Confusion Matrix
* ROC Curve

### 12. Hyperparameter Tuning

`RandomizedSearchCV` is used to tune **Random Forest** and improve performance.

### 13. Model Comparison

The notebook compares:

* best baseline model
* tuned Random Forest model

## Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Imbalanced-learn
* XGBoos

## Business Insights

This project can help telecom companies:

* identify customers likely to churn
* target high-risk customers with retention offers
* improve support for vulnerable customer groups
* reduce revenue loss due to customer churn

## Conclusion

This project provides a complete **machine learning workflow for customer churn prediction** using a telecom dataset.

