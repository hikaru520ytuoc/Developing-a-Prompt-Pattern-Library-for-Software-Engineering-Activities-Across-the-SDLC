# SDLC-PP05: Detailed Software Design Prompt Pattern

## Purpose

This prompt supports detailed design. It turns architecture into specific designs for modules, database/schema, APIs, UI screens, services/classes/components, sequence flows, validation, error handling, authorization, and requirement-design mapping.

## Required input

```text
1. Tên dự án:
2. Mô tả ngắn gọn hệ thống:
3. Danh sách yêu cầu chức năng:
4. Danh sách yêu cầu phi chức năng:
5. Danh sách actor và phân quyền:
6. Danh sách use case quan trọng:
7. Kiến trúc phần mềm đã chọn:
8. Danh sách module/component:
9. Entity nghiệp vụ đã phân tích:
10. Business rules quan trọng:
11. Công nghệ dự kiến:
12. Các chức năng cần thiết kế chi tiết:
```

## Official full prompt

```text
Bạn là một chuyên gia thiết kế phần mềm chi tiết trong lĩnh vực kỹ thuật phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 5 của vòng đời phát triển phần mềm SDLC: Thiết kế chi tiết phần mềm.

Dựa trên thông tin tôi cung cấp, hãy tạo tài liệu thiết kế chi tiết để lập trình viên có thể dùng làm cơ sở triển khai mã nguồn, kiểm thử và tích hợp hệ thống.

Thông tin dự án:

1. Tên dự án:
[Điền tên dự án]

2. Mô tả ngắn gọn hệ thống:
[Mô tả hệ thống cần xây dựng]

3. Danh sách yêu cầu chức năng:
[Dán danh sách FR]

4. Danh sách yêu cầu phi chức năng:
[Dán danh sách NFR]

5. Danh sách actor và phân quyền:
[Dán actor, vai trò, quyền hạn nếu có]

6. Danh sách use case quan trọng:
[Dán danh sách UC hoặc đặc tả use case]

7. Kiến trúc phần mềm đã chọn:
[Ví dụ: Layered Architecture, MVC, Modular Monolith, Client-Server...]

8. Danh sách module/component:
[Dán danh sách module đã xác định ở giai đoạn kiến trúc]

9. Entity nghiệp vụ đã phân tích:
[Dán các entity nghiệp vụ như User, Task, Label...]

10. Business rules quan trọng:
[Dán các quy tắc nghiệp vụ]

11. Công nghệ dự kiến:
[Ví dụ: React, Spring Boot, Node.js, PostgreSQL...]

12. Các chức năng cần thiết kế chi tiết:
[Ví dụ: đăng nhập, tạo task, cập nhật task, hoàn thành task, xóa task...]

Yêu cầu đầu ra:

1. Tổng quan thiết kế chi tiết
- Mô tả mục tiêu, phạm vi thiết kế, kiến trúc kế thừa từ giai đoạn trước.
- Ghi rõ giả định nếu thông tin đầu vào còn thiếu.

2. Thiết kế module chi tiết
- Liệt kê các module chính.
- Với mỗi module, mô tả trách nhiệm, chức năng con, actor sử dụng, dữ liệu liên quan, API liên quan và module phụ thuộc.
- Chỉ ra module cốt lõi và module hỗ trợ.

3. Thiết kế database/schema
- Xác định các bảng dữ liệu chính.
- Với mỗi bảng, liệt kê field, kiểu dữ liệu, khóa chính, khóa ngoại, ràng buộc và mô tả.
- Mô tả quan hệ giữa các bảng.
- Nêu ràng buộc dữ liệu quan trọng.

4. Thiết kế API chi tiết
- Liệt kê các API endpoint cần có.
- Với mỗi API, nêu method, endpoint, mục đích, actor/role được phép dùng, request, response, status code và error case.
- Nếu có authentication, chỉ rõ API nào cần token/session.
- Chuẩn hóa response lỗi.

5. Thiết kế giao diện người dùng
- Liệt kê các màn hình chính.
- Với mỗi màn hình, nêu actor sử dụng, mục đích, thành phần giao diện, dữ liệu hiển thị, hành động người dùng, validation và điều hướng.
- Nếu phù hợp, mô tả layout bằng text.

6. Thiết kế class/service/component
- Dựa trên kiến trúc đã chọn, đề xuất các class, service, controller, repository, DTO hoặc component chính.
- Với mỗi thành phần, nêu trách nhiệm và method/chức năng quan trọng.
- Chỉ rõ phụ thuộc giữa các thành phần.

7. Thiết kế sequence flow
- Với các chức năng quan trọng, mô tả thứ tự tương tác giữa actor, UI, controller/API, service, repository và database.
- Trình bày theo từng bước hoặc bảng.
- Bao gồm cả luồng thành công và luồng lỗi quan trọng.

8. Thiết kế validation
- Liệt kê validation cho input, form, API request và business rule.
- Với mỗi validation, nêu điều kiện kiểm tra và thông báo lỗi tương ứng.
- Phân biệt validation dữ liệu và validation nghiệp vụ.

9. Thiết kế xử lý lỗi
- Chuẩn hóa các loại lỗi chính.
- Tạo bảng gồm error code, HTTP status nếu có, tình huống lỗi, thông báo người dùng và cách xử lý.
- Chú ý lỗi xác thực, phân quyền, dữ liệu không hợp lệ, xung đột trạng thái và lỗi hệ thống.

10. Thiết kế phân quyền chi tiết
- Tạo ma trận phân quyền theo actor/role và chức năng.
- Chỉ ra chức năng nào cần kiểm tra ownership.
- Chỉ ra hành động nào cần ghi audit log.

11. Mapping yêu cầu với thiết kế
- Tạo bảng liên kết giữa Requirement ID, Use Case, Module, API, UI Screen và Test Case dự kiến.

12. Checklist kiểm tra thiết kế chi tiết
- Tạo checklist kiểm tra module, database, API, UI, class/service, sequence, validation, error handling, phân quyền và truy vết yêu cầu.

Yêu cầu trình bày:
- Viết bằng tiếng Việt.
- Văn phong học thuật, rõ ràng, phù hợp với báo cáo môn học kỹ thuật phần mềm.
- Ưu tiên trình bày bằng bảng khi phù hợp.
- Không viết code triển khai ở giai đoạn này, chỉ thiết kế.
- Nếu thiếu thông tin, hãy nêu giả định hợp lý.
- Thiết kế phải bám sát yêu cầu, use case và kiến trúc đã có.
- Không tự ý thêm chức năng lớn ngoài phạm vi.
```

## Expected output

- Detailed design overview.
- Module detailed design.
- Database/schema design.
- API design.
- UI design.
- Class/service/component design.
- Sequence flow design.
- Validation design.
- Error handling design.
- Authorization design.
- Requirement-design mapping.
- Detailed design checklist.

## Quality checklist

| Criteria | Yes/No |
|---|---|
| Modules are detailed. |  |
| Database/schema is clear. |  |
| APIs include request/response/error cases. |  |
| UI screens include behavior and validation. |  |
| Services/classes/components are identified. |  |
| Sequence flows are included. |  |
| Validation, error handling, and authorization are designed. |  |
| Requirement-design mapping is included. |  |

## Common mistakes to avoid

- Designing database without business entities.
- API missing request/response/error cases.
- UI description only visual, not behavioral.
- Writing code too early.
- Missing authorization matrix.
