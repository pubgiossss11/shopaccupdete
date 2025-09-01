# ACC SHOP — Static site (demo)

Một website tĩnh đơn giản để bán account game. Không cần server, dữ liệu lưu trên trình duyệt (localStorage). **Phù hợp để demo/khởi đầu**.

## Tính năng
- Danh sách sản phẩm, tìm kiếm, lọc theo game/giá.
- Giỏ hàng + tạo đơn hàng (lưu localStorage).
- Form thanh toán (chuyển khoản/Momo/ZaloPay — bạn tự xác nhận thủ công).
- Trang **Admin** (PIN mặc định `123456`):
  - Thêm/sửa/xoá sản phẩm (lưu vào localStorage).
  - Xem đơn hàng, đánh dấu trạng thái.
  - Xuất/nhập JSON sản phẩm & đơn hàng.

> Vì là site tĩnh, không ghi file lên server. Nếu cần thật sự bán tự động + giao acc tự động, bạn nên dùng backend (Node/Express + SQLite/PostgreSQL) hoặc dịch vụ CMS headless.

## Cách chạy
1. Tải toàn bộ thư mục `accshop` và mở `index.html` trong trình duyệt.
2. Hoặc host lên GitHub Pages/Netlify:
   - Với GitHub: push thư mục này lên repo → Settings → Pages → deploy root.
   - Với Netlify: kéo-thả thư mục vào dashboard.

## Tuỳ biến
- **Sửa sản phẩm**: vào `admin.html` (PIN `123456`) rồi chỉnh sửa → Lưu → Xuất JSON để backup.
- **Đổi PIN**: tab Cài đặt trong Admin.
- **Logo**: thay `assets/logo.svg` bằng logo của bạn.

## Lưu ý pháp lý/ToS
- Mua bán account có thể vi phạm điều khoản của từng game và có nguy cơ bị khoá. Bạn tự chịu trách nhiệm, hãy minh bạch với khách và tuân thủ pháp luật.

## Nâng cấp đề xuất (khi cần)
- Backend API (Node/Express) lưu đơn hàng & sản phẩm vào DB.
- Tích hợp thanh toán (VNPAY, ZaloPay, Momo) qua link thanh toán.
- Tự động giao acc: lưu sẵn kho acc mã hoá trên server, tự động trả sau khi thanh toán thành công.
- Xác thực admin đúng chuẩn (session/token).

Chúc bạn bán hàng thuận lợi!
