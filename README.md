# CNTT2..
Dưới đây là lời giải chi tiết và hướng dẫn các bước thực hiện cho **Bài 2: Chuẩn bị hồ sơ dự án trước khi triển khai hệ thống** thuộc phần Bài tập về nhà (BTVN) Buổi 12 môn Nhập Môn Công Nghệ Thông Tin trên hệ thống LMS:

---

1. **Phần 1: Phân tích (Sơ đồ cây cấu trúc Heading cho file SRS):**
Để thiết kế tài liệu Đặc tả Yêu cầu Phần mềm (SRS) cho module "Học trực tuyến" với 10 tiêu đề cấp 2 và kiểm soát qua Navigation Pane, sơ đồ cây phân cấp được cấu trúc như sau:

* **Heading 1: 1. Giới thiệu**
* Heading 2: 1.1. Mục đích tài liệu
* Heading 2: 1.2. Phạm vi module "Học trực tuyến"


* **Heading 1: 2. Mô tả tổng quan**
* Heading 2: 2.1. Bối cảnh dự án PTIT-Learning
* Heading 2: 2.2. Đối tượng người dùng


* **Heading 1: 3. Yêu cầu chức năng (Functional Requirements)**
* Heading 2: 3.1. Quản lý danh sách khóa học
* Heading 2: 3.2. Quản lý phòng học ảo
* Heading 2: 3.3. Tương tác và điểm danh trực tuyến


* **Heading 1: 4. Yêu cầu phi chức năng**
* Heading 2: 4.1. Hiệu năng hệ thống
* Heading 2: 4.2. Bảo mật dữ liệu người dùng


* **Heading 1: 5. Phụ lục và tài liệu tham khảo**
* Heading 2: 5.1. Thuật ngữ viết tắt




2. **Phần 2: Triển khai (Bộ file báo cáo hoàn chỉnh):**
* **Microsoft Word (Tài liệu SRS):** Xây dựng đầy đủ các mục Heading 1 và Heading 2 như trên, bật **Navigation Pane** (tab *View* -> tick chọn *Navigation Pane*) để kiểm soát cấu trúc, đồng thời cập nhật mục lục tự động (*Update entire table*) trước khi lưu file.
* **Microsoft Excel (Quản lý dữ liệu học viên):**
* Đảm bảo hàng đầu tiên là Header Row duy nhất, không chứa hàng tổng cộng ở giữa dữ liệu.
* Sử dụng tổ hợp phím `Ctrl + Shift + L` để kích hoạt **AutoFilter** đa điều kiện.
* Lọc danh sách sinh viên thỏa mãn điều kiện: Điểm chuyên cần dưới 7 VÀ thuộc khoa CNTT.


* **Microsoft PowerPoint (Slide giới thiệu tính năng):**
* Áp dụng Combo màu tối: Nền màu xanh hải quân (Navy), chữ màu trắng, và điểm nhấn (Accent) bằng màu cam để đảm bảo **Contrast Ratio** (tỷ lệ tương phản) cao.
* Trình bày lộ trình học tập bằng Flowchart được phân bổ trên slide chuẩn 3 vùng trực quan.




3. **Phần 3: Kiểm thử và Xử lý lỗi lọc tên (Dùng hàm TRIM):**
* **Nguyên nhân:** Khi thực hiện lọc sinh viên theo tên nhưng không hiển thị kết quả mặc dù nhìn thấy tên đó trên bảng, nguyên nhân chủ yếu là do dữ liệu xuất hiện các **khoảng trắng thừa** (dấu cách ẩn ở đầu, ở cuối hoặc lặp nhiều dấu cách ở giữa chuỗi) được sinh ra khi copy từ hệ thống khác vào Excel.
* **Cách khắc phục bằng hàm TRIM:**
1. Tạo một cột phụ bên cạnh danh sách gốc.
2. Sử dụng công thức `=TRIM(cell_chứa_tên_gốc)` (ví dụ: `=TRIM(A2)`) để hệ thống tự động loại bỏ toàn bộ khoảng trắng thừa.
3. Copy dữ liệu từ cột phụ sau khi đã lọc sạch khoảng trắng và **Paste Values** đè ngược lại vào cột dữ liệu chính, sau đó tiến hành bật AutoFilter lại bình thường.
