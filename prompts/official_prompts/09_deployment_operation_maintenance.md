# SDLC-PP09: Deployment, Operation, Maintenance and Improvement Prompt Pattern

## Purpose

This prompt supports deployment and operation. It creates deployment plans, environment setup, configuration management, build/package plan, CI/CD plan, database migration, release management, monitoring/logging, backup/restore, incident response, maintenance, change management, improvement roadmap, user support, and post-deployment review.

## Required input

```text
1. Tên dự án:
2. Mô tả ngắn gọn hệ thống:
3. Công nghệ sử dụng:
4. Kiến trúc triển khai:
5. Các thành phần hệ thống:
6. Môi trường triển khai mong muốn:
7. Database và file storage nếu có:
8. Cấu hình môi trường cần thiết:
9. Cách build/chạy hiện tại:
10. Công cụ CI/CD nếu có:
11. Yêu cầu backup/restore:
12. Yêu cầu monitoring/logging:
13. Danh sách chức năng trong bản release:
14. Các rủi ro triển khai đã biết:
15. Kế hoạch bảo trì hoặc cải tiến mong muốn:
```

## Official full prompt

```text
Bạn là một kỹ sư DevOps/kỹ sư triển khai và vận hành phần mềm có kinh nghiệm trong việc đưa hệ thống phần mềm từ môi trường phát triển sang môi trường sử dụng thực tế hoặc môi trường demo.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 9 của vòng đời phát triển phần mềm SDLC: Triển khai, vận hành, bảo trì và cải tiến phần mềm.

Dựa trên thông tin tôi cung cấp, hãy tạo tài liệu triển khai và vận hành hệ thống, bao gồm kế hoạch triển khai, cấu hình môi trường, build, CI/CD, migration database, release, monitoring, logging, backup, xử lý sự cố, bảo trì, quản lý thay đổi và lộ trình cải tiến.

Thông tin dự án:

1. Tên dự án:
[Điền tên dự án]

2. Mô tả ngắn gọn hệ thống:
[Mô tả hệ thống]

3. Công nghệ sử dụng:
[Ví dụ: React, Spring Boot, Node.js, Django, MySQL, PostgreSQL, Docker...]

4. Kiến trúc triển khai:
[Ví dụ: frontend + backend + database, monolith, client-server, Docker Compose...]

5. Các thành phần hệ thống:
[Frontend, backend, database, file storage, email service, external API...]

6. Môi trường triển khai mong muốn:
[Local, Docker, VPS, cloud, server trường, production...]

7. Database và file storage nếu có:
[Mô tả database, nơi lưu file upload nếu có]

8. Cấu hình môi trường cần thiết:
[Biến môi trường, port, domain, secret, config file...]

9. Cách build/chạy hiện tại:
[Dán lệnh chạy backend, frontend, database nếu có]

10. Công cụ CI/CD nếu có:
[GitHub Actions, GitLab CI, Jenkins, không có...]

11. Yêu cầu backup/restore:
[Mô tả nếu có]

12. Yêu cầu monitoring/logging:
[Mô tả nếu có]

13. Danh sách chức năng trong bản release:
[Dán chức năng đã hoàn thành]

14. Các rủi ro triển khai đã biết:
[Lỗi config, dependency, database, bảo mật...]

15. Kế hoạch bảo trì hoặc cải tiến mong muốn:
[Mô tả nếu có]

Yêu cầu đầu ra:

1. Tổng quan triển khai
- Mô tả mục tiêu, phạm vi và môi trường triển khai.
- Ghi rõ giả định nếu thông tin đầu vào còn thiếu.

2. Thiết lập môi trường
- Liệt kê phần mềm, runtime, framework, database và công cụ cần cài.
- Nêu yêu cầu hệ thống tối thiểu nếu cần.
- Nêu cấu trúc development, test/staging và production nếu phù hợp.

3. Quản lý cấu hình
- Liệt kê biến môi trường cần có.
- Tạo mẫu file .env.example nếu phù hợp.
- Chỉ rõ cấu hình nào không được commit lên Git.
- Nêu cách quản lý secret an toàn ở mức cơ bản.

4. Kế hoạch build và đóng gói
- Nêu các bước cài dependency, build backend/frontend, đóng gói Docker nếu phù hợp.
- Nêu bước kiểm tra trước khi build như chạy test hoặc kiểm tra cấu hình.

5. Kế hoạch triển khai
- Tạo danh sách bước triển khai theo thứ tự.
- Với mỗi bước, nêu người thực hiện, đầu vào, hành động và kết quả mong đợi.
- Bao gồm kiểm tra sau triển khai và rollback plan nếu triển khai lỗi.

6. CI/CD plan
- Đề xuất pipeline phù hợp gồm checkout, setup runtime, install dependencies, run tests, build, package, deploy.
- Nếu dự án nhỏ, đề xuất CI/CD ở mức đơn giản.

7. Database migration và seed data
- Nêu cách tạo/cập nhật database, chạy migration, seed data.
- Nêu backup trước migration nếu cần.
- Nêu cách kiểm tra database sau migration.

8. Release management
- Đề xuất cách đặt version, mẫu release note, tag source code, known issues và điều kiện release.

9. Monitoring và logging
- Đề xuất thành phần cần theo dõi.
- Đề xuất error log, access log, audit log, security log.
- Chỉ rõ dữ liệu không được ghi vào log.
- Nêu cách kiểm tra hệ thống đang hoạt động.

10. Backup và restore
- Xác định dữ liệu cần backup, tần suất, nơi lưu, quy trình restore và cách kiểm tra backup.

11. Incident response plan
- Tạo quy trình xử lý sự cố, mẫu incident report, phân loại mức độ nghiêm trọng.
- Nêu cách ghi nhận, xử lý, kiểm thử lại và tổng kết sự cố.

12. Kế hoạch bảo trì
- Phân loại corrective, adaptive, perfective và preventive maintenance.
- Với mỗi loại, nêu hoạt động cụ thể và lịch bảo trì phù hợp.

13. Kế hoạch quản lý thay đổi
- Tạo quy trình tiếp nhận và xử lý change request.
- Tạo mẫu change request.
- Nêu cách đánh giá tác động, ưu tiên, cập nhật tài liệu và kiểm thử hồi quy.

14. Lộ trình cải tiến
- Đề xuất cải tiến sau release theo chức năng, giao diện, hiệu năng, bảo mật, kiểm thử, triển khai và tài liệu.
- Trình bày theo phiên bản hoặc mức ưu tiên.

15. Kế hoạch hỗ trợ người dùng
- Đề xuất user guide, FAQ, troubleshooting, admin guide nếu cần.
- Nêu cách tiếp nhận phản hồi người dùng.

16. Mẫu tổng kết sau triển khai
- Tạo template post-deployment review gồm kết quả triển khai, lỗi phát sinh, hiệu năng, phản hồi người dùng, vấn đề bảo mật và bài học kinh nghiệm.

17. Checklist hoàn thành giai đoạn triển khai
- Bao gồm môi trường, cấu hình, build, database, security, test, monitoring, backup, release note, tài liệu và rollback.

Yêu cầu trình bày:
- Viết bằng tiếng Việt.
- Văn phong rõ ràng, phù hợp với báo cáo môn học kỹ thuật phần mềm.
- Ưu tiên trình bày bằng bảng.
- Không giả định hệ thống quá lớn nếu dự án nhỏ hoặc là đồ án sinh viên.
- Nếu thiếu thông tin, hãy nêu giả định hợp lý.
- Tập trung vào triển khai an toàn, có kiểm tra, có rollback, có bảo trì và có cải tiến.
```

## Expected output

- Deployment overview.
- Environment setup.
- Configuration management.
- Build and packaging plan.
- Deployment plan.
- CI/CD plan.
- Database migration and seed plan.
- Release management.
- Monitoring and logging plan.
- Backup and restore plan.
- Incident response plan.
- Maintenance plan.
- Change management plan.
- Improvement roadmap.
- User support plan.
- Post-deployment review template.
- Deployment completion checklist.

## Quality checklist

| Criteria | Yes/No |
|---|---|
| Deployment environment is clear. |  |
| Configuration and secrets are handled safely. |  |
| Build/package/deployment steps are clear. |  |
| Rollback plan is included. |  |
| CI/CD, migration, and release management are covered. |  |
| Monitoring, logging, backup, and incident response are included. |  |
| Maintenance, change management, and improvement roadmap are included. |  |

## Common mistakes to avoid

- Only writing local run commands.
- Not separating configuration from source code.
- No rollback plan.
- No backup before migration.
- No monitoring/logging or maintenance plan.
