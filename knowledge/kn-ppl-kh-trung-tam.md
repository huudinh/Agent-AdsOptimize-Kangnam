# PHƯƠNG PHÁP LUẬN — MARKETING LẤY KHÁCH HÀNG LÀM TRUNG TÂM
Version: 1.0 — áp dụng cho việc dựng bộ từ khoá Google Ads theo ZONE

> Bộ não và 3 rào cản giữ nguyên; **lớp chân dung KH** là phần bổ sung so với `kn-chan-dung-hanh-trinh.md`.
> Phương pháp này dùng chung với [`Agent-AdsOptimize-NhaKhoaParis`](../../Agent-AdsOptimize-NhaKhoaParis/); phần khác nhau nằm ở mục *Ba điều chỉnh*.

## Chuỗi quyết định

```
ZONE (lĩnh vực)
  └─ Đối tượng KH (nhóm chân dung)
       └─ Hành trình KH S1–S6 + insight từng chặng
            ├─ Kênh GOOGLE/WEBSITE → cụm truy vấn ưu tiên P1/P2/P3
            │     └─ cụm nội dung → thống nhất mục tiêu
            │          └─ thực thi: nội dung · tối ưu kỹ thuật SEO/GEO · báo cáo
            ├─ Kênh FB/TikTok → ngân hàng Hook × Format đúng chân dung
            │     └─ chọn hook ưu tiên · chọn format khả thi – hiệu quả
            └─ MKT automation (Caresoft / Zalo OA / app Kangnam Care)
```

**Nguyên tắc gốc: chọn NGƯỜI trước, chọn TỪ KHOÁ sau.**
Gom từ khoá trước rồi gán người sau là cách làm cũ — nó tạo ra nhóm quảng cáo đúng ngữ pháp
nhưng sai tâm lý, và không giải thích được vì sao lead rẻ mà không ra ca.

## ZONE của Kangnam

| ZONE | Dịch vụ lõi | Giá trị ca | Rào cản nặng nhất | Tuyến |
|---|---|---|---|---|
| **Mũi** | nâng mũi cấu trúc · sụn tự thân · thu gọn cánh mũi · **sửa mũi hỏng** | Cao | SỢ (lộ sóng · bóng đỏ · hỏng thấy bằng mắt) | Bệnh viện |
| **Mắt** | tạo mắt 2 mí · mở khoé · trẻ hoá mắt · **khắc phục sụp mí** | Trung bình–Cao | SỢ (mí lệch · sẹo · mắt trợn) | Bệnh viện |
| **Hàm mặt** | gọt góc hàm V-line · chỉnh hàm hô/móm · hạ gò má · tạo hình môi | **Rất cao** | SỢ (đại phẫu · gây mê · tổn thương thần kinh) | **Chỉ bệnh viện** |
| **Vòng 1** | nâng ngực · treo sa trễ | **Rất cao** | NGỜ (túi có chính hãng không · tay nghề bác sĩ) | **Chỉ bệnh viện** |
| **Lipo 360 & Giảm béo** | hút mỡ Lipo 360 · tạo hình thành bụng · cấy mỡ | Cao | SỢ (đau · da nhăn · tái béo) | Bệnh viện |
| **Trẻ hoá & Da liễu** | căng chỉ · tiêm trẻ hoá · nám – tàn nhang · mụn · sẹo · triệt lông | Thấp–Trung bình | NGẠI (ngại người thân biết · ngại nghỉ dưỡng) | Bệnh viện + viện tỉnh |

Mỗi ZONE = **1 file cấu hình** trong `zones/` = **1 workbook** trong `out/`.
Không trộn hai ZONE vào một bộ từ khoá: rào cản khác nhau thì bằng chứng gỡ cũng khác nhau.

