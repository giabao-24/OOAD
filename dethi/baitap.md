
Dưới đây là **Bộ 5 câu hỏi luyện tập mức độ dễ** và **2 Bộ đề thi mẫu hoàn chỉnh (chuẩn cấu trúc 4 câu tự luận 120 phút như Đề thi KTHP 2018-2019)**, đi kèm **Phần Đáp án & Hướng dẫn Giải Chi tiết** ở cuối.

---

# PHẦN 1: BỘ 5 CÂU HỎI LUYỆN TẬP MỨC ĐỘ DỄ (KHỞI ĐỘNG)

### **Câu 1 (Khái niệm OOAD & UML)**

Phân biệt sự khác nhau cơ bản giữa giai đoạn **Phân tích (Analysis - OOA)** và **Thiết kế (Design - OOD)** trong phát triển hệ thống hướng đối tượng. Hai câu hỏi cốt lõi mà hai giai đoạn này lần lượt trả lời là gì?

### **Câu 2 (Quan hệ trong Biểu đồ Use Case)**

Trong Biểu đồ Use Case, khi nào ta sử dụng quan hệ `<<include>>` và khi nào sử dụng quan hệ `<<extend>>`? Cho một ví dụ thực tế minh họa cho mỗi loại quan hệ.

### **Câu 3 (Stereotype trong Phân tích)**

Trình bày 3 stereotype lớp cơ bản trong pha phân tích hướng đối tượng (Boundary, Control, Entity). Cho biết vai trò của từng stereotype khi xử lý chức năng *"Đăng nhập hệ thống"*.

### **Câu 4 (Trích xuất Lớp thực thể)**

Cho đoạn mô tả ngắn: *"Một Khách hàng có thể đặt nhiều Đơn hàng. Mỗi Đơn hàng chứa nhiều Sản phẩm. Nhân viên bán hàng sẽ lập Hóa đơn thanh toán cho Đơn hàng đó."*
Hãy xác định các **Lớp thực thể (Entity Classes)** ứng cử viên và chỉ ra **Thuộc tính cơ bản** cho từng lớp.

### **Câu 5 (Quy tắc ánh xạ Class Diagram sang CSDL Quan hệ)**

Nêu quy tắc chuyển đổi một mối quan hệ **1 - N (Một - Nhiều)** và mối quan hệ **N - N (Nhiều - Nhiều)** từ Biểu đồ Lớp sang Lược đồ Cơ sở dữ liệu quan hệ (xác định Khóa chính PK và Khóa ngoại FK).

---

# PHẦN 2: 2 BỘ ĐỀ THI MẪU HOÀN CHỈNH (CHUẨN ĐỀ THI THẬT 120 PHÚT)

---

## 📝 BỘ ĐỀ THI SỐ 1

**Môn thi:** Phân tích và Thiết kế Hệ thống Thông tin (TIN3093)
**Thời gian làm bài:** 120 phút (Được sử dụng tài liệu)

### NỘI DUNG BÀI TOÁN: HỆ THỐNG QUẢN LÝ MƯỢN TRẢ SÁCH VÀ TÀI LIỆU TRỰC TUYẾN

Nhằm nâng cao chất lượng phục vụ, Thư viện Đại học xây dựng hệ thống quản lý mượn trả sách trực tuyến:

* **Thủ thư** quản lý danh mục Sách (Mã sách, Tên sách, Tác giả, Năm xuất bản, Số lượng bản sao) và thông tin Độc giả (Mã độc giả, Họ tên, Email, Số điện thoại, Loại độc giả: Sinh viên/Giảng viên).
* **Độc giả** tạo tài khoản trực tuyến và gửi yêu cầu kích hoạt cho Thủ thư. Sau khi được duyệt tài khoản, Độc giả đăng nhập để: (1) Tìm kiếm sách, (2) Đặt mượn sách trước qua mạng, (3) Xem lịch sử mượn sách và số tiền phạt (nếu có).
* Mỗi lần mượn, Độc giả tạo một **Phiếu mượn** (chứa tối đa 3 quyển sách cho sinh viên, 5 quyển cho giảng viên). Hệ thống lưu ngày mượn và ngày hẹn trả.
* Khi Độc giả đến thư viện nhận sách, Thủ thư xác nhận giao sách và chuyển trạng thái Phiếu mượn thành "Đang mượn".
* Khi trả sách, Thủ thư kiểm tra sách. Nếu trả quá hạn hoặc làm hư hỏng, hệ thống tự động tính **Tiền phạt** và lưu vào **Phiếu phạt** để Độc giả thanh toán.

