**Bài tập: Quy trình Đặt xe công nghệ (Ride-Hailing Flow - Grab/Be)**

**• Phân làn đề xuất (3 Swimlanes):** Hành khách | Hệ thống Ứng dụng | Tài xế

**• Mô tả nghiệp vụ:**

1. **Hành khách** bắt đầu bằng việc nhập điểm đón, điểm đến, chọn loại xe và bấm "Đặt xe".
2. **Hệ thống** tiếp nhận, tạo mã chuyến đi và "Gửi yêu cầu nhận cuốc" đến Tài xế gần nhất.
3. **Tài xế** nhận được yêu cầu và đưa ra quyết định:
* Nếu `[Từ chối hoặc Bỏ qua]`: Hệ thống đếm số lần quét. Nếu `[Dưới 3 lần]`, hệ thống quay lại bước "Gửi yêu cầu nhận cuốc" cho một tài xế khác. Nếu `[Từ 3 lần trở lên]`, hệ thống hiển thị thông báo "Không tìm thấy tài xế" cho Hành khách và kết thúc quy trình.
* Nếu `[Chấp nhận]`: Hệ thống hiển thị thông tin tài xế cho Hành khách chờ.


4. **Tài xế** di chuyển đến đón, bấm "Bắt đầu chuyến" và lái xe đến đích.
5. Khi đến nơi, **Tài xế** bấm "Kết thúc chuyến đi".
6. Ngay sau thao tác này, **Hệ thống** bắt buộc kích hoạt đồng thời 2 tiến trình:
* Luồng 1 (Hệ thống): Xử lý thanh toán chuyến đi và lưu lịch sử cuốc xe vào cơ sở dữ liệu.
* Luồng 2 (Hành khách): Hiển thị màn hình đánh giá sao, Hành khách thực hiện "Đánh giá tài xế".


7. Chỉ khi tiến trình thanh toán chạy ngầm xong VÀ Hành khách đã gửi đánh giá (hoặc bấm bỏ qua), hệ thống mới chốt lại bằng thông báo "Cảm ơn" và kết thúc quy trình.

**• Yêu cầu kỹ thuật cốt lõi (Kiểm tra tư duy logic):**

* Xử lý vòng lặp tìm tài xế bằng **Merge Node** chuẩn xác (tuyệt đối không cắm mũi tên quay lui trực tiếp vào Action).
* Sử dụng 2 khối **Decision Node** để tách bạch việc Tài xế từ chối và Hệ thống đếm số lần tìm kiếm.
* Cặp **Fork/Join** ở Bước 6 phải bao quát được sự tương tác chéo giữa Hệ thống chạy ngầm và thao tác bấm trên màn hình của Hành khách.
