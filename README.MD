# 🛒 [BIGTARGET]: EDA & Uplift Modeling with Business Insights

## 📌 Project Overview

This project focuses on **Exploratory Data Analysis (EDA)** and **Uplift Modeling** to predict customer response to marketing campaigns.

The objective is to identify:

- 🎯 Which customers are likely to respond to a marketing campaign
- 📈 Which customers are influenced positively by treatment (marketing)
- 💡 Actionable business insights from customer behavior

This project simulates a real-world **marketing experimentation scenario** with control and test groups.

---

## 📊 Problem Statement

- Target Variable: `response_att`
- Goal: Predict whether a customer will respond to a marketing mailing
- Dataset contains:
  - 196 features
  - Customer demographic data (age, number of children, etc.)
  - Purchase statistics
  - Discount behavior
  - Treatment group (test/control)

---

## 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Uplift Modeling Techniques
- EDA

---

## 📂 Project Structure

---

## 🔎 Project Workflow

### 1️⃣ Data Understanding

- 196 total columns
- Target variable: `response_att`
- Dataset divided into:
  - Test group (treatment)
  - Control group
- Includes numerical and categorical features

---

### 2️⃣ Data Preprocessing

- Handling missing values
- Encoding categorical variables
    - Gender mapped to binary
    - Group mapped to binary (test/control)
- Feature transformation
- Outlier detection

Example transformation:

```python
gender_map = {'X': 0, 'M': 1}
group_map = {'test': 0, 'control': 1}

pdf['gender'] = pdf['gender'].map(gender_map)
pdf['group'] = pdf['group'].map(group_map)

kaggle - https://www.kaggle.com/code/mrmorj/bigtarget-eda-uplift-model-insights-task/notebook