### YÊU CẦU:

* **Câu 1 (2.5 điểm):** Vẽ biểu đồ lớp mô tả mô hình miền (Domain Model). Mô tả ngắn gọn các lớp và giải thích các mối quan hệ (kèm bội số).
* **Câu 2 (2.5 điểm):** Vẽ biểu đồ Use Case mô tả các chức năng của hệ thống. Mô tả ngắn gọn từng Actor và Use Case.
* **Câu 3 (2.5 điểm):** Viết tài liệu đặc tả Use Case chi tiết cho chức năng *"Đánh dấu/Đặt mượn sách trực tuyến"*.
* **Câu 4 (2.5 điểm):** Thiết kế Cơ sở dữ liệu quan hệ (Vẽ lược đồ CSDL, chỉ rõ PK, FK và giải thích mối quan hệ giữa các bảng).

---

## 📝 BỘ ĐỀ THI SỐ 2

**Môn thi:** Phân tích và Thiết kế Hệ thống Thông tin (TIN3093)
**Thời gian làm bài:** 120 phút (Được sử dụng tài liệu)

### NỘI DUNG BÀI TOÁN: HỆ THỐNG ĐĂNG KÝ VÀ QUẢN LÝ ĐỀ TÀI NCKH SINH VIÊN

Trường Đại học triển khai phần mềm quản lý Nghiên cứu Khoa học (NCKH) của sinh viên:

* **Phòng Quản lý Khoa học (QLKH)** khởi tạo **Đợt đăng ký đề tài** (gồm Năm học, Kinh phí tối đa, Hạn nộp).
* **Sinh viên** (Trưởng nhóm) đăng ký tài khoản (Mã SV, Họ tên, Lớp, Email, SĐT) và được Trợ lý khoa duyệt tài khoản.
* Khi mở Đợt đăng ký, Sinh viên đăng nhập để: (1) Nộp **Thuyết minh đề tài** (Tên đề tài, Mục tiêu, Sản phẩm dự kiến, Kinh phí xin cấp), (2) Đăng ký Giảng viên hướng dẫn (GVHD).
* **Giảng viên hướng dẫn** đăng nhập để xem danh sách đề tài sinh viên mời và bấm "Đồng ý" hoặc "Từ chối" hướng dẫn.
* Sau khi GVHD đồng ý, đề tài chuyển sang trạng thái "Chờ duyệt". **Hội đồng khoa học** do Phòng QLKH thành lập sẽ đánh giá và chấm điểm thuyết minh.
* Nếu Đề tài đạt duyệt, hệ thống cấp Mã đề tài chính thức và kinh phí phê duyệt. Cuối kỳ, Sinh viên nộp Báo cáo tổng kết để Hội đồng chấm Báo cáo nghiệm thu và xuất Bảng điểm NCKH.

### YÊU CẦU:

* **Câu 1 (2.5 điểm):** Vẽ biểu đồ lớp mô tả mô hình miền (Domain Model). Mô tả ngắn gọn các lớp và giải thích mối quan hệ.
* **Câu 2 (2.5 điểm):** Vẽ biểu đồ Use Case mô tả các chức năng định thiết kế. Mô tả ngắn gọn các Actor và Use Case.
* **Câu 3 (2.5 điểm):** Viết tài liệu đặc tả Use Case chi tiết cho chức năng *"Đăng ký nộp Thuyết minh đề tài NCKH"*.
* **Câu 4 (2.5 điểm):** Thiết kế Cơ sở dữ liệu quan hệ (Lược đồ CSDL, chỉ rõ PK, FK và giải thích mối quan hệ).

