
# 📑 DATA ANALYSIS & VISUALIZATION PROPOSAL

**Dataset:** Mobile & Laptop Sales (50,000 transactions)  
**Goal:** Extract insights from product sales data, predict customer purchase intent, and visualize trends for business decision-making.

---

## ✅ 1. OBJECTIVES

### 🎯 Business Objectives:
- Understand customer purchasing behavior by region, brand, and product type.
- Predict purchase intent for marketing targeting.
- Generate visual reports and dashboards to support business insights.

---

## 📦 2. DATASET OVERVIEW

- Rows: 50,000
- Columns: 16
- Contains sales data for Mobile Phones and Laptops, including product specs, prices, customer locations, and transaction details.

---

## 🔍 3. ANALYSIS PIPELINE

### 🔹 Phase 1: Data Cleaning & EDA
- Handle missing values (e.g., SSD, Core Specification)
- Convert date formats
- Feature engineering:
  - `Days in Inventory`
  - `Month`, `Quarter`, `Year`
  - `Product Segment` (Business, Budget, Gaming, Standard)
- Encode categorical variables

---

### 🔹 Phase 2: Exploratory Analysis & Insight Discovery

| Area | Focus |
|------|-------|
| Sales by Segment | Best-performing product types |
| Revenue by Brand | Top-performing brands |
| Quantity by Region | Identify high-demand markets |
| Popular Configurations | RAM/ROM/Processor analysis |
| Inventory Time | Which products sell faster/slower |

---

### 🔹 Phase 3: Predictive Modeling

#### 🧠 Classification – Purchase_Intent
- Binary Target: 1 (Quantity Sold > 1), 0 (otherwise)
- Features: Price, Brand, Region, Specs, Time
- Models: Logistic Regression, Random Forest, XGBoost
- Metrics: Accuracy, Precision, Recall, AUC, Confusion Matrix

#### 📈 Regression – Quantity Sold
- Predict total quantity sold based on product features and time
- Metrics: MAE, RMSE, R²

---

### 🔹 Phase 4: Visualization & Dashboard

- Tools: Plotly, Streamlit
- Charts:
  - Bar: Sales by Segment, Brand, Region
  - Line: Revenue over Time
  - Pie: Product Segment Share
  - Heatmap: Feature Correlation
- Output: HTML dashboard, interactive charts

---

### 🔹 Phase 5: Reporting & Actionable Insight

- Summarize findings and KPIs
- Export results to:
  - `eda_report.html`
  - `dashboard.html`
  - `cleaned_data.csv`
  - `model_summary.pdf` (optional)
- Provide actionable recommendations

---

## 🧭 4. TIMELINE (Suggested)

| Phase | Time Estimate | Output |
|-------|---------------|--------|
| Cleaning + EDA | 1 day | Cleaned data + EDA Report |
| Insight Analysis | 1–2 days | Visuals + Key Findings |
| Modeling | 1–2 days | Trained Models |
| Dashboard | 1 day | Interactive Streamlit App |
| Reporting | 1 day | Final Report & Summary |

---

## 🔚 5. ACTIONABLE EXAMPLES

| Insight | Action |
|--------|--------|
| Budget Phones sell best | Increase inventory for mid-range |
| Business Laptops sell slow | Reevaluate pricing/marketing |
| Q4 has highest sales | Stock up before October |
| Central region has high intent | Focus ads/marketing there |

---
