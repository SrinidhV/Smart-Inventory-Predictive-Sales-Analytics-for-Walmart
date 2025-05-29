# 🛒 Smart Inventory and Promotion Optimization for Walmart

**Capstone Project | Predictive Sales Analytics | CRISP-DM | Random Forest | Inventory Policy | Promotion Classifier**

## 📌 Project Overview

This project presents a data-driven solution for Walmart to optimize inventory levels and promotional planning across its 45 stores and 81 departments. Using three years of weekly point-of-sale data enriched with weather, economic, and markdown variables, we forecast weekly sales and identify high-impact promotion weeks to reduce operational inefficiencies, improve service levels, and increase profitability.

---

## 📁 Datasets Used

| Dataset       | Description |
|---------------|-------------|
| `train.csv`   | Weekly sales per store-department-week (Feb 2010 – Nov 2012) |
| `features.csv`| Includes temperature, fuel prices, CPI, unemployment, and 5 Markdown fields |
| `stores.csv`  | Store type (A/B/C) and size in square feet |
| `test.csv`    | Future weeks without sales values; used for model predictions |

---

## 🧠 Problem Statement

Walmart must predict weekly sales at the **store-department-week** level to:
- Reduce stockouts and overstocking
- Improve inventory planning using a **three-tier buffer**
- Identify **high-potential promotion weeks**
- Account for **holidays**, **economic variables**, and **weather**

---

## 🛠️ Methodology

We followed the **CRISP-DM** process:
1. **Business Understanding** – Optimize stock & promotions to minimize cost and maximize service level
2. **Data Understanding** – Sales + markdowns + store features + external factors
3. **Data Preparation** – Merged datasets, extracted date components, filled missing values
4. **Modeling** – Trained Random Forest Regressor & Classifier
5. **Evaluation** – Metrics: R², RMSE, WMAE, Precision, Recall
6. **Deployment** – Inventory & promotion strategy saved as outputs for business use

---

## 📊 Exploratory Insights

- **Sales Peaks**: Week 47 (Thanksgiving) & Week 51 (Pre-Christmas)
- **Holiday Uplift**: +7.1% average sales
- **Store 20** had the highest sales; **Store 33** the lowest
- **Fuel price elasticity** = –0.084 (slightly inelastic)
- High-volatility Depts: 39, 72, 92 → need larger safety stock

---

## 🤖 Modeling

### Regression: **Random Forest Regressor**
- **R²** = 0.9745
- **WMAE** = $1,634.84
- **RMSE** = $3,644.74

### Classification: **Random Forest Classifier**
- Target: Identify weeks with predicted demand > 95ᵗʰ percentile
- Promotion Weeks Found: Week 6, Week 22, Week 51
- **Accuracy** = 1.000 | **Precision** = 1.000 | **Recall** = 1.000

---

## 📦 Inventory Optimization Strategy

- **Base Inventory** = Predicted Sales × 1.10
- **Safety Stock** = Base × 0.10
- **Final Inventory** = Predicted × 1.21

**Results:**
- 54.5% Overstock rows (Avg. surplus: $1,310)
- 45.5% Stockout rows (Avg. shortfall: $1,586)
- Holiday weeks handled seamlessly using same policy

---

## 📈 Promotion Opportunity Framework

- Identified **high-traffic weeks** using the 95ᵗʰ percentile threshold
- Classifier trained on these labels for predictive insight
- Enables **strategic promotional planning** for high ROI

---

## 🧠 Key Learnings

- Most influential features: `Department`, `Store Size`, `Store ID`
- Economic indicators add marginal but complementary value
- Localized and category-specific inventory rules perform better than global ones
- Robust predictions can directly translate into actionable business policies

---

## 📁 Folder Structure


---

## 🚀 Future Work

- Incorporate **daily sales** for finer-grained modeling
- Integrate **POS data**, **competitor pricing**, and **local events**
- Use **LSTM** or hybrid models for temporal forecasting
- Build a **Streamlit dashboard** for operational teams
- Add **financial optimization** and **sustainability metrics**

---

## 📚 References

- Walmart Store-Level Sales Forecasting Kaggle Dataset  
- Hyndman & Athanasopoulos (2018) – Forecasting Principles  
- Ferreira et al. (2016) – Random Forest in Retail  
- Walmart Inventory Optimization Whitepapers (2023–2024)

---

## 👥 Team

**Group 9 - Capstone Team**  
📍 San Jose, CA  
🗓️ 2024

---