---

# PHẦN 3: ĐÁP ÁN VÀ HƯỚNG DẪN GIẢI CHI TIẾT

---

## A. ĐÁP ÁN BỘ 5 CÂU HỎI MỨC ĐỘ DỄ

### **Đáp án Câu 1:**

* **Khác biệt cốt lõi**:
  * **Phân tích (OOA)**: Tập trung vào không gian bài toán (Problem Space). Trả lời câu hỏi **What** (Hệ thống cần làm gì để giải quyết yêu cầu người dùng).
  * **Thiết kế (OOD)**: Tập trung vào không gian giải pháp (Solution Space). Trả lời câu hỏi **How** (Hệ thống được cài đặt và tổ chức như thế nào trên công nghệ cụ thể).

### **Đáp án Câu 2:**

* **`<<include>>` (Bao hàm)**: Dùng khi ca sử dụng gốc **luôn luôn và bắt buộc** gọi ca sử dụng được bao hàm (chia sẻ luồng xử lý chung). *Ví dụ*: UC `Thanh toán đơn hàng` `<<include>>` UC `Xác thực tài khoản`.
* **`<<extend>>` (Mở rộng)**: Dùng khi ca sử dụng mở rộng chỉ thực thi **tùy ý/trong điều kiện ngoại lệ** để bổ sung chức năng cho ca sử dụng gốc. *Ví dụ*: UC `Áp mã giảm giá` `<<extend>>` UC `Thanh toán đơn hàng` (chỉ chạy khi người dùng có voucher).

### **Đáp án Câu 3:**

1. **Boundary Class (Lớp biên/giao diện)**: Trung gian tương tác giữa Actor và hệ thống. *Trong Đăng nhập*: `FormDangNhap` (hiển thị ô nhập Username/Password và nút Đăng nhập).
2. **Control Class (Lớp điều khiển)**: Điều phối logic nghiệp vụ. *Trong Đăng nhập*: `XuLyDangNhapController` (tiếp nhận thông tin từ Form, gọi Lớp thực thể để kiểm tra tài khoản và trả về kết quả).
3. **Entity Class (Lớp thực thể)**: Lưu trữ thông tin bền vững. *Trong Đăng nhập*: `TaiKhoan` hoặc `NguoiDung` (chứa Username, PasswordHash để so sánh).

### **Đáp án Câu 4:**

* Các Lớp thực thể ứng cử viên và Thuộc tính:
  1. `KhachHang` (`maKH`, `hoTen`, `soDienThoai`, `email`, `diaChi`)
  2. `DonHang` (`maDonHang`, `ngayDat`, `trangThai`, `tongTien`)
  3. `SanPham` (`maSP`, `tenSP`, `donGia`, `soLuongTon`)
  4. `HoaDon` (`maHoaDon`, `ngayLap`, `hinhThucThanhToan`, `tongTienThanhToan`)
  5. `NhanVien` (`maNV`, `hoTen`, `chucVu`)

### **Đáp án Câu 5:**

* **Quan hệ 1 - N**: Đưa Khóa chính (PK) của Bảng bên `1` sang làm Khóa ngoại (FK) ở Bảng bên `N`.
* **Quan hệ N - N**: Tạo một **Bảng trung gian (Junction Table)**. Khóa chính (PK) của Bảng trung gian là sự kết hợp của 2 Khóa ngoại (FK) tham chiếu tới Khóa chính của hai bảng ban đầu.

---

## B. ĐÁP ÁN BỘ ĐỀ THI SỐ 1 (QUẢN LÝ THƯ VIỆN SỐ)

### 💡 **Câu 1: Biểu đồ Lớp mô hình miền (Domain Model)**

