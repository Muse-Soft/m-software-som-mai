# DESIGN.md — Sớm Mai: quán cà phê specialty

## Khác biệt so với các project gần nhất

3 project gần nhất (mới → cũ), đọc theo thứ tự từ /api/office:

| Project | Archetype | Cặp font | Nhiệt màu |
|---|---|---|---|
| Đất Lành (xưởng gốm) | A1 Editorial dọc | Cormorant Garamond + Be Vietnam Pro | Trung tính trầm |
| Gác Sách (tiệm sách) | A4 Bento-masonry | EB Garamond + Be Vietnam Pro | Sáng-ấm |
| Thả Lỏng (studio yoga) | A3 Lệch tâm | Playfair Display + Be Vietnam Pro | Sáng-ấm |

Lựa chọn của Sớm Mai và lý do không vi phạm luật chống trùng (§16.5):

- **Archetype A8 Tạp chí nhiều cột** — khác A1 của Đất Lành (project liền trước) và khác A4 của Gác Sách (project thứ hai). Không dùng lại archetype của 2 project liền trước.
- **Cặp font Lora + Be Vietnam Pro** — khác cặp Cormorant Garamond + Be Vietnam Pro của Đất Lành. Lora là serif có chân nhưng nét mềm, đọc như chữ tạp chí, khác hẳn nét thanh mảnh kiểu editorial của Cormorant.
- **Nhiệt màu sáng-ấm** — chuỗi nhiệt màu: Sớm Mai (sáng-ấm) → Đất Lành (trung tính trầm) → Gác Sách (sáng-ấm): không có 3 project liên tiếp cùng nhiệt màu vì Đất Lành ở giữa đã đổi sang trung tính trầm.
- **Điểm nhấn riêng** (xem mục "Điểm nhấn đặc sắc"): thang rang 5 nấc — không project nào gần đây có.

## Tổng quan

- Sản phẩm: landing page 1 trang, visual-first, cho quán cà phê specialty Sớm Mai — rang hạt mỗi tuần, pha thủ công.
- Archetype: **A8 Tạp chí nhiều cột** — trang đọc như một số tạp chí cà phê: lưới nhiều cột, tiêu đề lớn kiểu bìa tạp chí, ảnh xen kẽ cột chữ, mỗi khối đánh số trang (folio) như mục lục tạp chí.
- Phong cách tham chiếu: **tạp chí cà phê specialty Standart** — bố cục thoáng, nhiều ảnh lớn, chữ serif trang nhã, khoảng trắng rộng, không chen chúc.
- Ngôn ngữ: tiếng Việt, hỗ trợ dấu đầy đủ (cả Lora và Be Vietnam Pro đều hỗ trợ tiếng Việt).

## Bảng màu (mã hex + vai trò)

| Mã hex | Vai trò |
|---|---|
| `#F3EDE3` | Nền chính toàn trang — kem giấy tạp chí, sáng và ấm |
| `#E4D9C6` | Nền khối phụ (khối xen kẽ, thẻ thực đơn) — kem đậm hơn nền chính một nấc |
| `#241A12` | Chữ chính, tiêu đề — nâu đen hạt rang đậm, tương phản cao trên nền kem |
| `#6B4E35` | Chữ phụ, chú thích ảnh, đường kẻ — nâu hạt rang vừa |
| `#9A6A2F` | Màu nhấn chính — vàng đồng hạt rang: tiêu đề khối, giá, nút, thang rang |
| `#B8A88F` | Đường chia cột, số trang folio, viền nhẹ — be xám trung tính |

Quy tắc dùng màu: nền luôn là kem (`#F3EDE3` hoặc `#E4D9C6` xen kẽ theo khối); không dùng khối nền tối toàn trang; màu nhấn `#9A6A2F` chỉ dùng cho tiêu đề khối, giá, nút và điểm nhấn — không tô nền lớn bằng màu nhấn.

## Font chữ

- **Tiêu đề: Lora, serif** — cỡ 56px desktop cho tiêu đề hero, 40px cho tiêu đề khối, 28px cho tiêu đề mục nhỏ. In đậm (700) cho tiêu đề khối, in nghiêng (italic) cho câu trích dẫn.
- **Nội dung: Be Vietnam Pro, sans-serif** — cỡ 17px, chiều cao dòng 1.7, cho đoạn văn, thực đơn, chú thích. Chú thích ảnh: 13px, màu `#6B4E35`, in nghiêng.
- Tiêu đề khối luôn đi kèm số trang folio (ví dụ "01 — Câu chuyện hạt") bằng Be Vietnam Pro 13px, màu `#B8A88F`, chữ hoa, đặt phía trên tiêu đề.

