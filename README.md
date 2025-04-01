# 📘 DATA ANALYTICS PROPOSAL

**Dự án:** Phân tích và dự đoán xu hướng bán hàng ngành hàng điện tử tiêu dùng  
**Dữ liệu đầu vào:** `consumer_electronics_sales_data.csv` – 9,000 bản ghi, 9 biến số

---

## I. 🎯 MỤC TIÊU DỰ ÁN

- Hiểu hành vi khách hàng và hiệu suất bán hàng theo danh mục, thương hiệu
- Trực quan hóa các yếu tố ảnh hưởng đến hành vi mua hàng
- Dự đoán ý định mua và dự báo doanh thu trong tương lai
- Phân khúc khách hàng để cá nhân hóa chiến lược marketing
- Xây dựng hệ thống phân tích hỗ trợ ra quyết định kinh doanh

---

## II. 📊 TỔNG QUAN DỮ LIỆU

- **Số dòng:** 9,000 | **Số cột:** 9
- Không có giá trị bị thiếu
- Các biến gồm: danh mục, thương hiệu, giá, độ tuổi, giới tính, tần suất mua, mức độ hài lòng, ý định mua hàng

---

## III. 🛠️ QUY TRÌNH ETL

- **Extract**: Đọc dữ liệu từ CSV, loại trùng, kiểm tra dữ liệu bất thường
- **Transform**: Xử lý định dạng dữ liệu, tạo biến mới (feature engineering), phân nhóm, mã hóa
- **Load**: Lưu dữ liệu sạch vào file `.csv` hoặc `.parquet` để phục vụ phân tích và modeling

---

## IV. 📈 PHÂN TÍCH MÔ TẢ (DESCRIPTIVE ANALYSIS)

### A. Phân tích cơ bản

1. Top 5 thương hiệu và danh mục bán chạy
2. Phân bố độ tuổi và giới tính khách hàng
3. Tương quan giữa giá – độ tuổi – mức độ hài lòng

### B. Phân tích mở rộng

4. Doanh thu trung bình theo thương hiệu / danh mục  
5. Hành vi khách hàng theo nhóm tuổi và giới tính  
6. Mối quan hệ giữa mức độ hài lòng và tần suất mua  
7. Phân tích ý định mua hàng theo thương hiệu  
8. Phân khúc khách hàng theo hành vi tiêu dùng  
9. So sánh hành vi mua hàng giữa nam và nữ  
10. Mối liên hệ giữa giá cao và mức độ hài lòng  
11. Top sản phẩm có tỷ lệ ý định mua cao nhất

---

## V. 🧠 PHÂN TÍCH DỰ ĐOÁN (PREDICTIVE ANALYSIS)

- **Mục tiêu:** Dự đoán hành vi hoặc kết quả tương lai dựa trên dữ liệu quá khứ

### ✔ Dự đoán ý định mua hàng (Purchase Intent)

- Mô hình phân loại: Logistic Regression, Random Forest, XGBoost
- Tối ưu tham số bằng GridSearchCV
- Xác định yếu tố ảnh hưởng lớn đến khả năng mua hàng

### ✔ Phân loại khách hàng có khả năng mua cao

- Chia nhóm khách hàng để nhắm lại quảng cáo (remarketing)

---

## VI. 🔮 PHÂN TÍCH DỰ BÁO (FORECASTING ANALYSIS)

- **Mục tiêu:** Dự báo giá trị tương lai như doanh thu, tần suất mua

### ✔ Dự báo doanh thu / lượt mua

- Mô hình: ARIMA, Prophet, Linear Regression
- Dự báo theo thương hiệu, danh mục hoặc toàn bộ

### ✔ Phân tích xu hướng thị trường

- Nhận diện thương hiệu/sản phẩm đang tăng hoặc giảm sức mua

---

## VII. 🧩 PHÂN KHÚC KHÁCH HÀNG (CUSTOMER SEGMENTATION)

- **Mục tiêu:** Nhóm khách hàng theo hành vi và tiềm năng

### ✔ Clustering (K-Means, DBSCAN)

- Dựa vào: độ tuổi, giới tính, tần suất mua, chi tiêu, hài lòng...

### ✔ Xác định nhóm khách hàng:

- "VIP" – giá trị cao và trung thành  
- "Tiềm năng" – sẵn sàng mua thêm  
- "Rủi ro" – cần tái kích hoạt

---

## VIII. 💵 PHÂN TÍCH GIÁ TRỊ KHÁCH HÀNG (CUSTOMER VALUE ANALYSIS)

### ✔ CLV (Customer Lifetime Value)

- Dự báo tổng giá trị một khách hàng mang lại trong vòng đời

### ✔ RFM Analysis (Recency – Frequency – Monetary)

- Phân tích hành vi mua hàng để phân khúc khách hàng theo giá trị tài chính

---

## IX. 🔁 PHÂN TÍCH LẶP LẠI – RỜI BỎ (CHURN & RETENTION)

- **Mục tiêu:** Dự đoán khả năng khách hàng quay lại hoặc bỏ đi

### ✔ Churn Prediction

- Xác định nhóm khách có rủi ro không quay lại
- Hỗ trợ ra quyết định tái tiếp thị

### ✔ Retention Analysis

- Tìm nhóm khách hàng trung thành – hỗ trợ tạo loyalty program

---

## X. 📅 TIMELINE 21 NGÀY LÀM VIỆC

| Ngày      | Công việc                                                                 |
|-----------|---------------------------------------------------------------------------|
| 1–2       | Khám phá dữ liệu ban đầu, kiểm tra chất lượng dữ liệu                     |
| 3–4       | Làm sạch dữ liệu, xử lý trùng lặp, kiểm tra outliers                      |
| 5–6       | Chuyển đổi dữ liệu, mã hóa, chuẩn hóa dữ liệu (ETL - Transform)           |
| 7         | Feature engineering (biến mới từ độ tuổi, phân nhóm giá, điểm hài lòng…)  |
| 8–9       | Phân tích mô tả cơ bản + trực quan hóa (Top thương hiệu, độ tuổi, v.v.)   |
| 10        | Phân tích mở rộng (ý định mua, mức độ hài lòng, phân khúc giới tính)      |
| 11–12     | Xây dựng mô hình phân loại dự đoán ý định mua (Purchase Intent)           |
| 13        | Đánh giá mô hình phân loại (Confusion Matrix, ROC, AUC, v.v.)             |
| 14        | Dự báo doanh thu / lượt mua tương lai (Forecast: ARIMA / Linear)          |
| 15        | Phân tích xu hướng thị trường (Brand / Category lên – xuống)              |
| 16        | Phân khúc khách hàng bằng K-Means hoặc DBSCAN                             |
| 17        | Phân tích giá trị khách hàng: CLV + RFM                                   |
| 18        | Dự đoán churn (khách rời bỏ) + phân tích khách trung thành                |
| 19        | Soát xét, tinh chỉnh các mô hình và biểu đồ quan trọng                    |
| 20        | Tổng hợp báo cáo, xây dựng dashboard                                      |
| 21        | Demo                                                                      |

---

## XI. 🧾 KẾT QUẢ DỰ KIẾN

- Bộ mô hình dự đoán ý định mua chính xác > 80%
- Phân khúc khách hàng theo hành vi và giá trị
- Dự báo xu hướng mua hàng theo thương hiệu và sản phẩm
- Đề xuất chiến lược tăng doanh thu và giữ chân khách hàng
- Dashboard trực quan
"""