> **Nha khoa (KDT) không phải một ZONE của agent này.** Niềng răng · bọc sứ · Implant thuộc sub-brand Kangnam Dental, và nghiệp vụ nha khoa có agent riêng ([`Agent-AdsOptimize-NhaKhoaParis`](../../Agent-AdsOptimize-NhaKhoaParis/) cho Paris). Màu nhóm `--g-nk` chỉ dùng khi hiển thị danh mục toàn hệ sinh thái.
> **Cơ xương khớp / bảo tồn khớp** là thương hiệu riêng, agent riêng (CXK-CPW) — không nằm trong ZONE nào ở đây.

## Lớp chân dung KH — phần bổ sung quan trọng nhất

Phễu 6 giai đoạn trả lời *khách đang ở đâu*. Chân dung trả lời *khách là ai*.
Thiếu lớp này thì hai người rất khác nhau bị gộp chung một nhóm quảng cáo:

> "nâng mũi cấu trúc giá bao nhiêu" và "sửa mũi hỏng ở đâu" cùng ZONE Mũi, cùng intent giá/địa điểm.
> Nhưng người gõ câu thứ nhất là **khách lần đầu, đang háo hức**; người gõ câu thứ hai là **khách đã làm ở nơi khác và đang thất vọng, mất niềm tin vào cả ngành**.
> Cùng một landing, cùng một mẫu quảng cáo → nhóm thứ hai bỏ đi ngay, dù họ là nhóm sẵn sàng trả nhiều nhất.

Mỗi chân dung phải trả lời được 5 câu:

1. **Ai** — tuổi, nghề, tình huống (lần đầu / đã làm ở nơi khác / sau sinh / trước cưới).
2. **Nỗi đau thật** — không phải "muốn đẹp", mà "tránh chụp ảnh nhóm", "không dám đi họp lớp", "con hỏi sao mẹ béo thế".
3. **Rào cản chốt chính** — đúng 1 trong SỢ / NGỜ / NGẠI.
4. **Người gõ Google có phải người điều trị không** — chồng tìm cho vợ sau sinh, mẹ tìm cho con cắt mí trước khi vào đại học. Nếu không, thông điệp viết cho **người mua hộ**.
5. **Giá trị ca** — quyết định được phép trả CPC bao nhiêu.

Riêng ngành thẩm mỹ thêm **câu thứ 6**:

6. **Khách có cần giữ kín việc này không** — nếu có, landing phải có kênh liên hệ riêng tư song song form, và thông điệp không dùng ngôn ngữ "khoe".

## Ánh xạ sang workbook

| Khối phương pháp luận | Nằm ở đâu trong file Excel |
|---|---|
| ZONE | Sheet 1, tiêu đề + mục tiêu |
| Đối tượng KH | Sheet 1 mục A · cột `Chân dung KH` ở sheet 2 · cột đầu sheet 4 |
| Hành trình S1–S6 + insight | Sheet 4 mục A |
| Cụm truy vấn ưu tiên P1/P2/P3 | Sheet 1 mục B (chiến dịch + cấp ưu tiên) · cột `Ưu tiên` sheet 2 |
| Cụm nội dung + thống nhất mục tiêu | Sheet 2 cột `Thông điệp / CTA` · Sheet 4 mục B (landing) |
| Hook × Format FB/TikTok | Sheet 4 mục C |
| Thực thi + báo cáo/đánh giá | Sheet 5: ngưỡng, lộ trình 3 pha, A/B test, rủi ro |

## Ba điều chỉnh của ngành thẩm mỹ

**① Rào cản SỢ nặng hơn NGỜ.** Ngược với nha khoa — ở đó khách không tự kiểm tra được vật liệu trong miệng nên NGỜ là nặng nhất. Ở thẩm mỹ, **kết quả hỏng nhìn thấy bằng mắt và nằm trên mặt**: lộ sóng, mí lệch, bóng đỏ. Thêm rủi ro gây mê của đại phẫu.
→ Bằng chứng mạnh nhất **không phải tên hãng** mà là: **giấy phép bệnh viện của Bộ Y tế → KCCS → hội đồng chuyên môn + quy trình 5 bước vô khuẩn → bảo hành minh bạch → case HTLX**.
→ Chặng S3 phải được ngân sách thật, **tối thiểu 10%**, không phải phần thừa sau khi chia cho S4.

