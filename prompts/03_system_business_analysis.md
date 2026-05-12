# SDLC-PP03: System and Business Analysis Prompt Pattern

## Giai đoạn

**Phân tích hệ thống và nghiệp vụ**

## Mục tiêu

Phân tích actor, quyền, quy trình hiện tại/đề xuất, use case, activity flow, dữ liệu, entity nghiệp vụ, trạng thái, business rules và ngoại lệ.

## Khi nào sử dụng?

Sử dụng prompt này khi bạn đang làm đúng giai đoạn **Phân tích hệ thống và nghiệp vụ** trong vòng đời phát triển phần mềm và cần AI hỗ trợ tạo tài liệu/kết quả có cấu trúc.

## Input cần cung cấp

- Tên dự án
- Mô tả
- Actor
- FR/NFR
- Business rules
- Quy trình hiện tại
- Quy trình mong muốn
- Chức năng quan trọng
- Ngoại lệ/ràng buộc

## Prompt đầy đủ

```text
Bạn là một chuyên gia phân tích hệ thống và phân tích nghiệp vụ.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 3 của SDLC: Phân tích hệ thống và nghiệp vụ.

Thông tin dự án:
1. Tên dự án: [Điền]
2. Mô tả ngắn gọn dự án: [Điền]
3. Danh sách actor: [Điền]
4. Danh sách yêu cầu chức năng: [Dán FR nếu có]
5. Danh sách yêu cầu phi chức năng: [Dán NFR nếu có]
6. Business rules đã biết: [Điền]
7. Quy trình nghiệp vụ hiện tại: [Điền]
8. Quy trình nghiệp vụ mong muốn: [Điền]
9. Chức năng quan trọng cần phân tích chi tiết: [Điền]
10. Ràng buộc hoặc ngoại lệ cần chú ý: [Điền]

Hãy tạo tài liệu phân tích hệ thống và nghiệp vụ gồm:
1. Tổng quan phân tích.
2. Phân tích actor và quyền tương tác.
3. Quy trình nghiệp vụ hiện tại: bước, người thực hiện, input, output, vấn đề.
4. Quy trình nghiệp vụ đề xuất: bước, vai trò hệ thống/người dùng, cải tiến.
5. Danh sách use case theo mã UC-01, UC-02..., actor, mục tiêu, mô tả, quan hệ include/extend nếu có.
6. Đặc tả use case quan trọng: tiền điều kiện, hậu điều kiện, luồng chính, luồng thay thế, luồng ngoại lệ, business rules.
7. Mô tả activity diagram bằng text, có start, action, decision, branch, end, swimlane nếu phù hợp.
8. Phân tích luồng dữ liệu sơ bộ.
9. Phân tích entity nghiệp vụ và thuộc tính sơ bộ.
10. Phân tích trạng thái đối tượng và điều kiện chuyển trạng thái.
11. Phân tích business rules chi tiết.
12. Phân tích ngoại lệ và tình huống biên.
13. Checklist kiểm tra kết quả phân tích.

Yêu cầu:
- Viết bằng tiếng Việt.
- Không thiết kế database vật lý hoặc code.
- Nếu thiếu thông tin, hãy nêu giả định hợp lý.
```

## Output mong muốn

- Analysis overview
- Actor interaction
- Current process
- Proposed process
- Use case list/spec
- Activity flow
- Data flow
- Business entity
- State analysis
- Exceptions

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

- Chỉ liệt kê chức năng
- Nhầm use case với màn hình
- Không có luồng ngoại lệ
- Không phân tích trạng thái
- Đi sớm vào database vật lý/code
