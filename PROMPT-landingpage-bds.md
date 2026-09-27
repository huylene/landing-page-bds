# Task: Landing Page — Vinhomes Grand Park (Thủ Đức)

## 1. Mục tiêu
Xây dựng **một trang Landing Page tĩnh (static)**, hoàn toàn phía client, quảng
bá dự án bất động sản **Vinhomes Grand Park** tại **Thành phố Thủ Đức**.

Không dùng bất kỳ ngôn ngữ / framework backend nào (không PHP, không Node
server, không database). Chỉ **HTML + CSS + JavaScript** thuần, chạy được
bằng cách mở trực tiếp file trong trình duyệt.

## 2. Tech stack
- **HTML5** — cấu trúc chính, lưu trong **1 file duy nhất: `index.html`**.
- **CSS** — dùng **Bootstrap 5 qua CDN** làm nền tảng layout/grid/responsive,
  kết hợp custom CSS (viết trong thẻ `<style>` ngay trong `index.html`) để
  áp bảng màu thương hiệu.
- **JavaScript** — vanilla JS (viết trong thẻ `<script>` trong `index.html`),
  không cần framework (React/Vue…), chỉ dùng cho tương tác nhẹ (menu, cuộn
  mượt, hiệu ứng xuất hiện khi cuộn, form liên hệ demo không gửi dữ liệu đi
  đâu).
- Không cần build tool, không cần npm/webpack. Bootstrap JS/CSS + icon (nếu
  cần) load qua CDN `<link>`/`<script>` tag.

## 3. Bảng màu (bắt buộc)
| Vai trò | Mã màu |
|---|---|
| Nền chính (background) | `#f2f2f2` |
| Chữ / màu thương hiệu chủ đạo (heading, nút, nav) | `#2d2d86` |

Toàn bộ trang phải theo tông **nền sáng – chữ/nhấn tối màu xanh tím than**
này, đồng nhất ở mọi section.

## 4. Cấu trúc trang (bố cục 1 trang, cuộn dọc)

### 4.1 Header / Navbar
- Logo dạng chữ: tên thương hiệu **"VINHOMES"** (có thể kèm tagline nhỏ
  "Grand Park").
- Menu điều hướng đơn giản, dạng anchor link cuộn tới các section trong
  trang (ví dụ: Trang chủ, Tiện ích, Ưu điểm, Liên hệ).
- Responsive: thu gọn thành menu hamburger trên mobile (dùng Bootstrap
  navbar collapse).

### 4.2 Hero Section
- Tiêu đề lớn, giật gân, gây chú ý (ví dụ nhấn mạnh "đẳng cấp sống xanh",
  "trung tâm Thủ Đức"…).
- Đoạn mô tả ngắn (1–3 câu) bổ trợ cho tiêu đề.
- **1 nút Call-to-Action (CTA)** nổi bật, màu nhấn `#2d2d86`, ví dụ "Nhận
  bảng giá & ưu đãi".
- **Hình ảnh minh họa nằm bên phải** (bố cục 2 cột trên desktop: chữ trái –
  ảnh phải; xếp chồng trên mobile). Ảnh thể hiện bất động sản / biệt thự
  nghỉ dưỡng / khuôn viên trường Vinschool.

### 4.3 Features Section
Trình bày dạng 3 card ngang hàng (responsive: 3 cột desktop → 1 cột
mobile), mỗi card có **hình ảnh minh họa riêng** + tiêu đề + mô tả ngắn:
1. **Lối sống thượng lưu** — không gian sống xanh, biệt thự/căn hộ cao cấp.
2. **Tiện ích tối ưu** — hệ sinh thái tiện ích nội khu (công viên, hồ bơi,
   trường học Vinschool, y tế Vinmec…).
3. **Pháp lý nhanh gọn** — sổ hồng lâu dài, minh bạch, hỗ trợ vay ngân hàng.

### 4.4 Form & Chức năng "Đăng ký tư vấn"
- Người dùng nhập thông tin cá nhân vào form: Họ và tên, Số điện thoại, Email,
  sản phẩm quan tâm (căn hộ, biệt thự, shophouse...) và lời nhắn tư vấn.
- Có thể điền form trực tiếp trên trang hoặc thông qua Popup Modal khi bấm nút
  "Đăng ký tư vấn" tại Navbar / Hero / Nút nổi.
- Khi người dùng gửi thông tin hợp lệ (đã validate phía client), **Popup hiện ra**:
  - Thông điệp: **"Email đã được gửi cho admin. Chúng tôi sẽ liên hệ trong thời gian sớm nhất"**
  - Kèm theo **1 hình Like ngón tay cái** (biểu tượng Like 👍 nổi bật).
  - Tự động làm sạch form sau khi gửi thành công.

### 4.5 Footer
- Thông tin bản quyền (© năm hiện tại, tên đơn vị truyền thông/dự án).
- Thông tin liên hệ: hotline, email, địa chỉ văn phòng bán hàng.
- (Tùy chọn) vài icon mạng xã hội dạng link tĩnh.

## 5. Yêu cầu JavaScript (tối thiểu)
- Cuộn mượt (smooth scroll) khi bấm vào menu/anchor link.
- Hiệu ứng fade-in / xuất hiện nhẹ cho các feature card khi cuộn tới (ví dụ
  dùng `IntersectionObserver`).
- Nút CTA ở Hero dẫn tới form/section liên hệ hoặc mở modal đăng ký tư vấn.
- Xử lý chức năng "Đăng ký tư vấn": validate dữ liệu đầu vào và hiển thị Popup
  thành công có hình Like ngón tay cái cùng thông báo *"Email đã được gửi cho
  admin. Chúng tôi sẽ liên hệ trong thời gian sớm nhất"* (chỉ demo phía client,
  không submit dữ liệu tới server nào).

## 6. Ràng buộc
- Chỉ trả về **mã nguồn tĩnh**: HTML/CSS/JS. Không dùng PHP, Node.js
  server, API, hay bất kỳ xử lý phía server nào.
- Toàn bộ CSS/JS custom nhúng trực tiếp trong `index.html` (không tách file
  ngoài), chỉ Bootstrap được load qua CDN.
- Hình ảnh có thể dùng link ảnh public (Unsplash…) làm minh họa tạm thời.
- Giao diện phải responsive tốt trên mobile lẫn desktop.

## 7. Deliverable
- 1 file duy nhất: **`index.html`** — mở trực tiếp bằng trình duyệt là chạy
  được ngay, không cần cài đặt gì thêm.
