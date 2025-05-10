# Phân loại thu nhập từ Census Adult Income Dataset

Dự án này sử dụng **bộ dữ liệu Census Adult Income** (nguồn từ Hoa Kỳ) để giải quyết bài toán **phân loại thu nhập cá nhân** thành hai nhóm: *trên 50K* và *dưới hoặc bằng 50K* USD/năm.

## 📊 Mục tiêu

Xây dựng mô hình học máy có khả năng **phát hiện càng nhiều người có thu nhập cao càng tốt**, nghĩa là **ưu tiên tối đa hóa recall**, đồng thời **duy trì sự cân bằng với precision thông qua tối ưu F1-score** và **AUC**.

---

## ⚙️ Tiền xử lý dữ liệu

Quá trình tiền xử lý bao gồm nhiều bước quan trọng:

- **Xử lý missing values** bằng phương pháp dựa trên Decision Tree.
- **Biến đổi và mã hóa các đặc trưng (features)** để phù hợp cho bài toán phân loại.
- **Giảm chiều dữ liệu** để tăng tốc độ huấn luyện và giảm nhiễu.

---

## 🤖 Các mô hình được thử nghiệm

Nhiều thuật toán phân loại đã được triển khai và so sánh hiệu suất:

- Decision Tree (CART)
- Random Forest
- Naive Bayes
- Support Vector Machine (SVM)
- Multi-Layer Perceptron (MLP)

Từng mô hình được đánh giá dựa trên:
- **Recall**: để đảm bảo phát hiện đúng nhiều người thu nhập cao.
- **F1-score**: để cân bằng giữa recall và precision.
- **AUC**: đo lường độ phân biệt giữa hai lớp.
- **Thời gian huấn luyện và suy luận (inference)**: để xét đến khả năng mở rộng và ứng dụng thực tế.

---

## ✅ Kết quả & Lựa chọn mô hình tối ưu

Dựa trên mục tiêu của bài toán, **Naive Bayes là mô hình tối ưu nhất** với các lý do sau:

- 🎯 **Recall cao nhất**: 0.491 — phát hiện tốt nhất nhóm thu nhập cao.
- 🏆 **F1-score cao nhất**: 0.430 — cân bằng tốt giữa recall và precision.
- 📈 **AUC đạt**: 0.784 — mô hình có khả năng phân biệt hai lớp khá tốt.
- ⚡️ **Thời gian huấn luyện và inference rất nhanh** — phù hợp cho các ứng dụng yêu cầu thời gian thực hoặc xử lý dữ liệu lớn.
