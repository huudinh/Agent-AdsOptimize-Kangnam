# PROMPT MẪU — dựng Landing Page (MODE 2 · LDP-BUILD)

Mặc định: **mobile-first, single-file HTML**.
Trang tham chiếu: <https://benhvienthammykangnam.com.vn/quyen-loi-thanh-vien/dep-ven-tron/> (bản lưu: `template/dep-ven-tron.html`)
Nguồn nội dung: **sheet 4 "Hành trình KH"** của workbook zone (`out/KN _ Google Ads _ Bộ từ khoá *.xlsx`).

---

## Trang tham chiếu dùng để làm gì — và KHÔNG dùng để làm gì

Trang mẫu là **trang quyền lợi thành viên** (`noindex`, chỉ dành cho khách đã nhận thông báo), chỉ có 3 section. Nó đã giải xong bài **khung trang và form mobile**, nhưng **không phải khung landing chạy Ads**.

| ✅ Lấy từ trang tham chiếu | ❌ Không lấy |
|---|---|
| **Token màu + khung trang** đầy đủ: nền `#D9E0E8` · `.app` 480px · header sticky kính mờ · `.sec-head` (pre Lora vàng + main navy + vạch amber) · footer sáng `#f1f1ef` | **Cấu trúc nội dung.** 3 section của nó không phải khung landing. Thứ tự section lấy từ khung **13 mục** ở `kn-khung-landing.md` |
| **Form + bottom sheet chọn dịch vụ** (dot màu nhóm) · honeypot · `aria-live` · màn cảm ơn dạng `.view` · popup chính sách dữ liệu | **Nội dung từng section** — lấy từ hành trình KH, không copy |
| Nút: `.btn-cta` 19px/800 uppercase trên `--cta`, `.btn-outline` viền navy | **Con số cứng.** Giá · voucher · số ca · hạn chương trình đều là dữ liệu động, đọc lại lúc chạy |
| Nhịp trình bày mobile: mật độ chữ, kích thước nút, khoảng trắng | **Cơ chế gating.** Trang mẫu chỉ dành cho khách đã nhận thông báo; landing Ads thì mở cho mọi traffic |
| `:focus-visible` viền amber · khối `prefers-reduced-motion` | **Danh sách bác sĩ.** Chỉ dùng tên có trong `kn-ho-so-thuong-hieu.md` |

**Trang tham chiếu đang THIẾU 5 thứ — LP chạy Ads bắt buộc phải có:**

1. **Khối trust** — giấy phép Bộ Y tế + KCCS + hội đồng chuyên môn + HTLX (trang mẫu chỉ có dòng giấy phép ở footer).
2. **Khối gỡ 3 rào cản** — section quan trọng nhất của chặng S3.
3. **FAQ xử lý nỗi sợ.**
4. **Sticky CTA mobile** — trang mẫu chỉ có CTA ở header, không có thanh cố định đáy.
5. **Kênh liên hệ riêng tư** (Zalo/chat) song song form — trục NGẠI "không muốn người thân biết".

> Điểm đáng học nhất của trang tham chiếu: **bottom sheet chọn dịch vụ có dot màu theo nhóm** (`--g-spa` · `--g-pttm` · `--g-nk` · `--g-oth`). Đây vừa là micro-conversion, vừa giúp khách tự phân loại mình trước khi để lại số. Giữ nguyên cơ chế này, chỉ đổi danh mục dịch vụ theo ZONE.

---

## 1 · PROMPT ĐẦY ĐỦ — dựng 1 landing page

> Thay 2 dòng trong ngoặc vuông. Mọi thứ còn lại Agent tự đọc từ file.

