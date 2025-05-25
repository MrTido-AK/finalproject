# Employee Productivity Data Analysis Project

## 📊 Overview

This project analyzes a dataset on employee productivity, exploring the key drivers of work performance and building a predictive model to estimate productivity scores. The analysis combines exploratory data analysis (EDA), machine learning modeling, and practical business insights.

## 🎯 Project Objectives

- Identify the main factors influencing actual employee productivity.
- Build and evaluate a machine learning model to predict productivity scores.
- Generate actionable insights for business application and HR policy design.

## 🗂️ Repository Structure

1. Data: dataset_social_media_vs_productivity.csv
2. Python: social_productivity.ipynb
3. Presentattion: Presentation-productivity.pdf
4. Dashboard: Visualization_Prd_Score.pdf

## 🛠️ Methodology
### 1. **Data loading & Cleaning**
- Imported and explored the raw dataset.
- Cleaned data by handling missing values, check duplicate, outliers and creating new group features (e.g., behavioral and satisfaction groups).
- Performed initial data validation and ensured all variables had appropriate data types for analysis.

### 2. **Exploratory Data Analysis (EDA)**
- Explored distributions of all numerical and categorical variables.
- Analyzed correlations and group differences.
- Key finding: Self-reported *perceived productivity* and *job satisfaction* are the strongest predictors of actual productivity.

### 3. **Predictive Modeling**
- Built a Random Forest Regression model using selected features:  
  - perceived_productivity_score  
  - job_satisfaction_score  
  - sleep_hours  
  - daily_social_media_time
- Split data into training and test sets (80/20).
- Evaluated with RMSE, MAE, and R² metrics.
- Tuned hyperparameters with GridSearchCV for optimal performance.

### 4. **Visualization & Insights**
- Visualized feature importances and model performance (Actual vs Predicted).
- Analyzed productivity distribution by behavioral and self-reported groups.
- Provided actionable recommendations for business application.

### 5. **Business Application & Reporting**
- Prepared interactive visual dashboards (Looker Studio) for stakeholders.
- Documented all code, findings, and insights for easy reproducibility and further exploration.

## 📈 Key Results

- **Best Model Performance:**  
  - RMSE: 0.70  
  - MAE: 0.52  
  - R²: 0.85
- **Top Predictors:** Perceived productivity score and job satisfaction score.
- **Business Recommendation:** Focus on employee engagement and satisfaction programs for maximum impact.

## 🚧 Limitations

- Heavy reliance on self-reported data (may include subjective bias).
- Limited number of features and a cross-sectional (single time point) dataset.
- Results may not generalize to all organizations or industries.

## 🖥️ Technologies & Tech Stack Used

- **Python**: Data analysis, preprocessing, and modeling
- **Google Colab**: Interactive analysis and prototyping
- **Pandas, NumPy**: Data manipulation & computation
- **Matplotlib, Seaborn**: Data visualization
- **Scikit-learn**: Machine learning algorithms and evaluation
- **Looker Studio**: Dashboard visualization and business reporting
- **GitHub**: Version control and collaboration

## 👤 Author

- **Name:** Hien Hoang
- **Role:** Data Analyst
