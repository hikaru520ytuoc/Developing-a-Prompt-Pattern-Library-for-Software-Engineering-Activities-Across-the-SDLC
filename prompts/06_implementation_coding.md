# SDLC-PP06: Implementation and Coding Prompt Pattern

## Giai đoạn

**Hiện thực / lập trình**

## Mục tiêu

Chuyển thiết kế thành mã nguồn có cấu trúc, bám kiến trúc, có validation, error handling, security cơ bản, unit test và hướng dẫn chạy.

## Khi nào sử dụng?

Sử dụng prompt này khi bạn đang làm đúng giai đoạn **Hiện thực / lập trình** trong vòng đời phát triển phần mềm và cần AI hỗ trợ tạo tài liệu/kết quả có cấu trúc.

## Input cần cung cấp

- Tên dự án
- Mô tả
- Kiến trúc
- Công nghệ
- Schema/API/UI
- Module cần code
- Business rules
- Validation/error
- Phân quyền
- Chức năng cụ thể
- Style code
- Test/README/Docker

## Prompt đầy đủ

```text
Bạn là một kỹ sư phần mềm có kinh nghiệm hiện thực hệ thống theo đúng kiến trúc và thiết kế chi tiết.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 6 của SDLC: Hiện thực và lập trình phần mềm.

Thông tin dự án:
1. Tên dự án: [Điền]
2. Mô tả ngắn gọn hệ thống: [Điền]
3. Kiến trúc đã chọn: [Điền]
4. Công nghệ sử dụng: [Điền]
5. Database/schema: [Dán nếu có]
6. API đã thiết kế: [Dán nếu có]
7. Màn hình UI: [Dán nếu có]
8. Module/service cần code: [Điền]
9. Business rules: [Điền]
10. Validation và error case: [Điền]
11. Phân quyền người dùng: [Điền]
12. Chức năng cụ thể muốn hiện thực: [Điền]
13. Yêu cầu style code/cấu trúc thư mục: [Điền]
14. Có cần unit test, README, Docker không: [Điền]

Hãy tạo kết quả hiện thực gồm:
1. Tổng quan module/chức năng được code.
2. Thiết lập môi trường phát triển.
3. Cấu trúc thư mục đề xuất.
4. Hiện thực database/entity/model/repository nếu cần.
5. Hiện thực backend/API theo kiến trúc phù hợp.
6. Hiện thực frontend/UI nếu cần.
7. Hiện thực business logic theo business rules.
8. Hiện thực validation ở frontend/backend/service nếu phù hợp.
9. Hiện thực xử lý lỗi thống nhất.
10. Hiện thực bảo mật/phân quyền cơ bản.
11. Unit test hoặc test cơ bản cho logic quan trọng.
12. Code review/refactor checklist.
13. README/run guide.
14. Checklist hoàn thành giai đoạn code.

Yêu cầu:
- Viết bằng tiếng Việt.
- Code rõ ràng, dễ chạy, có comment ngắn ở phần quan trọng.
- Nếu có nhiều file, trình bày theo từng file.
- Không hard-code secret/password/API key.
- Không tự ý thêm chức năng lớn ngoài phạm vi.
```

## Output mong muốn

- Implementation overview
- Environment setup
- Folder structure
- Database/entity
- Backend/API
- Frontend/UI
- Business logic
- Validation
- Error handling
- Security
- Unit tests
- README

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

- Code không bám thiết kế
- Logic trong controller/UI
- Không validation
- Không phân quyền
- Hard-code secret
- Không README/test