```
MODE 2 — LDP-BUILD. Dựng landing page mobile-first cho BVTM Kangnam.

LANDING:  [LP4: Nâng mũi có đau không - Hỏi đáp nỗi lo]
ZONE:     [Nâng mũi]  (file: zones/mui.json)

ĐỌC TRƯỚC, theo thứ tự:
  1. Sheet 4 "Hành trình KH" của workbook zone — mục B, dòng của landing này.
     Lấy đủ 7 trường: Loại khung · Chặng · Chân dung KH · Rào cản gỡ chính
     · Nội dung bắt buộc · CTA chính · Micro-conversion trước form.
  2. Sheet 4 mục A — dòng của CHẶNG tương ứng. Lấy: tâm lý & insight,
     bằng chứng BẮT BUỘC, chuyển đổi đo lường, hành động sau lead.
  3. Sheet 1 mục A — dòng của các CHÂN DUNG được gán cho landing này.
     Lấy insight là nỗi đau thật, ai là người gõ Google, và CÓ CẦN GIỮ KÍN KHÔNG.
  4. Sheet 2 — lọc cột Landing page = mã landing này. Đọc toàn bộ cột
     Từ khoá và cột Thông điệp / CTA chính. Trang phải trả lời ĐÚNG
     những câu khách đang gõ, bằng ĐÚNG thông điệp đã cam kết trên quảng cáo.
  5. knowledge/kn-khung-landing.md     - khung 13 section A1/A2, Design System
                                         v3.0, KHUNG TRANG, form + bottom sheet
  6. knowledge/kn-ho-so-thuong-hieu.md - USP, trust, bác sĩ, 6 quyền lợi, TUYẾN
  7. knowledge/kn-rao-phap-ly.md       - từ cấm, luật ảnh before-after
  8. template/dep-ven-tron.html        - CHỈ lấy khung trang, form, bottom sheet,
                                         token màu. KHÔNG lấy cấu trúc nội dung.

QUY TẮC CHỌN KHUNG:
  - Landing chạy Google Ads LUÔN là AIDA. Lấy A1 hay A2 theo cột "Loại khung"
    ở sheet 4. Nói rõ ở đầu output đang dùng khung nào và vì sao.
  - A2 "trả lời trước" (từ khoá nỗi sợ): hero gọi đúng nỗi lo rồi TRẢ LỜI NGAY
    ở section 2, KHÔNG khoét sâu. Trì hoãn câu trả lời làm tăng bounce, và khoét
    sâu nỗi sợ phẫu thuật là RỦI RO TUÂN THỦ (QC dịch vụ KCB không được gây
    hoang mang).
  - PAS chỉ dùng cho SEO/GEO/social nguội. KHÔNG dùng cho trang này.

QUY TẮC NỘI DUNG:
  - Section "Gỡ 3 rào cản" phải gỡ ĐÚNG rào cản ghi ở cột "Rào cản gỡ chính",
    không gỡ chung chung cả ba.
  - Mỗi lời hứa phải kèm 1 bằng chứng kiểm chứng được. Thứ tự ưu tiên bằng chứng:
    giấy phép KCB Bộ Y tế → KCCS → hội đồng chuyên môn + quy trình 5 bước vô khuẩn
    → bảo hành minh bạch → case HTLX đã phát sóng → báo chí.
    Ở thẩm mỹ, bằng chứng AN TOÀN và TAY NGHỀ thắng bằng chứng vật liệu.
  - Nếu người gõ Google không phải người điều trị (chồng tìm cho vợ sau sinh),
    viết hero và section chi phí cho NGƯỜI MUA HỘ.
  - Nếu chân dung CẦN GIỮ KÍN: thêm kênh liên hệ riêng tư (Zalo/chat) song song
    form, thêm dòng cam kết bảo mật dưới nút submit, và KHÔNG dùng ngôn ngữ "khoe".
  - Nhúng micro-conversion đúng vị trí: sau section "Gỡ 3 rào cản" (A2) hoặc sau
    section "Dịch vụ" (A1). Form booking chỉ xuất hiện SAU đó.
    KHÔNG xin số điện thoại ngay ở hero cho ca đại phẫu.
  - CTA lặp sau mỗi 2-3 section + sticky CTA mobile + popup CTA thoát trang.
  - THỜI GIAN HỒI PHỤC: nói dạng khoảng + "tùy cơ địa". KHÔNG hứa số ngày cứng.

QUY TẮC TUYẾN — kiểm TRƯỚC khi viết:
  - Trang này có mời đại phẫu không? Nếu CÓ thì địa chỉ ở footer phải là TUYẾN
    BỆNH VIỆN: 190 Trường Chinh (HN) hoặc 666 CMT8 (TP.HCM).
  - TUYỆT ĐỐI không gắn địa chỉ viện tỉnh (Hải Phòng · Nghệ An · Đà Nẵng · Cần
    Thơ · Thanh Hóa) vào trang mời đại phẫu — đó là vượt phạm vi giấy phép.
  - Nếu landing phục vụ khách tỉnh: nói rõ NGAY Ở HERO là khám/tư vấn tại viện
    tỉnh, PHẪU THUẬT TẠI TUYẾN BỆNH VIỆN.

QUY TẮC MOBILE (đây là mặc định, không phải tuỳ chọn):
  - Khung thiết kế chính: 360-430px, container .app max-width 480px.
    Desktop chỉ là bản nở ra của mobile.
  - Body >= 15px, INPUT BẮT BUỘC >= 16px (nhỏ hơn làm iOS tự zoom khi chạm).
  - Vùng chạm >= 44x44px. Khoảng cách giữa 2 nút >= 8px.
  - Hero: CTA chính phải nằm trong màn hình đầu, không cần cuộn.
  - Header sticky kính mờ: CHỈ logo + 1 CTA cam. Không nhồi menu.
    Mọi section có anchor phải có scroll-margin-top: var(--hdr-h).
  - Sticky CTA đáy màn hình. Hiện sau khi cuộn quá hero, ẩn khi form đang
    trong khung nhìn. Phải cùng max-width 480px với .app.
  - Form: 2 trường (tên, SĐT) + chọn dịch vụ (bottom sheet) + checkbox chính sách.
    input type="tel" inputmode="tel" autocomplete="tel".
    Có honeypot ẩn + aria-live cho trạng thái submit + màn cảm ơn dạng .view.
  - Bảng giá: card xếp dọc, KHÔNG dùng table cuộn ngang.
  - Before-after: tab hoặc swipe, không grid nhiều cột.
  - Ảnh: WebP, width/height cố định để không nhảy layout, lazy-load từ
    section 3 trở xuống. Hero là ảnh duy nhất được tải ngay (fetchpriority="high").
  - CHƯA CÓ ẢNH THẬT -> dựng Ô ẢNH TẠM, tuyệt đối không chèn ảnh stock/AI
    và không trỏ <img> tới URL không tồn tại. Mẫu bắt buộc:
      .ph{display:grid;place-content:center;gap:6px;text-align:center;margin:0;
          padding:16px;aspect-ratio:var(--ar,16/9);background:#E8EFFB;
          border:2px dashed var(--line);border-radius:var(--r);
          color:var(--ink-2);font-size:14px;line-height:1.45}
      .ph b{display:block;font-weight:700;color:var(--navy)}
      <figure class="ph" style="--ar:16/9">
        <b>Ảnh 16:9</b>
        Case nâng mũi cấu trúc trước-sau · phục vụ CD1 · cần giấy đồng ý KH
        + pháp chế duyệt
      </figure>
    Dòng mô tả phải nói rõ ảnh đó LÀ GÌ: nội dung · chân dung/section nó phục vụ
    · điều kiện pháp lý nếu là case thật. Không viết "ảnh minh hoạ".
    Tỉ lệ: hero 4/5 mobile và 16/9 desktop · before-after 1/1 · bác sĩ 3/4
    · công nghệ và cơ sở 16/9 · case HTLX 16/9 · icon 1/1.
  - Không hover-only: mọi thứ phải dùng được bằng ngón tay.
  - Giữ :focus-visible viền amber và khối prefers-reduced-motion của production.
  - Tổng trang mục tiêu < 500KB, không framework, CSS inline trong file.

DESIGN SYSTEM KANGNAM v3.0 — lấy nguyên từ production dep-ven-tron.html:
  --navy #074E84 · --navy-900 #04365E · --navy-950 #022544
  --ynavy #1F5FC4 · --cyan #00A5E0
  --gold #A66E29 · --amber #FBBF65 · --terra #D77927
  --cta #EF6103 · --cta-press #CF5300
  --bg #F3F6FA · --surface #FFFFFF
  --ink #0E2338 · --ink-2 #4A5C70 · --ink-3 #6E7E90 · --line #DCE3EC
  --r-sm 8px · --r 14px · --r-lg 20px · --hdr-h 56px
  --sh 0 2px 10px rgba(7,78,132,.08) · --sh-lg 0 10px 30px rgba(2,37,68,.16)
  nền trang body #D9E0E8 · khối form .reg nền #1B4182 · footer #f1f1ef chữ #254770
  - Tỷ lệ 80% trắng/--bg / 15% navy / 5% cam. KHÔNG nền toàn navy, không nền tối.
  - --cta LÀ MÀU NỀN NÚT, KHÔNG PHẢI MÀU CHỮ: trắng trên cam chỉ 3,29:1
    → chữ trên nút cam phải >= 19px/800. Nút nhỏ hơn thì dùng --navy (8,63 AAA).
  - KHÔNG --amber trên nền trắng (1,65:1) — amber chỉ trên navy và làm vạch.
  - KHÔNG --cyan làm chữ trên trắng (2,82:1) — cyan chỉ là màu nhóm/viền.
  - Chữ phụ dùng --ink-2 (6,87 AA), KHÔNG dùng --ink-3 (3,84).
  - --gold trên trắng 4,30 → chỉ heading >= 18px (đúng như .sec-head .pre).

KHUNG TRANG (bắt buộc — chép đúng từ kn-khung-landing.md, chỉ thay <section> giữa):
  - body nền #D9E0E8 · container .app max-width 480px, nền --bg,
    box-shadow, overflow-x clip — trang hiện ra như một thẻ khổ điện thoại
  - .hdr sticky top kính mờ (backdrop-filter blur 10px), min-height var(--hdr-h),
    gồm .hdr__logo (max-height 34px) + .hdr__cta pill cam
  - .wrap padding-inline 16px cho nội dung section
  - .sec-head căn giữa: .pre (Lora italic 600 18px, --gold) + .main (26px/800,
    --navy) + .bar (vạch 48x3px --amber)
  - card .gcard nền trắng, radius --r-lg, border-top 4px theo màu nhóm dịch vụ
  - khối form .reg nền #1B4182, card .fcard trắng radius --r-lg shadow --sh-lg;
    .input min-height 50px, border 1.5px --line, radius 12px, font 500 16px;
    focus border --ynavy + ring rgba(31,95,196,.18); lỗi dùng --err + --err-t
  - chọn dịch vụ = BOTTOM SHEET có dot màu nhóm, không dùng <select>
  - .privacy 12px dưới nút submit (dòng cam kết bảo mật)
  - footer .foot nền #f1f1ef chữ #254770: logo + DÒNG GIẤY PHÉP 287/BYT-GPHĐ
    NGUYÊN VĂN + .ft__hot (pill gradient vàng, hotline 24px/800) + danh sách
    cơ sở + social + logo Bộ Công Thương
  - HAI font, đúng như production. Không nạp font thứ ba:
    <link href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:wght@400;500;700;800&family=Lora:ital,wght@1,600&display=swap" rel="stylesheet">
    --f: 'Be Vietnam Pro' cho toàn bộ; --f2: 'Lora' italic 600 CHỈ cho .sec-head .pre
    và câu nhấn cảm xúc. Lora không dùng cho đoạn văn.
  - Card radius 20px · input 14px · button 999px · shadow chỉ 2 cấp --sh / --sh-lg.

RÀNG BUỘC PHÁP LÝ — vi phạm là loại thẳng, không tính điểm:
  - Cấm: tốt nhất · số 1 · duy nhất · đẹp tuyệt đối · khỏi 100% · không biến chứng
    · an toàn tuyệt đối · vĩnh viễn · không để lại sẹo.
  - KHÔNG hứa thời gian hồi phục cứng. Nói dạng khoảng + "tùy cơ địa".
  - KHÔNG mời đại phẫu cho viện tỉnh (xem QUY TẮC TUYẾN).
  - Mọi con số kết quả gắn dấu * + dòng "Hiệu quả phụ thuộc cơ địa mỗi người".
  - Chỉ dùng tên bác sĩ có trong kn-ho-so-thuong-hieu.md. Tên khác → [CHỜ CẬP NHẬT].
  - Giá, ưu đãi, điều kiện trả góp: đọc tại /bang-gia/ và /uu-dai/ LÚC CHẠY.
    Không truy cập được → [CHỜ CẬP NHẬT], không dùng số đã nhớ, không bịa.
  - Before-after chỉ dùng case đã duyệt pháp lý. Chưa có → ô ảnh tạm ghi rõ.
  - Phải có checkbox đồng ý dữ liệu cá nhân + popup chính sách.

TRƯỚC KHI VIẾT, hỏi tôi đúng 1 câu: xuất copy-deck trước, hay dựng thẳng HTML?

OUTPUT nếu dựng HTML: 1 file .html hoàn chỉnh, chạy được khi mở trực tiếp,
kèm HAI bảng ở cuối output:
  (a) Bảng đối chiếu:  Section | Phục vụ chân dung/rào cản nào | Bằng chứng đã dùng
  (b) BẢNG KÊ ẢNH CẦN CẤP: Section | Tỉ lệ | Nội dung ảnh cần | Ai duyệt
      — liệt kê đủ mọi ô ảnh tạm trong trang. Thiếu bảng này là chưa giao xong.
```

