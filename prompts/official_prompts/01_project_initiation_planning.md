# SDLC-PP01: Project Initiation and Planning Prompt Pattern

## Purpose

This prompt supports the first SDLC stage. It helps transform an early software idea into a clear project initiation document, including project context, problem statement, objectives, scope, stakeholders, initial features, risks, development model, and initial plan.

## Required input

```text
1. Tên hoặc ý tưởng dự án:
2. Lĩnh vực của dự án:
3. Đối tượng sử dụng chính:
4. Vấn đề hiện tại cần giải quyết:
5. Mục tiêu mong muốn:
6. Các chức năng dự kiến:
7. Công nghệ dự kiến sử dụng:
8. Quy mô nhóm phát triển:
9. Thời gian thực hiện:
10. Ràng buộc đặc biệt:
```

## Official full prompt

```text
Bạn là một chuyên gia phân tích và quản lý dự án phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 1 của vòng đời phát triển phần mềm SDLC: Khởi tạo và lập kế hoạch dự án.

Dựa trên thông tin tôi cung cấp, hãy phân tích và tạo ra tài liệu khởi tạo dự án phần mềm một cách rõ ràng, có cấu trúc và phù hợp với ngành kỹ thuật phần mềm.

Thông tin dự án:

1. Tên hoặc ý tưởng dự án:
[Điền tên hoặc ý tưởng dự án]

2. Lĩnh vực của dự án:
[Ví dụ: giáo dục, y tế, thương mại điện tử, quản lý nội bộ, tài chính, logistics...]

3. Đối tượng sử dụng chính:
[Ví dụ: người dùng cá nhân, nhân viên, khách hàng, quản trị viên...]

4. Vấn đề hiện tại cần giải quyết:
[Mô tả vấn đề, khó khăn hoặc hạn chế của quy trình hiện tại]

5. Mục tiêu mong muốn:
[Mô tả kết quả mong muốn khi xây dựng phần mềm]

6. Các chức năng dự kiến:
[Liệt kê các chức năng ban đầu nếu đã có]

7. Công nghệ dự kiến sử dụng:
[Ví dụ: Java, Spring Boot, React, Flutter, MySQL, Firebase... Nếu chưa có thì ghi “chưa xác định”]

8. Quy mô nhóm phát triển:
[Số lượng thành viên, vai trò nếu có]

9. Thời gian thực hiện:
[Ví dụ: 4 tuần, 8 tuần, 1 học kỳ...]

10. Ràng buộc đặc biệt:
[Ví dụ: phải có báo cáo, phải có sơ đồ UML, chỉ làm web app, không làm mobile app...]

Yêu cầu đầu ra:

Hãy trình bày kết quả theo các phần sau:

1. Tổng quan dự án
- Mô tả ngắn gọn dự án.
- Nêu bối cảnh ra đời của dự án.
- Giải thích vì sao dự án cần được thực hiện.

2. Phát biểu vấn đề
- Mô tả vấn đề hiện tại.
- Nêu đối tượng bị ảnh hưởng.
- Nêu hậu quả nếu không có hệ thống phần mềm hỗ trợ.

3. Mục tiêu dự án
- Mục tiêu nghiệp vụ.
- Mục tiêu người dùng.
- Mục tiêu kỹ thuật.

4. Phạm vi dự án
- Các chức năng nằm trong phạm vi thực hiện.
- Các chức năng ngoài phạm vi.
- Giả định ban đầu.
- Ràng buộc của dự án.

5. Stakeholder
- Liệt kê các bên liên quan.
- Mô tả vai trò, nhu cầu và mức độ ảnh hưởng của từng bên.

6. Danh sách chức năng sơ bộ
- Nhóm các chức năng chính của hệ thống.
- Mô tả ngắn gọn từng nhóm chức năng.
- Phân loại chức năng theo mức độ ưu tiên: Must-have, Should-have, Could-have.

7. Mô hình phát triển phần mềm đề xuất
- Đề xuất mô hình phát triển phù hợp.
- Giải thích lý do lựa chọn.
- Nêu cách áp dụng mô hình đó vào dự án.

8. Rủi ro ban đầu
- Liệt kê các rủi ro về yêu cầu, kỹ thuật, tiến độ, dữ liệu, bảo mật và vận hành.
- Với mỗi rủi ro, hãy nêu mức độ ảnh hưởng và hướng xử lý đề xuất.

9. Kế hoạch triển khai sơ bộ
- Chia dự án thành các mốc công việc chính.
- Với mỗi mốc, nêu công việc cần làm và sản phẩm đầu ra.
- Trình bày dưới dạng bảng.

10. Checklist hoàn thành giai đoạn khởi tạo
- Liệt kê các tiêu chí để đánh giá giai đoạn 1 đã hoàn thành.
- Checklist phải rõ ràng, có thể kiểm tra được.

Yêu cầu trình bày:
- Viết bằng tiếng Việt.
- Văn phong học thuật, rõ ràng, phù hợp với báo cáo môn học kỹ thuật phần mềm.
- Không viết quá chung chung.
- Nếu thông tin đầu vào còn thiếu, hãy tự đưa ra giả định hợp lý và ghi rõ phần giả định.
- Không đi sâu sang giai đoạn thiết kế chi tiết hoặc lập trình.
```

## Expected output

- Project overview.
- Problem statement.
- Project objectives.
- Project scope.
- Stakeholder list.
- Preliminary features.
- Recommended development model.
- Initial risk list.
- Initial project plan.
- Completion checklist.

## Quality checklist

| Criteria | Yes/No |
|---|---|
| Problem context is clear. |  |
| Objectives are separated into business, user, and technical objectives. |  |
| In-scope and out-of-scope are defined. |  |
| Stakeholders are identified. |  |
| Initial features are prioritized. |  |
| Risks and mitigation actions are included. |  |
| Initial plan is realistic. |  |

## Common mistakes to avoid

- Describing the project too generally.
- Mixing objectives with features.
- Skipping out-of-scope items.
- Ignoring stakeholders and risks.
- Jumping directly to coding.