## Điểm nhấn đặc sắc: thang rang 5 nấc

Mỗi món trong thực đơn và mỗi gói hạt rang đều kèm một **thang rang 5 nấc**: một hàng ngang 5 chấm tròn (đường kính 10px, cách nhau 6px). Số chấm tô màu vàng đồng `#9A6A2F` = mức rang (1 = rang nhạt nhất, 5 = rang đậm nhất), chấm còn lại viền `#B8A88F`, nền trong suốt. Bên phải thang là chữ mức rang bằng Be Vietnam Pro 13px (ví dụ "Rang vừa — nốt cam, mật ong"). Thang rang giúp khách chọn cà phê theo khẩu vị mà không cần đọc mô tả dài, và là dấu hiệu nhận biết riêng của Sớm Mai.

## Quy tắc hình ảnh

- **Tông ảnh:** ấm, ánh sáng tự nhiên buổi sáng, màu nâu hạt rang — cà phê — kem chiếm đa số; không dùng ảnh lạnh, xanh, neon.
- **Ảnh mẫu:** dùng ảnh mẫu chất lượng cao, đồng tông ấm; ghi rõ là ảnh mẫu trong bản dựng.
- **Tỉ lệ khung theo khối:**
  - Hero: ảnh toàn màn hình 16:9, ly cà phê đang rót, phủ tối 30% để chữ trắng kem đọc rõ.
  - Câu chuyện hạt: 2 ảnh dọc 4:5 đặt xen kẽ 2 cột chữ.
  - Thực đơn: ảnh món vuông 1:1, mỗi món một ảnh nhỏ kèm thang rang.
  - Quy trình pha: ảnh từng bước 3:2, xếp ngang 2 cột, mỗi bước đánh số 01–04.
  - Không gian + lớp cupping: ảnh ngang 3:2 xen kẽ, một ảnh lớn + hai ảnh nhỏ.
  - Form liên hệ: không ảnh lớn; chỉ một ảnh nhỏ 4:3 ở cột bên.

## Cấu trúc 6 khối theo archetype A8

1. **Hero (trang bìa):** ảnh lớn toàn màn hình ly cà phê đang rót; tiêu đề "Sớm Mai" Lora 56px; dòng phụ "Rang mỗi tuần. Pha bằng tay."; nút "Xem thực đơn" nền `#9A6A2F`, chữ kem.
2. **Câu chuyện hạt (trang 01):** lưới 2 cột — cột trái chữ (nông trại → rang → ly), cột phải 2 ảnh dọc 4:5; tiêu đề khối kèm folio "01".
3. **Thực đơn (trang 02):** lưới 3 cột desktop — mỗi món một ô: ảnh vuông 1:1, tên món Lora 28px, thang rang 5 nấc, giá mẫu. Cà phê pha tay 45.000–85.000đ; gói hạt rang 180.000–320.000đ. Giá ghi rõ là giá mẫu.
4. **Quy trình pha (trang 03):** lưới 2 cột, 4 bước pour-over/espresso bằng ảnh 3:2 từng bước, mỗi bước đánh số 01–04 và mô tả 1–2 câu.
5. **Không gian + lớp cupping (trang 04):** bố cục tạp chí — một ảnh lớn 3:2 + hai ảnh nhỏ; lịch lớp cupping cuối tuần mẫu; nút "Giữ chỗ".
6. **Liên hệ / đặt bàn (trang 05):** lưới 2 cột — cột trái form CHỈ giao diện (tên, số điện thoại, ngày, giờ, ghi chú; nút gửi không gửi dữ liệu thật), cột phải ảnh nhỏ 4:3 + thông tin quán. Địa chỉ, điện thoại, giờ mở cửa để `[CẦN BỔ SUNG]`, không bịa số liệu thật.

## Khoảng trắng và responsive

- Khoảng cách giữa các khối: 96px desktop, 64px tablet, 48px mobile.
- Lề trang: tối đa 1200px, căn giữa; cột cách nhau 32px.
- Responsive: dưới 768px lưới 3 cột → 2 cột, tiêu đề hero 40px; dưới 480px tất cả về 1 cột, tiêu đề hero 32px, ảnh dọc 4:5 giữ nguyên tỉ lệ, thang rang giữ nguyên kích thước.
- Chân trang: nền `#E4D9C6`, chữ `#6B4E35` 14px, ghi "Sớm Mai — Cà phê specialty" + dòng ảnh mẫu.
