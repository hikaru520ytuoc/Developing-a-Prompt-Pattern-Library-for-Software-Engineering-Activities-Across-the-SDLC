# SDLC Prompt Pattern Library

> Bộ thư viện Prompt Pattern hỗ trợ phát triển phần mềm theo từng giai đoạn của vòng đời SDLC.

Repo này cung cấp một bộ prompt có cấu trúc dành cho sinh viên/kỹ sư phần mềm khi cần dùng AI hỗ trợ các hoạt động trong phát triển phần mềm: khởi tạo dự án, yêu cầu, phân tích nghiệp vụ, kiến trúc, thiết kế chi tiết, lập trình, kiểm thử, bảo mật, triển khai và bảo trì.

## Mục tiêu

Bộ prompt này giúp người dùng:

- Chuyển ý tưởng phần mềm thành tài liệu kỹ thuật có cấu trúc.
- Chuẩn hóa đầu vào và đầu ra khi dùng AI trong các giai đoạn SDLC.
- Hạn chế việc AI trả lời chung chung, thiếu kiểm chứng hoặc nhảy bước.
- Tạo nền tảng tài liệu cho báo cáo môn học, đồ án hoặc dự án cá nhân.
- Hỗ trợ truy vết từ yêu cầu → phân tích → thiết kế → code → test → triển khai.

## 9 Prompt Pattern chính

| Mã | Giai đoạn SDLC | File |
|---|---|---|
| SDLC-PP01 | Khởi tạo và lập kế hoạch dự án | [`prompts/01_project_initiation_planning.md`](prompts/01_project_initiation_planning.md) |
| SDLC-PP02 | Thu thập và quản lý yêu cầu | [`prompts/02_requirements_engineering.md`](prompts/02_requirements_engineering.md) |
| SDLC-PP03 | Phân tích hệ thống và nghiệp vụ | [`prompts/03_system_business_analysis.md`](prompts/03_system_business_analysis.md) |
| SDLC-PP04 | Kiến trúc phần mềm | [`prompts/04_software_architecture.md`](prompts/04_software_architecture.md) |
| SDLC-PP05 | Thiết kế chi tiết | [`prompts/05_detailed_design.md`](prompts/05_detailed_design.md) |
| SDLC-PP06 | Hiện thực / lập trình | [`prompts/06_implementation_coding.md`](prompts/06_implementation_coding.md) |
| SDLC-PP07 | Kiểm thử và đánh giá chất lượng | [`prompts/07_testing_quality_evaluation.md`](prompts/07_testing_quality_evaluation.md) |
| SDLC-PP08 | An toàn, bảo mật và tuân thủ | [`prompts/08_security_safety_compliance.md`](prompts/08_security_safety_compliance.md) |
| SDLC-PP09 | Triển khai, vận hành, bảo trì và cải tiến | [`prompts/09_deployment_operation_maintenance.md`](prompts/09_deployment_operation_maintenance.md) |

## Cấu trúc repo

```text
sdlc-prompt-pattern-library/
│
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── .gitignore
│
├── prompts/
│   ├── 01_project_initiation_planning.md
│   ├── 02_requirements_engineering.md
│   ├── 03_system_business_analysis.md
│   ├── 04_software_architecture.md
│   ├── 05_detailed_design.md
│   ├── 06_implementation_coding.md
│   ├── 07_testing_quality_evaluation.md
│   ├── 08_security_safety_compliance.md
│   └── 09_deployment_operation_maintenance.md
│
├── docs/
│   ├── usage_guide.md
│   ├── sdlc_overview.md
│   ├── prompt_pattern_format.md
│   └── github_push_guide.md
│
├── examples/
│   └── todo_list_example.md
│
└── templates/
    ├── project_input_template.md
    └── prompt_output_template.md
```

## Cách sử dụng nhanh

1. Đọc [`docs/usage_guide.md`](docs/usage_guide.md).
2. Chuẩn bị thông tin dự án theo [`templates/project_input_template.md`](templates/project_input_template.md).
3. Chọn prompt tương ứng với giai đoạn SDLC trong thư mục `prompts/`.
4. Thay các phần `[Điền thông tin]` bằng dữ liệu dự án.
5. Dùng kết quả đầu ra của giai đoạn trước làm đầu vào cho giai đoạn sau.
6. Tham khảo ví dụ Todo List tại [`examples/todo_list_example.md`](examples/todo_list_example.md).

## Ví dụ dự án minh họa

Repo dùng ví dụ chung là **Todo List Application** để tránh phụ thuộc vào một lĩnh vực cụ thể.

Ví dụ này phù hợp vì gần như mọi người đều hiểu:

- Người dùng tạo công việc.
- Người dùng sửa/xóa công việc.
- Người dùng đánh dấu hoàn thành.
- Người dùng lọc công việc theo trạng thái.
- Hệ thống cần đăng nhập nếu có nhiều tài khoản.

## Lưu ý

Bộ prompt này không thay thế hoàn toàn chuyên gia kỹ thuật phần mềm. Người dùng cần đọc, kiểm tra, chỉnh sửa và xác nhận lại đầu ra của AI trước khi dùng trong báo cáo hoặc dự án thật.

## Gợi ý tên đề tài

**Xây dựng thư viện Prompt Pattern hỗ trợ kỹ nghệ phần mềm theo các giai đoạn của vòng đời phát triển phần mềm SDLC**