---

## 2 · PROMPT NGẮN — khi đã quen

```
MODE 2. Dựng [LP4] của zone [mui], mobile-first, single-file HTML.
Lấy loại khung, chặng, chân dung, rào cản, nội dung, CTA, micro-conversion từ
sheet 4 mục B. Lấy từ khoá và thông điệp đã hứa từ sheet 2 (lọc Landing page = LP4).
Theo kn-khung-landing.md: khung trang chuẩn + Design System v3.0 + khung 13 section.
Kiểm TUYẾN trước khi gắn địa chỉ. Tuân kn-rao-phap-ly.md. Giá và ưu đãi đọc động.
Hỏi tôi copy-deck hay HTML trước khi viết.
```

---

## 3 · PROMPT DỰNG CẢ BỘ — một zone, nhiều landing

```
Đọc sheet 4 mục B của workbook zone [mui]. Với TỪNG landing trong bảng,
lập blueprint 13 section theo đúng loại khung của nó.

Xuất 1 bảng tổng hợp trước, các cột:
  Mã LP | Loại khung | Chặng | Chân dung | Rào cản gỡ | 3 section quan trọng nhất
  | Micro-conversion | Bằng chứng chủ lực | Tuyến cơ sở | Số từ khoá đang trỏ về
  (đếm ở sheet 2)

Sau bảng, chỉ ra:
  - Landing nào đang nhận từ khoá của NHIỀU chặng khác nhau → phải tách trang.
  - Landing nào chưa có từ khoá nào trỏ về → xây xong sẽ không có traffic,
    nên hoãn hay nên bổ sung từ khoá?
  - Landing nào đang gỡ cùng một rào cản bằng cùng một bằng chứng → đang trùng lặp.
  - ⚠️ Landing nào đang mời đại phẫu mà gắn địa chỉ viện tỉnh → rủi ro pháp lý,
    sửa trước mọi việc khác.

Thứ tự ưu tiên dựng: theo tổng ngân sách của các chiến dịch trỏ về landing đó
(sheet 1 mục B), cao nhất làm trước.
CHƯA dựng HTML. Chờ tôi chọn landing cụ thể.
```

