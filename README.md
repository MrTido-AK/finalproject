# Mobile Dataset Analysis: Insights and Strategy  
**Prepared for Hien Hoang/ DA-course**  

## Table of Contents  
1. [Introduction & Objectives](#introduction-objectives)  
2. [Data Overview & Cleaning Plan](#data-overview-cleaning-plan)  
3. [Proposed Analyses](#proposed-analyses)  
4. [Tools & Methods](#tools-methods)  
5. [Deliverables](#deliverables)  
6. [Setup & Usage](#setup-usage)  
7. [Example Visualizations](#example-visualizations)  

---

## 1. Introduction & Objectives  
**Goal**: Extract actionable insights from the **Mobiles Dataset (2025)** to inform decision-making for market positioning, pricing strategy, and product development.  

**Key Objectives**:  
- **Market Trends**: Track evolution of RAM, battery size, and price over time.  
- **Competitive Analysis**: Compare brands like Realme, POCO, and Oppo.  
- **Customer Value Drivers**: Identify features (RAM, camera quality) that drive price.  
- **Regional Pricing Strategy**: Analyze price variations across currencies.  
- **Product Segmentation**: Classify devices into budget, mid-range, and flagship.  

---

## 2. Data Overview & Cleaning Plan  
### **Data Structure**  
- **Fields**: Brand, Model, Storage, Weight, RAM, Front/Back Camera, Processor, Battery, Screen Size, Prices (PKR/INR/USD/AED), Release Year.  
- **Sample Size**: ~200+ entries (2020–2025).  

### **Cleaning Challenges**  
- **Formatting**:  
  - Split camera specs (e.g., "50MP + 2MP" → Primary/Secondary).  
  - Normalize prices (e.g., "PKR 99,999" → 99999 USD).  
  - Extract release years from strings (e.g., "2020POCO,M2 Pro..." → 2020).  
- **Standardization**:  
  - Normalize processor names (e.g., "Snapdragon 8 Gen 2" → High-tier).  
  - Handle missing data (battery capacity, camera details).  

---

## 3. Proposed Analyses  
### **3.1 Market Trends Over Time**  
- **Analysis**: Track RAM, battery size, and price trends.  
- **Visualization**:  
  - **Line chart** (Matplotlib): RAM trung bình theo năm.  
  - **Bar chart** (Seaborn): Giá trung bình theo năm.  

### **3.2 Brand Comparison**  
- **Analysis**: So sánh giá, cấu hình giữa các thương hiệu.  
- **Visualization**:  
  - **Heatmap** (Seaborn): So sánh RAM, pin, và giá giữa các thương hiệu.  
  - **Radar chart** (Plotly): Đánh giá đa chỉ số (RAM, pin, camera).  

### **3.3 Feature-Price Relationship**  
- **Analysis**: Xác định tính năng ảnh hưởng đến giá.  
- **Visualization**:  
  - **Correlation matrix** (Seaborn): Tương quan giữa RAM, camera, và giá.  
  - **Scatter plot** (Plotly): Giá vs. RAM/camera.  

### **3.4 Regional Pricing Strategy**  
- **Analysis**: So sánh giá USD theo khu vực.  
- **Visualization**:  
  - **World map** (Plotly): Giá trung bình theo quốc gia.  
  - **Scatter plot** (Matplotlib): Giá USD vs. PKR/INR.  

### **3.5 Processor & Hardware Trends**  
- **Analysis**: Phân tích xu hướng chip và dung lượng pin.  
- **Visualization**: **Bar chart** (Matplotlib): Tỷ lệ chip high/mid/low theo phân khúc giá.  

### **3.6 Camera Evolution**  
- **Analysis**: So sánh độ phân giải camera theo năm.  
- **Visualization**: **Line chart** (Matplotlib): Độ phân giải camera trung bình theo năm.  

---

## 4. Tools & Methods  
- **Programming**: Python (Pandas, NumPy, Matplotlib, Seaborn, Plotly, Scikit-learn).  
- **Visualization**:  
  - **Matplotlib/Seaborn**: Biểu đồ tĩnh.  
  - **Plotly**: Biểu đồ tương tác.  
  - **Dash/Streamlit**: Dashboard trực quan.  
- **Statistical Methods**: Phân tích hồi quy, clustering, phân tích tương quan.  

---

## 5. Deliverables  
1. **Cleaned Dataset**: CSV với dữ liệu chuẩn hóa (giá USD, phân loại chip).  
2. **Summary Report**: Báo cáo xu hướng, so sánh thương hiệu, chiến lược giá.  
3. **Interactive Dashboard**:  
   - **Công cụ**: Plotly Dash hoặc Streamlit.  
   - **Ví dụ**: Dashboard cho phép lọc theo năm, thương hiệu, hoặc tính năng.  
4. **Recommendations**: Đề xuất chiến lược dựa trên phân tích.
    
---

## 6. Timeline  
| **Phase**               | **Duration** |  
|-------------------------|--------------|  
| Data Cleaning           | 2 days       |  
| Exploratory Analysis    | 3 days       |  
| In-depth Analysis       | 5 days       |  
| Dashboard Development   | 2 days       |  
| Final Report            | 1 day        |  

---

## 7. Setup & Usage  
### **Dependencies**  
```bash
pip install pandas numpy matplotlib seaborn scikit-learn forex-python plotly

# Workflow
## 1. Data Cleaning (Xử lý dữ liệu)  
**File**: `clean_data.py`  
**Công việc**:  
- Xử lý dữ liệu thô (raw data) để chuẩn hóa định dạng.  
- Tách thông số camera thành hai giá trị riêng biệt (primary và secondary).  
- Chuyển đổi giá tiền từ chuỗi có ký hiệu tiền tệ sang số liệu định lượng (ví dụ: "PKR 99,999" → 99999 USD).  
- Tách năm phát hành từ tên cột hoặc chuỗi cuối cùng của mỗi dòng.  
**Kết quả đầu ra**:  
- Tệp `cleaned_mobile_data.csv` chứa dữ liệu đã làm sạch, chuẩn hóa và sẵn sàng cho phân tích.  

---

## 2. Exploratory Analysis (Phân tích khám phá)  
**File**: `exploratory_analysis.ipynb`  
**Công việc**:  
- Vẽ các biểu đồ xu hướng (line charts) để theo dõi sự thay đổi của RAM, dung lượng pin, kích thước màn hình và giá theo năm.  
- Tạo heatmap để phân tích tương quan giữa các đặc tính (RAM, camera, dung lượng pin) và giá cả.  
- Sử dụng radar chart để so sánh hiệu năng giữa các thương hiệu (ví dụ: Realme, POCO, Oppo) dựa trên RAM, dung lượng pin và giá.  
- Phân tích tương quan thống kê giữa các tính năng kỹ thuật và giá thành sản phẩm.  
**Kết quả đầu ra**:  
- Các biểu đồ trực quan (line chart, heatmap, radar chart).  
- Ma trận tương quan giữa các đặc tính và giá.  
- Insights ban đầu về xu hướng thị trường và mối liên hệ giữa tính năng và giá.  

---

## 3. In-depth Analysis (Phân tích sâu)  
**File**: `clustering_analysis.ipynb`  
**Công việc**:  
- Áp dụng mô hình **K-means clustering** để phân loại thiết bị thành các nhóm "best value" (thiết bị có tính năng cao nhưng giá thấp).  
- Xây dựng mô hình **hồi quy tuyến tính** để xác định các tính năng (RAM, độ phân giải camera, dung lượng pin) có ảnh hưởng mạnh đến giá bán.  
- Đánh giá độ chính xác và giải thích kết quả của mô hình.  
**Kết quả đầu ra**:  
- Kết quả phân nhóm (clusters) của các thiết bị theo giá trị.  
- Báo cáo kết quả hồi quy, chỉ số hệ số hồi quy.  
- Đề xuất chiến lược dựa trên các tính năng ảnh hưởng đến giá.  

---

## 4. Dashboard Development (Xây dựng dashboard)  
**File**: `dashboard.py`  
**Công việc**:  
- Tạo dashboard tương tác sử dụng thư viện **Plotly/Dash**.  
- Bao gồm các thành phần:  
  - Biểu đồ line chart để theo dõi xu hướng giá theo năm.  
  - Heatmap tương quan giữa các tính năng.  
  - Radar chart so sánh hiệu năng thương hiệu.  
  - Bảng điều khiển cho phép lọc dữ liệu theo năm, thương hiệu, hoặc phân khúc giá.  
- Tối ưu giao diện người dùng (UI) để dễ dàng thao tác và trình bày.  
**Kết quả đầu ra**:  
- Ứng dụng dashboard trực quan (file HTML hoặc web app) cho phép phân tích dữ liệu linh hoạt và tương tác.  

---
 
