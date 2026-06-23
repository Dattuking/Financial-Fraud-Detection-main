# 🛡️ Financial Fraud Detection System

## 🌟 Overview

The **Financial Fraud Detection System** is an end-to-end Machine Learning application designed to identify fraudulent financial transactions and assist financial institutions in minimizing losses caused by fraud.

This project leverages data preprocessing, feature engineering, class balancing techniques, machine learning models, and an interactive Streamlit dashboard to analyze transaction behavior and predict whether a transaction is fraudulent or legitimate.

The system provides real-time fraud prediction, risk scoring, transaction analytics, and model performance visualization through a user-friendly web interface.

---

## 🌐 Live Demo

🚀 **Streamlit Application**

https://financial-fraud-detection-main-cqhnrfpa92d8m6wi3kpnyt.streamlit.app/

💻 **GitHub Profile**

https://github.com/Dattuking

---

# 🎯 Problem Statement

Financial fraud is a major concern for banks, digital payment providers, and financial institutions worldwide.

Challenges include:

* Massive transaction volumes
* Highly imbalanced fraud datasets
* Evolving fraud patterns
* Real-time fraud detection requirements
* Reducing false alarms while maintaining high detection accuracy

This project addresses these challenges using machine learning techniques and intelligent feature engineering to identify suspicious transactions effectively.

---

# 🏗️ System Workflow

```text
Raw Transaction Data
          │
          ▼
Data Cleaning
          │
          ▼
Feature Engineering
          │
          ▼
Feature Scaling
          │
          ▼
SMOTE Balancing
          │
          ▼
Model Training
(Logistic Regression,
Gradient Boosting,
XGBoost)
          │
          ▼
Model Evaluation
          │
          ▼
Best Model Selection
          │
          ▼
Streamlit Dashboard
          │
          ▼
Real-Time Fraud Prediction
```

---

# 📊 Dataset Description

The dataset contains financial transaction records with information such as:

* Transaction Amount
* Transaction Type
* Sender Balance
* Receiver Balance
* Transaction Time
* Fraud Status

### Target Variable

| Value | Meaning                |
| ----- | ---------------------- |
| 0     | Legitimate Transaction |
| 1     | Fraudulent Transaction |

Since fraudulent transactions represent only a small portion of all transactions, special preprocessing techniques are required to handle class imbalance.

---

# 🧹 Data Preprocessing

The preprocessing pipeline includes:

### Data Cleaning

* Handling missing values
* Data validation
* Feature selection

### Feature Scaling

Numerical features are standardized using:

* StandardScaler

### Class Balancing

Fraud detection datasets are naturally imbalanced.

To improve model performance:

* SMOTE (Synthetic Minority Oversampling Technique)

is applied to generate synthetic fraud samples and balance the dataset before training.

---

# ⚙️ Feature Engineering

Several custom features were created to capture transaction behavior patterns.

### Transaction Features

* Transaction Amount
* Transaction Hour
* Weekend Transaction Indicator

### Sender Features

* Sender Balance Change
* Sender Utilization Ratio
* Sender Transaction Count

### Receiver Features

* Receiver Balance Change
* Receiver Growth Ratio
* Receiver Transaction Count

### Risk Indicators

* Large Transaction Flag
* Account Drained Indicator
* New Receiver Account Indicator
* High Risk Transaction Type Indicator

These engineered features significantly improve fraud detection capability.

---

# 🤖 Machine Learning Models

The project evaluates multiple machine learning algorithms.

## 1️⃣ Logistic Regression

A simple and interpretable baseline classification model.

### Advantages

* Fast training
* Easy interpretation
* Good baseline performance

---

## 2️⃣ Gradient Boosting Classifier

An ensemble learning algorithm that combines multiple weak learners.

### Advantages

* Strong predictive performance
* Captures non-linear relationships
* Robust against overfitting

---

## 3️⃣ XGBoost Classifier

An advanced gradient boosting framework optimized for speed and accuracy.

### Advantages

* High accuracy
* Efficient handling of large datasets
* Excellent fraud detection performance

---

# 📈 Model Evaluation Metrics

The models are evaluated using:

| Metric    | Description                            |
| --------- | -------------------------------------- |
| Accuracy  | Overall prediction correctness         |
| Precision | Measures false positives               |
| Recall    | Measures fraud detection effectiveness |
| F1 Score  | Balance between precision and recall   |
| ROC-AUC   | Overall classification capability      |