---

## 4 · PROMPT RÀ SOÁT — trước khi đẩy traffic

```
Đọc file landing [đường dẫn hoặc URL] và dòng tương ứng ở sheet 4 mục B.
Chấm theo 12 câu, mỗi câu ĐẠT/KHÔNG kèm dẫn chứng cụ thể trong trang:

 1. Khung có khớp cột "Loại khung" ở sheet 4 không? Có đang dùng PAS cho trang
    chạy Ads không (nếu có là SAI)?
 2. Với khung A2: hero có TRẢ LỜI NGAY nỗi lo không, hay đang khoét sâu?
 3. Hero có gọi đúng nỗi đau/mong muốn của chân dung được gán không?
 4. Section "Gỡ 3 rào cản" có gỡ ĐÚNG rào cản ghi ở sheet 4 không,
    hay đang gỡ chung chung cả ba?
 5. Mọi lời hứa có bằng chứng đi kèm không? Liệt kê lời hứa chưa có bằng chứng.
 6. Thông điệp trên trang có khớp cột "Thông điệp / CTA chính" của các từ khoá
    trỏ về landing này (sheet 2) không? Lệch chỗ nào?
 7. Micro-conversion có xuất hiện TRƯỚC form booking không? Có xin số ngay ở
    hero cho ca đại phẫu không (nếu có là SAI)?
 8. Chân dung cần giữ kín có được cấp kênh liên hệ riêng tư không?
 9. Mobile: CTA hero trong màn hình đầu · sticky CTA · input >= 16px
    · vùng chạm >= 44px · bảng giá không cuộn ngang · form có honeypot
    · scroll-margin-top theo --hdr-h.
10. Màu: có chữ < 19px trên nút cam không? Có amber/cyan làm chữ trên trắng không?
    Có dùng --ink-3 cho chữ nhỏ không?
11. ⚠️ TUYẾN: trang có mời đại phẫu không? Địa chỉ ở footer là tuyến nào?
    Có dòng giấy phép 287/BYT-GPHĐ nguyên văn không?
12. Có từ cấm không? Có hứa thời gian hồi phục cứng không? Giá/ưu đãi/trả góp
    có khớp dữ liệu đang hiệu lực không? Trích nguyên văn nếu có vi phạm.

Kết luận: ĐƯỢC CHẠY / SỬA RỒI CHẠY / LÀM LẠI. Nếu phải sửa, liệt kê theo
thứ tự ảnh hưởng tới tỷ lệ chuyển đổi, không theo thứ tự xuất hiện trong trang.
Riêng lỗi TUYẾN và từ cấm thì xếp đầu bất kể ảnh hưởng chuyển đổi.
```

