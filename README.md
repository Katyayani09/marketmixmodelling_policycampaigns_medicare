### **Market Mix Modeling: Causation and Correlation**
#### **Understanding the Impact of Marketing Strategies on Sales Performance**

📌 **Technologies Used:** Python, Pandas, NumPy, Statsmodels, Seaborn, Matplotlib  

---

## 📜 **Project Overview**
This project investigates the impact of different **marketing strategies** on sales performance. Using **Market Mix Modeling (MMM)**, the analysis distinguishes **causation from correlation** in marketing investments, helping businesses optimize resource allocation. 

The study leverages **regression analysis, correlation analysis, and exploratory data analysis (EDA)** to derive insights from historical campaign data.

---

## 📂 **Table of Contents**
1. [Introduction](#introduction)  
2. [Data Preprocessing](#data-preprocessing)  
3. [Feature Engineering](#feature-engineering)  
4. [Exploratory Data Analysis (EDA) & Statistical Analysis](#exploratory-data-analysis--statistical-analysis)  
5. [Correlation & Causal Inference - Regression Analysis](#causal-inference---regression-analysis)  
6. [Recommendations & Strategies](#recommendations--strategies)  
7. [How to Run](#how-to-run)  

---

## 1️⃣ **Introduction**
Marketing campaigns influence customer acquisition, but **which strategies truly impact revenue?** This project aims to determine:
- **Which marketing channels drive the most revenue?**
- **Are campaigns causally linked to sales growth or just correlated?**
- **How do different customer types respond to campaigns?**

This project uses **OLS Regression** to quantify marketing effectiveness.

---

## 2️⃣ **Data Preprocessing**
The dataset contains **campaign-related variables** such as:
- `Campaign_Email`, `Campaign_Flyer`, `Campaign_Phone`
- `Sales_Contact_1`, `Sales_Contact_2`, ..., `Sales_Contact_5`
- `Amount_Collected` (Target variable)
- `Client_Type` (Large, Medium, Small, Private Facility)

#### **Preprocessing Steps**
✔ Handling missing values  
✔ Standardizing column names  
✔ Creating **time-based features** (Month, Year)  

---

## 3️⃣ **Feature Engineering**
- **Time-based aggregation:** `Calendar_Month`, `Calendar_Year`
- **Customer segmentation analysis:** Grouping by `Client_Type`
- **Sales impact analysis:** Summarizing key revenue drivers  

---

## 4️⃣ **Exploratory Data Analysis & Statistical Analysis**
#### 🔹 **Key Insights**
- Distribution of revenue (`Amount_Collected`) across client types
- Correlation of campaigns with sales revenue
- Visualization of marketing effectiveness

#### 📊 **Example Visualization**
- Sales distribution per `Client_Type`
- Time-series trend of `Amount_Collected`
- Correlation heatmap of campaign effectiveness

---

## 5️⃣ **Causal Inference - Regression Analysis**
We performed **OLS Regression** to measure the impact of marketing campaigns on revenue.

### 🔹 **Model Summary**
```plaintext
R-squared = 0.480  # 48% variance explained
F-statistic = 342.1 (p-value = 0.00)  # Model is statistically significant
Durbin-Watson = 0.624  # Suggests autocorrelation
```

#### 🔹 **Significant Predictors (p < 0.05)**
| Feature              | Coefficient | p-value  | Impact on Revenue |
|----------------------|------------|----------|--------------------|
| Campaign_Flyer      | 3.34       | 0.000   | 🚀 Positive        |
| Sales_Contact_1     | 4.24       | 0.000   | 🚀 Positive        |
| Sales_Contact_2     | 3.64       | 0.000   | 🚀 Positive        |
| Sales_Contact_3     | 2.34       | 0.000   | 🚀 Positive        |
| Sales_Contact_4     | 10.95      | 0.000   | 🚀 Strongest Impact |

❌ **Not significant predictors:** `Campaign_Email`, `Campaign_Phone`, `Sales_Contact_5`  

---

## 6️⃣ **Recommendations & Strategies**
📌 **Actionable Insights:**
1. **Increase investment in flyer campaigns & sales contacts** (significant positive effect).
2. **Campaign phone calls are ineffective**—reallocate budget.
3. **Sales Contact 4 has the highest impact**—focus on optimizing this interaction.
4. **Different client types respond differently**—customized strategies needed.

---

## 7️⃣ **How to Run**
### 📥 **Installation**
Ensure you have the required Python libraries installed:
```bash
pip install pandas numpy seaborn statsmodels matplotlib
```

### ▶ **Run the Notebook**
Launch Jupyter Notebook or Google Colab and execute:
```python
!pip install pytimetk -q
import pandas as pd, numpy as np, seaborn as sns, statsmodels.api as sm
import statsmodels.formula.api as smf
```

### 📊 **Reproduce Results**
1. Run all cells to process the data and generate insights.
2. Analyze the regression summary and visualizations.

---

## 🏆 **Final Thoughts**
This project provides a **data-driven strategy** to optimize marketing investments by identifying **causal** relationships, not just correlations. Future improvements include:
- Implementing **A/B testing** for campaign effectiveness.
- Exploring **machine learning models** (e.g., Random Forest, XGBoost) for better predictions.

📢 *Feel free to contribute, raise issues, or suggest improvements!* 🚀  