1. **Các lớp thực thể**:

   * `DocGia`: `maDocGia`, `hoTen`, `email`, `soDienThoai`, `loaiDocGia`.
   * `TaiKhoanDocGia`: `tenDangNhap`, `matKhau`, `trangThaiDuyet`.
   * `ThuThu`: `maThuThu`, `hoTen`, `soDienThoai`.
   * `DauSach`: `maSach`, `tenSach`, `tacGia`, `namXB`, `soLuongBanSao`.
   * `PhieuMuon`: `maPhieu`, `ngayMuon`, `ngayHenTra`, `trangThai` (ChoDuyet/DangMuon/DaTra).
   * `ChiTietPhieuMuon`: `maPhieu`, `maSach`, `tinhTrangSachKhiMuon`.
   * `PhieuPhat`: `maPhieuPhat`, `soTienPhat`, `lyDoPhat`, `trangThaiThanhToan`.
2. **Mối quan hệ & Bội số**:

   * `DocGia` - `TaiKhoanDocGia`: **`1` - `0..1`** (Mỗi độc giả có 1 tài khoản).
   * `DocGia` - `PhieuMuon`: **`1` - `0..*`** (Một độc giả có thể tạo nhiều phiếu mượn).
   * `PhieuMuon` - `ChiTietPhieuMuon` - `DauSach`: `PhieuMuon` chứa nhiều `ChiTietPhieuMuon` (`1` - `1..*`), mỗi chi tiết ứng với 1 `DauSach` (`1` - `1`).
   * `ThuThu` - `PhieuMuon`: **`1` - `0..*`** (Thủ thư duyệt/xác nhận nhiều phiếu mượn).
   * `PhieuMuon` - `PhieuPhat`: **`1` - `0..1`** (Một phiếu mượn nếu quá hạn/hỏng sách sẽ phát sinh tối đa 1 phiếu phạt).

---

### 💡 **Câu 2: Biểu đồ Use Case & Mô tả**

1. **Actors**:
   * `Độc giả`: Người đăng ký, tìm kiếm sách, đặt mượn sách trực tuyến và xem phạt.
   * `Thủ thư`: Người duyệt tài khoản, quản lý sách, xác nhận giao/nhận sách và lập phiếu phạt.
2. **Use Cases chính**:
   * `Đăng ký tài khoản`, `Duyệt tài khoản độc giả`, `Đăng nhập` (`<<include>>` cho các chức năng sau).
   * `Tìm kiếm sách`, `Đặt mượn sách trực tuyến`, `Xác nhận giao sách`, `Xác nhận trả sách`.
   * `Tính tiền phạt & Lập phiếu phạt` (`<<extend>>` UC `Xác nhận trả sách` khi trả quá hạn/hỏng sách).

---

### 💡 **Câu 3: Đặc tả Use Case "Đặt mượn sách trực tuyến"**

* **Tên Use Case**: Đặt mượn sách trực tuyến.
* **Tác nhân**: `Độc giả`.
* **Tiền điều kiện**: Độc giả đã đăng nhập, tài khoản đã được phê duyệt và không bị khóa.
* **Hậu điều kiện**: Phiếu mượn được khởi tạo ở trạng thái "Chờ nhận sách".
* **Luồng sự kiện chính (Main Flow)**:
  1. Độc giả tìm kiếm và chọn các cuốn sách cần mượn vào "Giỏ sách mượn".
  2. Độc giả nhấn nút "Tiến hành đặt mượn".
  3. Hệ thống kiểm tra hạn mức mượn (SV \\(\le 3\\) cuốn, GV \\(\le 5\\) cuốn) và kiểm tra sách còn bản sao rảnh hay không.
  4. Hệ thống hiển thị Form xác nhận ngày hẹn đến thư viện nhận sách.
  5. Độc giả xác nhận.
  6. Hệ thống tạo `PhieuMuon` mới, giảm số lượng sách khả dụng và thông báo thành công.
* **Luồng ngoại lệ**:
  * **3a. Vượt quá hạn mức mượn**: Hệ thống báo lỗi "Bạn đã mượn quá số lượng quy định" và dừng lại.
  * **3b. Sách đã hết bản sao**: Hệ thống thông báo "Sách hiện đã được mượn hết" và yêu cầu bỏ sách đó ra khỏi giỏ.

