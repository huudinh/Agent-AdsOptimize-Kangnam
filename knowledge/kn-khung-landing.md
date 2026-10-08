# KHUNG LANDING PAGE & CHUẨN GIAO HÀNG — Kangnam
Version: 2.0 — kế thừa mục 5.2 + MODE 2 bản v1.3

## Chọn loại landing

| | **LOẠI A — Khách hàng làm đẹp** | **LOẠI B — Vấn đề khách hàng** |
|---|---|---|
| **Intent xuất phát** | Đã muốn đẹp, hỏi "làm gì / ở đâu" | Từ nỗi đau / khiếm khuyết |
| **Khung** | **AIDA** — khát khao kết quả trước | **PAS** — Vấn đề → Khoét sâu → Giải pháp |
| **Mạnh nhất ở** | Giai đoạn 2 và 4 | **Giai đoạn 3 (cân nhắc & nỗi sợ)** |
| **Ví dụ từ khóa** | "nâng mũi đẹp tự nhiên", "gọt hàm v-line ở đâu" | "mũi hỏng sửa được không", "hút mỡ có nguy hiểm không" |

Chọn sai loại là nguyên nhân phổ biến nhất của **CTR ổn nhưng không ai điền form**.

---

## LOẠI A — AIDA (11 section)

1. **Hero** — kết quả khát khao (headline lợi ích) + subheadline + CTA chính + CTA phụ + trust badge
2. **Chứng minh nhanh** — số liệu / giải thưởng / HTLX
3. **Dịch vụ & công nghệ** (chuẩn Hàn)
4. **Vì sao chọn Kangnam** — 6 quyền lợi + KCCS + Bộ Y tế
5. **Bác sĩ thực hiện** (tên thật, có trong hồ sơ thương hiệu)
6. **Ảnh / case trước–sau thật** (đã duyệt pháp lý)
7. **Bảng giá / ưu đãi** `[động — lấy tại thời điểm chạy]`
8. **Review khách**
9. **CTA booking + form**
10. **FAQ ngắn**
11. **Footer** — hotline, chi nhánh

---

## LOẠI B — PAS (12 section)

1. **Hero** — gọi đúng **Vấn đề / nỗi đau** (headline) + hứa hẹn giải pháp + CTA
2. **Khoét sâu** — hệ quả nếu không xử lý / hiểu lầm thường gặp
3. **Giải pháp** — phương pháp Kangnam giải quyết đúng vấn đề đó
4. **Gỡ 3 rào cản (Sợ–Ngờ–Ngại)** — an toàn Bộ Y tế · KCCS · quy trình 5 bước · bảo hành
5. **Bằng chứng** — case thật **đúng vấn đề đó**, không phải case chung chung
6. **Bác sĩ** (tên thật)
7. **Quy trình an toàn**
8. **Chi phí / ưu đãi** `[động]`
9. **Review người từng gặp đúng vấn đề đó**
10. **CTA booking + form**
11. **FAQ xử lý nỗi sợ**
12. **Footer**

> Section 4 là trái tim của loại B. Làm hời hợt ở đây thì cả trang mất tác dụng.

---

## Quy tắc chung cho cả hai loại
- **CTA lặp sau mỗi 2 section** — người đọc quyết định ở nhiều điểm khác nhau, không chỉ ở cuối.
- Giá và ưu đãi **luôn là dữ liệu động** — lấy tại `/bang-gia/` và `/uu-dai/` lúc chạy, không dùng số cũ.
- Mọi con số gắn dấu `*` + dòng *"Hiệu quả phụ thuộc cơ địa mỗi người"*.
- Before–after chỉ dùng case đã duyệt pháp lý.

---

## Chuẩn giao hàng HTML

| Hạng mục | Quy định |
|---|---|
| **File** | Single-file HTML |
| **Breakpoint** | **Mobile-first 480px** |
| **Primary** | `#003c77` (navy) |
| **CTA** | `#f6871f` (cam) |
| **Nền** | Trắng `#FFFFFF`, **≥ 80% diện tích** |
| **Text** | `#1D2939` |
| **Font** | Be Vietnam Pro |
| **CTA / form booking** | Nổi bật, không chìm vào nền |
| **Tần suất CTA** | ≥ 1 CTA sau mỗi 2 section |

**Không:** nền tối toàn trang · quá 3 màu chính · gradient/neon mạnh · nhiều style icon lẫn lộn · card chồng nhiều shadow · animation rối.

---

## Luồng làm việc MODE 2
1. Nhận cụm từ khóa + dịch vụ → xác định loại LDP, **nói rõ chọn A hay B và vì sao**.
2. Lấy USP / trust / bác sĩ từ `kn-ho-so-thuong-hieu.md`; giá & KM lấy động.
3. **Mặc định hỏi:** *"Xuất copy-deck trước, hay dựng thẳng HTML?"*
4. Dựng HTML thì tuân bảng chuẩn giao hàng ở trên.
