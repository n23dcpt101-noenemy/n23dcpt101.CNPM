# Project Report – Hệ thống bán hàng online (Mini Project)

## 1. Giới thiệu
**Mục tiêu dự án:** Xây dựng một mô-đun cơ bản của hệ thống bán hàng online (mini) tập trung vào quy trình **Đặt hàng & Thanh toán** và **Giao diện đăng nhập**.  
Báo cáo này gom tất cả artifacts: Use Case, Sequence Diagram, mã nguồn giao diện (login), hướng dẫn quản lý source trên GitHub và quy trình phát triển chi tiết.
## 2. Artifacts đã hoàn thành
- UCase Lab 03.png — Use Case Diagram (PlantUML)
- SQ diagram Lab 03.png — Sequence Diagram (PlantUML)
- Coding form login.html — Form Login (HTML + CSS + JavaScript)
- `Project_Report.md` — (this file)
## 3. Quy trình phát triển
1. **Phân tích yêu cầu:** xác định actor, chức năng chính.  
2. **Thiết kế UML:** Use Case + Sequence Diagram.  
3. **Coding:** form login bằng HTML/CSS/JS.  
4. **Tích hợp:** gom UML + code + báo cáo.  
5. **Triển khai:** quản lý trên GitHub.
4. Lập trình (Implementation) — viết `login.html` và tổ chức file  
## 4. Quản lý Source Code trên GitHub
### 4.1 Push code lên GitHub
```bash
git init
git add .
git commit -m "First commit - add UML, Login Form, Report"
git branch -M main
git remote add origin https://github.com/<username>/<repo>.git
git push -u origin main
# Online Shopping System
## Artifacts
- Use Case Diagram: `usecase.puml`
- Sequence Diagram: `sequence.puml`
- Login Form: `login.html`
## How to run
Open `login.html` in browser.
git tag v1.0
git push origin v1.0