---

### 💡 **Câu 4: Thiết kế CSDL Quan hệ (Relational Schema)**

1. **Các Bảng & Khóa**:
   * **`DocGia`** (`<u>MaDocGia</u>`, `HoTen`, `Email`, `SoDienThoai`, `LoaiDocGia`)
   * **`TaiKhoan`** (`<u>TenDangNhap</u>`, `MatKhau`, `TrangThaiDuyet`, `MaDocGia` [FK tham chiếu `DocGia`])
   * **`DauSach`** (`<u>MaSach</u>`, `TenSach`, `TacGia`, `NamXB`, `SoLuongBanSao`)
   * **`PhieuMuon`** (`<u>MaPhieu</u>`, `NgayMuon`, `NgayHenTra`, `TrangThai`, `MaDocGia` [FK tham chiếu `DocGia`], `MaThuThu` [FK tham chiếu `ThuThu`])
   * **`ChiTietPhieuMuon`** (`<u>MaPhieu</u>` [FK], `<u>MaSach</u>` [FK], `TinhTrangKhiMuon`) \\(\rightarrow\\) Khóa chính phức hợp (`MaPhieu`, `MaSach`).
   * **`PhieuPhat`** (`<u>MaPhieuPhat</u>`, `SoTienPhat`, `LyDoPhat`, `TrangThaiThanhToan`, `MaPhieu` [FK tham chiếu `PhieuMuon`])

---

## C. ĐÁP ÁN BỘ ĐỀ THI SỐ 2 (QUẢN LÝ NCKH SINH VIÊN)

### 💡 **Câu 1: Biểu đồ Lớp mô hình miền (Domain Model)**

1. **Các lớp thực thể**:

   * `SinhVien`: `maSV`, `hoTen`, `lop`, `email`, `soDienThoai`.
   * `GiangVien`: `maGV`, `hoTen`, `khoa`, `email`, `soDienThoai`.
   * `DotDangKy`: `maDot`, `tenDot`, `namHoc`, `kinhPhiToiDa`, `hanNop`.
   * `DeTaiNCKH`: `maDeTai`, `tenDeTai`, `mucTieu`, `kinhPhiXinCap`, `kinhPhiPheDuyet`, `trangThai` (ChoGVHD/ChoDuyet/DaDuyet/KhongDuyet).
   * `HoiDongKhoaHoc`: `maHoiDong`, `tenHoiDong`, `ngayThanLap`.
   * `PhieuDanhGiaNCKH`: `maPhieu`, `diemThuyetMinh`, `diemNghiệmThu`, `yKienNhanXet`.
2. **Mối quan hệ & Bội số**:

   * `SinhVien` - `DeTaiNCKH`: **`1..*` - `1`** (Một đề tài do 1 hoặc nhiều SV thực hiện, 1 SV đại diện nộp 1 đề tài trong đợt).
   * `GiangVien` - `DeTaiNCKH`: **`1` - `0..*`** (Một giảng viên có thể hướng dẫn nhiều đề tài).
   * `DotDangKy` - `DeTaiNCKH`: **`1` - `0..*`** (Một đợt chứa nhiều đề tài đăng ký).
   * `HoiDongKhoaHoc` - `DeTaiNCKH`: **`1` - `0..*`** (Một Hội đồng chấm duyệt nhiều đề tài).
   * `DeTaiNCKH` - `PhieuDanhGiaNCKH`: **`1` - `1..*`** (Một đề tài có các phiếu đánh giá thuyết minh và nghiệm thu từ Hội đồng).

---

### 💡 **Câu 2: Biểu đồ Use Case & Mô tả**

1. **Actors**:
   * `Sinh viên (Trưởng nhóm)`: Nộp thuyết minh, chọn GVHD, nộp báo cáo tổng kết.
   * `Giảng viên hướng dẫn`: Duyệt/Từ chối tiếp nhận hướng dẫn đề tài.
   * `Hội đồng Khoa học`: Chấm điểm thuyết minh và nghiệm thu đề tài.
   * `Phòng QLKH`: Khởi tạo đợt đăng ký, thành lập Hội đồng, duyệt kinh phí.
