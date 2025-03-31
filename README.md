# Mobile Dataset Analysis: Insights and Strategy  
**Created by Hien-hoang/ DA_240923**  

---

## Table of Contents  
1. [Introduction & Objectives](#1-introduction-objectives)  
2. [Data Overview & Cleaning Plan](#2-data-overview-cleaning-plan)  
3. [Proposed Analyses](#3-proposed-analyses)  
4. [Tools & Methods](#4-tools-methods)  
5. [Deliverables](#5-deliverables)  
6. [Timeline](#6-timeline)  
7. [Additional Considerations](#7-additional-considerations)  

---

## 1. Introduction & Objectives  
**Goal**: Extract actionable insights from the **Mobiles Dataset (2025)** to inform decision-making for market positioning, pricing strategy, and product development.  

**Key Objectives**:  
- **Market Trends**: Track evolution of device specifications (RAM, battery, screen size) and pricing over time.  
- **Competitive Analysis**: Compare brands (e.g., Realme, POCO, Oppo) across performance, pricing, and market segments.  
- **Customer Value Drivers**: Identify features (RAM, camera quality) that strongly correlate with price.  
- **Regional Pricing Strategy**: Analyze price variations across currencies (PKR, INR, USD, etc.) and markets.  
- **Product Segmentation**: Classify devices into budget, mid-range, and flagship categories.  

---

## 2. Data Overview & Cleaning Plan  

### **Data Structure**  
- **Fields**: Brand, Model, Storage, Weight, RAM, Front/Back Camera, Processor, Battery, Screen Size, Prices (in multiple currencies), Release Year.  
- **Sample Size**: 930  

### **Cleaning Challenges**  
#### **Formatting**:  
- Split camera specs (e.g., "50MP + 2MP" → Primary/Secondary).  
- Normalize prices (e.g., "PKR 99,999" → numeric USD values).  
- Extract release years from strings (e.g., "2020POCO,M2 Pro..." → 2020).  

#### **Standardization**:  
- Normalize processor names (e.g., "Snapdragon 8 Gen 2" → "High-tier").  
- Handle missing data (e.g., battery capacity, camera details).  

---

## 3. Proposed Analyses  

### **3.1 Market Trends Over Time**  
- **Analysis**: Track changes in RAM, battery size, screen resolution, and price per year.  
- **Visualization**:  
  - **Line charts** (Matplotlib): RAM and price trends over time.  
  - **Bar charts** (Seaborn): Average battery size by year.  

### **3.2 Brand Comparison**  
- **Analysis**: Compare brands on price competitiveness, flagship vs. budget offerings, and processor usage.  
- **Visualization**:  
  - **Heatmaps** (Seaborn): Correlation between brand features and price.  
  - **Radar charts** (Plotly): Multi-variable comparison (RAM, battery, price).  

### **3.3 Feature-Price Relationship**  
- **Analysis**: Use regression models to identify price-correlated features (RAM, camera megapixels).  
- **Visualization**:  
  - **Scatter plots** (Plotly): Price vs. RAM/camera.  
  - **Correlation matrices** (Seaborn): Feature-price relationships.  

### **3.4 Regional Pricing Strategy**  
- **Analysis**: Convert prices to USD and identify over/underpriced regions.  
- **Visualization**:  
  - **World maps** (Plotly): Price distribution by region.  
  - **Scatter plots** (Matplotlib): Price comparisons (USD vs. PKR/INR).  

### **3.5 Processor & Hardware Trends**  
- **Analysis**: Track processor popularity by price tier and analyze hardware trends (e.g., battery size).  

### **3.6 Camera Evolution**  
- **Analysis**: Compare front/back camera megapixel trends and dual-camera adoption over time.  

---

## 4. Tools & Methods  
- **Programming**: Python (Pandas, NumPy, Matplotlib, Seaborn, Plotly, Scikit-learn).  
- **Visualization**:  
  - **Matplotlib/Seaborn**: Static charts (line, bar, heatmap).  
  - **Plotly**: Interactive charts (scatter, radar, maps).  
  - **Plotly Dash**: For creating an interactive dashboard.  
- **Statistical Methods**: Regression analysis, clustering (K-means), correlation analysis.  

---

## 5. Deliverables  
- **Cleaned Dataset**: `cleaned_mobile_data.csv` (standardized fields, numeric prices, categorized processors).  
- **Summary Report**: Key findings on trends, brand comparisons, and pricing strategies.  
- **Interactive Dashboard**:  
  - Built with **Plotly Dash** for dynamic filtering (year, brand, price tier).  
  - Includes line charts, heatmaps, radar charts, and maps.  
- **Recommendations**: Strategic insights for product development, pricing, and market positioning.  

---

## 6. Timeline  

| **Phase**               | **Duration (Days)** |  
|-------------------------|---------------------|  
| Data Cleaning           | 2                   |  
| Exploratory Analysis    | 3                   |  
| In-depth Analysis       | 6                   |  
| Dashboard Development   | 2                   |  
| Final Report            | 1                   |  
| **Total**               | **14 days**         |  

---

## 7. Additional Considerations  
- **Currency Conversion**: Use historical exchange rates (e.g., OANDA API).  
- **Data Limitations**: Ensure global market representation (coverage of all brands/regions).  
- **Ethical Considerations**: Address missing data to avoid biased clustering/comparisons.  

---
