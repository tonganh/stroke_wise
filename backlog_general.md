# Product Backlog

## 1. Đăng ký thông tin cơ bản

- **Mô tả**: Người dùng đăng ký thông tin cơ bản như tên, tuổi, địa chỉ, số điện thoại và email.
- **Tính năng**:
  - Form nhập thông tin cá nhân cơ bản.
  - Validation email, số điện thoại.
  - Lưu trữ và xác minh thông tin người dùng.

## 2. Đăng nhập và xác thực

- **Mô tả**: Cho phép người dùng đăng nhập bằng username + password và thực hiện xác thực 2FA.
- **Tính năng**:
  - Form đăng nhập với trường `username` và `password`.
  - Tích hợp xác thực 2FA qua SMS hoặc ứng dụng (Google Authenticator, Authy, v.v).

## 3. Xác nhận đồng ý chia sẻ dữ liệu

- **Mô tả**: Sau khi đăng nhập lần đầu, người dùng cần xác nhận đồng ý chia sẻ dữ liệu với các trung tâm đột quỵ và đồng ý với điều khoản miễn trừ trách nhiệm.
- **Tính năng**:
  - Popup yêu cầu người dùng xác nhận hai mục "Đồng ý chia sẻ dữ liệu" và "Miễn trừ trách nhiệm".
  - Thông báo rõ về cách thức dữ liệu sẽ được sử dụng.

## 4. Điền thông tin cá nhân bổ sung

- **Mô tả**: Người dùng điền các thông tin bổ sung sau khi đăng nhập lần đầu, bao gồm tuổi, giới tính, tình trạng đột quỵ, địa chỉ, tỉnh/thành phố, bệnh viện khám và mã bệnh nhân.
- **Tính năng**:
  - Form nhập thông tin theo yêu cầu (tuổi, giới tính, đột quỵ, địa chỉ).
  - Tích hợp dữ liệu tỉnh/thành phố, xã/phường từ CSDL.
  - Nhập tên bệnh viện khám và mã bệnh nhân.

## 5. Luồng cho người chưa có tiền sử đột quỵ (Case 1)

- **Mô tả**: Người dùng chưa từng bị đột quỵ sẽ điền thông tin về tiền sử bệnh gia đình (bố mẹ có từng bị đột quỵ), bệnh tim mạch, tăng huyết áp, và chế độ sinh hoạt (ăn rau xanh, thịt đỏ, đồ ngọt, lượng muối tiêu thụ hàng ngày).
- **Tính năng**:
  - Form nhập thông tin về tiền sử bệnh gia đình, bệnh lý cá nhân.
  - Form nhập thông tin chế độ sinh hoạt (tần suất ăn rau, trái cây, thịt đỏ, đồ chiên, đồ ngọt, lượng muối tiêu thụ).

## 6. Chỉ số sức khỏe (BMI)

- **Mô tả**: Người dùng có thể xem các chỉ số sức khỏe như BMI sau khi nhập thông tin.
- **Tính năng**:
  - Màn hình hiển thị các chỉ số sức khỏe hiện tại như BMI, huyết áp, v.v.
  - Mỗi lần nhập dữ liệu sẽ tự động tính toán và hiển thị chỉ số BMI.

## 7. Luồng cho người đã từng bị đột quỵ (Case 2)

- **Mô tả**: Người dùng từng bị đột quỵ sẽ cần điền thêm thông tin về mức độ tuân thủ thuốc, triệu chứng (đau đầu, chóng mặt, tê bì, khó nói, khó nuốt, mất thính lực), và hoạt động thể chất.
- **Tính năng**:
  - Form nhập thông tin về mức độ tuân thủ thuốc (quên uống thuốc, tự ý ngừng thuốc, mong muốn được hỗ trợ thêm).
  - Form nhập thông tin về triệu chứng và hoạt động thể chất.
  - Cung cấp video hướng dẫn về triệu chứng và quản lý sức khỏe.

## 8. Đào tạo và video hướng dẫn

- **Mô tả**: Người dùng sẽ được hướng dẫn thông qua các video đào tạo về triệu chứng, cách quản lý sức khỏe, chế độ ăn uống và tuân thủ thuốc.
- **Tính năng**:
  - Màn hình hiển thị các video hướng dẫn liên quan đến triệu chứng đột quỵ và cách phòng tránh.
  - Cung cấp video về chế độ sinh hoạt, luyện tập thể chất.

## 9. Quản lý thông tin tài khoản người dùng

- **Mô tả**: Quản lý và cho phép thay đổi thông tin đã khai báo trong tài khoản người dùng.
- **Tính năng**:
  - Cho phép người dùng thay đổi thông tin đã khai báo (tên, địa chỉ, số điện thoại, bệnh viện, mã bệnh nhân).
  - Cập nhật trạng thái người dùng từ "Chưa bị đột quỵ" sang "Đã bị đột quỵ" khi có thay đổi.

## 10. Quét mã QR để lấy thông tin ngoài vào

- **Mô tả**: Thêm chức năng quét mã QR để người dùng nhập thông tin từ bên ngoài vào.
- **Tính năng**:
  - Thêm chức năng quét mã QR để tự động lấy thông tin từ hệ thống bên ngoài.
  - Ghi nhận thông tin quét từ mã QR vào hệ thống.