2. **Use Cases chính**:
   * `Tạo đợt đăng ký NCKH`, `Đăng ký & Nộp thuyết minh đề tài`, `Phê duyệt hướng dẫn` (GVHD).
   * `Đánh giá thuyết minh` (Hội đồng), `Nộp báo cáo nghiệm thu`, `Chấm nghiệm thu đề tài`.

---

### 💡 **Câu 3: Đặc tả Use Case "Đăng ký nộp Thuyết minh đề tài NCKH"**

* **Tên Use Case**: Đăng ký nộp Thuyết minh đề tài NCKH.
* **Tác nhân**: `Sinh viên (Trưởng nhóm)`.
* **Tiền điều kiện**: Đợt đăng ký NCKH đang mở và còn hạn nộp bài.
* **Hậu điều kiện**: Đề tài được lưu vào hệ thống ở trạng thái "Chờ GVHD xác nhận".
* **Luồng sự kiện chính (Main Flow)**:
  1. Sinh viên chọn chức năng "Đăng ký đề tài NCKH mới".
  2. Hệ thống hiển thị Form đăng ký gồm các trường thông tin đề tài và danh sách Giảng viên.
  3. Sinh viên nhập Tên đề tài, Mục tiêu, Kinh phí xin cấp, chọn Danh sách thành viên nhóm và chọn Giảng viên hướng dẫn.
  4. Sinh viên đính kèm file Đề cương Thuyết minh (.pdf) và nhấn nút "Nộp đăng ký".
  5. Hệ thống kiểm tra Kinh phí xin cấp (\\(\le\\) Kinh phí tối đa của Đợt) và kiểm tra tính hợp lệ của file.
  6. Hệ thống lưu đề tài, gửi thông báo đến GVHD và thông báo thành công cho Sinh viên.
* **Luồng ngoại lệ**:
  * **5a. Kinh phí vượt quy định**: Hệ thống báo lỗi "Kinh phí xin cấp vượt quá hạn mức đợt" và yêu cầu điều chỉnh.
  * **5b. Hết thời hạn đợt đăng ký**: Hệ thống hiển thị thông báo "Đã hết thời hạn đăng ký" và khóa Form.

---

### 💡 **Câu 4: Thiết kế CSDL Quan hệ (Relational Schema)**

1. **Các Bảng & Khóa**:
   * **`SinhVien`** (`<u>MaSV</u>`, `HoTen`, `Lop`, `Email`, `SoDienThoai`)
   * **`GiangVien`** (`<u>MaGV</u>`, `HoTen`, `Khoa`, `Email`, `SoDienThoai`)
   * **`DotDangKy`** (`<u>MaDot</u>`, `TenDot`, `NamHoc`, `KinhPhiToiDa`, `HanNop`)
   * **`DeTaiNCKH`** (`<u>MaDeTai</u>`, `TenDeTai`, `MucTieu`, `KinhPhiXinCap`, `KinhPhiPheDuyet`, `TrangThai`, `MaDot` [FK], `MaGVHD` [FK tham chiếu `GiangVien`], `MaSV_TruongNhom` [FK tham chiếu `SinhVien`])
   * **`ThanhVienDeTai`** (`<u>MaDeTai</u>` [FK], `<u>MaSV</u>` [FK], `VaiTro`) \\(\rightarrow\\) Bảng trung gian giải quyết quan hệ N - N giữa `SinhVien` và `DeTaiNCKH`.
   * **`HoiDong`** (`<u>MaHoiDong</u>`, `TenHoiDong`, `NgayThanhLap`)
   * **`PhieuDanhGia`** (`<u>MaPhieu</u>`, `LoaiDanhGia`, `DiemSo`, `YKienNhanXet`, `MaDeTai` [FK], `MaHoiDong` [FK])
