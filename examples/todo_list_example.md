# Ví dụ áp dụng: Todo List Application

Tài liệu này minh họa cách dùng bộ prompt với một dự án chung: **Todo List Application**.

## 1. Mô tả dự án

Todo List Application là một ứng dụng web giúp người dùng quản lý danh sách công việc cá nhân.

Người dùng có thể:

- Đăng ký tài khoản.
- Đăng nhập.
- Tạo công việc mới.
- Sửa nội dung công việc.
- Xóa công việc.
- Đánh dấu công việc đã hoàn thành.
- Lọc công việc theo trạng thái.
- Tìm kiếm công việc theo từ khóa.

## 2. Actor

| Actor | Vai trò |
|---|---|
| Guest | Xem trang giới thiệu, đăng ký, đăng nhập |
| Registered User | Quản lý công việc cá nhân |
| Admin | Quản lý tài khoản người dùng cơ bản |

## 3. Input mẫu cho Giai đoạn 1

```text
Tên dự án:
Todo List Application

Lĩnh vực:
Ứng dụng quản lý công việc cá nhân

Đối tượng sử dụng chính:
Người dùng cá nhân cần quản lý danh sách công việc hằng ngày

Vấn đề hiện tại:
Người dùng thường ghi chú công việc rời rạc trên giấy, tin nhắn hoặc nhiều ứng dụng khác nhau, gây khó theo dõi trạng thái hoàn thành.

Mục tiêu mong muốn:
Xây dựng ứng dụng web đơn giản cho phép người dùng tạo, cập nhật, xóa, đánh dấu hoàn thành và lọc công việc.

Chức năng dự kiến:
- Đăng ký tài khoản
- Đăng nhập
- Tạo task
- Sửa task
- Xóa task
- Đánh dấu hoàn thành
- Lọc task theo trạng thái

Công nghệ dự kiến:
Chưa xác định

Quy mô nhóm:
1-3 sinh viên

Thời gian thực hiện:
4-8 tuần

Ràng buộc:
Ứng dụng web, có tài liệu yêu cầu, thiết kế, kiểm thử và hướng dẫn chạy.
```

## 4. Một số yêu cầu chức năng mẫu

| Mã | Yêu cầu chức năng |
|---|---|
| FR-01 | Hệ thống cho phép người dùng đăng ký tài khoản mới. |
| FR-02 | Hệ thống cho phép người dùng đăng nhập bằng email và mật khẩu. |
| FR-03 | Hệ thống cho phép người dùng tạo công việc mới. |
| FR-04 | Hệ thống cho phép người dùng sửa nội dung công việc của mình. |
| FR-05 | Hệ thống cho phép người dùng xóa công việc của mình. |
| FR-06 | Hệ thống cho phép người dùng đánh dấu công việc là hoàn thành hoặc chưa hoàn thành. |
| FR-07 | Hệ thống cho phép người dùng lọc công việc theo trạng thái. |

## 5. Một số yêu cầu phi chức năng mẫu

| Mã | Yêu cầu phi chức năng |
|---|---|
| NFR-01 | Hệ thống phản hồi thao tác thông thường trong vòng 3 giây. |
| NFR-02 | Mật khẩu người dùng không được lưu dưới dạng văn bản rõ. |
| NFR-03 | Người dùng chỉ được xem và chỉnh sửa công việc thuộc tài khoản của mình. |
| NFR-04 | Giao diện phải dễ sử dụng trên trình duyệt phổ biến. |

## 6. Một số business rules mẫu

| Mã | Quy tắc |
|---|---|
| BR-01 | Người dùng phải đăng nhập trước khi quản lý task. |
| BR-02 | Một task phải có tiêu đề. |
| BR-03 | Người dùng chỉ được sửa/xóa task của chính mình. |
| BR-04 | Trạng thái task chỉ có thể là `pending` hoặc `completed`. |

## 7. Một số use case mẫu

| Mã | Use case | Actor |
|---|---|---|
| UC-01 | Đăng ký tài khoản | Guest |
| UC-02 | Đăng nhập | Guest |
| UC-03 | Tạo task | Registered User |
| UC-04 | Cập nhật task | Registered User |
| UC-05 | Xóa task | Registered User |
| UC-06 | Lọc task | Registered User |

## 8. API mẫu

| Method | Endpoint | Mục đích |
|---|---|---|
| POST | `/api/auth/register` | Đăng ký |
| POST | `/api/auth/login` | Đăng nhập |
| GET | `/api/tasks` | Lấy danh sách task |
| POST | `/api/tasks` | Tạo task |
| PATCH | `/api/tasks/{id}` | Cập nhật task |
| DELETE | `/api/tasks/{id}` | Xóa task |

## 9. Test case mẫu

| Test Case ID | Requirement | Scenario | Expected Result |
|---|---|---|---|
| TC-AUTH-01 | FR-02 | Đăng nhập bằng tài khoản hợp lệ | Đăng nhập thành công |
| TC-TASK-01 | FR-03 | Tạo task với tiêu đề hợp lệ | Task được tạo |
| TC-TASK-02 | FR-03 | Tạo task không có tiêu đề | Hệ thống báo lỗi |
| TC-TASK-03 | FR-05 | Xóa task của chính mình | Task bị xóa |
| TC-SEC-01 | NFR-03 | User A truy cập task của User B | Hệ thống từ chối |
