# End-to-End Data Processing & Machine Learning Modeling

## 📌 Project Overview

This project demonstrates an end-to-end machine learning workflow covering data preprocessing, exploratory data analysis, feature engineering, model training, hyperparameter tuning, and model evaluation.

Two supervised machine learning problems are explored:

- **Classification:** Adult Income Prediction
- **Regression:** Automobile Price Prediction

The project uses datasets from the UCI Machine Learning Repository and compares multiple machine learning algorithms.

---

## 🎯 Project Objectives

- Explore and understand real-world datasets
- Handle missing values and inconsistent data
- Detect and treat outliers
- Encode categorical features
- Scale numerical features
- Split data into training and testing sets
- Train multiple machine learning models
- Perform hyperparameter tuning
- Evaluate model performance
- Compare different algorithms
- Select the best-performing model for each task

---

# 📊 Part A — Adult Income Classification

## Dataset

The Adult Income dataset contains information about individuals and is used to predict whether their annual income is:

- `<=50K`
- `>50K`

The original dataset contains **48,842 records and 14 features**.

After preprocessing and splitting:

- **Training samples:** 36,177
- **Testing samples:** 9,045
- **Features after encoding:** 96

## Data Preprocessing

The classification pipeline includes:

- Missing value detection
- Handling `?` values
- Removing rows with missing values in important categorical columns
- Median imputation for numerical features
- Mode imputation for categorical features
- Outlier detection using the IQR method
- Outlier capping
- One-hot encoding
- Standardization using `StandardScaler`
- Stratified train-test split

## Models

The following classification algorithms were evaluated:

- Support Vector Classifier (SVC)
- Logistic Regression
- Decision Tree
- Random Forest
- Gradient Boosting
- K-Nearest Neighbors (KNN)
- Gaussian Naive Bayes

## Hyperparameter Tuning

`GridSearchCV` was used to optimize the SVC model.

### Best Parameters

```text
C = 1
kernel = rbf
gamma = scale
```

The best 5-fold cross-validation accuracy was approximately **83.61%**.

## Classification Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| SVC | 83% | 83% | 83% | 83% |
| Logistic Regression | 83% | 82% | 83% | 82% |
| Gradient Boosting | 83% | 83% | 83% | 83% |
| KNN | 82% | 81% | 82% | 81% |
| Random Forest | 82% | 82% | 82% | 82% |
| Decision Tree | 78% | 78% | 78% | 78% |
| Naive Bayes | 58% | 81% | 58% | 60% |

### Classification Conclusion

SVC and Gradient Boosting achieved the strongest overall results, with an accuracy of approximately **83%** and an F1-score of **0.83**.

SVC also achieved a mean 5-fold cross-validation accuracy of approximately **83.61%**, making it a strong candidate for the final classification model.

---

# 🚗 Part B — Automobile Price Regression

## Dataset

The Automobile dataset is used to predict automobile prices based on vehicle characteristics.

After removing records with missing target values:

- **Samples:** 201
- **Input features:** 24

## Data Preprocessing

The regression pipeline includes:

- Missing value analysis
- Median imputation for numerical features
- Mode imputation for categorical features
- Outlier detection using the IQR method
- Outlier capping
- One-hot encoding of categorical variables
- Standardization using `StandardScaler`
- Train-test splitting

## Models

The following regression algorithms were evaluated:

- Linear Regression
- Support Vector Regression (SVR)
- K-Nearest Neighbors Regression

## Regression Results

| Model | R² Score | MSE |
|---|---:|---:|
| **Linear Regression** | **0.82** | **22,328,417.61** |
| KNN Regression | 0.74 | 32,347,029.92 |
| SVR | -0.22 | 149,167,165.11 |

### Regression Conclusion

Linear Regression achieved the best performance with an **R² score of 0.82** and the lowest MSE among the evaluated models.

KNN Regression achieved a lower R² score of **0.74**, while SVR performed poorly with a negative R² score of **-0.22**.

Therefore, **Linear Regression was selected as the best-performing regression model** for this dataset.

---

# 🔄 Machine Learning Workflow

```text
Raw Data
    ↓
Data Exploration
    ↓
Data Cleaning
    ↓
Missing Value Handling
    ↓
Outlier Detection & Treatment
    ↓
Feature Engineering
    ↓
Categorical Encoding
    ↓
Train-Test Split
    ↓
Feature Scaling
    ↓
Model Training
    ↓
Hyperparameter Tuning
    ↓
Model Evaluation
    ↓
Model Comparison
    ↓
Final Model Selection
```

---

# 🛠️ Technologies Used

- **Python**
- **NumPy**
- **Pandas**
- **Matplotlib**
- **Seaborn**
- **Scikit-learn**
- **UCI Machine Learning Repository**
- **Google Colab**

---

# 📈 Evaluation Metrics

### Classification

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### Regression

- Mean Squared Error (MSE)
- R² Score

---

# 📁 Repository Structure

```text
End-to-End-Data-Processing-Machine-Learning-Modeling/
│
├── Machine_Learning_Project.ipynb
├── README.md
└── requirements.txt
```

---

# ▶️ How to Run

The notebook was developed using **Google Colab**.

It can also be opened and executed using **Jupyter Notebook** after installing the required Python dependencies.

---

# 👨‍💻 Author

**Mohamed Ahmed Abdel Motaleb**

Computer Engineering Student
