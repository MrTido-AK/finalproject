
# 📄 DATA ANALYTICS PROJECT PROPOSAL

## 📌 Project Title:
**Analyzing Factors Influencing Purchase Decisions in the Consumer Electronics Sector**

---

## 🎯 Objective:
Identify which factors (e.g., product price, brand, customer age, gender, purchase frequency, satisfaction...) have the most influence on **PurchaseIntent** of consumers.

---

## 📦 Data Source:
-- Dataset Overview:
  Total number of rows (observations): 9,000
  Total number of columns (features): 9
  Link get dataset: https://www.kaggle.com/datasets/rabieelkharoua/consumer-electronics-sales-dataset

Consumer electronics dataset with the following columns:
- `ProductCategory` – Product category
- `ProductBrand` – Product brand
- `ProductPrice` – Price of the product
- `CustomerAge` – Age of the customer
- `CustomerGender` – Gender (0 = Female, 1 = Male)
- `PurchaseFrequency` – Number of purchases
- `CustomerSatisfaction` – Satisfaction score (1–5)
- `PurchaseIntent` – Purchase intent (0 = No, 1 = Yes)

Assumption: 1 user had 1 order
---

## 🧱 Project Workflow:

### 1. Data Cleaning & Preparation
- Handle missing values and outliers
- Normalize numeric values and encode categorical features

### 2. Exploratory Data Analysis (EDA)
- Descriptive Analysis of Variables
- Correlation matrix with `PurchaseIntent`
- Visualizations of relationships between features and intent

### 🔍 Additional EDA Highlights:
Here are three expanded EDA steps chosen for their simplicity and insightfulness:

  a. **Purchase Intent Distribution by Product Category**
   - Identify which types of products attract higher purchase intent

  b. **Purchase Intent by Gender**
   - Compare purchase behavior between male and female customers

  c. **Average Customer Age by Purchase Intent**
   - Determine which age groups show higher interest in purchasing
     
### 3. Modeling & Feature Impact
- Logistic Regression: interpret feature effects
- Random Forest: extract feature importance
- Model Evaluation: Accuracy, Confusion Matrix, ROC-AUC

### 4. Looker Studio Dataset Preparation
- Export cleaned and enriched data
- Create summary tables by age, gender, brand, satisfaction

### 5. Visualization with Looker Studio
- Interactive Dashboard: filters for age, gender, brand...
- Feature impact visualizations
- User behavior breakdown by segment

---

## 🧠 Expected Outcome:
- Identify top 3–5 features influencing `PurchaseIntent`
- Behavioral patterns by demographics
- Ready-to-use Looker Studio Dashboard for presentation

---

## ⚙️ Tools & Technologies:
- **Language**: Python (Pandas, Scikit-learn, Seaborn, Matplotlib)
- **Visualization**: Looker Studio (Google Data Studio)
- **Environment**: Jupyter Notebook / Google Colab

---


