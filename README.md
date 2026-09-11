
Dưới đây là **Hệ thống Lý thuyết & Bài tập Chuẩn bị Cho Đề thi Phân tích và Thiết kế Hệ thống Thông tin (OOAD & UML)** được tổng hợp và cấu trúc hóa logic, khoa học bám sát chương trình học và đề thi chính thức.

---

# PHẦN 1: LÝ THUYẾT NỀN TẢNG THEO CHƯƠNG & MỤC CẦN ĐẠT

## CHƯƠNG 1: TỔNG QUAN VỀ OOAD VÀ KHUNG NHÌN MÔ HÌNH HÓA (UML)

### 1.1 Mục tiêu cần đạt

* Nắm vững khái niệm **Phân tích và Thiết kế Hướng đối tượng (OOAD)**.
* Hiểu rõ kiến trúc **4+1 Khung nhìn (Views)** trong UML.
* Phân biệt được **3 Stereotypes lớp phân tích** cơ bản (Boundary, Entity, Control).

### 1.2 Khái niệm quan trọng & Mô hình hóa

* **Phân tích & Thiết kế Hướng đối tượng (OOAD)**: Quá trình xem hệ thống gồm các đối tượng tương tác với nhau, nhằm trả lời hai câu hỏi **What** (Hệ thống làm gì?) ở pha phân tích và **How** (Hệ thống làm như thế nào?) ở pha thiết kế.
* **Khung nhìn (Views) trong UML (Kiến trúc 4+1)**:
  * **Use Case View**: Khung nhìn ca sử dụng thể hiện yêu cầu chức năng dưới góc nhìn người dùng cuối.
  * **Logical View**: Khung nhìn luận lý phân rã hệ thống thành các lớp, đối tượng và mối quan hệ.
  * **Process View**: Khung nhìn xử lý/tiến trình (thể hiện qua Sequence, State, Activity Diagram).
  * **Component View & Deployment View**: Khung nhìn thực hiện và triển khai kiến trúc phần cứng/phần mềm.
* **Stereotypes lớp phân tích**:
  * **Entity Class (Lớp thực thể)**: Lưu trữ thông tin bền vững (sẽ ánh xạ thành bảng CSDL).
  * **Boundary Class (Lớp biên/giao diện)**: Trung gian tương tác giữa tác nhân bên ngoài và hệ thống.
  * **Control Class (Lớp điều khiển)**: Điều phối luồng xử lý nghiệp vụ của ca sử dụng.

---

## CHƯƠNG 2: MÔ HÌNH HÓA YÊU CẦU CHỨC NĂNG – BIỂU ĐỒ USE CASE

### 2.1 Mục tiêu cần đạt

* Xác định chính xác **Tác nhân (Actor)** và **Ca sử dụng (Use Case - UC)** từ đặc tả bài toán.
* Phân biệt và sử dụng đúng các mối quan hệ: **Association**, **`<<include>>`**, **`<<extend>>`**, **Generalization**.

### 2.2 Khái niệm & Quy tắc biểu diễn

* **Actor (Tác nhân)**: Con người, nhóm người hoặc hệ thống bên ngoài tương tác trực tiếp với hệ thống.
* **Use Case (Ca sử dụng)**: Tập hợp các hành vi/chức năng mà hệ thống thực hiện để mang lại một kết quả có giá trị cho tác nhân.
* **Các mối quan hệ trong Biểu đồ Use Case**:
  * **Association (Liên kết)**: Đường nối giữa Actor và Use Case mà họ tham gia.
  * **`<<include>>` (Bao hàm)**: Use Case chính **bắt buộc** phải gọi Use Case bao hàm (dùng để chia sẻ chức năng chung giữa nhiều UC). *Ví dụ: UC `Đăng nhập` được include bởi các giao dịch.*
  * **`<<extend>>` (Mở rộng)**: Use Case mở rộng chỉ được thực thi **tùy ý/trong điều kiện đặc biệt** để bổ sung chức năng cho UC gốc. *Ví dụ: UC `Xử lý PIN không hợp lệ` extend UC `Đăng nhập`.*
  * **Generalization (Tổng quát hóa / Kế thừa)**: Tác nhân con kế thừa mọi quyền hạn/UC của tác nhân cha, hoặc UC cụ thể kế thừa UC tổng quát.

