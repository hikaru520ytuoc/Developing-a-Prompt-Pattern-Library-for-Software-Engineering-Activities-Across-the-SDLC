# SDLC-PP02: Requirements Engineering Prompt Pattern

## Giai đoạn

**Thu thập và quản lý yêu cầu**

## Mục tiêu

Chuyển mô tả dự án thành yêu cầu chức năng, phi chức năng, user story, acceptance criteria, business rules, ưu tiên và truy vết yêu cầu.

## Khi nào sử dụng?

Sử dụng prompt này khi bạn đang làm đúng giai đoạn **Thu thập và quản lý yêu cầu** trong vòng đời phát triển phần mềm và cần AI hỗ trợ tạo tài liệu/kết quả có cấu trúc.

## Input cần cung cấp

- Tên dự án
- Mô tả dự án
- Actor/người dùng
- Quy trình hiện tại
- Chức năng mong muốn
- Vấn đề đang gặp
- Business rules
- Ràng buộc kỹ thuật

## Prompt đầy đủ

```text
Bạn là một chuyên gia phân tích yêu cầu phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 2 của SDLC: Thu thập và quản lý yêu cầu phần mềm.

Thông tin dự án:
1. Tên dự án: [Điền]
2. Mô tả ngắn gọn dự án: [Điền]
3. Danh sách actor/người dùng dự kiến: [Điền]
4. Quy trình nghiệp vụ hiện tại: [Điền hoặc ghi chưa xác định]
5. Các chức năng mong muốn ban đầu: [Điền]
6. Các vấn đề đang gặp phải: [Điền]
7. Các quy định hoặc điều kiện nghiệp vụ: [Điền]
8. Yêu cầu kỹ thuật/ràng buộc: [Điền]
9. Mức độ chi tiết mong muốn: [Cơ bản/Trung bình/Chi tiết]

Hãy tạo tài liệu yêu cầu phần mềm gồm:
1. Tổng quan yêu cầu và giả định.
2. Danh sách actor và vai trò.
3. Yêu cầu chức năng theo mã FR-01, FR-02..., gồm tên, mô tả, actor, input/output, ưu tiên.
4. Yêu cầu phi chức năng theo mã NFR-01, NFR-02..., gồm hiệu năng, bảo mật, usability, reliability, maintainability.
5. Business rules theo mã BR-01, BR-02...
6. User story theo cấu trúc: Là một [vai trò], tôi muốn [chức năng], để [mục đích].
7. Acceptance criteria cho yêu cầu quan trọng, có thể dùng Given–When–Then.
8. Ưu tiên yêu cầu theo MoSCoW.
9. Các yêu cầu thiếu, mơ hồ, xung đột và câu hỏi cần hỏi stakeholder.
10. Ma trận truy vết yêu cầu sơ bộ: Requirement ID, User Story, Use Case dự kiến, Module dự kiến, Test Case dự kiến.
11. Checklist kiểm tra chất lượng yêu cầu.

Yêu cầu:
- Viết bằng tiếng Việt.
- Trình bày bằng bảng khi phù hợp.
- Yêu cầu phải rõ ràng, có thể kiểm thử.
- Không đi sâu sang thiết kế database, kiến trúc hoặc code.
```

## Output mong muốn

- Requirement overview
- Actor list
- Functional requirements
- Non-functional requirements
- Business rules
- User stories
- Acceptance criteria
- Priority
- Ambiguity list
- Traceability matrix

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

- Yêu cầu quá chung chung
- Không có acceptance criteria
- Không mã hóa yêu cầu
- Tự ý thêm chức năng lớn
- Nhảy sang thiết kế database/code
