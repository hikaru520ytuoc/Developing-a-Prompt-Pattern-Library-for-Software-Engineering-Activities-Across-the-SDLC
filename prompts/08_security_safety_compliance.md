# SDLC-PP08: Security, Safety and Compliance Prompt Pattern

## Giai đoạn

**An toàn, bảo mật và tuân thủ**

## Mục tiêu

Rà soát tài sản, yêu cầu bảo mật, threat model, authentication, authorization, input/output, data protection, dependencies, secure coding, logging, security test và pre-release checklist.

## Khi nào sử dụng?

Sử dụng prompt này khi bạn đang làm đúng giai đoạn **An toàn, bảo mật và tuân thủ** trong vòng đời phát triển phần mềm và cần AI hỗ trợ tạo tài liệu/kết quả có cấu trúc.

## Input cần cung cấp

- Tên dự án
- Mô tả
- Actor/role
- Phân quyền
- FR/NFR
- Kiến trúc/API/database
- Dữ liệu nhạy cảm
- Cơ chế đăng nhập
- Công nghệ/dependency
- Chức năng rủi ro cao
- Môi trường

## Prompt đầy đủ

```text
Bạn là một chuyên gia an toàn, bảo mật và tuân thủ trong phát triển phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 8 của SDLC: An toàn, bảo mật và tuân thủ.

Thông tin dự án:
1. Tên dự án: [Điền]
2. Mô tả hệ thống: [Điền]
3. Actor/role: [Điền]
4. Ma trận phân quyền nếu có: [Điền]
5. Yêu cầu chức năng: [Dán FR]
6. Yêu cầu phi chức năng: [Dán NFR]
7. Kiến trúc/API/database: [Điền]
8. Dữ liệu nhạy cảm hệ thống xử lý: [Điền]
9. Cơ chế đăng nhập/xác thực: [Điền]
10. Công nghệ và dependency chính: [Điền]
11. Chức năng rủi ro cao: [Điền]
12. Môi trường triển khai dự kiến: [Điền]

Hãy tạo tài liệu bảo mật gồm:
1. Tổng quan bảo mật và phạm vi rà soát.
2. Tài sản cần bảo vệ, mức nhạy cảm và cách bảo vệ.
3. Yêu cầu bảo mật theo mã SEC-01, SEC-02...
4. Threat model: tài sản, mối đe dọa, tác nhân, tác động, giảm thiểu.
5. Rà soát authentication: login, password, session/token, logout, token hết hạn.
6. Rà soát authorization/access control: role, permission, ownership, API-level authorization.
7. Rà soát input validation và output handling.
8. Rà soát bảo vệ dữ liệu: lưu trữ, truyền tải, hiển thị, log.
9. Rà soát dependency/package: version, package dư, lỗ hổng, license, lockfile.
10. Secure coding checklist.
11. Rà soát logging và audit.
12. Security test cases.
13. Privacy and compliance checklist.
14. Security risk register.
15. Checklist bảo mật trước release.

Yêu cầu:
- Viết bằng tiếng Việt.
- Tập trung vào phòng vệ, kiểm tra, giảm thiểu rủi ro.
- Không đưa hướng dẫn khai thác lỗ hổng hoặc tấn công chi tiết.
- Nếu thiếu thông tin, hãy nêu giả định hợp lý.
```

## Output mong muốn

- Security overview
- Assets
- Security requirements
- Threat model
- Auth review
- Access control review
- Input/output review
- Data protection
- Dependency review
- Secure coding
- Audit
- Security tests
- Compliance
- Risk register
- Pre-release checklist

## Checklist đánh giá đầu ra

| Tiêu chí | Đạt/Chưa đạt | Ghi chú |
|---|---|---|
| Bám sát input được cung cấp |  |  |
| Có cấu trúc rõ ràng |  |  |
| Có bảng khi phù hợp |  |  |
| Có mã định danh nếu cần |  |  |
| Có nêu giả định khi thiếu thông tin |  |  |
| Có checklist cuối giai đoạn |  |  |
| Không tự ý mở rộng phạm vi |  |  |
| Có thể dùng làm đầu vào cho giai đoạn tiếp theo |  |  |

## Lỗi cần tránh

- Chỉ ẩn nút frontend
- Lưu password plain text
- Hard-code secret
- Không validate input
- Không ownership check
- Log token/password
- Hướng dẫn khai thác lỗ hổng