---

## CHƯƠNG 3: ĐẶC TẢ CHI TIẾT CA SỬ DỤNG (USE CASE SPECIFICATION)

### 3.1 Mục tiêu cần đạt

* Viết tài liệu đặc tả luồng sự kiện cho ca sử dụng một cách bài bản, rõ ràng.
* Xác định đúng **Tiền điều kiện (Pre-conditions)**, **Hậu điều kiện (Post-conditions)**, **Luồng sự kiện chính (Main Flow)** và các **Luồng ngoại lệ/rẽ nhánh (Alternate/Exception Flows)**.

### 3.2 Cấu trúc mẫu chuẩn cho một Đặc tả Use Case

1. **Tên Use Case**: Động từ + Danh từ (Ví dụ: *Tự đánh giá điểm rèn luyện*).
2. **Mô tả ngắn gọn**: Tóm tắt mục đích của UC.
3. **Tác nhân chính (Primary Actor)**: Người khởi tạo hoặc tham gia thực hiện UC.
4. **Tiền điều kiện**: Điều kiện bắt buộc phải thỏa mãn trước khi UC bắt đầu.
5. **Hậu điều kiện**: Trạng thái hệ thống đạt được sau khi UC hoàn thành công việc.
6. **Luồng sự kiện chính (Main Flow)**: Trình tự các bước tương tác chuẩn giữa Actor và Hệ thống.
7. **Luồng ngoại lệ / rẽ nhánh (Alternate Flows)**: Xử lý các tình huống lỗi hoặc điều kiện rẽ nhánh.

---

## CHƯƠNG 4: MÔ HÌNH HÓA MIỀN DỮ LIỆU – BIỂU ĐỒ LỚP (CLASS DIAGRAM)

### 4.1 Mục tiêu cần đạt

* Rút trích các **Lớp thực thể (Domain Classes)** từ yêu cầu nghiệp vụ bằng phương pháp phân tích danh từ.
* Xác định thuộc tính, phương thức và **Bội số (Multiplicity)** giữa các lớp.

### 4.2 Các thành phần & Quy tắc xác định Lớp

* **Cấu trúc một Lớp**: Gồm **Tên lớp**, **Thuộc tính (Attributes)** và **Phương thức (Operations)**.
* **Kỹ thuật trích xuất Lớp & Thuộc tính**:
  * Nghiên cứu văn bản yêu cầu: **Danh từ** đóng vai trò là thực thể \\(\rightarrow\\) **Lớp ứng cử viên**.
  * Loại bỏ các danh từ dư thừa, không thuộc phạm vi hệ thống, danh từ chỉ vai trò hoặc thuật ngữ lập trình.
  * Các danh từ mô tả đặc trưng của lớp \\(\rightarrow\\) **Thuộc tính**.
  * Các **Động từ** đi kèm \\(\rightarrow\\) **Phương thức cơ bản**.
* **Mối quan hệ & Bội số (Multiplicity)**:
  * **Association (Liên kết)**: Quan hệ giữa 2 lớp độc lập. Bội số đi kèm: `1` (đúng một), `0..*` (không hoặc nhiều), `1..*` (một hoặc nhiều), `3..10` (trong khoảng).
  * **Aggregation / Composition (Tập hợp / Cấu thành)**: Quan hệ "mối chứa / bộ phận".
  * **Generalization (Kế thừa)**: Mối quan hệ giữa lớp cha và lớp con.

---

## CHƯƠNG 5: THIẾT KẾ CƠ SỞ DỮ LIỆU QUAN HỆ TỪ MÔ HÌNH LỚP

### 5.1 Mục tiêu cần đạt

* Ánh xạ chính xác từ **Class Diagram (Mô hình miền)** sang **Lược đồ CSDL Quan hệ (Relational Schema)**.
* Xác định Khóa chính (**Primary Key - PK**), Khóa ngoại (**Foreign Key - FK**) và ràng buộc toàn vẹn.