---

## 5 · PROMPT ĐỐI CHIẾU TRANG MẪU

```
So sánh template/dep-ven-tron.html với yêu cầu của [LP4] ở sheet 4 mục B.

Trả lời 5 câu:
 1. Trang mẫu đang dùng được những gì cho LP4 (khung trang, form, token màu)?
    Liệt kê cụ thể từng khối CSS/HTML tái dùng được.
 2. Trang mẫu KHÔNG dùng được những gì? Vì sao (nó là trang quyền lợi thành viên
    noindex 3 section, không phải landing Ads)?
 3. 5 thứ trang mẫu đang thiếu (trust · gỡ 3 rào cản · FAQ nỗi sợ · sticky CTA
    · kênh liên hệ riêng tư) — thứ nào quan trọng nhất với chân dung của LP4?
 4. Bottom sheet chọn dịch vụ của trang mẫu nên đổi danh mục thế nào cho ZONE này?
 5. Nên SỬA trang mẫu hay DỰNG trang mới theo khung 13 section?
    Nêu lý do bằng chặng và rào cản, không bằng cảm tính.

Không viết code ở bước này.
```

---

## Checklist giao hàng

**Nội dung**
- [ ] Khung A1/A2 khớp sheet 4 · nói rõ lý do ở đầu output · **không dùng PAS cho trang Ads**
- [ ] Với A2: hero trả lời ngay, **không khoét sâu nỗi sợ**
- [ ] Section "Gỡ 3 rào cản" gỡ đúng rào cản của chân dung được gán
- [ ] Mọi lời hứa có bằng chứng · không dùng tính từ thay bằng chứng
- [ ] Thông điệp khớp với cam kết trên quảng cáo (cột Thông điệp, sheet 2)
- [ ] Micro-conversion đứng trước form booking · không xin số ở hero cho đại phẫu
- [ ] Chân dung cần giữ kín có kênh liên hệ riêng tư + cam kết bảo mật
- [ ] CTA lặp sau mỗi 2–3 section

