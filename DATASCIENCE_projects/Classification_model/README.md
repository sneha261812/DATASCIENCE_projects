# 🌳 Customer Purchase Prediction with Decision Tree

Predict whether a customer will purchase a product or subscribe to a service using their **demographic** and **behavioral** data. This project uses the **Bank Marketing dataset** from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing) and applies a **Decision Tree Classifier** to make predictions.

---

## 📌 Project Overview

Marketing campaigns are most successful when they reach the right people. In this project, we build a machine learning model to help a bank predict which clients are most likely to subscribe to a term deposit based on their past behavior and personal details.

---

## 🧠 Objectives

- 🔍 Explore and preprocess the bank marketing dataset
- 🌳 Build a Decision Tree Classifier
- 📊 Evaluate model performance using classification metrics
- 📈 Visualize the decision tree for interpretability

---

## 📂 Dataset

**Source:** [UCI Bank Marketing Dataset](https://archive.ics.uci.edu/ml/datasets/Bank+Marketing)

**Description:**  
The dataset contains details of direct marketing campaigns (phone calls) of a Portuguese banking institution.

**Key Features:**

- `age`, `job`, `marital`, `education`, `default`, `housing`, `loan`
- `contact`, `month`, `day_of_week`, `duration`
- `campaign`, `pdays`, `previous`
- `emp.var.rate`, `cons.price.idx`, `euribor3m`, `nr.employed`
- `y` (target: has the client subscribed? yes/no)

---

## 🔧 Tools & Technologies

- Python 🐍
- Pandas & NumPy for data handling
- Scikit-learn for machine learning
- Matplotlib & Seaborn for visualization
- Graphviz / `plot_tree()` for Decision Tree plotting

---

## 🚀 Project Workflow

1. **Data Loading**  
   Load the CSV file and explore the data structure.

2. **Data Cleaning**  
   - Handle missing values
   - Encode categorical features

3. **Exploratory Data Analysis (EDA)**  
   - Understand feature distributions
   - Analyze correlations and target variable behavior

4. **Model Building**  
   - Train a Decision Tree classifier
   - Hyperparameter tuning (max depth, min samples split)

5. **Evaluation**  
   - Accuracy, Precision, Recall, F1-score
   - Confusion Matrix

6. **Visualization**  
   - Plot the Decision Tree
   - Feature Importance chart

---

## 📊 Results

- 📈 Accuracy Achieved: ~87% (depending on tuning)
- 🧠 Top Predictive Features: `duration`, `poutcome`, `previous`, `emp.var.rate`

---

## 📁 Folder Structure