### 5.2 Quy tắc ánh xạ (Mapping Rules)

1. **Lớp thực thể $\rightarrow$ Bảng (Table)**: Mỗi Lớp thực thể biến thành 1 Bảng CSDL. Các thuộc tính của Lớp biến thành các Cột (Columns) tương ứng.
2. **Thêm Khóa chính (PK)**: Mỗi bảng phải có 1 thuộc tính định danh duy nhất (ví dụ: `MaSV`, `MaLop`, `MaDot`).
3. **Ánh xạ Quan hệ 1 - N**: Đưa **Khóa chính của bảng bên 1** sang làm **Khóa ngoại (FK)** ở bảng bên N.
4. **Ánh xạ Quan hệ N - N**: Tạo một **Bảng trung gian (Junction Table)** chứa cặp Khóa ngoại tham chiếu tới Khóa chính của hai bảng ban đầu (Khoá chính của bảng trung gian là sự kết hợp của 2 khoá ngoại này).

---

# PHẦN 2: HỆ THỐNG BÀI TẬP TỪ KHỞI ĐỘNG ĐẾN CHUẨN ĐỀ THI

## BÀI TẬP 1: KHỞI ĐỘNG (MỨC ĐỘ CƠ BẢN)

### Bài tập 1.1: Mua hàng và Diễn đàn Trực tuyến (Use Case Diagram)

* **Đề bài A**: Hệ thống mua hàng trực tuyến cho phép Khách hàng xem, tìm kiếm hàng, đặt thanh toán online qua Ngân hàng trung gian. Bộ phận kinh doanh giao hàng và xuất hóa đơn. Khách hàng có thể gửi khiếu kiện để Bộ phận CSKH giải quyết.
* **Đề bài B**: Diễn đàn cho phép Người dùng chưa đăng ký đọc và tìm kiếm bài viết. Thành viên đăng ký/đăng nhập có thể đăng bài, tải tài liệu, gửi tin nhắn. Quản trị viên (được cấp quyền từ thành viên tích cực) có thể kiểm duyệt và xóa bài.
* **Yêu cầu**: Xác định Tác nhân, Use Case và vẽ Biểu đồ Use Case cho từng hệ thống.

### Bài tập 1.2: Quản lý Đăng ký Học phần (Class Diagram & CSDL)

* **Đề bài**: Trường đại học tổ chức đăng ký học. Giáo vụ lập Chương trình giảng dạy. Sinh viên đăng ký các Môn học. Mỗi Môn học có thể mở thành nhiều Lớp học phần (`CourseOffering`). Giảng viên được phân công dạy các Lớp học phần.
* **Yêu cầu**: Vẽ Biểu đồ Lớp mô hình miền và chuyển thành Lược đồ CSDL Quan hệ.

---

## BÀI TẬP 2: TỔNG HỢP CHUẨN ĐỀ THI (DỰA TRÊN ĐỀ THI KẾT THÚC HỌC PHẦN 2018-2019)

> **ĐỀ BÀI THỰC TẾ (Đề thi KTHP Học kỳ II 2018-2019 - Môn TIN3093)**:
>
> Ban cần xây dựng hệ thống hỗ trợ **Đánh giá điểm rèn luyện trực tuyến**:
>
> * **Giáo viên cố vấn học tập (CVHT)** sẽ quản lý danh sách các sinh viên trong lớp do mình phụ trách.
> * Mỗi **sinh viên** sẽ đăng ký tài khoản của mình (Mã sinh viên, Họ tên, Số điện thoại, Email, Địa chỉ, Mật khẩu).
> * CVHT phê duyệt tài khoản sinh viên đăng ký. Tài khoản sau khi phê duyệt mới có thể đăng nhập để: (1) Đánh giá điểm rèn luyện, (2) Xem kết quả đánh giá.
> * Vào cuối mỗi học kỳ, CVHT tạo một đợt đánh giá điểm rèn luyện với danh sách các tiêu chí (tổng điểm các tiêu chí là 100).
> * Các sinh viên trong lớp tham gia đánh giá: (1) Sinh viên tự đánh giá điểm rèn luyện của mình; (2) Hệ thống chọn ngẫu nhiên \\(N\\) sinh viên khác trong lớp (\\(N = 1/3\\) số sinh viên trong lớp) để sinh viên đánh giá chéo.
> * Sau khi sinh viên đánh giá xong hoặc hết thời hạn, CVHT sẽ đánh giá điểm rèn luyện của từng sinh viên (dựa trên điểm trung bình sinh viên khác đánh giá + ý kiến riêng của CVHT) và tổng hợp bảng điểm.