**② Rào cản NGẠI có trục "người thân biết".** Thẩm mỹ là quyết định riêng tư theo cách nha khoa không phải.
→ Trường `chan_dung` phải ghi rõ khách này có cần giữ kín không. Landing của chân dung đó cần nút Zalo/chat riêng tư + cam kết bảo mật, và **không** dùng ngôn ngữ khoe kết quả.
→ Thêm vào đó là trục **thời gian hồi phục** — "nghỉ bao lâu mới đi làm được" là câu chặn thật, phải có câu trả lời trên trang.

**③ TUYẾN CƠ SỞ là ràng buộc cứng, không có tương đương ở nha khoa.**
Đại phẫu chỉ được làm tại tuyến bệnh viện: **190 Trường Chinh (HN)** · **666 CMT8 (TP.HCM)**. Viện tỉnh làm da/spa/tiểu phẫu + tư vấn/tái khám.
→ Mọi chiến dịch local phải khai rõ **tuyến** của cơ sở nó phục vụ.
→ **Từ khoá đại phẫu + tên tỉnh có viện tỉnh** (vd "nâng ngực Đà Nẵng") là **bẫy**: chạy được nhưng landing không được mời mổ tại đó. Hai cách xử lý hợp lệ, phải chọn một và ghi vào `ghi_chu`:
  - đổ về landing **tư vấn + đặt khám tại viện tỉnh, mổ tại tuyến bệnh viện** — nói rõ điều đó trên trang; hoặc
  - cho vào **phủ định** của chiến dịch local.
Để mặc không xử lý là rủi ro pháp lý, không phải chỉ là lead kém.

**④ Hệ sinh thái 5 sub-brand làm S6 phức tạp hơn.** Khách nâng mũi xong tự nhiên chuyển sang da liễu (KBS) hoặc giảm béo (KWL).
→ S6 là **cầu nối giữa các ZONE**, không phải đuôi phễu. Nhưng cross-sell sang **KDT (nha khoa)** hoặc **cơ xương khớp** là **đổi sub-brand/thương hiệu** — chỉ gợi ý, không viết nội dung bằng giọng thẩm mỹ.

## Sai lầm hay gặp

| Sai | Đúng |
|---|---|
| Chia ngân sách theo volume tìm kiếm | Chia theo **ý định mua × giá trị ca** |
| Đánh giá chiến dịch bằng CPL | Đánh giá bằng **chi phí/ca chốt** và doanh thu |
| Phủ định để loại truy vấn lệch | Phủ định chéo để **điều hướng** về đúng chiến dịch; chỉ loại khi không chân dung nào khớp |
| Một landing cho mọi intent | 1 nhóm = 1 dịch vụ × 1 chặng × 1 intent = **1 trang** |
| Báo cáo theo chiến dịch | Báo cáo **theo chiến dịch VÀ theo chân dung KH** — cần trường chân dung trong Caresoft từ Pha 1 |
| Cắt S3 vì CPL cao | S3 là chặng rụng khách nhiều nhất; giữ tối thiểu 6 tuần trước khi phán xét |
| Gộp "khách lần đầu" và "khách đi sửa lại" vào một nhóm | Tách hẳn chân dung: nhóm sửa lại đã mất niềng tin, cần bằng chứng khác và CPC cao hơn |
| Chạy từ khoá đại phẫu cho viện tỉnh mà không khai tuyến | Khai `tuyen` cho từng chiến dịch local; hoặc điều hướng, hoặc phủ định |

## Công cụ

- Schema cấu hình: `zones/README.md`
- Generator: `tools/build_keyword_workbook.py`
- Prompt mẫu: `prompts/prompt-sinh-bo-tu-khoa-zone.md`
- Ví dụ hoàn chỉnh: `zones/mui.json`