## 11. Đánh giá sức khỏe người dùng

- **Mô tả**: Mỗi lần người dùng hoàn thành các bước điền thông tin, hệ thống sẽ đưa ra chỉ số đánh giá sức khỏe.
- **Tính năng**:
  - Sau mỗi lần người dùng nhập thông tin, hệ thống tính toán và hiển thị chỉ số sức khỏe.
  - Cho phép người dùng đánh giá nhiều lần trong ngày và lưu trữ các bản ghi đánh giá.

## 12. Cập nhật thông tin theo yêu cầu bác sĩ

- **Mô tả**: Các thông tin/trường dữ liệu input có thể bị thay đổi theo yêu cầu sau này của bác sĩ.
- **Tính năng**:
  - Cập nhật và sửa đổi các trường thông tin theo yêu cầu mới từ bác sĩ (ví dụ, bổ sung các trường về bệnh lý mới, chế độ ăn uống, luyện tập).

---

## **Giao diện Web Bác Sĩ**

## 13. Hiển thị số liệu tổng quan cho bác sĩ

- **Mô tả**: Bác sĩ cần xem được các số liệu tổng quan về bệnh nhân.
- **Tính năng**:
  - Hiển thị số lượng bệnh nhân có nguy cơ cao.
  - Hiển thị số lượng bệnh nhân có nguy cơ tái phát.
  - Hiển thị tổng số ca tái phát.
  - Các số liệu được cập nhật theo thời gian thực.

## 14. Hiển thị danh sách bệnh nhân và hỗ trợ tìm kiếm

- **Mô tả**: Bác sĩ cần xem được danh sách bệnh nhân và hỗ trợ tìm kiếm.
- **Tính năng**:
  - Hiển thị danh sách bệnh nhân với các thông tin cơ bản (tên, độ tuổi, mã bệnh nhân, tình trạng sức khỏe).
  - Cung cấp chức năng tìm kiếm theo tên, mã bệnh nhân, hoặc các tiêu chí khác.
  - Tính năng lọc danh sách bệnh nhân theo các nhóm nguy cơ (cao, thấp, tái phát, chưa tái phát).

## 15. Xem thông tin chi tiết của bệnh nhân

- **Mô tả**: Bác sĩ cần xem được thông tin chi tiết của từng bệnh nhân.
- **Tính năng**:
  - Xem thông tin cá nhân của bệnh nhân (tuổi, giới tính, địa chỉ, bệnh lý liên quan).
  - Xem lịch sử bệnh án, các chỉ số sức khỏe (BMI, huyết áp, v.v.).
  - Xem lịch sử ghi chú của bác sĩ về tình trạng bệnh và các điều trị đã thực hiện.
  - Hiển thị các thông tin cập nhật về tình trạng bệnh nhân theo thời gian.

## 16. Trực quan hóa dữ liệu

- **Mô tả**: Bác sĩ cần có công cụ để trực quan hóa dữ liệu bệnh nhân, giúp dễ dàng phân tích và ra quyết định.
- **Tính năng**:
  - Button hoặc công cụ cho phép trực quan hóa dữ liệu về các chỉ số sức khỏe của bệnh nhân.
  - Xem các biểu đồ về BMI, huyết áp, lượng muối tiêu thụ hàng ngày, chế độ ăn uống của bệnh nhân.
  - Các biểu đồ có thể tùy chỉnh theo ngày, tuần, tháng để theo dõi xu hướng thay đổi sức khỏe của bệnh nhân.

## 17. Lọc và phân loại bệnh nhân theo nhóm nguy cơ

- **Mô tả**: Bác sĩ cần có công cụ lọc và phân loại bệnh nhân theo mức độ nguy cơ.
- **Tính năng**:
  - Lọc bệnh nhân theo nhóm nguy cơ cao, trung bình, thấp.
  - Phân loại bệnh nhân theo tình trạng bệnh (đột quỵ chưa xảy ra, đã từng đột quỵ, tái phát).
  - Tính năng cảnh báo khi có bệnh nhân thuộc nhóm nguy cơ cao hoặc tái phát.

## 18. Cập nhật và thêm ghi chú cho bệnh nhân

- **Mô tả**: Bác sĩ cần có khả năng cập nhật và thêm ghi chú cho bệnh nhân trong hệ thống.
- **Tính năng**:
  - Cung cấp form cho bác sĩ nhập các ghi chú điều trị, triệu chứng mới hoặc các thông tin quan trọng khác.
  - Lưu trữ và hiển thị lịch sử ghi chú cho mỗi bệnh nhân.
  - Tính năng chỉnh sửa hoặc xóa ghi chú nếu cần thiết.

## 19. Hệ thống thông báo về tình trạng bệnh nhân

- **Mô tả**: Bác sĩ cần nhận thông báo về tình trạng sức khỏe của bệnh nhân.
- **Tính năng**:
  - Cảnh báo khi bệnh nhân có dấu hiệu nguy cơ cao hoặc tái phát.
  - Cung cấp thông báo khi có thay đổi về chỉ số sức khỏe của bệnh nhân.
  - Thông báo về các cuộc hẹn kiểm tra, tái khám của bệnh nhân.
