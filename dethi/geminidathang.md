**Bài tập: Quy trình Xử lý Đơn hàng Thương mại điện tử**

**• Mô tả nghiệp vụ:**

1. **Khách hàng** bắt đầu quy trình bằng hành động "Chọn sản phẩm và Đặt hàng".
2. **Hệ thống** kiểm tra số lượng tồn kho của sản phẩm:
* Nếu điều kiện là `[Hết hàng]`: Hệ thống hiển thị thông báo lỗi và yêu cầu Khách hàng quay lại bước chọn sản phẩm ban đầu.
* Nếu điều kiện là `[Còn hàng]`: Hệ thống tạo mã đơn và yêu cầu Khách hàng "Thực hiện thanh toán".


3. **Hệ thống** xử lý giao dịch thanh toán:
* Nếu `[Thất bại]`: Hệ thống tự động "Hủy đơn hàng" và kết thúc quy trình.
* Nếu `[Thành công]`: Hệ thống bắt buộc kích hoạt **đồng thời** 2 tiến trình sau:
* Luồng 1 (Hệ thống): Xuất hóa đơn điện tử và gửi Email xác nhận cho Khách hàng.
* Luồng 2 (Bộ phận Kho): Nhận phiếu xuất kho và tiến hành đóng gói sản phẩm.




4. Sau khi cả việc gửi Email và Đóng gói đều đã hoàn tất, **Bộ phận Kho** thực hiện "Bàn giao hàng cho đơn vị vận chuyển".
5. **Hệ thống** "Cập nhật trạng thái Đang giao" lên ứng dụng và kết thúc quy trình.

**• Yêu cầu thực hiện (Tương tự đề thi thực tế):**

* Khởi tạo đúng 3 Swimlanes: **Khách hàng**, **Hệ thống**, **Bộ phận Kho**.
* Đặt **Initial Node** và **Activity Final Node** ở đúng cột đảm nhiệm hành động.
* Sử dụng **Decision Node** kèm điều kiện `[ ]` cho các bước kiểm tra tồn kho và thanh toán.
* Bắt buộc dùng **Merge Node** để đón luồng lặp khi khách hàng chọn lại sản phẩm (không cắm thẳng mũi tên vào khối hành động).
* Bắt buộc dùng cặp **Fork Node** và **Join Node** để tách - gộp 2 luồng công việc song song sau khi thanh toán thành công.
