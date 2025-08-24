# 📊 Income Level Prediction – Capstone Project

## 📌 Project Overview

This project focuses on analyzing the **Adult Income Dataset** (census data) to predict whether an individual earns **more than \$50,000 per year** based on demographic and socio-economic attributes.

The notebook walks through all the stages of a **data science pipeline**, including:

* Data exploration
* Cleaning and preprocessing
* Feature engineering
* Model building and evaluation
* Insights and recommendations

---

## 📂 Dataset

* **Source**: Census dataset in CSV format
* **Target Variable**: `income` (<=50K or >50K per year)
* **Key Features**: Age, education, occupation, marital status, hours-per-week, etc.

**Data issues identified**:

* Imbalanced dataset (more people earn <=50K).
* Missing values (\~2203) and duplicates (\~53).
* Categorical variables with invalid entries (`?`).
* Outliers detected.
* Correlated features (e.g., `education` vs `education-num`).

---

## 🛠️ Methodology

### 1. Exploratory Data Analysis (EDA)

* Distribution analysis of categorical and numerical features.
* Identified imbalance in income classes.
* Plotted correlation matrix to understand feature relationships.

### 2. Data Cleaning & Preprocessing

* Replaced invalid categorical values (`?`) with mode.
* Handled missing values and removed duplicates.
* Encoded categorical variables.
* Dropped irrelevant features:

  * `fnlwgt` (final census weight, not predictive of income).
  * `education-num` (duplicate of `education`).

### 3. Feature Engineering

* Reduced categories within some features to prevent overfitting.
* Standardized data for model compatibility.

### 4. Model Building

* Tested multiple machine learning models.
* Focused on **Random Forest Classifier** due to robustness with noisy data and outliers.

### 5. Model Evaluation

* Since the dataset is imbalanced, **accuracy was not reliable**.
* Used **F1-score** and **AUC (Area Under the Curve)** as evaluation metrics.
* **Best Model**: Random Forest

  * F1-score: **84% (weighted average)**
  * AUC: **89%**

---

## 📈 Key Insights

1. **Imbalance in income**: Majority of individuals earn <=50K.
2. **Gender disparity**: More men than women in the labor force.
3. **Age factor**: Younger people earning more than 50K is relatively rare.
4. **Education**: Higher education correlates strongly with higher income.
5. **Irrelevant features**: `fnlwgt`, `education-num`, and `native-country` had little to no direct impact on income.

---

## ✅ Recommendations

* Collect additional relevant socio-economic features to boost model performance.
* Use **ensemble methods** like XGBoost and apply **hyperparameter tuning** for optimization.
* Address **class imbalance** (e.g., SMOTE, resampling, or cost-sensitive learning).
* Expand the study with cross-country datasets to improve generalization.

---

## 🚀 How to Run the Notebook

1. Clone this repository:

   ```bash
   git clone https://github.com/<username>/<repo>.git
   cd <repo>
   ```
2. Install required libraries:

   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook in Jupyter:

   ```bash
   jupyter notebook Babatunde_Akinbo_Capstone_Project.ipynb
   ```
4. Run all cells to reproduce the analysis and results.

---

## 📚 Technologies Used

* **Python**
* **Jupyter Notebook**
* **Libraries**: pandas, numpy, matplotlib, seaborn, scikit-learn

---

## 👨‍💻 Author

**Babatunde Akinbo**
Capstone Project for Income Level Prediction
