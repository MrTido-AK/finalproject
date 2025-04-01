# 📊 Đề xuất Phân tích & Trực quan hóa Dữ liệu Mobile Dataset (2025)

---

## 1. 🎯 Mục tiêu

Phân tích dữ liệu các mẫu điện thoại nhằm:

- So sánh giá và thông số kỹ thuật giữa các hãng.
- Hiểu xu hướng thị trường theo năm, khu vực.
- Dự đoán giá bán trong tương lai dựa trên các đặc điểm kỹ thuật.

---

## 2. 🚀 Các bước phân tích đề xuất

### 🔍 Tiền xử lý dữ liệu

- Chuyển đổi các cột giá (PKR, INR, USD, v.v.) thành định dạng số.
- Chuyển đổi thông số kỹ thuật (RAM, Camera, Battery, Weight) về định dạng số.
- Chuẩn hóa các đơn vị (GB, MP, mAh, inches...).
- Xử lý dữ liệu trùng lặp (nếu có).

---

### 📈 Phân tích mô tả (Exploratory Data Analysis)

- Số lượng mẫu theo hãng (`Company Name`).
- Phân phối giá theo từng quốc gia.
- Phân tích xu hướng cấu hình (RAM, Camera, Battery) theo năm.
- Top mẫu điện thoại có dung lượng pin, RAM, camera lớn nhất.

---

### 🧠 Phân tích mối quan hệ & trực quan hóa

- **Biểu đồ scatter**: Giá vs RAM, Camera, Battery.
- **Heatmap tương quan**: giữa các thông số và giá.
- **Boxplot**: Phân tích giá theo hãng.
- **Bar chart**: So sánh giá trung bình theo quốc gia.

---

### 🔮 Dự đoán giá (Forecasting & Predictive Modeling)

**Mục tiêu**: Dự đoán "Launched Price (USD)" dựa trên:

- RAM
- Camera
- Battery
- Screen Size
- Company Name

**Các mô hình có thể dùng**:

- Linear Regression
- Random Forest Regressor
- XGBoost

**Đánh giá mô hình bằng**: MAE, RMSE

---

## 3. ✅ Kết quả kỳ vọng

- Dashboard trực quan để so sánh điện thoại.
- Báo cáo phân tích xu hướng thị trường điện thoại.
- Mô hình dự đoán giá điện thoại mới dựa trên cấu hình.

---

## 🔧 ETL Pipeline & Timeline (Tổng cộng: 15 ngày)

---

### 🟢 Giai đoạn 1: Extract – Trích xuất dữ liệu

**Mục tiêu**: Đọc và thu thập dữ liệu từ file đầu vào.

| Bước | Mô tả | Công cụ |
|------|------|--------|
| 1.1 | Đọc file CSV với encoding phù hợp | `pandas.read_csv()` |
| 1.2 | Kiểm tra sơ bộ dữ liệu: số dòng, cột, kiểu dữ liệu | `df.info()`, `df.describe()` |
| 1.3 | Xác định các cột cần phân tích và chuẩn hóa | Manual Review |

⏱ Thời gian: **1 ngày**

---

### 🟡 Giai đoạn 2: Transform – Làm sạch & xử lý dữ liệu

**Mục tiêu**: Chuẩn hóa, làm sạch và xử lý các cột định dạng sai.

| Bước | Mô tả | Công cụ |
|------|------|--------|
| 2.1 | Xử lý dữ liệu thiếu, trùng lặp | `dropna()`, `drop_duplicates()` |
| 2.2 | Tách và chuyển đổi các cột định dạng text (RAM, Camera, Battery, Weight) thành số | Regex, String methods |
| 2.3 | Chuyển đổi các cột giá (USD, INR, PKR...) từ dạng `"USD 799"` → `799` | Regex, `.str.replace()` |
| 2.4 | Đưa về một đơn vị chung nếu cần (vd: chỉ giữ lại giá USD) | Logic business |
| 2.5 | Encoding các giá trị phân loại nếu cần (vd: `Company Name`) | Label Encoding / One-Hot |

⏱ Thời gian: **4 ngày**

---

### 🔵 Giai đoạn 3: Load – Phân tích & trực quan hóa

**Mục tiêu**: Phân tích mô tả và trực quan hóa dữ liệu đã làm sạch.

| Bước | Mô tả | Công cụ |
|------|------|--------|
| 3.1 | EDA: thống kê mô tả, phân phối, giá trung bình theo hãng | `pandas`, `matplotlib`, `seaborn` |
| 3.2 | Biểu đồ: bar chart, scatter, boxplot, heatmap | `matplotlib.pyplot` |
| 3.3 | Dashboard tạm thời (nếu cần) bằng Jupyter | Markdown + Code |

⏱ Thời gian: **4 ngày**

---

### 🟣 Giai đoạn 4: Forecast – Mô hình dự đoán giá

**Mục tiêu**: Xây dựng mô hình ML để dự đoán giá bán điện thoại.

| Bước | Mô tả | Công cụ |
|------|------|--------|
| 4.1 | Tạo tập train/test | `train_test_split()` |
| 4.2 | Xây dựng mô hình hồi quy | Linear Regression, Random Forest, XGBoost |
| 4.3 | Đánh giá mô hình | MAE, RMSE |
| 4.4 | Dự đoán thử mẫu mới và so sánh thực tế |

⏱ Thời gian: **4 ngày**

---

### 📦 Giai đoạn 5: Tổng hợp & Báo cáo

**Mục tiêu**: Xuất kết quả, tạo báo cáo, trình bày dashboard.

| Bước | Mô tả | Công cụ |
|------|------|--------|
| 5.1 | Xuất file CSV kết quả, bảng tổng hợp | `pandas.to_csv()` |
| 5.2 | Tạo dashboard demo nếu cần | Streamlit / Power BI |

⏱ Thời gian: **2 ngày**

---

## 🧮 Tổng thời gian: **15 ngày làm việc**

