# Subscription Conversion Prediction using Machine Learning

## 📌 Project Overview

This project uses **Machine Learning** to predict whether a free user is likely to convert into a **paid subscriber** based on their engagement and usage behavior.

The project is designed as an **end-to-end supervised binary classification pipeline**, starting from data cleaning and exploratory analysis to model training, evaluation, interpretation, and conversion probability reporting.

---

## 🎯 Business Problem

A subscription-based application may have a large number of free users, but only some of them convert into paid subscribers.

The objective of this project is to identify users who are more likely to convert so that businesses can:

* Identify high-potential users
* Prioritize conversion campaigns
* Personalize offers and communication
* Improve marketing efficiency
* Understand engagement signals related to conversion

---

## 🤖 Machine Learning Problem

This is a **Supervised Binary Classification** problem.

### Target Variable

`Converted`

* `1` → User became a paid subscriber
* `0` → User did not become a paid subscriber

---

## 📊 Dataset Features

The model uses user engagement and demographic information, including:

* Age
* Days Since Signup
* Sessions
* Visits
* Features Used
* Average Session Minutes
* Trial Days Used
* Support Interactions
* Sessions Per Day
* Visits Per Day

`User_ID` is treated as an identifier and is not used as a predictive feature.

---

## 🔄 Project Workflow

```text
Data Collection
      ↓
Data Understanding
      ↓
Data Cleaning
      ↓
Outlier Detection & Treatment
      ↓
Exploratory Data Analysis
      ↓
Feature Engineering
      ↓
Feature Selection
      ↓
Train-Test Split
      ↓
Feature Standardisation
      ↓
Model Building
      ↓
Model Training
      ↓
Prediction
      ↓
Model Evaluation
      ↓
Best Model Selection
      ↓
Model Interpretation
      ↓
Prediction & Reporting
```

---

## 🧹 Data Preprocessing

The dataset is prepared using the following steps:

* Duplicate records are removed.
* Missing numerical values are filled using the **median**.
* Outliers are detected using the **IQR method**.
* Instead of removing observations, outliers are capped using winsorization.
* Numerical features are standardised using `StandardScaler`.
* The target variable is encoded using `LabelEncoder`.

---

## 🔧 Feature Engineering

Two additional engagement-rate features are created:

### Sessions Per Day

```text
Sessions_Per_Day = Sessions / Days_Since_Signup
```

### Visits Per Day

```text
Visits_Per_Day = Visits / Days_Since_Signup
```

These features help represent how frequently users engage with the application.

---

## 🧠 Machine Learning Models

Three classification algorithms are trained and compared:

1. **Logistic Regression**
2. **Decision Tree**
3. **Random Forest**

The models are evaluated on the test dataset.

---

## 📈 Model Evaluation

The project evaluates the models using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC
* Confusion Matrix
* Classification Report

The **F1 Score** is used as the primary metric for selecting the best-performing model in the notebook.

---

## 🔍 Model Interpretation

The selected model is interpreted using feature importance or model coefficients.

A confusion matrix is also used to understand:

* Correctly predicted conversions
* Correctly predicted non-conversions
* False positives
* False negatives

---

## 💡 Business Reporting

The final model generates:

* Actual conversion status
* Predicted conversion status
* Conversion probability
* User potential segment

Users are segmented based on predicted conversion probability into:

| Conversion Probability | Segment          |
| ---------------------- | ---------------- |
| 0–33%                  | Low Potential    |
| 33–66%                 | Medium Potential |
| 66–100%                | High Potential   |

---

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Google Colab
* Jupyter Notebook

---

## 📁 Repository Structure

```text
subscription-conversion-prediction-ml/
│
├── Subscription_Conversion_Prediction_ML_Project_Final.ipynb
├── subscription_conversion_100_users_dirty.csv
└── README.md
```

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/subscription-conversion-prediction-ml.git
```

### 2. Open the notebook

Open:

```text
Subscription_Conversion_Prediction_ML_Project_Final.ipynb
```

using **Google Colab** or **Jupyter Notebook**.

### 3. Upload the dataset

Upload:

```text
subscription_conversion_100_users_dirty.csv
```

when prompted by the notebook.

### 4. Run all cells

Execute the notebook from beginning to end to perform preprocessing, EDA, model training, evaluation, and prediction.

---

## 📌 Key Outcome

The project demonstrates how user engagement data can be transformed into actionable machine learning predictions for **subscription conversion**.

The final pipeline provides both **model performance metrics** and **individual conversion probabilities**, making the output useful for potential marketing and customer-conversion strategies.

---

## 👩‍💻 Author

**Harkirat Kaur Arora**

BBA Student | Chitkara University

### Project Area

**Introduction to Artificial Intelligence & Machine Learning**
