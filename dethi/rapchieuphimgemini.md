**Bài tập 1.3: Quy trình Đặt vé xem phim trực tuyến**

**• Mô tả nghiệp vụ:**

1. Khách hàng chọn suất chiếu, chọn ghế trên ứng dụng và bấm "Xác nhận".
2. Hệ thống Ứng dụng kiểm tra trạng thái ghế:

* Nếu `[Ghế đã bị đặt]`: Hiển thị thông báo lỗi và yêu cầu Khách hàng quay lại màn hình chọn ghế.
* Nếu `[Ghế hợp lệ]`: Chuyển sang màn hình thanh toán và yêu cầu Khách hàng thực hiện thanh toán.

3. Khách hàng nhập thông tin thẻ và nhập mã OTP.
4. Hệ thống Ngân hàng tiến hành xác thực giao dịch:

* Nếu OTP `[Sai]`: Cho phép Khách hàng nhập lại (tối đa 3 lần). Nếu sai `[Quá 3 lần]`, hủy giao dịch, giải phóng ghế và kết thúc luồng.
* Nếu OTP `[Đúng]`: Thực hiện trừ tiền trong tài khoản thành công.

5. Xử lý kết quả giao dịch thành công:

* Ngay sau khi trừ tiền, Hệ thống Ứng dụng bắt buộc thực hiện **đồng thời** 2 tiến trình:
* Gửi vé điện tử (QR Code) vào Email của Khách hàng.
* Cập nhật trạng thái ghế thành "Đã bán" lên Cơ sở dữ liệu rạp.
* Sau khi cả hai tiến trình trên hoàn tất, ứng dụng hiển thị màn hình "Đặt vé thành công" cho Khách hàng và kết thúc quy trình.

**• Yêu cầu thực hiện:**

* Phân chia đúng 3 Swimlanes: **Khách hàng**, **Hệ thống Ứng dụng**, **Hệ thống Ngân hàng**.
* Sử dụng đúng ký hiệu Initial Node và Activity Final Node.
* Thể hiện rõ các điểm rẽ nhánh (Decision) kèm điều kiện bảo vệ (Guard Condition) trong ngoặc vuông `[ ]`.
* Bắt buộc sử dụng **Merge Node** khi xử lý 2 luồng lặp: Khách hàng chọn lại ghế và Khách hàng nhập lại mã OTP.
* Bắt buộc sử dụng cặp **Fork / Join** cho các tác vụ đồng thời ở Bước 5.