**Mobile**
- [ ] CTA hero nằm trong màn hình đầu · sticky CTA đáy · popup thoát trang
- [ ] Body ≥ 15px · **input ≥ 16px** · vùng chạm ≥ 44px · không hover-only
- [ ] Form 2 trường + bottom sheet chọn dịch vụ · `type="tel"` · honeypot · `aria-live`
- [ ] Bảng giá dạng card dọc · before-after dạng tab/swipe
- [ ] **Khung trang đúng mẫu**: nền `#D9E0E8` · `.app` 480px · header sticky kính mờ · footer `#f1f1ef` + dòng giấy phép · sticky khớp 480px
- [ ] `scroll-margin-top: var(--hdr-h)` cho mọi section có anchor
- [ ] Màu v3.0 · chữ nút cam ≥19px/800 · không amber/cyan làm chữ trên trắng
- [ ] Be Vietnam Pro toàn bộ + Lora italic chỉ cho dòng pre · không font thứ ba
- [ ] Giữ `:focus-visible` amber + `prefers-reduced-motion`
- [ ] Ảnh WebP có width/height · lazy-load từ section 3 · trang < 500KB
- [ ] Ảnh chưa có → ô ảnh tạm đúng mẫu · **không có ảnh stock/AI**
- [ ] Có **bảng kê ảnh cần cấp** ở cuối, ghi rõ nội dung và người duyệt

**Pháp lý** — một dòng không đạt là chặn phát hành
- [ ] Không có từ cấm · **không hứa thời gian hồi phục cứng**
- [ ] ⚠️ **TUYẾN**: trang mời đại phẫu thì địa chỉ là 190 Trường Chinh hoặc 666 CMT8
- [ ] Dòng giấy phép **287/BYT-GPHĐ** nguyên văn ở footer
- [ ] Số kết quả có `*` + *"Hiệu quả phụ thuộc cơ địa mỗi người"*
- [ ] Tên bác sĩ có trong `kn-ho-so-thuong-hieu.md`
- [ ] Giá · ưu đãi · trả góp lấy động, không dùng số cũ
- [ ] Before-after đã duyệt pháp lý
- [ ] Checkbox đồng ý dữ liệu cá nhân + popup chính sách
- [ ] Người có thẩm quyền duyệt trước khi chạy
