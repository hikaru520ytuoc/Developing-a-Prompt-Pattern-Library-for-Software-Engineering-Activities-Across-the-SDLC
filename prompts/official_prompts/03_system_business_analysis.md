# SDLC-PP03: System and Business Analysis Prompt Pattern

## Purpose

This prompt supports the analysis stage. It converts requirements into a deeper understanding of actors, business workflows, use cases, data flow, business entities, object states, rules, and exceptions.

## Required input

```text
1. Tên dự án:
2. Mô tả ngắn gọn dự án:
3. Danh sách actor:
4. Danh sách yêu cầu chức năng:
5. Danh sách yêu cầu phi chức năng nếu có:
6. Business rules đã biết:
7. Quy trình nghiệp vụ hiện tại:
8. Quy trình nghiệp vụ mong muốn:
9. Các chức năng quan trọng cần phân tích chi tiết:
10. Các ràng buộc hoặc ngoại lệ cần chú ý:
```

## Official full prompt

```text
Bạn là một chuyên gia phân tích hệ thống và phân tích nghiệp vụ trong lĩnh vực kỹ thuật phần mềm.

Nhiệm vụ của bạn là hỗ trợ tôi thực hiện giai đoạn 3 của vòng đời phát triển phần mềm SDLC: Phân tích hệ thống và nghiệp vụ.

Dựa trên thông tin tôi cung cấp, hãy phân tích hệ thống ở mức nghiệp vụ và hành vi, nhằm chuẩn bị cho giai đoạn kiến trúc, thiết kế chi tiết, lập trình và kiểm thử sau này.

Thông tin dự án:

1. Tên dự án:
[Điền tên dự án]

2. Mô tả ngắn gọn dự án:
[Mô tả hệ thống cần xây dựng]

3. Danh sách actor:
[Liệt kê actor, ví dụ: Guest, User, Admin...]

4. Danh sách yêu cầu chức năng:
[Dán danh sách FR nếu đã có]

5. Danh sách yêu cầu phi chức năng:
[Dán danh sách NFR nếu đã có]

6. Business rules đã biết:
[Dán các quy tắc nghiệp vụ nếu có]

7. Quy trình nghiệp vụ hiện tại:
[Mô tả quy trình hiện tại trước khi có phần mềm]

8. Quy trình nghiệp vụ mong muốn:
[Mô tả quy trình mong muốn sau khi có phần mềm]

9. Các chức năng quan trọng cần phân tích chi tiết:
[Ví dụ: đăng ký tài khoản, đăng nhập, tạo task, cập nhật task, hoàn thành task, xóa task...]

10. Các ràng buộc hoặc ngoại lệ cần chú ý:
[Ví dụ: user chỉ được xem dữ liệu của mình, admin mới được khóa tài khoản...]

Yêu cầu đầu ra:

Hãy tạo tài liệu phân tích hệ thống và nghiệp vụ gồm các phần sau:

1. Tổng quan phân tích hệ thống
- Tóm tắt mục tiêu phân tích.
- Nêu phạm vi phân tích.
- Ghi rõ các giả định nếu thông tin đầu vào còn thiếu.

2. Phân tích actor và quyền tương tác
- Liệt kê actor.
- Mô tả vai trò của từng actor.
- Nêu các chức năng actor được phép thực hiện.
- Nêu các giới hạn hoặc quyền không được phép thực hiện.

3. Phân tích quy trình nghiệp vụ hiện tại
- Mô tả quy trình hiện tại theo từng bước.
- Xác định người thực hiện từng bước.
- Xác định dữ liệu đầu vào và đầu ra.
- Chỉ ra vấn đề, điểm nghẽn hoặc hạn chế của quy trình hiện tại.

4. Phân tích quy trình nghiệp vụ đề xuất
- Mô tả quy trình mới khi có hệ thống phần mềm.
- Chỉ rõ bước nào do người dùng thực hiện, bước nào do hệ thống hỗ trợ.
- Chỉ ra các cải tiến so với quy trình hiện tại.
- Nếu có thể, mô tả trạng thái của các đối tượng chính trong quy trình.

5. Danh sách use case
- Tạo danh sách use case theo mã UC-01, UC-02...
- Với mỗi use case, nêu tên use case, actor chính, actor phụ nếu có, mục tiêu và mô tả ngắn.
- Gợi ý quan hệ include/extend/generalization nếu có.
- Trình bày dưới dạng bảng.

6. Đặc tả use case quan trọng
- Chọn các use case quan trọng nhất để đặc tả.
- Với mỗi use case, trình bày: ID, tên, actor chính, actor phụ, mục tiêu, tiền điều kiện, hậu điều kiện, luồng chính, luồng thay thế, luồng ngoại lệ, business rules liên quan.

7. Mô tả activity diagram
- Với mỗi quy trình quan trọng, hãy mô tả luồng hoạt động theo thứ tự.
- Chỉ rõ điểm bắt đầu, hành động, quyết định, nhánh rẽ và điểm kết thúc.
- Nếu phù hợp, hãy chia theo swimlane của từng actor.
- Trình bày đủ rõ để người dùng có thể vẽ activity diagram.

8. Phân tích luồng dữ liệu sơ bộ
- Xác định dữ liệu đầu vào, dữ liệu xử lý, dữ liệu đầu ra.
- Xác định actor tạo dữ liệu và actor sử dụng dữ liệu.
- Xác định nơi dữ liệu cần được lưu trữ ở mức nghiệp vụ.
- Không thiết kế bảng database vật lý ở giai đoạn này.

9. Phân tích entity nghiệp vụ
- Liệt kê các entity nghiệp vụ quan trọng.
- Với mỗi entity, mô tả ý nghĩa và thuộc tính sơ bộ.
- Nêu quan hệ nghiệp vụ giữa các entity nếu có.
- Không đi sâu vào khóa chính, khóa ngoại hoặc chuẩn hóa database.

10. Phân tích trạng thái đối tượng
- Xác định các đối tượng có trạng thái quan trọng.
- Liệt kê các trạng thái có thể có.
- Mô tả điều kiện chuyển trạng thái.
- Nêu actor hoặc sự kiện gây ra chuyển trạng thái.

11. Phân tích business rules chi tiết
- Chuẩn hóa các business rules theo mã BR-01, BR-02...
- Mỗi rule cần nêu điều kiện áp dụng, hành động hệ thống và use case liên quan.
- Phát hiện rule còn mơ hồ hoặc có thể xung đột.

12. Phân tích ngoại lệ và tình huống biên
- Liệt kê các trường hợp lỗi, dữ liệu thiếu, sai quyền, sai trạng thái, sai thời gian.
- Với mỗi tình huống, nêu cách hệ thống nên xử lý.
- Ưu tiên các ngoại lệ có ảnh hưởng đến thiết kế và kiểm thử.

13. Checklist kiểm tra kết quả phân tích
- Tạo checklist để kiểm tra giai đoạn phân tích đã hoàn thành chưa.
- Checklist cần kiểm tra: actor, use case, luồng nghiệp vụ, dữ liệu, trạng thái, business rules và ngoại lệ.

Yêu cầu trình bày:
- Viết bằng tiếng Việt.
- Văn phong học thuật, rõ ràng, phù hợp với báo cáo môn học kỹ thuật phần mềm.
- Ưu tiên trình bày bằng bảng khi phù hợp.
- Không đi sâu sang thiết kế kiến trúc, thiết kế database vật lý hoặc code.
- Nếu thiếu thông tin, hãy nêu giả định hợp lý.
- Phải chỉ ra các điểm còn thiếu, mơ hồ hoặc cần hỏi lại stakeholder.
```

## Expected output

- System analysis overview.
- Actor interaction analysis.
- Current and proposed business process.
- Use case list.
- Use case specifications.
- Activity flow descriptions.
- Data flow analysis.
- Business entity analysis.
- State analysis.
- Business rule analysis.
- Exception and edge case analysis.
- Analysis validation checklist.

## Quality checklist

| Criteria | Yes/No |
|---|---|
| Actors and interaction rights are analyzed. |  |
| Current and proposed processes are described. |  |
| Use cases are listed and key use cases are specified. |  |
| Activity flow is clear enough to draw a diagram. |  |
| Data flow and business entities are identified. |  |
| Object states and transitions are analyzed. |  |
| Business rules and exceptions are covered. |  |

## Common mistakes to avoid

- Only listing features without analyzing workflows.
- Treating UI screens as use cases.
- Missing exceptions and edge cases.
- Jumping into database schema too early.
