# Hướng dẫn sử dụng bộ SDLC Prompt Pattern

## 1. Khi nào nên dùng bộ prompt này?

Bạn nên dùng bộ prompt này khi:

- Cần xây dựng tài liệu kỹ thuật phần mềm theo từng giai đoạn SDLC.
- Cần dùng AI để hỗ trợ phân tích, thiết kế, lập trình, kiểm thử hoặc triển khai.
- Cần chuẩn hóa cách hỏi AI để đầu ra có cấu trúc, rõ ràng, dễ đưa vào báo cáo.
- Cần phát triển một repo học thuật hoặc công cụ prompt cho sinh viên kỹ thuật phần mềm.

## 2. Nguyên tắc sử dụng

Không nên dùng tất cả prompt một cách rời rạc. Kết quả của giai đoạn trước nên trở thành đầu vào cho giai đoạn sau.

```text
Giai đoạn 1 → tạo Project Brief
Giai đoạn 2 → dùng Project Brief để tạo Requirements
Giai đoạn 3 → dùng Requirements để phân tích Use Case/Workflow
Giai đoạn 4 → dùng Analysis để đề xuất Architecture
Giai đoạn 5 → dùng Architecture để thiết kế chi tiết
Giai đoạn 6 → dùng Detailed Design để code
Giai đoạn 7 → dùng Requirements + Code để test
Giai đoạn 8 → dùng toàn bộ tài liệu để review bảo mật
Giai đoạn 9 → dùng hệ thống đã hoàn thiện để deploy/bảo trì
```

## 3. Cách chạy một prompt

Mỗi file trong thư mục `prompts/` gồm các phần:

- Mục tiêu
- Khi nào sử dụng
- Input cần cung cấp
- Prompt đầy đủ
- Output mong muốn
- Checklist đánh giá
- Lỗi cần tránh

Bạn chỉ cần copy phần **Prompt đầy đủ**, dán vào AI, sau đó thay các chỗ `[Điền ...]` bằng thông tin dự án.

## 4. Cách dùng với ví dụ Todo List

Ví dụ đầu vào ngắn:

```text
Tên dự án: Todo List Application

Mô tả:
Ứng dụng web giúp người dùng quản lý danh sách công việc cá nhân.

Actor:
- Guest
- Registered User
- Admin

Chức năng:
- Đăng ký tài khoản
- Đăng nhập
- Tạo công việc
- Sửa công việc
- Xóa công việc
- Đánh dấu hoàn thành
- Lọc công việc theo trạng thái
```

Sau đó dùng lần lượt:

1. `01_project_initiation_planning.md`
2. `02_requirements_engineering.md`
3. `03_system_business_analysis.md`
4. ...
5. `09_deployment_operation_maintenance.md`

## 5. Cách đánh giá đầu ra của AI

Đầu ra tốt cần đạt:

- Có cấu trúc rõ ràng.
- Có bảng khi cần.
- Có mã định danh như FR-01, UC-01, TC-01.
- Không trả lời quá chung chung.
- Có giả định nếu thiếu thông tin.
- Có checklist kiểm tra.
- Có liên kết giữa yêu cầu, thiết kế, code và test.

## 6. Lỗi thường gặp khi dùng prompt

| Lỗi | Cách tránh |
|---|---|
| Cung cấp đầu vào quá ít | Điền đầy đủ template đầu vào |
| Dùng prompt code khi chưa có thiết kế | Đi tuần tự qua giai đoạn 1-5 trước |
| Để AI tự thêm quá nhiều chức năng | Ghi rõ phạm vi in-scope/out-of-scope |
| Không kiểm tra đầu ra | Luôn đọc lại, chỉnh sửa và xác nhận |
| Không lưu version tài liệu | Commit từng giai đoạn vào GitHub |

## 7. Khuyến nghị cho báo cáo môn học

Khi viết báo cáo, có thể trình bày bộ prompt theo cấu trúc:

1. Cơ sở lý thuyết về SDLC
2. Cơ sở lý thuyết về Prompt Pattern
3. Thiết kế bộ prompt theo từng giai đoạn
4. Minh họa áp dụng với Todo List Application
5. Đánh giá ưu điểm, hạn chế
6. Kết luận và hướng phát triển