### Yêu cầu bài thi:

1. **Câu 1 (2.5 điểm)**: Vẽ biểu đồ lớp mô tả mô hình miền (domain model). Mô tả ngắn gọn từng lớp và giải thích mối quan hệ giữa các lớp.
2. **Câu 2 (2.5 điểm)**: Vẽ biểu đồ use case mô tả các chức năng định thiết kế. Mô tả ngắn gọn từng Use Case và Actor xuất hiện.
3. **Câu 3 (2.5 điểm)**: Viết tài liệu đặc tả Use Case chi tiết cho chức năng *"Tự đánh giá điểm rèn luyện của một sinh viên"*.
4. **Câu 4 (2.5 điểm)**: Thiết kế cơ sở dữ liệu quan hệ (Vẽ lược đồ CSDL và giải thích mối quan hệ giữa các bảng).

---

# PHẦN 3: GIẢI THÍCH CHI TIẾT BÀI TẬP VÀ ĐÁP ÁN (Ở CUỐI TÀI LIỆU)

## A. ĐÁP ÁN BÀI TẬP KHỞI ĐỘNG (BÀI TẬP 1)

### Đáp án Bài tập 1.1A (Mua hàng trực tuyến)

* **Actors**: `Khách hàng`, `Bộ phận kinh doanh`, `Bộ phận CSKH`, `Ngân hàng trung gian` (Hệ thống ngoài).
* **Use Cases**: `Tìm kiếm sản phẩm`, `Lựa chọn mua hàng`, `Thanh toán online`, `Giao hàng & Xuất hóa đơn`, `Theo dõi đơn hàng`, `Gửi khiếu kiện`, `Giải quyết khiếu kiện`.
* **Quan hệ đặc biệt**: UC `Thanh toán online` bao hàm (`<<include>>`) UC `Thực hiện giao dịch ngân hàng` và mở rộng (`<<extend>>`) từ UC `Lựa chọn mua hàng`.

### Đáp án Bài tập 1.1B (Diễn đàn)

* **Actors**: `Khách` (chưa đăng ký), `Thành viên` (kế thừa từ Khách), `Quản trị viên` (kế thừa từ Thành viên).
* **Use Cases**:
  * `Khách`: `Đọc bài viết`, `Tìm kiếm bài viết`, `Đăng ký tài khoản`.
  * `Thành viên`: `Đăng nhập`, `Đăng bài viết`, `Tải tài liệu`, `Gửi/Nhận tin nhắn`.
  * `Quản trị viên`: `Kiểm duyệt bài viết`, `Xóa bài viết vi phạm`.
* **Mối quan hệ**: Actor `Thành viên` generalization `Khách`; Actor `Quản trị viên` generalization `Thành viên`.

---

## B. GIẢI THÍCH CHI TIẾT & ĐÁP ÁN BÀI TẬP CHUẨN ĐỀ THI (ĐỀ THI 2018-2019)

### 💡 LỜI GIẢI CÂU 1: BIỂU ĐỒ LỚP MÔ HÌNH MIỀN (DOMAIN MODEL)

#### 1. Danh sách các Lớp thực thể xuất hiện trong mô hình miền:

1. **`SinhVien`**: Đại diện cho thông tin sinh viên thuộc lớp quản lý.
   * *Thuộc tính*: `maSV`, `hoTen`, `soDienThoai`, `email`, `diaChi`.
2. **`TaiKhoanSinhVien`**: Lưu trữ thông tin tài khoản hệ thống của sinh viên.
   * *Thuộc tính*: `tenDangNhap` (Mã SV), `matKhau`, `trangThaiPheDuyet` (True/False).
