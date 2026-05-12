# SDLC-PP01: Project Initiation and Planning Prompt Pattern

## Giai đoạn

**Khởi tạo và lập kế hoạch dự án**

## Mục tiêu

Biến ý tưởng phần mềm ban đầu thành tài liệu khởi tạo dự án: bối cảnh, vấn đề, mục tiêu, phạm vi, stakeholder, rủi ro và kế hoạch sơ bộ.

## Khi nào sử dụng?

Sử dụng prompt này khi bạn đang làm đúng giai đoạn **Khởi tạo và lập kế hoạch dự án** trong vòng đời phát triển phần mềm và cần AI hỗ trợ tạo tài liệu/kết quả có cấu trúc.

## Input cần cung cấp

- Tên hoặc ý tưởng dự án
- Lĩnh vực của dự án
- Đối tượng sử dụng chính
- Vấn đề hiện tại cần giải quyết
- Mục tiêu mong muốn
- Chức năng dự kiến
- Công nghệ dự kiến
- Quy mô nhóm
- Thời gian thực hiện
- Ràng buộc đặc biệt

## Prompt đầy đủ

```text
Bạn là một chuyên gia phân tích và quản lý dự án phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 1 của SDLC: Khởi tạo và lập kế hoạch dự án.

Thông tin dự án:
1. Tên hoặc ý tưởng dự án: [Điền]
2. Lĩnh vực của dự án: [Điền]
3. Đối tượng sử dụng chính: [Điền]
4. Vấn đề hiện tại cần giải quyết: [Điền]
5. Mục tiêu mong muốn: [Điền]
6. Các chức năng dự kiến: [Điền]
7. Công nghệ dự kiến sử dụng: [Điền hoặc ghi chưa xác định]
8. Quy mô nhóm phát triển: [Điền]
9. Thời gian thực hiện: [Điền]
10. Ràng buộc đặc biệt: [Điền]

Hãy tạo tài liệu khởi tạo dự án gồm:
1. Tổng quan dự án.
2. Phát biểu vấn đề.
3. Mục tiêu dự án, chia thành mục tiêu nghiệp vụ, người dùng và kỹ thuật.
4. Phạm vi dự án: in-scope, out-of-scope, giả định, ràng buộc.
5. Stakeholder: vai trò, nhu cầu, mức độ ảnh hưởng.
6. Danh sách chức năng sơ bộ, phân loại Must-have, Should-have, Could-have, Won’t-have.
7. Mô hình phát triển phần mềm đề xuất và lý do lựa chọn.
8. Rủi ro ban đầu: yêu cầu, kỹ thuật, tiến độ, dữ liệu, bảo mật, vận hành.
9. Kế hoạch triển khai sơ bộ theo mốc công việc.
10. Checklist hoàn thành giai đoạn khởi tạo.

Yêu cầu:
- Viết bằng tiếng Việt.
- Trình bày rõ ràng, ưu tiên bảng khi phù hợp.
- Phù hợp với báo cáo môn học kỹ thuật phần mềm.
- Nếu thiếu thông tin, hãy nêu giả định hợp lý.
- Không đi sâu sang thiết kế chi tiết hoặc lập trình.
```

## Output mong muốn

- Tổng quan dự án
- Phát biểu vấn đề
- Mục tiêu dự án
- Phạm vi dự án
- Stakeholder
- Chức năng sơ bộ
- Mô hình phát triển đề xuất
- Rủi ro ban đầu
- Kế hoạch triển khai sơ bộ
- Checklist hoàn thành

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

- Mô tả dự án quá chung chung
- Không xác định phạm vi
- Không xác định stakeholder
- Nhầm mục tiêu với chức năng
- Đi thẳng vào code
- Không ghi giả định khi thiếu thông tin
