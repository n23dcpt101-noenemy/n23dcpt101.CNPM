# Project Report – Hệ thống bán hàng online

## 1. Giới thiệu
Mini Project: Xây dựng hệ thống bán hàng online.
Bao gồm các bước từ phân tích yêu cầu, thiết kế UML, coding giao diện, đến quản lý source code trên GitHub.

---

## 2. Artifacts đã hoàn thành
### 2.1 Use Case Diagram
- File: use case diagram lab2.png | UCase Lab 03.png
- Mô tả: Chức năng chính gồm Xem sản phẩm, Đặt hàng, Thanh toán online, Quản lý đơn hàng.

### 2.2 Sequence Diagram
- File: SQ diagram Lab03.png
- Mô tả: Luồng tương tác chi tiết trong quy trình đặt hàng và thanh toán online.

### 2.3 Form Login (HTML/CSS/JS)
- File: Coding form login.html
- Chức năng: Nhập Username/Password, Remember me, nút Login/Cancel, kiểm tra dữ liệu bằng JavaScript.

---

## 3. Quy trình phát triển
1. **Phân tích yêu cầu:** xác định actor, chức năng chính.  
2. **Thiết kế UML:** Use Case + Sequence Diagram.  
3. **Coding:** form login bằng HTML/CSS/JS.  
4. **Tích hợp:** gom UML + code + báo cáo.  
5. **Triển khai:** quản lý trên GitHub.

---

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