3. **`CoVanHocTap`**: Đại diện cho giáo viên cố vấn quản lý lớp.
   * *Thuộc tính*: `maGV`, `hoTen`, `soDienThoai`, `email`.
4. **`LopHoc`**: Đại diện cho lớp sinh viên do CVHT phụ trách.
   * *Thuộc tính*: `maLop`, `tenLop`, `siSo`.
5. **`DotDanhGia`**: Đợt đánh giá điểm rèn luyện theo học kỳ.
   * *Thuộc tính*: `maDot`, `tenDot`, `hocKy`, `namHoc`, `hanDanhGia`.
6. **`TieuChi`**: Danh mục tiêu chí đánh giá.
   * *Thuộc tính*: `maTieuChi`, `tenTieuChi`, `diemToiDa` (Tổng điểm các tiêu chí = 100).
7. **`PhieuDanhGia`**: Phiếu ghi nhận kết quả đánh giá (Tự đánh giá, Đánh giá chéo, CVHT đánh giá).
   * *Thuộc tính*: `maPhieu`, `loaiDanhGia` (TuDanhGia / DanhGiaCheo / CoVanDanhGia), `tongDiem`, `yKienCoVan`.
8. **`ChiTietPhieu`**: Chi tiết điểm số cho từng tiêu chí.
   * *Thuộc tính*: `diemDat`.

#### 2. Mối quan hệ và Bội số giữa các lớp:

* **`CoVanHocTap` - `LopHoc`**: **`1` - `1..*`** (Một Cố vấn học tập phụ trách một hoặc nhiều Lớp học).
* **`LopHoc` - `SinhVien`**: **`1` - `1..*`** (Một Lớp học chứa nhiều Sinh viên).
* **`SinhVien` - `TaiKhoanSinhVien`**: **`1` - `0..1`** (Một Sinh viên có tối đa 1 Tài khoản được tạo/phê duyệt).
* **`CoVanHocTap` - `DotDanhGia`**: **`1` - `0..*`** (CVHT tạo ra các Đợt đánh giá vào cuối mỗi học kỳ).
* **`DotDanhGia` - `TieuChi`**: **`1` - `1..*`** (Một Đợt đánh giá gồm danh sách nhiều Tiêu chí).
* **`SinhVien` - `PhieuDanhGia`**: **`1` - `0..*`** (Sinh viên thực hiện hoặc nhận nhiều Phiếu đánh giá).
* **`PhieuDanhGia` - `ChiTietPhieu` - `TieuChi`**: `PhieuDanhGia` chứa nhiều `ChiTietPhieu` (`1` - `1..*`), mỗi chi tiết ứng với 1 `TieuChi` (`1` - `1`).

---

### 💡 LỜI GIẢI CÂU 2: BIỂU ĐỒ USE CASE & MÔ TẢ CHỨC NĂNG

#### 1. Các Actor (Tác nhân):

* **`Sinh viên`**: Người dùng tham gia đăng ký tài khoản, tự đánh giá điểm rèn luyện, đánh giá chéo bạn học và xem kết quả.
* **`Cố vấn học tập (CVHT)`**: Người quản lý lớp, phê duyệt tài khoản, khởi tạo đợt đánh giá, tổng hợp và chấm điểm rèn luyện cuối cùng.
* **`Hệ thống (System Timer/Scheduler)`**: Tác nhân hệ thống thực hiện phân công ngẫu nhiên \\(N = 1/3\\) sinh viên trong lớp để đánh giá chéo.

#### 2. Các Use Case (Ca sử dụng) & Mô tả:

* **`Đăng ký tài khoản`**: Sinh viên điền thông tin cá nhân để tạo tài khoản mới.
* **`Phê duyệt tài khoản`**: CVHT duyệt các tài khoản đăng ký hợp lệ.
* **`Đăng nhập`**: Tác nhân xác thực vào hệ thống (được `<<include>>` bởi các chức năng sau).
* **`Tạo đợt đánh giá & Tiêu chí`**: CVHT thiết lập đợt đánh giá cuối học kỳ và cài đặt điểm tiêu chí.
* **`Tự đánh giá điểm rèn luyện`**: Sinh viên tự nhập điểm theo từng tiêu chí.
* **`Đánh giá chéo sinh viên`**: Sinh viên đánh giá \\(N\\) sinh viên khác do hệ thống chỉ định.
* **`Phân công đánh giá chéo`**: Hệ thống chọn ngẫu nhiên \\(1/3\\) số sinh viên trong lớp cho mỗi SV.
* **`Chấm điểm & Tổng hợp bảng điểm`**: CVHT tổng hợp điểm trung bình đánh giá chéo + ý kiến riêng để đưa ra kết quả cuối cùng.
* **`Xem kết quả rèn luyện`**: Sinh viên xem điểm rèn luyện chính thức.

---

### 💡 LỜI GIẢI CÂU 3: ĐẶC TẢ CHI TIẾT USE CASE "TỰ ĐÁNH GIÁ ĐIỂM RÈN LUYỆN"

| Mục                                                       | Nội dung đặc tả chi tiết                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :--------------------------------------------------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Tên Use Case**                                    | **Tự đánh giá điểm rèn luyện của một sinh viên**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **Mô tả vắn tắt**                                | Mô tả quá trình sinh viên đăng nhập, xem danh sách tiêu chí của đợt đánh giá hiện tại, nhập điểm tự đánh giá cho bản thân và lưu lại vào hệ thống.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Tác nhân**                                       | `Sinh viên`.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Tiền điều kiện**                               | 1. Sinh viên đã có tài khoản và được CVHT phê duyệt.2. Đợt đánh giá điểm rèn luyện của học kỳ hiện tại đang mở và chưa hết hạn.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| **Hậu điều kiện**                                | Phiếu tự đánh giá điểm rèn luyện của sinh viên được lưu trữ thành công vào hệ thống.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Luồng sự kiện chính (Main Flow)**              | **1.** Sinh viên chọn chức năng "Tự đánh giá điểm rèn luyện".**2.** Hệ thống kiểm tra điều kiện thời gian của đợt đánh giá và hiển thị Form tự đánh giá gồm danh sách các tiêu chí và điểm tối đa của từng tiêu chí.**3.** Sinh viên nhập điểm tự đánh giá cho từng tiêu chí và nhập ghi chú minh chứng (nếu có).**4.** Sinh viên nhấn nút "Lưu/Nộp bài đánh giá".**5.** Hệ thống kiểm tra tính hợp lệ của dữ liệu (điểm mỗi tiêu chí \\(\le\\) điểm tối đa, tổng điểm \\(\le 100\\)).**6.** Hệ thống ghi nhận phiếu đánh giá, cập nhật trạng thái "Đã tự đánh giá" và thông báo thành công cho Sinh viên. |
| **Luồng rẽ nhánh / Ngoại lệ (Alternate Flows)** | **3a. Hết thời hạn đánh giá**: Nếu đợt đánh giá đã đóng, hệ thống hiển thị thông báo "Đã hết thời hạn tự đánh giá" và khóa Form.**5a. Điểm nhập không hợp lệ**: Nếu sinh viên nhập điểm vượt quá điểm tối đa của tiêu chí hoặc nhập ký tự không phải số, hệ thống báo lỗi tại tiêu chí đó và yêu cầu sinh viên nhập lại.                                                                                                                                                                                                                                                                                                                                                   |

---

### 💡 LỜI GIẢI CÂU 4: THIẾT KẾ CƠ SỞ DỮ LIỆU QUAN HỆ

#### 1. Danh sách các Bảng CSDL Quan hệ & Cấu trúc Thuộc tính:

* **`LopHoc`** (`<u>MaLop</u>`, `TenLop`, `SiSo`, `MaGV`)
  * *Khoá chính*: `MaLop` | *Khoá ngoại*: `MaGV` tham chiếu `CoVanHocTap(MaGV)`.
* **`CoVanHocTap`** (`<u>MaGV</u>`, `HoTen`, `SoDienThoai`, `Email`)
  * *Khoá chính*: `MaGV`.
