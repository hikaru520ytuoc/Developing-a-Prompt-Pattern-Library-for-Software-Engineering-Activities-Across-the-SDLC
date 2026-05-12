# SDLC-PP09: Deployment, Operation, Maintenance and Improvement Prompt Pattern

## Giai đoạn

**Triển khai, vận hành, bảo trì và cải tiến**

## Mục tiêu

Tạo kế hoạch triển khai, cấu hình, build, CI/CD, migration, release, monitoring, backup, incident response, maintenance, change management, roadmap và support.

## Khi nào sử dụng?

Sử dụng prompt này khi bạn đang làm đúng giai đoạn **Triển khai, vận hành, bảo trì và cải tiến** trong vòng đời phát triển phần mềm và cần AI hỗ trợ tạo tài liệu/kết quả có cấu trúc.

## Input cần cung cấp

- Tên dự án
- Mô tả
- Công nghệ
- Kiến trúc triển khai
- Thành phần
- Môi trường
- Database/file storage
- Config
- Build/run
- CI/CD
- Backup/monitoring
- Release scope
- Rủi ro
- Cải tiến

## Prompt đầy đủ

```text
Bạn là một kỹ sư DevOps/kỹ sư triển khai và vận hành phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 9 của SDLC: Triển khai, vận hành, bảo trì và cải tiến phần mềm.

Thông tin dự án:
1. Tên dự án: [Điền]
2. Mô tả hệ thống: [Điền]
3. Công nghệ sử dụng: [Điền]
4. Kiến trúc triển khai: [Điền]
5. Các thành phần hệ thống: [Điền]
6. Môi trường triển khai mong muốn: [Điền]
7. Database và file storage nếu có: [Điền]
8. Cấu hình môi trường cần thiết: [Điền]
9. Cách build/chạy hiện tại: [Điền]
10. Công cụ CI/CD nếu có: [Điền]
11. Yêu cầu backup/restore: [Điền]
12. Yêu cầu monitoring/logging: [Điền]
13. Chức năng trong bản release: [Điền]
14. Rủi ro triển khai đã biết: [Điền]
15. Kế hoạch bảo trì/cải tiến mong muốn: [Điền]

Hãy tạo tài liệu triển khai, vận hành, bảo trì và cải tiến gồm:
1. Tổng quan triển khai.
2. Thiết lập môi trường.
3. Quản lý cấu hình và .env.example nếu phù hợp.
4. Kế hoạch build và đóng gói.
5. Kế hoạch triển khai theo từng bước, có kiểm tra sau deploy và rollback.
6. CI/CD plan.
7. Database migration và seed data.
8. Release management: version, release note, tag, known issues, điều kiện release.
9. Monitoring và logging.
10. Backup và restore.
11. Incident response plan và mẫu incident report.
12. Kế hoạch bảo trì: corrective, adaptive, perfective, preventive.
13. Kế hoạch quản lý thay đổi và mẫu change request.
14. Lộ trình cải tiến.
15. Kế hoạch hỗ trợ người dùng.
16. Mẫu tổng kết sau triển khai.
17. Checklist hoàn thành triển khai.

Yêu cầu:
- Viết bằng tiếng Việt.
- Trình bày rõ ràng, có bảng.
- Không giả định hệ thống quá lớn nếu là đồ án nhỏ.
- Tập trung vào triển khai an toàn, có kiểm tra, rollback, backup, logging, bảo trì và cải tiến.
```

## Output mong muốn

- Deployment overview
- Environment setup
- Config management
- Build plan
- Deployment plan
- CI/CD
- Migration/seed
- Release management
- Monitoring/logging
- Backup/restore
- Incident response
- Maintenance
- Change management
- Roadmap
- User support
- Review
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

- Chỉ hướng dẫn chạy local
- Không tách config
- Không rollback
- Không backup
- Không monitoring/logging
- Không release note
- Không bảo trì/cải tiến
