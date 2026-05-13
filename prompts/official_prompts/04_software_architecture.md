# SDLC-PP04: Software Architecture Prompt Pattern

## Purpose

This prompt supports architecture design. It helps choose the architecture style, logical structure, modules, data architecture, API/integration approach, security architecture, deployment view, technology stack, trade-offs, ADRs, and architecture risks.

## Required input

```text
1. Tên dự án:
2. Mô tả ngắn gọn hệ thống:
3. Danh sách actor:
4. Danh sách yêu cầu chức năng chính:
5. Danh sách yêu cầu phi chức năng:
6. Business rules quan trọng:
7. Các use case hoặc module chính:
8. Dữ liệu/entity nghiệp vụ quan trọng:
9. Công nghệ dự kiến nếu có:
10. Ràng buộc về thời gian, nhân lực, kỹ năng, triển khai:
11. Yêu cầu bảo mật hoặc phân quyền:
12. Môi trường triển khai mong muốn:
```

## Official full prompt

```text
Bạn là một kiến trúc sư phần mềm có kinh nghiệm trong phân tích, thiết kế và xây dựng hệ thống phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 4 của vòng đời phát triển phần mềm SDLC: Kiến trúc phần mềm.

Dựa trên thông tin tôi cung cấp, hãy đề xuất kiến trúc phần mềm phù hợp, rõ ràng, có thể giải thích trong báo cáo kỹ thuật phần mềm và có thể làm cơ sở cho giai đoạn thiết kế chi tiết, lập trình, kiểm thử và triển khai.

Thông tin dự án:

1. Tên dự án:
[Điền tên dự án]

2. Mô tả ngắn gọn hệ thống:
[Mô tả hệ thống cần xây dựng]

3. Danh sách actor:
[Liệt kê actor chính và phụ]

4. Danh sách yêu cầu chức năng chính:
[Dán các FR quan trọng]

5. Danh sách yêu cầu phi chức năng:
[Dán các NFR quan trọng như hiệu năng, bảo mật, khả dụng, dễ dùng, bảo trì...]

6. Business rules quan trọng:
[Dán các quy tắc nghiệp vụ ảnh hưởng đến kiến trúc]

7. Use case hoặc module chính:
[Dán danh sách use case hoặc module đã phân tích]

8. Dữ liệu/entity nghiệp vụ quan trọng:
[Ví dụ: User, Role, Task, Label, Project...]

9. Công nghệ dự kiến nếu có:
[Ví dụ: Spring Boot, React, Node.js, Express, PostgreSQL...]

10. Ràng buộc về thời gian, nhân lực, kỹ năng và triển khai:
[Ví dụ: nhóm 3 người, thời gian 8 tuần, cần Docker...]

11. Yêu cầu bảo mật hoặc phân quyền:
[Mô tả nếu có]

12. Môi trường triển khai mong muốn:
[Local, Docker, cloud, server nội bộ, VPS...]

Yêu cầu đầu ra:

1. Tổng quan kiến trúc
- Mô tả mục tiêu của kiến trúc, cách hệ thống được tổ chức và phạm vi kiến trúc.
- Ghi rõ giả định nếu thông tin đầu vào còn thiếu.

2. Architectural drivers
- Xác định các yếu tố ảnh hưởng đến kiến trúc: FR quan trọng, NFR, ràng buộc kỹ thuật, ràng buộc nhóm và rủi ro kỹ thuật.
- Trình bày dưới dạng bảng.

3. Phân tích thuộc tính chất lượng
- Phân tích performance, security, scalability, availability, maintainability, usability, reliability, testability, deployability.
- Với mỗi thuộc tính, nêu tác động đến kiến trúc và tiêu chí đánh giá nếu có thể.

4. Đề xuất phong cách kiến trúc
- Cân nhắc Layered Architecture, MVC, Client-Server, Modular Monolith, Microservices, Event-driven, Clean Architecture.
- Đề xuất phong cách phù hợp nhất, giải thích lý do chọn và vì sao không chọn phương án quá phức tạp nếu không cần.

5. Kiến trúc logic
- Mô tả các layer hoặc khối chính của hệ thống.
- Với mỗi layer, nêu trách nhiệm và tương tác với layer khác.
- Trình bày bằng bảng và mô tả luồng xử lý tổng quát.

6. Kiến trúc module/component
- Chia hệ thống thành các module hoặc component chính.
- Với mỗi module, nêu trách nhiệm, actor sử dụng, dữ liệu liên quan và module phụ thuộc.
- Chỉ rõ module cốt lõi và module hỗ trợ.

7. Kiến trúc dữ liệu tổng quan
- Xác định loại database phù hợp.
- Nêu các nhóm dữ liệu chính cần lưu trữ.
- Mô tả chiến lược lưu trữ dữ liệu ở mức tổng quan.
- Nêu yêu cầu backup, migration, bảo vệ dữ liệu nếu cần.
- Không thiết kế bảng chi tiết ở giai đoạn này.

8. Kiến trúc API và tích hợp
- Đề xuất kiểu giao tiếp giữa các thành phần.
- Nếu dùng REST API, hãy mô tả convention endpoint ở mức tổng quan.
- Nêu định dạng dữ liệu trao đổi, cách xử lý lỗi API và cách xác thực request nếu có.

9. Kiến trúc bảo mật
- Đề xuất authentication, authorization/phân quyền, bảo vệ mật khẩu, dữ liệu cá nhân và file nếu có.
- Nêu input validation, access control, logging và error handling.
- Trình bày phân quyền theo vai trò nếu hệ thống có nhiều actor.

10. Kiến trúc triển khai
- Mô tả client, frontend, backend, database, file storage, external service.
- Mô tả môi trường triển khai đề xuất: local, Docker, cloud, server nội bộ.
- Nếu phù hợp, gợi ý sơ đồ deployment dạng text.

11. Đề xuất công nghệ
- Đề xuất công nghệ cho frontend, backend, database, authentication, deployment, documentation và testing.
- Với mỗi công nghệ, giải thích lý do chọn và nêu phương án thay thế nếu có.

12. Phân tích trade-off kiến trúc
- Trình bày các quyết định kiến trúc quan trọng.
- Với mỗi quyết định, nêu ưu điểm, nhược điểm và tác động.

13. Architecture Decision Record
- Tạo danh sách ADR cho các quyết định chính.
- Mỗi ADR gồm: mã ADR, tiêu đề, bối cảnh, quyết định, phương án thay thế, hệ quả.

14. Rủi ro kiến trúc
- Liệt kê rủi ro bảo mật, hiệu năng, tích hợp, triển khai và bảo trì.
- Với mỗi rủi ro, nêu tác động và hướng giảm thiểu.

15. Checklist kiểm tra kiến trúc
- Tạo checklist đánh giá kiến trúc đã đủ rõ chưa.

Yêu cầu trình bày:
- Viết bằng tiếng Việt.
- Văn phong học thuật, rõ ràng, phù hợp với báo cáo môn học kỹ thuật phần mềm.
- Ưu tiên trình bày bằng bảng khi phù hợp.
- Không chọn kiến trúc quá phức tạp nếu dự án nhỏ hoặc nhóm phát triển ít người.
- Nếu thiếu thông tin, hãy nêu giả định hợp lý.
- Không đi sâu sang thiết kế chi tiết class, database table hoặc code.
```

## Expected output

- Architecture overview.
- Architectural drivers.
- Quality attribute analysis.
- Architecture style recommendation.
- Logical architecture.
- Module/component architecture.
- Data architecture overview.
- API/integration architecture.
- Security architecture.
- Deployment architecture.
- Technology stack recommendation.
- Trade-off analysis.
- ADR list.
- Architecture risk list.
- Architecture validation checklist.

## Quality checklist

| Criteria | Yes/No |
|---|---|
| Architectural drivers are identified. |  |
| Quality attributes are analyzed. |  |
| Architecture style is justified. |  |
| Logical, module, data, API, security, and deployment views are included. |  |
| Technology choices include rationale. |  |
| Trade-offs and ADRs are included. |  |
| Architecture risks are identified. |  |

## Common mistakes to avoid

- Choosing architecture by trend rather than need.
- Using microservices for a small project without justification.
- Ignoring non-functional requirements.
- Missing security and deployment views.
