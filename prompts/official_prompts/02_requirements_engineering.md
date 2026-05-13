# SDLC-PP02: Requirements Engineering Prompt Pattern

## Purpose

This prompt supports the requirements engineering stage. It turns project ideas, stakeholder needs, and business rules into structured, testable, prioritized, and traceable software requirements.

## Required input

```text
1. Tên dự án:
2. Mô tả ngắn gọn dự án:
3. Danh sách actor/người dùng dự kiến:
4. Quy trình nghiệp vụ hiện tại nếu có:
5. Các chức năng mong muốn ban đầu:
6. Các vấn đề đang gặp phải:
7. Các quy định hoặc điều kiện nghiệp vụ:
8. Các yêu cầu kỹ thuật nếu có:
9. Các ràng buộc về thời gian, công nghệ, nhân lực:
10. Mức độ chi tiết mong muốn của tài liệu yêu cầu:
```

## Official full prompt

```text
Bạn là một chuyên gia phân tích yêu cầu phần mềm trong lĩnh vực kỹ thuật phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 2 của vòng đời phát triển phần mềm SDLC: Thu thập và quản lý yêu cầu phần mềm.

Dựa trên thông tin tôi cung cấp, hãy phân tích, chuẩn hóa và tổ chức lại yêu cầu phần mềm thành một tài liệu rõ ràng, có cấu trúc, có thể dùng cho các giai đoạn phân tích, thiết kế, lập trình và kiểm thử sau này.

Thông tin dự án:

1. Tên dự án:
[Điền tên dự án]

2. Mô tả ngắn gọn dự án:
[Mô tả hệ thống cần xây dựng]

3. Danh sách actor/người dùng dự kiến:
[Ví dụ: Guest, User, Admin, Customer, Employee...]

4. Quy trình nghiệp vụ hiện tại:
[Mô tả cách công việc đang được thực hiện hiện nay. Nếu chưa có thì ghi “chưa xác định”]

5. Các chức năng mong muốn ban đầu:
[Liệt kê các chức năng người dùng mong muốn]

6. Các vấn đề đang gặp phải:
[Mô tả các khó khăn, lỗi, điểm bất tiện hoặc hạn chế của quy trình hiện tại]

7. Các quy định hoặc điều kiện nghiệp vụ:
[Ví dụ: mỗi người dùng chỉ được xem dữ liệu của mình, chỉ admin được khóa tài khoản...]

8. Yêu cầu kỹ thuật nếu có:
[Ví dụ: web app, mobile app, dùng MySQL, dùng Spring Boot, dùng React...]

9. Ràng buộc về thời gian, công nghệ, nhân lực:
[Mô tả ràng buộc nếu có]

10. Mức độ chi tiết mong muốn:
[Ví dụ: cơ bản, trung bình, chi tiết cho báo cáo môn học]

Yêu cầu đầu ra:

Hãy tạo tài liệu yêu cầu phần mềm với các phần sau:

1. Tổng quan yêu cầu
- Tóm tắt mục tiêu của hệ thống.
- Mô tả phạm vi yêu cầu trong giai đoạn này.
- Nêu các giả định nếu thông tin đầu vào còn thiếu.

2. Danh sách actor và vai trò
- Liệt kê tất cả actor tham gia hệ thống.
- Với mỗi actor, mô tả vai trò, quyền hạn và nhu cầu chính.
- Phân biệt actor chính và actor phụ nếu cần.

3. Yêu cầu chức năng
- Liệt kê các yêu cầu chức năng theo mã FR-01, FR-02, FR-03...
- Mỗi yêu cầu cần viết rõ: actor, hành động, dữ liệu đầu vào, kết quả đầu ra.
- Trình bày dưới dạng bảng gồm: mã yêu cầu, tên yêu cầu, mô tả, actor liên quan, mức ưu tiên.

4. Yêu cầu phi chức năng
- Liệt kê các yêu cầu phi chức năng theo mã NFR-01, NFR-02...
- Bao gồm các nhóm: hiệu năng, bảo mật, phân quyền, khả dụng, dễ sử dụng, tương thích, bảo trì.
- Mỗi yêu cầu cần có tiêu chí đo hoặc điều kiện đánh giá nếu có thể.

5. Quy tắc nghiệp vụ
- Liệt kê các business rules theo mã BR-01, BR-02...
- Mỗi quy tắc phải rõ ràng, tránh mơ hồ.
- Ghi rõ quy tắc đó ảnh hưởng đến chức năng nào.

6. User story
- Viết user story cho từng actor chính.
- Dùng cấu trúc: “Là một [vai trò], tôi muốn [chức năng], để [mục đích].”
- Mỗi user story cần có mã US-01, US-02...

7. Acceptance criteria
- Với mỗi user story hoặc yêu cầu quan trọng, hãy viết tiêu chí chấp nhận.
- Có thể trình bày theo dạng Given–When–Then hoặc checklist.
- Tiêu chí phải đủ rõ để chuyển thành test case.

8. Ưu tiên yêu cầu
- Phân loại yêu cầu theo MoSCoW: Must-have, Should-have, Could-have, Won’t-have.
- Giải thích ngắn gọn lý do ưu tiên.

9. Phát hiện yêu cầu thiếu, mơ hồ hoặc xung đột
- Chỉ ra các yêu cầu chưa rõ.
- Chỉ ra thông tin còn thiếu.
- Chỉ ra điểm có thể gây xung đột.
- Đề xuất câu hỏi cần hỏi lại stakeholder.

10. Ma trận truy vết yêu cầu sơ bộ
- Tạo bảng gồm: Requirement ID, User Story, Use Case dự kiến, Module dự kiến, Test Case dự kiến.
- Nếu chưa đủ thông tin, hãy ghi “cần xác định ở giai đoạn sau”.

11. Checklist kiểm tra chất lượng yêu cầu
- Tạo checklist để đánh giá tài liệu yêu cầu đã đủ rõ chưa.
- Checklist cần kiểm tra: rõ ràng, đầy đủ, nhất quán, có thể kiểm thử, có thể thực hiện, có thể truy vết.

Yêu cầu trình bày:
- Viết bằng tiếng Việt.
- Văn phong học thuật, rõ ràng, phù hợp với báo cáo môn học kỹ thuật phần mềm.
- Ưu tiên trình bày bằng bảng khi phù hợp.
- Không viết yêu cầu quá chung chung.
- Không tự ý thêm chức năng lớn ngoài phạm vi dự án nếu chưa có cơ sở.
- Nếu thông tin đầu vào thiếu, hãy nêu giả định rõ ràng.
- Không đi sâu sang thiết kế database, kiến trúc hoặc code ở giai đoạn này.
```

## Expected output

- Requirement overview.
- Actor list.
- Functional requirements.
- Non-functional requirements.
- Business rules.
- User stories.
- Acceptance criteria.
- Requirement priority.
- Missing/ambiguous/conflicting requirements.
- Requirement traceability matrix.
- Requirement validation checklist.

## Quality checklist

| Criteria | Yes/No |
|---|---|
| Actors and roles are clear. |  |
| Functional requirements are numbered and testable. |  |
| Non-functional requirements are measurable where possible. |  |
| Business rules are included. |  |
| User stories and acceptance criteria are included. |  |
| Requirements are prioritized. |  |
| Ambiguities and missing information are identified. |  |
| Traceability matrix is included. |  |

## Common mistakes to avoid

- Writing vague requirements.
- Confusing requirements with technical solutions.
- Missing acceptance criteria.
- Ignoring business rules.
- Adding out-of-scope features.
