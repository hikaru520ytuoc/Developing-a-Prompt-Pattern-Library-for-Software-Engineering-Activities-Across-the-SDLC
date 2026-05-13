# SDLC-PP06: Implementation and Coding Prompt Pattern

## Purpose

This prompt supports implementation. It helps turn detailed design into structured source code with environment setup, folder structure, database/entity implementation, backend/API, frontend/UI, business logic, validation, error handling, security, unit tests, and run guide.

## Required input

```text
1. Tên dự án:
2. Mô tả ngắn gọn hệ thống:
3. Kiến trúc đã chọn:
4. Công nghệ sử dụng:
5. Cấu trúc database/schema:
6. Danh sách API đã thiết kế:
7. Danh sách màn hình UI:
8. Danh sách module/service cần code:
9. Business rules quan trọng:
10. Validation và error case cần xử lý:
11. Phân quyền người dùng:
12. Chức năng cụ thể muốn hiện thực:
13. Yêu cầu về style code hoặc cấu trúc thư mục:
14. Có cần unit test, README, Docker không:
```

## Official full prompt

```text
Bạn là một kỹ sư phần mềm có kinh nghiệm trong hiện thực hệ thống phần mềm theo đúng kiến trúc, thiết kế chi tiết và yêu cầu đã phân tích.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 6 của vòng đời phát triển phần mềm SDLC: Hiện thực và lập trình phần mềm.

Dựa trên thông tin tôi cung cấp, hãy giúp tôi triển khai chức năng hoặc hệ thống thành mã nguồn có cấu trúc rõ ràng, đúng kiến trúc, đúng yêu cầu, có xử lý lỗi, validation, bảo mật cơ bản và có thể kiểm thử.

Thông tin dự án:

1. Tên dự án:
[Điền tên dự án]

2. Mô tả ngắn gọn hệ thống:
[Mô tả hệ thống cần xây dựng]

3. Kiến trúc đã chọn:
[Ví dụ: Layered Architecture, MVC, Modular Monolith, Client-Server...]

4. Công nghệ sử dụng:
[Ví dụ: Spring Boot, React, MySQL, Node.js, Express, Flutter, Firebase...]

5. Cấu trúc database/schema:
[Dán thiết kế bảng/entity nếu có]

6. Danh sách API đã thiết kế:
[Dán endpoint, method, request, response nếu có]

7. Danh sách màn hình UI:
[Dán các màn hình cần triển khai nếu có]

8. Danh sách module/service cần code:
[Dán module như Auth, User, Task, Admin...]

9. Business rules quan trọng:
[Dán các quy tắc nghiệp vụ]

10. Validation và error case cần xử lý:
[Dán validation/error case nếu có]

11. Phân quyền người dùng:
[Dán role và quyền hạn]

12. Chức năng cụ thể muốn hiện thực:
[Ví dụ: đăng nhập, tạo task, cập nhật task, hoàn thành task, xóa task...]

13. Yêu cầu về style code hoặc cấu trúc thư mục:
[Ví dụ: code rõ ràng, có comment, tách controller-service-repository...]

14. Có cần unit test, README, Docker không:
[Ghi rõ có/không và mức độ cần thiết]

Yêu cầu đầu ra:

1. Tổng quan hiện thực
- Tóm tắt chức năng hoặc module sẽ được code.
- Nêu kiến trúc/layer được áp dụng.
- Nêu giả định nếu thông tin đầu vào còn thiếu.

2. Thiết lập môi trường phát triển
- Liệt kê công cụ, framework, package cần cài.
- Nêu lệnh cài đặt nếu phù hợp.
- Nêu biến môi trường hoặc cấu hình quan trọng nếu có.

3. Cấu trúc thư mục đề xuất
- Tạo cấu trúc thư mục phù hợp với kiến trúc đã chọn.
- Giải thích vai trò của các thư mục chính.
- Đảm bảo code dễ bảo trì và dễ mở rộng.

4. Hiện thực database/entity
- Tạo hoặc mô tả migration/schema nếu cần.
- Tạo entity/model tương ứng với database.
- Tạo repository/DAO để truy cập dữ liệu.
- Đảm bảo field, constraint và quan hệ bám sát thiết kế.

5. Hiện thực backend/API
- Tạo controller/API endpoint theo thiết kế.
- Tạo DTO/request/response nếu cần.
- Tạo service xử lý nghiệp vụ.
- Tạo repository truy cập dữ liệu.
- Chuẩn hóa response thành công và response lỗi.
- Không đặt business logic phức tạp trực tiếp trong controller.

6. Hiện thực frontend/UI
- Tạo page/screen/component theo thiết kế giao diện.
- Tạo service gọi API.
- Xử lý trạng thái loading, success và error.
- Thêm validation form cơ bản.
- Đảm bảo giao diện bám đúng luồng người dùng.

7. Hiện thực business logic
- Code logic nghiệp vụ theo business rules.
- Xử lý đầy đủ luồng chính, luồng thay thế và luồng ngoại lệ.
- Ghi chú rõ các phần logic quan trọng.
- Không tự ý thay đổi quy tắc nghiệp vụ nếu chưa có cơ sở.

8. Hiện thực validation
- Thêm validation ở frontend nếu có form.
- Thêm validation ở backend cho request.
- Thêm business validation trong service.
- Nêu rõ thông báo lỗi tương ứng với từng validation.

9. Hiện thực xử lý lỗi
- Tạo cơ chế xử lý lỗi thống nhất.
- Nếu là API, tạo error response gồm errorCode, message, timestamp và path nếu phù hợp.
- Không để lộ stack trace hoặc lỗi nội bộ cho người dùng.
- Phân biệt lỗi 400, 401, 403, 404, 409 và 500 nếu dùng HTTP API.

10. Hiện thực bảo mật cơ bản
- Thêm authentication nếu chức năng yêu cầu.
- Thêm authorization theo role.
- Kiểm tra ownership nếu người dùng chỉ được truy cập dữ liệu của mình.
- Không hard-code secret/password/API key trong source code.
- Nêu các điểm cần kiểm tra bảo mật thêm ở giai đoạn sau.

11. Viết unit test hoặc test cơ bản
- Tạo test cho service/business logic quan trọng.
- Tạo test cho validation và error case.
- Nếu có API, gợi ý test request/response.
- Nếu không viết code test đầy đủ, hãy tạo danh sách test case cần viết.

12. Code review và refactor
- Kiểm tra code theo các tiêu chí: đúng yêu cầu, đúng kiến trúc, dễ đọc, ít lặp, có xử lý lỗi, có bảo mật, có test.
- Chỉ ra các điểm cần refactor nếu có.
- Đề xuất cách cải thiện maintainability.

13. Tài liệu hướng dẫn chạy project
- Tạo README hoặc run guide gồm công nghệ sử dụng, cách cài dependencies, cấu hình môi trường, chạy backend/frontend, chạy database, chạy test và tài khoản demo nếu có.

14. Checklist hoàn thành giai đoạn hiện thực
- Tạo checklist bao gồm code, database, API, UI, validation, error handling, security, test và documentation.

Yêu cầu trình bày:
- Viết bằng tiếng Việt.
- Code nếu có phải rõ ràng, dễ chạy, có comment ngắn ở phần quan trọng.
- Bám sát kiến trúc và thiết kế chi tiết đã cung cấp.
- Không tự ý thêm chức năng lớn ngoài phạm vi.
- Nếu thiếu thông tin, hãy nêu giả định hợp lý trước khi code.
- Nếu có nhiều file code, hãy trình bày theo từng file rõ ràng.
```

## Expected output

- Implementation overview.
- Development environment setup.
- Project folder structure.
- Database/entity implementation plan.
- Backend/API implementation.
- Frontend/UI implementation.
- Business logic implementation.
- Validation implementation.
- Error handling implementation.
- Security implementation.
- Unit test implementation.
- Code review checklist.
- README/run guide.
- Implementation completion checklist.

## Quality checklist

| Criteria | Yes/No |
|---|---|
| Code follows selected architecture. |  |
| Folder structure is clear. |  |
| Database/entity and API implementation match design. |  |
| Business logic follows rules. |  |
| Validation and error handling are implemented. |  |
| Security/authorization is addressed. |  |
| Unit tests or test cases are included. |  |
| Run guide is included. |  |

## Common mistakes to avoid

- Putting all logic in controller/UI.
- Missing validation and error handling.
- Hard-coding secrets.
- Ignoring unit tests.
- Producing disconnected code snippets without file structure.
