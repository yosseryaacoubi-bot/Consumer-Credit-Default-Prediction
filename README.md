# Consumer-Credit-Default-Prediction
# 🚀 Credit Default Prediction using Machine Learning

## 📌 Project Overview

This project aims to predict whether a borrower will default on a loan using Machine Learning techniques on an imbalanced dataset (default rate ≈ 6.7%).

The objective is not only to build a performant model, but also to align evaluation with real-world financial risk, where missing a default (false negative) is significantly more costly than rejecting a good client.

---

## 📊 Problem Statement

Credit default prediction is a binary classification problem where:

* **Class 1 (Positive)** → Default
* **Class 0 (Negative)** → Non-default

The dataset is highly imbalanced, making traditional metrics like accuracy misleading.

---

## ⚙️ Workflow

### 1. Data Preprocessing

* Handling missing values
* Feature scaling
* Encoding categorical variables

### 2. Exploratory Data Analysis (EDA)

* Class distribution analysis
* Feature correlation insights
* Data imbalance visualization

### 3. Modeling

The following models were trained and compared:

* Logistic Regression
* Random Forest
* Gradient Boosting
* XGBoost (selected final model)

### 4. Evaluation Strategy

Due to class imbalance, the following metrics were prioritized:

* **Recall** → detect as many defaults as possible
* **ROC-AUC** → overall ranking performance
* **PR-AUC** → performance on rare positive class

---

## 📈 Results (Final Model: XGBoost)

| Metric       | Value |
| ------------ | ----- |
| Recall       | 0.808 |
| ROC-AUC      | 0.848 |
| PR-AUC       | 0.321 |
| Default Rate | 0.067 |

### 🔍 Interpretation

* The model detects ~80% of default cases
* ROC-AUC shows strong class separation
* PR-AUC is ~5× higher than the random baseline (0.067), indicating strong performance under class imbalance

---

## 📉 Key Visualizations

The notebook includes:

* ROC Curve
* Precision-Recall Curve
* Confusion Matrix
* Feature Importance (XGBoost)

---

## 🧠 Key Insights

* Accuracy is not suitable for imbalanced problems
* PR-AUC provides a more realistic view of performance
* Recall is critical in financial risk modeling
* Model evaluation must reflect business costs, not only statistical metrics

---

## 🛠️ Tech Stack

* Python
* Scikit-learn
* XGBoost
* Pandas / NumPy
* Matplotlib / Seaborn

---

## 📁 Project Structure

```
├── data/
├── notebooks/
├── models/
├── README.md
```

---

## 🚀 How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/credit-default-prediction.git
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the notebook:

```bash
jupyter notebook
```

---

## 🎯 Future Improvements

* Hyperparameter tuning (Optuna / GridSearch)
* Threshold optimization based on business cost
* Model explainability (SHAP values)
* Deployment (API / Streamlit app)

---

## 🤝 Contact

Feel free to reach out for feedback, collaboration, or opportunities in Data Science / Machine Learning.
