# Định dạng chuẩn của một Prompt Pattern

Mỗi prompt trong thư viện này nên có cùng cấu trúc để dễ dùng, dễ mở rộng và dễ đánh giá.

## Cấu trúc chuẩn

```text
Tên prompt:
Mã prompt:
Giai đoạn SDLC:

Mục tiêu:
Khi nào sử dụng:
Input cần cung cấp:
Prompt đầy đủ:
Output mong muốn:
Checklist đánh giá:
Lỗi cần tránh:
```

## Ý nghĩa từng phần

| Thành phần | Ý nghĩa |
|---|---|
| Tên prompt | Tên dễ hiểu của prompt |
| Mã prompt | Mã định danh, ví dụ SDLC-PP01 |
| Giai đoạn SDLC | Prompt thuộc giai đoạn nào |
| Mục tiêu | Prompt giúp giải quyết vấn đề gì |
| Khi nào sử dụng | Bối cảnh nên dùng prompt |
| Input cần cung cấp | Dữ liệu người dùng phải đưa vào |
| Prompt đầy đủ | Nội dung prompt chính để copy dùng |
| Output mong muốn | Cấu trúc kết quả AI cần trả về |
| Checklist đánh giá | Tiêu chí kiểm tra kết quả |
| Lỗi cần tránh | Các lỗi thường gặp khi dùng prompt |

## Quy tắc thiết kế prompt

Một prompt tốt nên:

- Giao vai trò rõ cho AI.
- Nêu nhiệm vụ cụ thể.
- Liệt kê input rõ ràng.
- Định nghĩa output bắt buộc.
- Yêu cầu bảng khi phù hợp.
- Có checklist đánh giá.
- Có giới hạn phạm vi.
- Yêu cầu AI nêu giả định nếu thiếu thông tin.
- Tránh yêu cầu quá rộng hoặc mơ hồ.
