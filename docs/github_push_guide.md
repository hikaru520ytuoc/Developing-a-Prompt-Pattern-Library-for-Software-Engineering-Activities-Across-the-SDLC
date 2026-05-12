# Hướng dẫn đẩy repo lên GitHub

## 1. Giải nén file zip

Giải nén file `sdlc-prompt-pattern-library.zip`.

## 2. Mở terminal trong thư mục repo

```bash
cd sdlc-prompt-pattern-library
```

## 3. Khởi tạo Git

```bash
git init
git add .
git commit -m "Initial commit: add SDLC prompt pattern library"
```

## 4. Tạo repo mới trên GitHub

Trên GitHub, tạo repository mới, ví dụ:

```text
sdlc-prompt-pattern-library
```

Không cần chọn README vì repo đã có sẵn README.

## 5. Kết nối remote

Thay `<your-username>` bằng username GitHub của bạn.

```bash
git branch -M main
git remote add origin https://github.com/<your-username>/sdlc-prompt-pattern-library.git
git push -u origin main
```

## 6. Gợi ý mô tả repo trên GitHub

```text
A Vietnamese SDLC Prompt Pattern Library for software engineering activities: requirements, analysis, architecture, design, coding, testing, security, deployment and maintenance.
```

## 7. Gợi ý topic GitHub

```text
prompt-engineering
software-engineering
sdlc
requirements-engineering
software-architecture
software-testing
secure-sdlc
vietnamese
```
