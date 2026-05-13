# SDLC-PP08: Security, Safety and Compliance Prompt Pattern

## Purpose

This prompt supports security, safety, and compliance review. It identifies assets, security requirements, threats, authentication/authorization issues, input/output risks, data protection needs, dependencies, secure coding concerns, logs/audits, security tests, privacy/compliance checks, and pre-release security checklist.

## Required input

```text
1. Tên dự án:
2. Mô tả ngắn gọn hệ thống:
3. Danh sách actor/role:
4. Ma trận phân quyền nếu có:
5. Danh sách yêu cầu chức năng:
6. Danh sách yêu cầu phi chức năng:
7. Kiến trúc hệ thống:
8. Danh sách API endpoint:
9. Danh sách màn hình giao diện:
10. Database/entity chính:
11. Loại dữ liệu nhạy cảm hệ thống xử lý:
12. Cơ chế đăng nhập/xác thực đang dùng:
13. Công nghệ và dependency chính:
14. Các chức năng có rủi ro cao:
15. Môi trường triển khai dự kiến:
```

## Official full prompt

```text
Bạn là một chuyên gia an toàn, bảo mật và tuân thủ trong phát triển phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 8 của vòng đời phát triển phần mềm SDLC: An toàn, bảo mật và tuân thủ.

Dựa trên thông tin tôi cung cấp, hãy rà soát hệ thống từ góc nhìn bảo mật, xác định tài sản cần bảo vệ, yêu cầu bảo mật, threat model, kiểm tra xác thực, phân quyền, bảo vệ dữ liệu, input validation, dependency, secure coding, logging, security testing và checklist trước release.

Thông tin dự án:

1. Tên dự án:
[Điền tên dự án]

2. Mô tả ngắn gọn hệ thống:
[Mô tả hệ thống]

3. Danh sách actor/role:
[Ví dụ: Guest, User, Admin...]

4. Ma trận phân quyền nếu có:
[Dán ma trận phân quyền hoặc mô tả quyền của từng role]

5. Danh sách yêu cầu chức năng:
[Dán FR]

6. Danh sách yêu cầu phi chức năng:
[Dán NFR]

7. Kiến trúc hệ thống:
[Ví dụ: client-server, layered architecture, REST API, database...]

8. Danh sách API endpoint:
[Dán endpoint nếu có]

9. Danh sách màn hình giao diện:
[Dán UI screen nếu có]

10. Database/entity chính:
[Dán entity/bảng chính]

11. Loại dữ liệu nhạy cảm hệ thống xử lý:
[Ví dụ: mật khẩu, email, thông tin cá nhân, file upload...]

12. Cơ chế đăng nhập/xác thực đang dùng:
[Ví dụ: session, JWT, OAuth, Firebase Auth, chưa xác định...]

13. Công nghệ và dependency chính:
[Ví dụ: Spring Boot, React, MySQL, Express, Django...]

14. Các chức năng có rủi ro cao:
[Ví dụ: đăng nhập, phân quyền, upload file, thanh toán, xóa dữ liệu...]

15. Môi trường triển khai dự kiến:
[Local, Docker, cloud, production...]

Yêu cầu đầu ra:

1. Tổng quan bảo mật
- Tóm tắt mục tiêu bảo mật, phạm vi rà soát và giả định.
- Nhấn mạnh bảo mật cần được áp dụng xuyên suốt SDLC.

2. Xác định tài sản cần bảo vệ
- Liệt kê tài sản quan trọng.
- Phân loại mức độ nhạy cảm: thấp, trung bình, cao, rất cao.
- Đề xuất cách bảo vệ.

3. Yêu cầu bảo mật
- Tạo danh sách SEC-01, SEC-02...
- Bao gồm authentication, authorization, password, input validation, data protection, logging, error handling, file upload nếu có.

4. Threat model
- Xác định mối đe dọa chính.
- Với mỗi threat, nêu tài sản bị ảnh hưởng, tác nhân, cách tấn công ở mức mô tả, tác động và biện pháp giảm thiểu.
- Trình bày dưới dạng bảng.

5. Rà soát authentication
- Kiểm tra đăng nhập, mật khẩu, session/token, logout, token hết hạn, đăng nhập sai nhiều lần.
- Chỉ ra điểm còn thiếu hoặc rủi ro.

6. Rà soát authorization và access control
- Kiểm tra phân quyền theo role.
- Tạo hoặc kiểm tra ma trận phân quyền.
- Chỉ ra chức năng cần kiểm tra ownership.
- Nhấn mạnh backend phải kiểm tra quyền, không chỉ frontend ẩn nút.

7. Rà soát input validation và output handling
- Xác định input quan trọng cần validate.
- Nêu rule kiểm tra cho từng input.
- Chỉ ra rủi ro nếu không validate.
- Đề xuất cách xử lý output an toàn khi hiển thị dữ liệu.

8. Rà soát bảo vệ dữ liệu
- Xác định dữ liệu nhạy cảm.
- Đề xuất cách lưu trữ, truyền tải, hiển thị và ghi log an toàn.
- Chỉ ra dữ liệu không nên xuất hiện trong API response hoặc log.

9. Rà soát dependency/package
- Liệt kê các nhóm dependency cần kiểm tra.
- Đề xuất checklist kiểm tra version, package dư thừa, lỗ hổng, license và lockfile.

10. Secure coding checklist
- Tạo checklist kiểm tra code an toàn: authentication, authorization, validation, database query, error handling, secrets, logging, file handling, configuration.

11. Rà soát logging và audit
- Đề xuất hành động cần ghi log/audit.
- Chỉ ra dữ liệu không được ghi vào log.
- Đề xuất cấu trúc log ở mức tổng quan.

12. Security test cases
- Tạo test case bảo mật cơ bản gồm Test Case ID, mục tiêu, precondition, bước kiểm thử, expected result.
- Bao gồm authentication, authorization, access control, input validation, error handling, file upload, token/session nếu có.

13. Privacy and compliance checklist
- Tạo checklist về dữ liệu cá nhân, mục đích sử dụng, phân quyền truy cập, lưu trữ, xóa dữ liệu, báo cáo và log.

14. Security risk register
- Tạo bảng Risk ID, mô tả rủi ro, nguyên nhân, tác động, khả năng xảy ra, mức độ ưu tiên, biện pháp giảm thiểu.

15. Checklist bảo mật trước release
- Bao gồm secret, tài khoản demo, password, token, API, phân quyền, input validation, error handling, dependency, log và README.

Yêu cầu trình bày:
- Viết bằng tiếng Việt.
- Văn phong rõ ràng, phù hợp với báo cáo môn học kỹ thuật phần mềm.
- Ưu tiên trình bày bằng bảng.
- Không đưa hướng dẫn tấn công chi tiết.
- Không tạo nội dung khai thác lỗ hổng.
- Tập trung vào phòng vệ, kiểm tra, giảm thiểu rủi ro và cải thiện an toàn hệ thống.
- Nếu thiếu thông tin, hãy nêu giả định hợp lý.
```

## Expected output

- Security overview.
- Asset identification.
- Security requirements.
- Threat model.
- Authentication review.
- Authorization review.
- Input/output security review.
- Data protection review.
- Dependency review.
- Secure coding checklist.
- Logging and audit review.
- Security test cases.
- Privacy and compliance checklist.
- Security risk register.
- Pre-release security checklist.

## Quality checklist

| Criteria | Yes/No |
|---|---|
| Assets are identified and classified. |  |
| Security requirements are clear. |  |
| Threat model is included. |  |
| Authentication and authorization are reviewed. |  |
| Input/output and data protection are reviewed. |  |
| Dependency and secure coding checklists are included. |  |
| Security test cases and risk register are included. |  |
| Pre-release security checklist is included. |  |

## Common mistakes to avoid

- Treating security as only a final step.
- Checking permissions only in frontend.
- Storing passwords in plain text.
- Hard-coding secrets.
- Providing offensive exploitation instructions.
