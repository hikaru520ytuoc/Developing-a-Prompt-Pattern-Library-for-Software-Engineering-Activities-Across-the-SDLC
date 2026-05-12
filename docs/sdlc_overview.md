# Tổng quan SDLC cho bộ Prompt Pattern

## SDLC là gì?

SDLC, viết tắt của Software Development Life Cycle, là vòng đời phát triển phần mềm. Đây là quy trình có hệ thống để phát triển, kiểm thử, triển khai và bảo trì phần mềm.

Trong repo này, SDLC được chia thành 9 giai đoạn chính để phù hợp với việc xây dựng Prompt Pattern.

## 9 giai đoạn

| STT | Giai đoạn | Mục tiêu |
|---|---|---|
| 1 | Khởi tạo và lập kế hoạch | Xác định dự án, phạm vi, stakeholder, rủi ro và kế hoạch |
| 2 | Thu thập và quản lý yêu cầu | Xác định hệ thống cần làm gì |
| 3 | Phân tích hệ thống và nghiệp vụ | Mô hình hóa actor, use case, workflow, dữ liệu và rule |
| 4 | Kiến trúc phần mềm | Xác định cấu trúc tổng thể, module, công nghệ, triển khai |
| 5 | Thiết kế chi tiết | Thiết kế database, API, UI, class/service, sequence |
| 6 | Hiện thực/lập trình | Chuyển thiết kế thành mã nguồn |
| 7 | Kiểm thử và đánh giá chất lượng | Kiểm tra phần mềm đúng, đủ, ổn định |
| 8 | An toàn, bảo mật và tuân thủ | Rà soát bảo mật, dữ liệu, phân quyền, rủi ro |
| 9 | Triển khai, vận hành, bảo trì | Deploy, monitor, backup, incident, maintenance, improvement |

## Vì sao tách bảo mật thành một giai đoạn riêng?

Bảo mật thực tế cần chạy xuyên suốt SDLC. Tuy nhiên, trong bộ prompt này, bảo mật được tách thành một prompt riêng để người dùng có một bước rà soát tập trung, dễ kiểm tra và dễ đưa vào báo cáo.

## Vì sao dùng Todo List làm ví dụ?

Todo List là ví dụ chung, dễ hiểu, không phụ thuộc ngành cụ thể. Ví dụ này vẫn đủ để minh họa:

- Actor
- Functional requirements
- Non-functional requirements
- Use case
- API
- Database
- UI
- Testing
- Security
- Deployment
