# SDLC-PP07: Software Testing and Quality Evaluation Prompt Pattern

## Purpose

This prompt supports testing and quality evaluation. It generates test plans, strategies, scenarios, functional/API/UI/non-functional/security test cases, bug report templates, traceability matrix, and test summary report.

## Required input

```text
1. Tên dự án:
2. Mô tả ngắn gọn hệ thống:
3. Danh sách yêu cầu chức năng:
4. Danh sách yêu cầu phi chức năng:
5. Danh sách use case:
6. Danh sách API endpoint:
7. Danh sách màn hình giao diện:
8. Business rules quan trọng:
9. Phân quyền người dùng:
10. Thiết kế database hoặc entity chính:
11. Chức năng/module đã code:
12. Môi trường kiểm thử:
13. Công cụ kiểm thử dự kiến:
14. Mức độ kiểm thử mong muốn:
```

## Official full prompt

```text
Bạn là một chuyên gia kiểm thử phần mềm và đánh giá chất lượng phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 7 của vòng đời phát triển phần mềm SDLC: Kiểm thử và đánh giá chất lượng phần mềm.

Dựa trên thông tin tôi cung cấp, hãy xây dựng tài liệu kiểm thử đầy đủ, bao gồm kế hoạch kiểm thử, chiến lược kiểm thử, test scenario, test case, kiểm thử chức năng, kiểm thử API, kiểm thử giao diện, kiểm thử phi chức năng, kiểm thử bảo mật cơ bản, ma trận truy vết yêu cầu-test và mẫu báo cáo kiểm thử.

Thông tin dự án:

1. Tên dự án:
[Điền tên dự án]

2. Mô tả ngắn gọn hệ thống:
[Mô tả hệ thống cần kiểm thử]

3. Danh sách yêu cầu chức năng:
[Dán danh sách FR]

4. Danh sách yêu cầu phi chức năng:
[Dán danh sách NFR]

5. Danh sách use case:
[Dán danh sách UC hoặc đặc tả use case]

6. Danh sách API endpoint:
[Dán endpoint, method, request, response nếu có]

7. Danh sách màn hình giao diện:
[Dán các màn hình UI đã thiết kế]

8. Business rules quan trọng:
[Dán các quy tắc nghiệp vụ]

9. Phân quyền người dùng:
[Dán role và quyền hạn]

10. Thiết kế database hoặc entity chính:
[Dán entity/bảng chính nếu có]

11. Chức năng/module đã code:
[Dán module đã hiện thực]

12. Môi trường kiểm thử:
[Ví dụ: local, staging, Docker, Chrome, PostgreSQL test database...]

13. Công cụ kiểm thử dự kiến:
[Ví dụ: JUnit, Pytest, Jest, Postman, Newman, Selenium, Cypress...]

14. Mức độ kiểm thử mong muốn:
[Ví dụ: cơ bản, trung bình, chi tiết cho báo cáo môn học]

Yêu cầu đầu ra:

1. Tổng quan kiểm thử
- Tóm tắt mục tiêu, phạm vi và ngoài phạm vi kiểm thử.
- Ghi rõ giả định nếu thông tin đầu vào còn thiếu.

2. Kế hoạch kiểm thử
- Xác định mục tiêu, phạm vi, môi trường kiểm thử, dữ liệu kiểm thử, người thực hiện nếu cần.
- Nêu tiêu chí bắt đầu, tiêu chí kết thúc và tiêu chí pass/fail.

3. Chiến lược kiểm thử
- Đề xuất unit, integration, API, UI, system, acceptance, regression testing.
- Với mỗi mức, nêu mục tiêu và thành phần cần kiểm thử.

4. Danh sách test scenario
- Tạo các scenario cho chức năng quan trọng.
- Mỗi scenario có mã TS-xx, tên tình huống, mục tiêu và yêu cầu liên quan.
- Bao gồm luồng thành công, luồng thay thế và luồng ngoại lệ.

5. Test case chức năng
- Tạo test case chi tiết cho yêu cầu chức năng.
- Mỗi test case gồm: Test Case ID, Requirement ID, Scenario, Preconditions, Test Data, Test Steps, Expected Result, Actual Result, Status.
- Bao gồm test case hợp lệ và không hợp lệ.

6. Test case API
- Nếu hệ thống có API, tạo test case cho các endpoint quan trọng.
- Kiểm tra method, endpoint, request body, response body, status code, authentication, authorization và error case.

7. Test case giao diện người dùng
- Tạo test case cho các màn hình chính.
- Kiểm tra hiển thị dữ liệu, form validation, button/action, navigation, loading state, error display và responsive nếu cần.

8. Test case phi chức năng
- Tạo test case cho performance, usability, compatibility, reliability, maintainability nếu phù hợp.
- Mỗi test case cần có tiêu chí đánh giá rõ ràng.

9. Test case bảo mật cơ bản
- Tạo test case kiểm tra authentication, authorization, access control, input validation, error handling, password security và file upload nếu có.

10. Kế hoạch đo coverage và chất lượng code
- Đề xuất statement, branch, function, requirement coverage.
- Đề xuất complexity, duplication, maintainability, naming, dependency.
- Nêu mục tiêu coverage hợp lý.

11. Mẫu báo cáo lỗi
- Tạo template bug report gồm: Bug ID, Title, Severity, Priority, Environment, Preconditions, Steps to Reproduce, Expected Result, Actual Result, Evidence, Assignee, Status.
- Đưa ra ví dụ một bug report mẫu.

12. Ma trận truy vết yêu cầu-test
- Tạo bảng liên kết Requirement ID với Test Case ID.
- Mỗi yêu cầu quan trọng phải có ít nhất một test case tương ứng.
- Chỉ ra yêu cầu nào chưa có test case nếu có.

13. Mẫu báo cáo tổng kết kiểm thử
- Tạo cấu trúc test summary report gồm tổng số test case, pass/fail/blocked/not run, pass rate, lỗi, coverage và khuyến nghị release.

14. Checklist đánh giá chất lượng phần mềm
- Tạo checklist theo functionality, reliability, usability, performance, security, maintainability, compatibility.

15. Checklist hoàn thành giai đoạn kiểm thử
- Bao gồm test plan, test case, execution, bug report, retest, regression test, traceability và summary.

Yêu cầu trình bày:
- Viết bằng tiếng Việt.
- Văn phong học thuật, rõ ràng, phù hợp với báo cáo môn học kỹ thuật phần mềm.
- Ưu tiên trình bày bằng bảng khi phù hợp.
- Test case phải cụ thể, có input và expected result.
- Không viết test case quá chung chung.
- Nếu thiếu thông tin, hãy nêu giả định hợp lý.
- Không tự ý thêm chức năng ngoài phạm vi hệ thống.
```

## Expected output

- Testing overview.
- Test plan.
- Test strategy.
- Test scenario list.
- Functional test cases.
- API test cases.
- UI test cases.
- Non-functional test cases.
- Security test cases.
- Coverage plan.
- Bug report template.
- Requirement-test traceability matrix.
- Test summary report template.
- Quality evaluation checklist.
- Testing completion checklist.

## Quality checklist

| Criteria | Yes/No |
|---|---|
| Test plan and strategy are included. |  |
| Test scenarios include success and failure flows. |  |
| Test cases have preconditions, data, steps, expected result. |  |
| API, UI, non-functional, and security tests are covered where applicable. |  |
| Bug report template is included. |  |
| Requirement-test traceability is included. |  |
| Test summary template is included. |  |

## Common mistakes to avoid

- Only testing happy paths.
- Missing expected results.
- Missing test data.
- Not linking tests to requirements.
- Ignoring security and authorization tests.
