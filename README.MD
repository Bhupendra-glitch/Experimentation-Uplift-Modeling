# 📊 Experimentation & Uplift Modeling Project

## 🚀 BIGTARGET Hackathon (LENTA)

> Optimizing marketing campaigns using **causal inference and uplift modeling** to target the *right customers* and maximize ROI.

---

## 📖 Overview

Traditional machine learning models predict *who is likely to buy*.  
However, they fail to answer a more important business question:

> ❓ *Who will buy **because of** the campaign?*

This project solves that problem using **Uplift Modeling**, a technique that estimates the **incremental impact of a treatment (campaign)** on user behavior.

---

## 🎯 Objectives

- Identify **persuadable customers** who respond positively to campaigns  
- Avoid targeting:
  - Customers who will buy anyway  
  - Customers who will never respond  
- Improve **marketing efficiency and ROI**  
- Compare uplift modeling with traditional A/B testing  

---

## 📂 Dataset Description

The dataset contains customer-level information, including:

- 👤 Demographics (Age, Income, etc.)  
- 🛒 Purchase history  
- 📱 Campaign exposure (SMS / Viber)  
- 🎯 Treatment flag (1 = treated, 0 = control)  
- ✅ Target variable (conversion / purchase)  

---

## 📌 Table of Contents

- [Project Workflow](#project-workflow)
- [Exploratory Data Analysis](#exploratory-data-analysis)
  - [Quick View](#quick-view)
  - [Missing Values](#missing-values)
  - [Outliers](#outliers)
- [Experimentation (A/B Testing)](#experimentaion-ab-testing)
  - [Test vs Control](#test-vs-control)
  - [Feature Comparison](#feature-comparison)
- [Uplift Modeling](#uplift-modeling)
  - [Concept](#concept)
  - [Customer Segments](#customer-segments)
  - [Model Approach](#model-approach)
- [Model Evaluation](#model-evaluation)
- [Insights](#insights)
- [Results](#results)
- [Tech Stack](#tech-stack)
- [Future Improvements](#future-improvements)
- [Author](#author)

---

## 🔄 Project Workflow

1. Data Understanding  
2. Data Cleaning & Preprocessing  
3. Exploratory Data Analysis (EDA)  
4. A/B Testing (Baseline)  
5. Uplift Modeling  
6. Model Evaluation  
7. Business Insights  

---

## 🔍 Exploratory Data Analysis

### ⚡ Quick View
- Checked dataset shape and column types  
- Observed class imbalance  
- Analyzed target variable distribution  

---

### 🧹 Missing Values
- Identified missing values across features  
- Applied:
  - Mean/median imputation  
  - Dropping irrelevant features  

---

### 📉 Outliers
- Detected outliers using:
  - Boxplots  
  - Statistical thresholds  
- Handled extreme values to improve model robustness  

---

## 🧪 Experimentation (A/B Testing)

### ⚖️ Test vs Control
- Divided dataset into:
  - **Treatment Group** → Received campaign  
  - **Control Group** → No campaign  

#### 📊 Key Observations:
- Conversion rate difference  
- Behavioral variation between groups  

---

### 🔍 Feature Comparison
- Compared features such as:
  - Age  
  - Purchase frequency  
  - Income level  

👉 Helped identify factors influencing campaign response  

---

## 📈 Uplift Modeling

### 🧠 Concept

Uplift modeling estimates:

> **Uplift = P(Response | Treatment) - P(Response | Control)**

Instead of predicting outcomes, it predicts **causal impact**.

---

### 👥 Customer Segments

| Segment           | Behavior |
|------------------|--------|
| Persuadable      | Respond only if treated ✅ |
| Sure Things      | Will respond anyway |
| Lost Causes      | Won’t respond |
| Do Not Disturb   | Negative effect ⚠️ |

---

### 🤖 Model Approach

Implemented:

#### 🔹 T-Learner (Two-Model Approach)
- Model 1 → Trained on treatment group  
- Model 2 → Trained on control group  
- Uplift = Difference in predictions  

#### 🔹 Algorithms Used:
- Logistic Regression  
- Random Forest  

---

## 📊 Model Evaluation

Evaluated using:

- 📈 Uplift Curve  
- 📊 Qini Curve  
- 🔢 AUUC (Area Under Uplift Curve)  

👉 These metrics measure how well the model ranks **persuadable customers**

---

## 📊 Insights

### 📌 Dependence of Purchase Share
- Purchase behavior varies significantly with treatment  
- Certain customer segments show higher uplift  

---

### 🔥 Crazy Purchases
- Some users exhibit unusually high purchase activity  
- Indicates potential **high-value customers**  

---

### 📱 Response SMS & Viber
- Communication channels impact response rate  
- SMS vs Viber shows different effectiveness  

---

### 👴 Aged People
- Older customers respond differently  
- Age plays a key role in campaign success  

---

## 🏆 Results

- 🎯 Improved targeting efficiency  
- 💰 Reduced marketing costs  
- 📈 Increased conversion rate compared to random targeting  
- 🚀 Demonstrated superiority over traditional ML models  

---

## 🛠️ Tech Stack

- **Language:** Python 🐍  
- **Libraries:**  
  - Pandas, NumPy  
  - Scikit-learn  
  - Matplotlib, Seaborn  
- **Advanced (optional):**  
  - CausalML  
  - EconML  

---

## 💡 Future Improvements

- 🔹 Deploy as a **Streamlit Web App**  
- 🔹 Use advanced learners (X-Learner, DR-Learner)  
- 🔹 Real-time recommendation system  
- 🔹 Integrate with business dashboards  

---

## 📸 Demo (Optional)
_Add screenshots or Streamlit demo here_

---

## 🧑‍💻 Author

**Bhupendra Sahu**  
🎓 B.Tech Student | 📊 Data Science Enthusiast  

- 🔗 LinkedIn: *Add Link*  
- 💻 GitHub: *Add Link*  

---

## ⭐ Support

If you found this project useful:

⭐ Star this repository  
🍴 Fork it  
📢 Share it  

---

## 📜 License

This project is open-source and available under the **MIT License**.
