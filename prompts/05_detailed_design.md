# SDLC-PP05: Detailed Software Design Prompt Pattern

## Giai đoạn

**Thiết kế chi tiết**

## Mục tiêu

Thiết kế module, database/schema, API, UI, class/service/component, sequence flow, validation, error handling, authorization và requirement-design mapping.

## Khi nào sử dụng?

Sử dụng prompt này khi bạn đang làm đúng giai đoạn **Thiết kế chi tiết** trong vòng đời phát triển phần mềm và cần AI hỗ trợ tạo tài liệu/kết quả có cấu trúc.

## Input cần cung cấp

- Tên dự án
- Mô tả
- FR/NFR
- Actor/role
- Use case
- Kiến trúc
- Module
- Entity
- Business rules
- Công nghệ
- Chức năng cần thiết kế

## Prompt đầy đủ

```text
Bạn là một chuyên gia thiết kế phần mềm chi tiết.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 5 của SDLC: Thiết kế chi tiết phần mềm.

Thông tin dự án:
1. Tên dự án: [Điền]
2. Mô tả ngắn gọn hệ thống: [Điền]
3. Yêu cầu chức năng: [Dán FR]
4. Yêu cầu phi chức năng: [Dán NFR]
5. Actor và phân quyền: [Điền]
6. Use case quan trọng: [Dán UC]
7. Kiến trúc phần mềm đã chọn: [Điền]
8. Module/component: [Điền]
9. Entity nghiệp vụ: [Điền]
10. Business rules: [Điền]
11. Công nghệ dự kiến: [Điền]
12. Chức năng cần thiết kế chi tiết: [Điền]

Hãy tạo tài liệu thiết kế chi tiết gồm:
1. Tổng quan thiết kế chi tiết.
2. Thiết kế module chi tiết: trách nhiệm, chức năng con, actor, dữ liệu, API, phụ thuộc.
3. Thiết kế database/schema: bảng, field, type, PK, FK, constraint, relationship.
4. Thiết kế API: method, endpoint, role, request, response, status code, error case.
5. Thiết kế giao diện: màn hình, actor, thành phần UI, dữ liệu hiển thị, hành động, validation, điều hướng.
6. Thiết kế class/service/component: controller, service, repository, DTO, entity, component.
7. Thiết kế sequence flow cho chức năng quan trọng.
8. Thiết kế validation: input, form, API, business rule.
9. Thiết kế xử lý lỗi: error code, HTTP status nếu có, message, handling.
10. Ma trận phân quyền chi tiết và ownership check.
11. Mapping yêu cầu với thiết kế: Requirement ID, Use Case, Module, API, UI Screen, Test Case dự kiến.
12. Checklist kiểm tra thiết kế chi tiết.

Yêu cầu:
- Viết bằng tiếng Việt.
- Chỉ thiết kế, chưa viết code triển khai.
- Bám sát yêu cầu, use case và kiến trúc.
- Không tự ý thêm chức năng lớn ngoài phạm vi.
```

## Output mong muốn

- Detailed design overview
- Module design
- Database design
- API design
- UI design
- Class/service design
- Sequence flow
- Validation
- Error handling
- Authorization matrix
- Mapping

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

- Thiết kế lệch yêu cầu
- API thiếu request/response/error
- UI không mô tả hành vi
- Không validation/error handling
- Viết code quá sớm
