# SDLC-PP04: Software Architecture Prompt Pattern

## Giai đoạn

**Kiến trúc phần mềm**

## Mục tiêu

Đề xuất kiến trúc tổng thể, architectural drivers, quality attributes, module/component, dữ liệu, API, bảo mật, triển khai, công nghệ, trade-off và ADR.

## Khi nào sử dụng?

Sử dụng prompt này khi bạn đang làm đúng giai đoạn **Kiến trúc phần mềm** trong vòng đời phát triển phần mềm và cần AI hỗ trợ tạo tài liệu/kết quả có cấu trúc.

## Input cần cung cấp

- Tên dự án
- Mô tả
- Actor
- FR/NFR
- Business rules
- Use case/module
- Entity
- Công nghệ dự kiến
- Ràng buộc
- Bảo mật/phân quyền
- Môi trường triển khai

## Prompt đầy đủ

```text
Bạn là một kiến trúc sư phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 4 của SDLC: Kiến trúc phần mềm.

Thông tin dự án:
1. Tên dự án: [Điền]
2. Mô tả ngắn gọn hệ thống: [Điền]
3. Danh sách actor: [Điền]
4. Yêu cầu chức năng chính: [Dán FR]
5. Yêu cầu phi chức năng: [Dán NFR]
6. Business rules quan trọng: [Điền]
7. Use case hoặc module chính: [Điền]
8. Entity nghiệp vụ quan trọng: [Điền]
9. Công nghệ dự kiến nếu có: [Điền]
10. Ràng buộc về thời gian, nhân lực, kỹ năng, triển khai: [Điền]
11. Yêu cầu bảo mật/phân quyền: [Điền]
12. Môi trường triển khai mong muốn: [Điền]

Hãy tạo tài liệu kiến trúc phần mềm gồm:
1. Tổng quan kiến trúc.
2. Architectural drivers: FR quan trọng, NFR, ràng buộc, rủi ro.
3. Phân tích quality attributes: performance, security, scalability, availability, maintainability, usability, reliability, testability, deployability.
4. Đề xuất phong cách kiến trúc phù hợp: Layered, MVC, Client-Server, Modular Monolith, Microservices, Event-driven, Clean Architecture.
5. Kiến trúc logic: layer/component và trách nhiệm.
6. Kiến trúc module/component: trách nhiệm, actor, dữ liệu, phụ thuộc.
7. Kiến trúc dữ liệu tổng quan.
8. Kiến trúc API và tích hợp.
9. Kiến trúc bảo mật.
10. Kiến trúc triển khai.
11. Đề xuất technology stack và lý do.
12. Phân tích trade-off kiến trúc.
13. Architecture Decision Record cho các quyết định chính.
14. Rủi ro kiến trúc và hướng giảm thiểu.
15. Checklist kiểm tra kiến trúc.

Yêu cầu:
- Viết bằng tiếng Việt.
- Không chọn kiến trúc quá phức tạp nếu dự án nhỏ.
- Không đi sâu sang thiết kế class, database table hoặc code.
```

## Output mong muốn

- Architecture overview
- Drivers
- Quality attributes
- Style recommendation
- Logical architecture
- Modules
- Data/API/Security/Deployment architecture
- Tech stack
- Trade-off
- ADR
- Risks

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

- Chọn kiến trúc theo trend
- Dùng microservices cho dự án nhỏ
- Không xét NFR
- Không có trade-off
- Nhảy vào class/database chi tiết/code
