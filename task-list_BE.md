# Kế hoạch cho Team Backend và Frontend

## Thời gian: 10/05 - 01/07

### Mục tiêu:

- Hoàn thành các tính năng từ Product Backlog liên quan đến việc đăng ký, đăng nhập, quản lý thông tin người dùng và bác sĩ.
- Xây dựng các API cho các tính năng tương tác với hệ thống (bao gồm dữ liệu người dùng, bệnh lý, quét mã QR, thống kê sức khỏe, v.v.).
- Đảm bảo dữ liệu và tính năng của hệ thống hoạt động ổn định.

## Sprint 1: 10/05 - 16/05

### Mục tiêu:

- Triển khai các tính năng cơ bản liên quan đến đăng ký, đăng nhập và thông tin người dùng.

### Công việc:

1. **Chuẩn bị dữ liệu**

   - Nhập dữ liệu về **tỉnh/thành phố, xã/phường** từ nguồn bên ngoài vào hệ thống.

2. **Đăng ký thông tin cơ bản**

   - **Xây dựng API** cho việc nhận và lưu trữ thông tin người dùng cơ bản (tên, tuổi, địa chỉ, số điện thoại, email).
   - **Validation email và số điện thoại**.

3. **Đăng nhập và xác thực**

   - **Xây dựng API đăng nhập** với `username` và `password`.
   - Tích hợp **xác thực 2FA** qua SMS hoặc ứng dụng (Google Authenticator, Authy).

4. **Xác nhận đồng ý chia sẻ dữ liệu**
   - **API xác nhận dữ liệu chia sẻ**: Cập nhật thông tin chia sẻ từ phía client mà không cần lưu trữ backend.

## Sprint 2: 17/05 - 23/05

### Mục tiêu:

- Triển khai các API liên quan đến thông tin bổ sung của người dùng và bệnh viện.

### Công việc:

1. **Quản lý bệnh viện**

   - **Tạo bảng quản lý bệnh viện** trong cơ sở dữ liệu.
   - **Xây dựng API** cho phép người dùng thêm bệnh viện nếu chưa có trong hệ thống.

2. **Điền thông tin cá nhân bổ sung**

   - **Xây dựng API** cho việc nhận và lưu trữ thông tin bổ sung như tuổi, giới tính, tình trạng đột quỵ, địa chỉ.
   - **Tích hợp dữ liệu tỉnh/thành phố, xã/phường** vào phần nhập liệu.

3. **Luồng cho người chưa có tiền sử đột quỵ (Case 1)**

   - **Xây dựng API nhận thông tin** về tiền sử bệnh gia đình, bệnh lý cá nhân, chế độ sinh hoạt.

4. **Chỉ số sức khỏe (BMI)**
   - **API tính toán và lưu trữ BMI**: Cập nhật chỉ số sức khỏe của người dùng.

# Task List cho Trang Web Dành Cho Bác Sĩ (Gộp Sprint 3 và Sprint 4)

## Sprint 3: 24/05 - 30/05

### Mục tiêu: Triển khai các tính năng người dùng và video hướng dẫn

### Công việc:

1. **Hiển thị số liệu tổng quan cho bác sĩ**

   - **Tạo API cung cấp số liệu tổng quan** về bệnh nhân:
     - Số lượng bệnh nhân có nguy cơ cao.
     - Số lượng bệnh nhân có nguy cơ tái phát.
     - Tổng số ca tái phát.
   - **Xây dựng giao diện web** cho bác sĩ xem số liệu tổng quan:
     - Hiển thị số liệu theo dạng bảng hoặc đồ thị.

2. **Hiển thị danh sách bệnh nhân và hỗ trợ tìm kiếm**

   - **Tạo API để hiển thị danh sách bệnh nhân** với các thông tin cơ bản (tên, độ tuổi, mã bệnh nhân, tình trạng sức khỏe).
   - **Tính năng tìm kiếm** bệnh nhân theo tên, mã bệnh nhân, hoặc các tiêu chí khác (theo tình trạng bệnh, nhóm nguy cơ, v.v.).
   - **Tính năng lọc danh sách** bệnh nhân theo các nhóm nguy cơ (cao, thấp, tái phát, chưa tái phát).
   - **Thiết kế giao diện tìm kiếm** và lọc bệnh nhân.

3. **Đào tạo và video hướng dẫn**
   - **Tạo API cho việc cung cấp video hướng dẫn** về triệu chứng và cách quản lý sức khỏe, chế độ ăn uống và tuân thủ thuốc.
   - **Thiết kế giao diện hiển thị video** và tích hợp chúng vào hệ thống web.

---

## Sprint 4: 31/05 - 06/06

### Mục tiêu: Triển khai các tính năng lọc phân loại bệnh nhân theo nhóm nguy cơ, trực quan hóa dữ liệu và ghi chú cho bệnh nhân

### Công việc:

1. **Trực quan hóa dữ liệu**

   - **Xây dựng API cho phép trực quan hóa dữ liệu** bệnh nhân, đặc biệt các chỉ số sức khỏe như BMI, huyết áp, lượng muối tiêu thụ, v.v.
   - **Hiển thị biểu đồ sức khỏe** (BMI, huyết áp, v.v.) theo ngày, tuần, tháng.
   - **Tích hợp các công cụ trực quan hóa** vào giao diện web của bác sĩ.

2. **Lọc và phân loại bệnh nhân theo nhóm nguy cơ**

   - **Tạo API lọc bệnh nhân** theo nhóm nguy cơ (cao, trung bình, thấp).
   - **Phân loại bệnh nhân** theo tình trạng bệnh (đột quỵ chưa xảy ra, đã từng đột quỵ, tái phát).
   - **Tính năng cảnh báo** khi bệnh nhân thuộc nhóm nguy cơ cao hoặc tái phát.
   - **Thiết kế giao diện lọc bệnh nhân** theo các nhóm nguy cơ và tình trạng bệnh.

3. **Cập nhật và thêm ghi chú cho bệnh nhân**

   - **Xây dựng API để bác sĩ thêm ghi chú** cho mỗi bệnh nhân.
   - **Lưu trữ lịch sử ghi chú** và hiển thị các ghi chú của bác sĩ về tình trạng bệnh nhân.
   - **Cung cấp tính năng chỉnh sửa và xóa ghi chú** nếu cần thiết.

4. **Hệ thống thông báo về tình trạng bệnh nhân**
   - **Tạo hệ thống thông báo** về tình trạng sức khỏe của bệnh nhân:
     - Cảnh báo khi bệnh nhân có dấu hiệu nguy cơ cao hoặc tái phát.
     - Thông báo về các thay đổi trong chỉ số sức khỏe của bệnh nhân.
   - **Thiết kế giao diện thông báo** cho bác sĩ nhận thông báo về bệnh nhân.