* **`SinhVien`** (`<u>MaSV</u>`, `HoTen`, `SoDienThoai`, `Email`, `DiaChi`, `MaLop`)
  * *Khoá chính*: `MaSV` | *Khoá ngoại*: `MaLop` tham chiếu `LopHoc(MaLop)`.
* **`TaiKhoan`** (`<u>TenDangNhap</u>`, `MatKhau`, `TrangThaiDuyet`, `MaSV`)
  * *Khoá chính*: `TenDangNhap` | *Khoá ngoại*: `MaSV` tham chiếu `SinhVien(MaSV)`.
* **`DotDanhGia`** (`<u>MaDot</u>`, `TenDot`, `HocKy`, `NamHoc`, `HanDanhGia`, `MaGV`)
  * *Khoá chính*: `MaDot` | *Khoá ngoại*: `MaGV` tham chiếu `CoVanHocTap(MaGV)`.
* **`TieuChi`** (`<u>MaTieuChi</u>`, `TenTieuChi`, `DiemToiDa`, `MaDot`)
  * *Khoá chính*: `MaTieuChi` | *Khoá ngoại*: `MaDot` tham chiếu `DotDanhGia(MaDot)`.
* **`PhieuDanhGia`** (`<u>MaPhieu</u>`, `LoaiDanhGia`, `TongDiem`, `YKienCoVan`, `MaDot`, `MaSV_DuocDanhGia`, `MaSV_NguoiDanhGia`)
  * *Khoá chính*: `MaPhieu`
  * *Khoá ngoại*: `MaDot` tham chiếu `DotDanhGia(MaDot)`, `MaSV_DuocDanhGia` tham chiếu `SinhVien(MaSV)`, `MaSV_NguoiDanhGia` tham chiếu `SinhVien(MaSV)` (Có thể NULL nếu do CVHT đánh giá).
* **`ChiTietPhieu`** (`<u>MaPhieu</u>`, `<u>MaTieuChi</u>`, `DiemDat`)
  * *Khoá chính phức hợp*: (`MaPhieu`, `MaTieuChi`)
  * *Khoá ngoại*: `MaPhieu` tham chiếu `PhieuDanhGia(MaPhieu)`, `MaTieuChi` tham chiếu `TieuChi(MaTieuChi)`.

#### 2. Giải thích mối quan hệ giữa các bảng:

* **`CoVanHocTap` - `LopHoc` (1 - N)**: Một giáo viên cố vấn quản lý nhiều lớp học, khóa ngoại `MaGV` nằm ở bảng `LopHoc`.
* **`LopHoc` - `SinhVien` (1 - N)**: Một lớp chứa nhiều sinh viên, khóa ngoại `MaLop` nằm ở bảng `SinhVien`.
* **`SinhVien` - `TaiKhoan` (1 - 1)**: Mỗi sinh viên có duy nhất 1 tài khoản, khóa ngoại `MaSV` nằm ở bảng `TaiKhoan`.
* **`DotDanhGia` - `TieuChi` (1 - N)**: Mỗi đợt đánh giá bao gồm nhiều tiêu chí nhỏ.
* **`SinhVien` - `PhieuDanhGia` (1 - N)**: Một sinh viên có thể có nhiều phiếu đánh giá (1 phiếu tự đánh giá, \\(N\\) phiếu đánh giá chéo từ bạn học, 1 phiếu từ CVHT).
* **`PhieuDanhGia` - `ChiTietPhieu` - `TieuChi` (N - N)**: Mối quan hệ nhiều - nhiều giữa `PhieuDanhGia` và `TieuChi` được giải quyết bằng bảng trung gian `ChiTietPhieu` chứa điểm đạt của từng tiêu chí.

---

💡 **Gợi ý bước tiếp theo**: Bạn có muốn mình tạo một bài thi trắc nghiệm (Quiz) ôn tập nhanh các khái niệm UML này, hay muốn khởi tạo một bộ Flashcards ghi nhớ các ký hiệu và quy tắc vẽ biểu đồ không?
