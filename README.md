# 📡 Telco Customer Churn Prediction

This project focuses on predicting customer churn for a telecom company using machine learning algorithms.

The project includes:
- Exploratory Data Analysis (EDA)
- Data Preprocessing
- Feature Engineering
- Model Comparison
- Hyperparameter Optimization

The main goal is to identify customers who are likely to leave the company based on customer behavior and service-related information.

---

## 📊 Dataset

The dataset used in this project is the 
[Telco Customer Churn Dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn).

The dataset contains information about:
- Customer demographics
- Internet and phone services
- Contract and payment information
- Monthly and total charges

### Target Variable
- `Churn` → Indicates whether the customer churned or not.

---

## 🚀 Project Steps

### 1. Exploratory Data Analysis
- Variable type analysis
- Categorical and numerical variable examination
- Missing value analysis
- Outlier analysis using the IQR method
- Target variable analysis

---

### 2. Data Preprocessing
- Converted `TotalCharges` variable from string to numeric
- Removed missing observations
- Applied Label Encoding and One-Hot Encoding
- Standardized numerical variables using `StandardScaler`

---

### 3. Feature Engineering
New variables were created to better capture customer behavior patterns.

Examples:
- Customer engagement indicators
- Service usage features
- Tenure-based segmentation

Some engineered features were later removed after observing that they did not improve model performance.

---

### 4. Modeling

The following machine learning algorithms were evaluated using 5-Fold Cross Validation:

- Logistic Regression
- Decision Tree
- K-Nearest Neighbors
- Random Forest
- Gradient Boosting
- XGBoost
- LightGBM
- CatBoost

Evaluation metrics:
- Accuracy
- F1-Score
- ROC-AUC

---

### 5. Hyperparameter Optimization

Hyperparameter tuning was applied using `GridSearchCV` for the best-performing models:
- Logistic Regression
- Gradient Boosting
- CatBoost

---

## 📈 Final Results

| Model | Accuracy | F1-Score | ROC-AUC |
|------|------|------|------|
| Logistic Regression | 0.8047 | 0.5899 | 0.8455 |
| Gradient Boosting | 0.8044 | 0.5891 | 0.8455 |
| CatBoost | 0.8047 | 0.5818 | 0.8482 |

### Best Model
CatBoost achieved the highest ROC-AUC score after hyperparameter optimization.

---

## 🔍 Key Findings

- Customers with month-to-month contracts are more likely to churn.
- Higher monthly charges are associated with higher churn risk.
- Customers without additional support services tend to churn more frequently.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- LightGBM
- CatBoost

---

## ⚙️ Installation

```bash
git clone https://github.com/furkandonmeez/telco-churn-prediction.git

cd telco-churn-prediction

pip install -r requirements.txt
```

---

## ▶️ Run the Project

```bash
jupyter notebook notebooks/telco_churn_prediction.ipynb
```
