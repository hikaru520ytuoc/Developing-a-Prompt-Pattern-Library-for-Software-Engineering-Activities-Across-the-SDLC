# SDLC-PP07: Software Testing and Quality Evaluation Prompt Pattern

## Giai đoạn

**Kiểm thử và đánh giá chất lượng**

## Mục tiêu

Tạo test plan, strategy, scenario, test case chức năng/API/UI/NFR/security, coverage plan, bug report, traceability và test summary.

## Khi nào sử dụng?

Sử dụng prompt này khi bạn đang làm đúng giai đoạn **Kiểm thử và đánh giá chất lượng** trong vòng đời phát triển phần mềm và cần AI hỗ trợ tạo tài liệu/kết quả có cấu trúc.

## Input cần cung cấp

- Tên dự án
- Mô tả
- FR/NFR
- Use case
- API
- UI
- Business rules
- Phân quyền
- Entity
- Module đã code
- Môi trường
- Công cụ kiểm thử
- Mức độ chi tiết

## Prompt đầy đủ

```text
Bạn là một chuyên gia kiểm thử phần mềm và đánh giá chất lượng phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 7 của SDLC: Kiểm thử và đánh giá chất lượng phần mềm.

Thông tin dự án:
1. Tên dự án: [Điền]
2. Mô tả hệ thống: [Điền]
3. Yêu cầu chức năng: [Dán FR]
4. Yêu cầu phi chức năng: [Dán NFR]
5. Use case: [Dán UC]
6. API endpoint: [Dán nếu có]
7. Màn hình giao diện: [Dán nếu có]
8. Business rules: [Điền]
9. Phân quyền người dùng: [Điền]
10. Entity/database chính: [Điền]
11. Chức năng/module đã code: [Điền]
12. Môi trường kiểm thử: [Điền]
13. Công cụ kiểm thử dự kiến: [Điền]
14. Mức độ kiểm thử mong muốn: [Cơ bản/Trung bình/Chi tiết]

Hãy tạo tài liệu kiểm thử gồm:
1. Tổng quan kiểm thử.
2. Kế hoạch kiểm thử: mục tiêu, phạm vi, môi trường, dữ liệu, tiêu chí bắt đầu/kết thúc/pass-fail.
3. Chiến lược kiểm thử: unit, integration, API, UI, system, acceptance, regression.
4. Danh sách test scenario theo mã TS-xx.
5. Test case chức năng: ID, Requirement ID, scenario, precondition, test data, steps, expected result, actual result, status.
6. Test case API: method, endpoint, request, response, status code, auth, error case.
7. Test case giao diện: hiển thị, form, button, navigation, loading, error, responsive.
8. Test case phi chức năng: performance, usability, compatibility, reliability, maintainability.
9. Test case bảo mật cơ bản: authentication, authorization, access control, input validation, error handling, file upload.
10. Kế hoạch đo coverage và chất lượng code.
11. Mẫu bug report và ví dụ bug report.
12. Ma trận truy vết yêu cầu-test.
13. Mẫu báo cáo tổng kết kiểm thử.
14. Checklist đánh giá chất lượng phần mềm.
15. Checklist hoàn thành giai đoạn kiểm thử.

Yêu cầu:
- Viết bằng tiếng Việt.
- Test case phải cụ thể, có input và expected result.
- Không tự ý thêm chức năng ngoài phạm vi.
```

## Output mong muốn

- Testing overview
- Test plan
- Test strategy
- Scenarios
- Functional/API/UI/NFR/security tests
- Coverage plan
- Bug template
- Traceability
- Summary report
- Checklist

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

- Test case chung chung
- Chỉ test luồng đúng
- Không expected result
- Không test phân quyền
- Không traceability
- Không bug report
