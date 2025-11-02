# 🧠 Feature Engineering and Preprocessing on the Titanic Dataset

## 📘 Project Overview
This project demonstrates **data preprocessing and feature engineering** on the **Titanic Survival Dataset** from Kaggle.  
The goal is to clean, transform, and prepare the dataset for machine learning classification tasks — predicting whether a passenger survived or not.

---

## 📊 Dataset Information
- **Name:** Titanic Dataset  
- **Source:** [Kaggle Titanic: Machine Learning from Disaster](https://www.kaggle.com/c/titanic/data)  
- **Type:** Classification  
- **Target Variable:** `Survived` (0 = No, 1 = Yes)  
- **Size:** 891 rows × 12 columns  

---

## ⚙️ Steps Performed

### 1️⃣ Data Loading and Exploration
- Loaded dataset using `pandas`.
- Checked data types and missing values.

### 2️⃣ Missing Value Handling
- `Age`: Replaced missing values with **median**.  
- `Embarked`: Replaced missing values with **mode**.  
- Dropped `Cabin` due to excessive missing data.

### 3️⃣ Encoding
- **Label Encoding** for `Sex` (male=1, female=0).  
- **One-Hot Encoding** for `Embarked` categories.

### 4️⃣ Feature Scaling
- Used **StandardScaler** for numeric columns (`Age`, `Fare`).

### 5️⃣ Feature Extraction
- Applied **PCA (2 components)** to reduce dimensionality and visualize variance.

### 6️⃣ Feature Selection
- Used **SelectKBest (f_classif)** to select top 5 features most correlated with survival.

---

## 📈 Key Insights
- Most significant features: `Sex`, `Pclass`, `Fare`, `Age`, `SibSp`.  
- PCA retained ~75% of total variance.  
- After preprocessing, dataset became clean, numerical, and ready for model training.

---

## 🧩 Ethical Discussion
Models using sensitive features like **Gender** or **Marital Status** can introduce unfair bias.  
### 🔒 Mitigation Strategies:
- Avoid using sensitive attributes as predictors when unnecessary.  
- Test for fairness metrics (e.g., disparate impact ratio).  
- Apply reweighing or fairness-aware learning techniques.  
- Use explainability tools such as **SHAP** or **LIME**.

---

## 🗂️ Repository Structure
