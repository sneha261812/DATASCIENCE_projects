# 🚢 Titanic Dataset – Data Cleaning & Exploratory Data Analysis (EDA)

This project explores the famous **Titanic** dataset to uncover insights about passenger survival using data cleaning and visualization techniques. The analysis focuses on understanding how features like **gender**, **passenger class**, and **age** influenced survival outcomes.

---

## 🎯 Objective

Perform comprehensive **data cleaning** and **exploratory data analysis (EDA)** to:

- Handle missing or inconsistent values
- Understand data distribution and types
- Identify patterns in survival based on key features

---

## 📦 Dataset

- Source: [Titanic - Kaggle Competition](https://www.kaggle.com/c/titanic/data)
- Files: `train.csv`, `test.csv`

---

## 🛠️ Tools & Libraries

| Library       | Purpose                           |
|---------------|-----------------------------------|
| `Pandas`      | Data manipulation and inspection  |
| `NumPy`       | Numerical operations              |
| `Matplotlib`  | Data visualization                |
| `Seaborn`     | Statistical plotting              |

---

## 🧹 Data Cleaning Steps

✔ Checked for null values and missing data  
✔ Converted data types where necessary (e.g., age as float)  
✔ Imputed missing values in `Age`, `Embarked`  
✔ Dropped irrelevant columns like `Cabin`, `Ticket` if needed  
✔ Encoded categorical variables (e.g., `Sex`, `Embarked`)

```python
df['Age'].fillna(df['Age'].median(), inplace=True)
df['Embarked'].fillna(df['Embarked'].mode()[0], inplace=True)
```
# 📊 Exploratory Data Analysis (EDA)
## 🔹 1. Survival Rate by Gender
```python
sns.barplot(data=df, x='Sex', y='Survived')
```
**Insight: Females had a significantly higher survival rate than males.**
## 🔹 2. Survival Rate by Passenger Class
```python
sns.barplot(data=df, x='Pclass', y='Survived')
```
**Insight: First-class passengers had the highest chance of survival.**
##🔹 3. Age Distribution of Survivors vs Non-Survivors
```python
sns.kdeplot(df[df['Survived'] == 1]['Age'], label='Survived', shade=True)
sns.kdeplot(df[df['Survived'] == 0]['Age'], label='Not Survived', shade=True)
```
**Insight: Children and younger adults had higher survival rates.**
## 🔹 4. Heatmap of Correlation Between Features
```python
sns.heatmap(df.corr(), annot=True, cmap='coolwarm')
```
**Helps understand the correlation between numerical variables.**
