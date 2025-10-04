# Mô tả chi tiết luồng tương tác hệ thống: Quy trình “Đặt hàng & Thanh toán online”
# Tên Use Case: Đặt hàng & Thanh toán online
Tác nhân chính: Khách hàng (Customer)
Tác nhân phụ: Payment Gateway
Mục tiêu: Khách hàng chọn sản phẩm, đặt hàng và thanh toán trực tuyến thành công.
Điều kiện tiên quyết:
Khách hàng đã đăng nhập.
Có ít nhất 1 sản phẩm trong giỏ hàng.
# Luồng chính (Main Flow):
- Customer truy cập hệ thống và xem danh sách sản phẩm.
- System hiển thị thông tin chi tiết sản phẩm.
- Customer chọn sản phẩm và thêm vào giỏ hàng.
- System lưu sản phẩm vào giỏ và hiển thị giỏ hàng cập nhật.
- Customer bấm “Đặt hàng”.
- System yêu cầu xác nhận thông tin giao hàng (địa chỉ, SĐT, phương thức nhận hàng).
- Customer xác nhận thông tin.
- System tạo đơn hàng và hiển thị yêu cầu thanh toán.
- Customer chọn “Thanh toán online”.
- System chuyển hướng tới Payment Gateway.
Customer nhập thông tin thẻ/ ví điện tử.
Payment Gateway xác thực giao dịch.
Payment Gateway gửi kết quả về cho System.
System cập nhật trạng thái đơn hàng: “Đã thanh toán thành công”.
System thông báo kết quả thanh toán cho Customer.
# Luồng thay thế (Alternative Flow):
- A1 – Giỏ hàng rỗng:
Nếu khách hàng chọn “Đặt hàng” nhưng giỏ trống → System thông báo lỗi và yêu cầu chọn sản phẩm.
- A2 – Thông tin giao hàng sai:
Nếu khách hàng nhập thiếu hoặc sai địa chỉ/ SĐT → System hiển thị thông báo và yêu cầu nhập lại.
- A3 – Thanh toán thất bại:
Nếu Payment Gateway trả về lỗi (thẻ hết tiền, thông tin sai, hệ thống lỗi) → System cập nhật trạng thái đơn hàng là “Thanh toán thất bại” và cho phép khách hàng thử lại hoặc chọn phương thức thanh toán khác.
# Điều kiện sau cùng (Post-condition):
Đơn hàng được ghi nhận trong hệ thống.
Nếu thanh toán thành công → đơn hàng chuyển sang trạng thái “Chờ giao hàng”.
Nếu thanh toán thất bại → đơn hàng giữ trạng thái “Chưa thanh toán” và khách hàng có thể thử lại.

#### Use Case Diagram (UC)
- Các tác nhân (Actors):
Khách hàng (Customer): người mua hàng, thực hiện đặt hàng và thanh toán.
Hệ thống bán hàng (System): quản lý giỏ hàng, đơn hàng, kết nối cổng thanh toán.
Cổng thanh toán (Payment Gateway): xử lý giao dịch online.
- Các Use Case chính:
Xem sản phẩm
Thêm vào giỏ hàng
Đặt hàng
Thanh toán online

#### Sequence Diagram (SQ)
- Các đối tượng tham gia:
Customer – người dùng cuối.
System – hệ thống bán hàng online.
Payment Gateway – cổng thanh toán.
- Luồng sự kiện:
Customer xem sản phẩm → System hiển thị danh sách sản phẩm.
Customer chọn sản phẩm và thêm vào giỏ hàng → System lưu giỏ hàng.
Customer chọn “Đặt hàng” → System tạo đơn hàng.
Customer chọn “Thanh toán online” → System chuyển sang Payment Gateway.
Customer nhập thông tin thanh toán → Payment Gateway xác thực giao dịch.
Payment Gateway trả kết quả (Thành công/Thất bại) → System cập nhật đơn hàng.
System thông báo kết quả cho Customer.
PlantUML code cho Sequence Diagram:
