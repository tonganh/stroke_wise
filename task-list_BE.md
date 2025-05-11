# Kế hoạch cho Team Backend và Frontend

## Thời gian: 10/05 - 01/07

### Mục tiêu:

- Hoàn thành các tính năng từ Product Backlog liên quan đến việc đăng ký, đăng nhập, quản lý thông tin người dùng và bác sĩ.
- Xây dựng các API cho các tính năng tương tác với hệ thống (bao gồm dữ liệu người dùng, bệnh lý, quét mã QR, thống kê sức khỏe, v.v.).
- Đảm bảo dữ liệu và tính năng của hệ thống hoạt động ổn định.

## Sprint 1: 10/05 - 16/05

### Mục tiêu:

- Triển khai các tính năng cơ bản liên quan đến đăng ký, đăng nhập và thông tin người dùng, đồng thời triển khai frontend cho trang web bác sĩ.

### Công việc:

1. **Frontend cho Web Bác Sĩ**

   - **Thiết kế giao diện đăng nhập** cho bác sĩ với `username` và `password`.
   - **Tích hợp xác thực 2FA** cho bác sĩ qua SMS hoặc ứng dụng (Google Authenticator, Authy).
   - **Hiển thị số liệu tổng quan cho bác sĩ** (số lượng bệnh nhân, nguy cơ tái phát, tổng số ca tái phát).
   - **Hiển thị danh sách bệnh nhân và hỗ trợ tìm kiếm**.

2. **Backend**:

   - **Chuẩn bị dữ liệu**: Nhập dữ liệu về **tỉnh/thành phố, xã/phường** từ nguồn bên ngoài vào hệ thống.
   - **Đăng ký thông tin cơ bản**: Xây dựng API cho việc nhận và lưu trữ thông tin người dùng cơ bản (tên, tuổi, địa chỉ, số điện thoại, email).
   - **Validation email và số điện thoại**.
   - **Đăng nhập và xác thực**: Xây dựng API đăng nhập với `username` và `password`, tích hợp **xác thực 2FA**.

3. **Xác nhận đồng ý chia sẻ dữ liệu**:
   - **API xác nhận dữ liệu chia sẻ**: Cập nhật thông tin chia sẻ từ phía client mà không cần lưu trữ backend.

## Sprint 2: 17/05 - 23/05

### Mục tiêu:

- Triển khai các API liên quan đến thông tin bổ sung của người dùng và bệnh viện, đồng thời tiếp tục phát triển frontend.

### Công việc:

1. **Frontend**:

   - **Hiển thị thông tin cá nhân bổ sung**: Giao diện nhập thông tin bổ sung như tuổi, giới tính, tình trạng đột quỵ, bệnh viện.
   - **Tích hợp tìm kiếm bệnh viện** và cho phép người dùng thêm bệnh viện nếu chưa có trong hệ thống.

2. **Backend**:
   - **Quản lý bệnh viện**: Tạo bảng quản lý bệnh viện trong cơ sở dữ liệu và xây dựng API cho phép người dùng thêm bệnh viện nếu chưa có trong hệ thống.
   - **Điền thông tin cá nhân bổ sung**: Xây dựng API cho việc nhận và lưu trữ thông tin bổ sung như tuổi, giới tính, tình trạng đột quỵ, địa chỉ.
   - **Luồng cho người chưa có tiền sử đột quỵ (Case 1)**: Xây dựng API nhận thông tin về tiền sử bệnh gia đình, bệnh lý cá nhân, chế độ sinh hoạt.
   - **Chỉ số sức khỏe (BMI)**: API tính toán và lưu trữ BMI của người dùng.

## Sprint 3: 24/05 - 30/05

### Mục tiêu:

- Triển khai các tính năng người dùng và video hướng dẫn cho bác sĩ.

### Công việc:

1. **Frontend**:

   - **Hiển thị số liệu tổng quan cho bác sĩ**: Xây dựng giao diện bác sĩ xem số liệu tổng quan.
   - **Hiển thị danh sách bệnh nhân và hỗ trợ tìm kiếm**: Thiết kế giao diện tìm kiếm bệnh nhân theo các tiêu chí.
   - **Đào tạo và video hướng dẫn**: Tích hợp giao diện video hướng dẫn cho bác sĩ về triệu chứng và quản lý sức khỏe.

2. **Backend**:
   - **Cung cấp API tổng quan cho bác sĩ**: API cung cấp số liệu tổng quan về bệnh nhân (nguy cơ cao, tái phát).
   - **Tạo API hiển thị danh sách bệnh nhân** và hỗ trợ tìm kiếm theo tên, mã bệnh nhân.
   - **Tạo API cung cấp video hướng dẫn** và tích hợp vào giao diện frontend của bác sĩ.

## Sprint 4: 31/05 - 06/06

### Mục tiêu:

- Triển khai các tính năng lọc phân loại bệnh nhân theo nhóm nguy cơ, trực quan hóa dữ liệu và ghi chú cho bệnh nhân.

### Công việc:

1. **Frontend**:

   - **Trực quan hóa dữ liệu**: Hiển thị biểu đồ sức khỏe (BMI, huyết áp, v.v.) cho bác sĩ.
   - **Lọc và phân loại bệnh nhân theo nhóm nguy cơ**: Giao diện lọc bệnh nhân theo nhóm nguy cơ và tình trạng bệnh.
   - **Cập nhật và thêm ghi chú cho bệnh nhân**: Giao diện thêm và chỉnh sửa ghi chú của bác sĩ về bệnh nhân.

2. **Backend**:

   - **Trực quan hóa dữ liệu**: Cung cấp API cho phép trực quan hóa các chỉ số sức khỏe của bệnh nhân.
   - **Lọc và phân loại bệnh nhân theo nhóm nguy cơ**: API lọc bệnh nhân theo nhóm nguy cơ (cao, thấp, tái phát).
   - **Cập nhật và thêm ghi chú cho bệnh nhân**: API cho phép bác sĩ thêm và lưu trữ ghi chú.

3. **Hệ thống thông báo về tình trạng bệnh nhân**:
   - **Tạo hệ thống thông báo** khi bệnh nhân có dấu hiệu nguy cơ cao hoặc tái phát.

---

### Tổng kết:

- **Sprint 1** sẽ triển khai frontend cho đăng nhập, xác thực 2FA và hiển thị số liệu tổng quan cho bác sĩ, đồng thời thực hiện các công việc backend cơ bản.
- **Frontend cho bác sĩ** sẽ được triển khai song song với backend từ Sprint 1, đảm bảo các tính năng được tích hợp hoàn chỉnh vào giao diện web.
- Các **tính năng liên quan đến video hướng dẫn**, **lọc bệnh nhân** và **trực quan hóa dữ liệu** sẽ được hoàn thiện dần dần trong Sprint 3 và Sprint 4.

Những công việc này sẽ giúp bác sĩ có công cụ mạnh mẽ trong việc theo dõi và quản lý bệnh nhân, đồng thời các tính năng frontend sẽ được triển khai đồng thời với backend để đảm bảo hiệu quả phát triển.