The best-performing model is automatically selected based on the highest F1 Score.

---

# 📊 Dashboard Features

The Streamlit dashboard consists of four main modules.

---

## 📈 Overview Dashboard

Provides a high-level summary of transaction statistics.

### Visualizations

* Fraud vs Legitimate Distribution
* Fraud Rate Analysis
* Transaction Amount Distribution
* Fraud by Transaction Hour
* Fraud by Transaction Type

---

## 🔍 Transaction Analysis

Allows detailed exploration of transaction patterns.

### Features

* Filter transactions by type
* Filter fraud and legitimate records
* Amount range filtering
* Transaction behavior analysis
* Raw transaction inspection

---

## 🤖 Model Performance Dashboard

Displays performance comparison across models.

### Includes

* Accuracy Comparison
* Precision Comparison
* Recall Comparison
* F1 Score Comparison
* ROC-AUC Comparison
* Radar Charts
* Confusion Matrices

---

## 🎯 Fraud Prediction Module

Users can manually enter transaction details.

The system returns:

* Fraud Prediction
* Fraud Probability
* Risk Score
* Fraud Risk Factors
* Visual Risk Gauge

---

# 🔄 Prediction Process

1. User enters transaction details.
2. Features are generated automatically.
3. Input data is standardized.
4. Best trained model performs prediction.
5. Fraud probability is calculated.
6. Risk indicators are analyzed.
7. Final fraud assessment is displayed.

---

# 🛠️ Technology Stack

## Programming Language

* Python

## Data Processing

* Pandas
* NumPy

## Machine Learning

* Scikit-Learn
* XGBoost
* SMOTE

## Visualization

* Plotly
* Plotly Express

## Dashboard Development

* Streamlit

## Database

* SQLite

## Model Serialization

* Joblib

---

# 📂 Project Structure

```text
Financial-Fraud-Detection/
│
├── app.py
├── data_preprocessing.py
├── train_model.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── models/
│   ├── best_model.pkl
│   ├── best_model_name.pkl
│   ├── scaler.pkl
│   ├── feature_cols.pkl
│   ├── logistic_regression.pkl
│   ├── gradient_boosting.pkl
│   └── xgboost.pkl
│
└── fraud_data.db
```

---

# 🚀 Installation

### Clone Repository

```bash
git clone https://github.com/Dattuking/Financial-Fraud-Detection.git
cd Financial-Fraud-Detection
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Data Preprocessing

```bash
python data_preprocessing.py
```

### Train Models

```bash
python train_model.py
```

### Launch Application

```bash
streamlit run app.py
```

---

# 📦 Required Libraries

```text
pandas
numpy
scikit-learn
xgboost
imbalanced-learn
streamlit
plotly
joblib
```

---

# 🔮 Future Enhancements

* Deep Learning-Based Fraud Detection
* Explainable AI (SHAP & LIME)
* Real-Time Transaction Monitoring
* Fraud Alert Notification System
* REST API Development
* AWS/Azure Cloud Deployment
* Streaming Data Integration

---

# 🎓 Learning Outcomes

Through this project, I gained hands-on experience in:

* Data Cleaning and Preprocessing
* Feature Engineering
* Fraud Analytics
* Handling Imbalanced Datasets
* Machine Learning Model Development
* Model Evaluation Techniques
* Streamlit Application Development
* Interactive Data Visualization
* End-to-End ML Deployment

---

# 👨‍💻 Author

## Kona Venkata Datta Sai Krishna

🎓 B.Tech – Computer Science and Engineering (Artificial Intelligence)

🏫 Amrita Vishwa Vidyapeetham, Amaravati

📧 Email: [datthukona@gmail.com](mailto:datthukona@gmail.com)

💻 GitHub: https://github.com/Dattuking

🌐 Live Project:
https://financial-fraud-detection-main-cqhnrfpa92d8m6wi3kpnyt.streamlit.app/

---

## ⭐ Support

If you found this project useful, please consider:

⭐ Starring the repository

🍴 Forking the project

🤝 Connecting with me on GitHub

📢 Sharing feedback and suggestions

---

**"Using Machine Learning to build smarter, safer, and more secure financial systems."**
