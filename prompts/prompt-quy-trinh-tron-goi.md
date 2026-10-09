# PROMPT MẪU — QUY TRÌNH TRỌN GÓI: từ ZONE tới file HTML

Nối 3 mode thành một dây chuyền 6 bước, có **3 chốt dừng** để người duyệt chen vào.

```
B1 bộ từ khóa → B2 ưu tiên → B3 insight → B4 mẫu QC → B5 layout LDP → B6 HTML
   └── MODE 4 ──────┘          └──── MODE 1 ────┘       └──── MODE 2 ────┘
                ▲CHỐT 1                      ▲CHỐT 2              ▲CHỐT 3
```

| Bước | Việc | Mode | Cổng phải qua mới được đi tiếp |
|---|---|---|---|
| **B1** | Phân tích & tổ chức bộ từ khóa | 4 · Z1–Z7 | Mọi từ khóa có chân dung + chặng · tổng ngân sách = 100% · **bẫy TUYẾN đã khai cách xử lý** |
| **B2** | Phân loại mức độ ưu tiên | 4 · Z4 + §7 | Chấm **cổng WIN 2/3** cho từng cụm · xếp P1–P4 |
| **B3** | Nghiên cứu insight theo từ khóa | 1 · B1 | Có **3–5 câu nói nguyên văn của khách** + nguồn. Không có → nói rõ, **không bịa** |
| **B4** | Thông điệp — mẫu Google Ads | 1 · B2–B7 | **Chấm WIN ≥ 10/12**; tiêu chí tuân thủ bị 0 → loại thẳng |
| **B5** | Dựng layout landing page | 2 · ①–④ | Khung A1/A2 khớp sheet 4 · **message match** với B4 · **tuyến đúng** |
| **B6** | Xuất file HTML | 2 · ⑤–⑧ | Checklist mobile + pháp lý + **bảng kê ảnh cần cấp** |

> **Luật xuyên suốt — MESSAGE MATCH.** Thông điệp hứa ở B4 phải xuất hiện nguyên vẹn ở hero của B5.
> Lệch chỗ này là nguyên nhân số một của *"CTR ổn nhưng không ai điền form"*.

> **Luật xuyên suốt — TUYẾN.** Đại phẫu chỉ tại 190 Trường Chinh (HN) · 666 CMT8 (TP.HCM).
> Kiểm ở B1 (từ khóa), kiểm lại ở B5 (địa chỉ landing). Sai là rủi ro pháp lý, không phải lỗi hiệu suất.

---

## 1 · PROMPT TỔNG — chạy cả 6 bước, dừng ở 3 chốt

> Thay 3 dòng trong ngoặc vuông. Dán một lần, Agent chạy tới chốt rồi chờ bạn.

```
Chạy QUY TRÌNH TRỌN GÓI 6 bước cho BVTM Kangnam, từ bộ từ khóa tới file HTML.

ZONE:          [Nâng mũi]
NGÂN SÁCH:     [180.000.000đ/tháng]
ĐÍCH CUỐI:     [1 landing page cho nhóm khách sợ đau và sợ lộ sóng]

ĐỌC TRƯỚC: kn-rao-phap-ly.md → kn-ho-so-thuong-hieu.md → kn-ppl-kh-trung-tam.md
→ kn-chan-dung-hanh-trinh.md → kn-cong-win-tu-khoa.md → kn-engine-win-ad.md
→ kn-khung-landing.md. Pháp lý trước, dữ liệu sau.

CÁCH CHẠY: tuần tự B1→B6, KHÔNG nhảy bước. Sau B2, B4 và B5 thì DỪNG,
in CHỐT KIỂM rồi chờ tôi gõ "tiếp". Bước sau chỉ được dùng dữ liệu bước trước
đã sinh ra — không tự nghĩ lại từ đầu.

─────────────────────────────────────────────────────────────
B1 · PHÂN TÍCH & TỔ CHỨC BỘ TỪ KHÓA   (MODE 4, Z1→Z7)
Chọn NGƯỜI trước, TỪ KHÓA sau.
  Z1 chốt ZONE · Z2 4-7 chân dung KH (nỗi đau thật · 1 rào cản chính
  · ai gõ Google có phải người điều trị không · giá trị ca · CÓ CẦN GIỮ KÍN KHÔNG)
  Z3 hành trình S1-S6 · Z4 chiến dịch + ngân sách · Z5 landing
  Z6 90-130 từ khóa · Z7 phủ định chéo
TÁCH HẲN khách lần đầu và khách ĐI SỬA LẠI — nhóm sửa lại đã mất niềm tin,
cần bằng chứng khác và trả được CPC cao hơn.
XUẤT: bảng chân dung → bảng hành trình → bảng chiến dịch → bảng từ khóa
      → bảng phủ định.
RÀNG BUỘC: chỉ Exact/Phrase · ĐỂ TRỐNG lượng tìm kiếm và CPC
           · tổng tỷ trọng ngân sách đúng 100% · S3 tối thiểu 10%
           · MỌI từ khóa đại phẫu + tên tỉnh phải khai cách xử lý TUYẾN
             (điều hướng về landing tư vấn + mổ tại tuyến BV, HOẶC phủ định).

─────────────────────────────────────────────────────────────
B2 · PHÂN LOẠI MỨC ĐỘ ƯU TIÊN   (MODE 4 Z4 + cổng WIN §7)
Với TỪNG cụm từ khóa ở B1:
  - Chấm cổng WIN 3 tiêu chí (sát chuyển đổi · cạnh tranh ít · giá trị lớn)
  - Xếp P1-P4 theo Ý ĐỊNH MUA × GIÁ TRỊ CA, không theo lượng tìm kiếm
  - Chấm điểm chiến dịch = ý định × giá trị ca × khả năng chốt (thang 1-5)
XUẤT: bảng xếp hạng + ngân sách/tháng từng chiến dịch + lý do thứ hạng.
      Cụm nào dưới 2/3 thì ghi rõ "giữ để hứng volume, KHÔNG sản xuất nội dung".

>>> CHỐT 1 — in bảng xếp hạng + danh sách từ khóa bẫy TUYẾN và cách xử lý.
    Hỏi tôi chọn cụm nào đi tiếp B3. DỪNG.

─────────────────────────────────────────────────────────────
B3 · NGHIÊN CỨU INSIGHT THEO TỪ KHÓA   (MODE 1, B1)
Chỉ đào cụm tôi đã chọn, không đào cả bộ.
  - Khách là ai · đang ở chặng nào · nỗi đau/khát khao · job-to-be-done
  - BẮT BUỘC rút 3-5 CÂU NÓI NGUYÊN VĂN của khách (SERP · gợi ý tìm kiếm
    · comment · review · group). Ghi nguồn từng câu.
  - Không tìm được thì nói rõ "chưa có voice of customer" — KHÔNG BỊA CÂU NÓI.
  - Chốt rào cản chính đang chặn họ: SỢ hay NGỜ hay NGẠI.
  - Khách này có cần GIỮ KÍN không? Nếu có thì ghi rõ, B5 phải cấp kênh riêng tư.
XUẤT: hồ sơ insight + danh sách câu nói thật + rào cản chính + bằng chứng
      nào của Kangnam gỡ được rào cản đó (theo thứ tự: giấy phép BYT → KCCS
      → hội đồng chuyên môn + quy trình 5 bước → bảo hành → HTLX).

─────────────────────────────────────────────────────────────
B4 · THÔNG ĐIỆP — MẪU QUẢNG CÁO GOOGLE ADS   (MODE 1, B2→B7)
  - Chọn khung A1 (khát khao) hay A2 (trả lời trước) + nói rõ vì sao.
    Landing chạy Ads luôn là AIDA; PAS chỉ cho SEO/GEO/social nguội
  - >=3 hook KHÁC ARCHETYPE, mỗi hook = 1 insight B3 + 1 bằng chứng thật
  - Google RSA: 15 headline <=30 ký tự + 4 description <=90 + path
  - Chấm WIN 6 tiêu chí x0-2, tổng __/12
XUẤT: phiếu cổng WIN → hook → RSA đầy đủ → bảng chấm WIN → kế hoạch test T1-T5.
RÀNG BUỘC: dưới 10/12 thì SỬA RỒI CHẤM LẠI, không xuất. Tiêu chí tuân thủ
           bị 0 điểm là loại thẳng bất kể tổng điểm. Quảng cáo đại phẫu cho
           viện tỉnh là tự động 0 điểm tiêu chí tuân thủ.

>>> CHỐT 2 — in mẫu QC + bảng chấm. Hỏi tôi duyệt mẫu nào. DỪNG.

─────────────────────────────────────────────────────────────
B5 · DỰNG LAYOUT LANDING PAGE   (MODE 2)
  - Khung A1 hay A2 lấy theo cột "Loại khung" của landing ở B1
  - Với A2: hero gọi đúng nỗi lo rồi TRẢ LỜI NGAY ở section 2.
    KHÔNG khoét sâu — QC dịch vụ KCB không được gây hoang mang
  - Blueprint đủ 13 section, mỗi section ghi: phục vụ chân dung nào
    · gỡ rào cản nào · bằng chứng dùng ở đây
  - Section "Gỡ 3 rào cản" phải gỡ ĐÚNG rào cản chốt ở B3
  - Micro-conversion đặt TRƯỚC form booking: chọn dịch vụ quan tâm
    / chọn mức ưu đãi / ĐẶT KHÁM MIỄN PHÍ với bác sĩ chuyên khoa.
    KHÔNG xin số điện thoại ngay ở hero cho ca đại phẫu
  - Khách cần giữ kín → thêm kênh liên hệ riêng tư (Zalo/chat) song song form
KIỂM TUYẾN: trang này có mời đại phẫu không? Nếu có thì địa chỉ footer BẮT BUỘC
            là 190 Trường Chinh (HN) hoặc 666 CMT8 (TP.HCM). In 1 dòng xác nhận.
MESSAGE MATCH: headline hero phải lặp lại gần như nguyên văn hook đã duyệt ở B4.
               In 1 dòng đối chiếu: "Hook B4: ... → Hero B5: ..."
XUẤT: blueprint 13 section + copy từng section.

>>> CHỐT 3 — in blueprint + dòng message match + dòng xác nhận tuyến.
    Hỏi tôi duyệt trước khi code. DỪNG.

─────────────────────────────────────────────────────────────
B6 · XUẤT FILE HTML   (MODE 2, giao hàng)
1 file .html single-file, mở trình duyệt là chạy, mobile-first 360-430px.
  - KHUNG TRANG chuẩn theo kn-khung-landing.md — chép đúng, chỉ thay <section>:
    nền body #D9E0E8 · container .app 480px nền --bg · header sticky kính mờ
    (logo + 1 CTA cam) · .sec-head (pre Lora vàng + main navy + vạch amber)
    · khối form .reg nền #1B4182 với card trắng · footer #f1f1ef + DÒNG GIẤY PHÉP
    287/BYT-GPHĐ NGUYÊN VĂN · sticky CTA đáy khớp 480px
  - Design System Kangnam v3.0: --navy #074E84 · --cta #EF6103 · --bg #F3F6FA
    · --ink #0E2338 · --ink-2 #4A5C70 · --line #DCE3EC · --gold #A66E29
    · --amber #FBBF65 · --r 14px / --r-lg 20px
    Tỷ lệ 80 trắng / 15 navy / 5 cam. KHÔNG nền toàn navy.
    --cta LÀ MÀU NỀN NÚT: chữ trên nút cam phải >=19px/800, nhỏ hơn dùng --navy.
    KHÔNG amber/cyan làm chữ trên trắng. Chữ phụ dùng --ink-2.
  - HAI font: Be Vietnam Pro cho toàn bộ, Lora italic 600 CHỈ cho dòng pre
  - Body >=15px · INPUT >=16px · vùng chạm >=44px · sticky CTA đáy
    · form 2 trường + bottom sheet chọn dịch vụ + honeypot + aria-live
    · scroll-margin-top: var(--hdr-h) cho section có anchor
  - Ảnh chưa có → Ô ẢNH TẠM viền đứt, ghi rõ nội dung ảnh cần cấp.
    TUYỆT ĐỐI không ảnh stock/AI, không <img> trỏ URL không tồn tại.
XUẤT kèm 3 bảng cuối file:
  (a) Section | Chân dung/rào cản phục vụ | Bằng chứng đã dùng
  (b) BẢNG KÊ ẢNH CẦN CẤP: Section | Tỉ lệ | Nội dung ảnh | Ai duyệt
  (c) GHI CHÚ NGƯỜI DUYỆT: chỗ [CHỜ CẬP NHẬT] + điểm cần pháp chế duyệt
      + xác nhận tuyến cơ sở

─────────────────────────────────────────────────────────────
RÀNG BUỘC TOÀN TUYẾN — vi phạm là dừng, không tính điểm:
  - Cấm: tốt nhất · số 1 · duy nhất · đẹp tuyệt đối · khỏi 100%
    · không biến chứng · an toàn tuyệt đối · vĩnh viễn · không để lại sẹo.
  - KHÔNG hứa thời gian hồi phục cứng — nói dạng khoảng + "tùy cơ địa".
  - KHÔNG quảng cáo/mời đại phẫu cho viện tỉnh (Hải Phòng · Nghệ An · Đà Nẵng
    · Cần Thơ · Thanh Hóa). Đó là vượt phạm vi giấy phép.
  - Không bịa giá · ưu đãi · số ca · % · tên bác sĩ · review → [CHỜ CẬP NHẬT].
    Giá đọc tại /bang-gia/ và ưu đãi tại /uu-dai/ LÚC CHẠY.
  - Mọi con số kết quả gắn * + "Hiệu quả phụ thuộc cơ địa mỗi người".
  - Mọi đầu ra là BẢN ĐỀ XUẤT, phải qua người duyệt trước khi chạy.

BẮT ĐẦU TỪ B1.
```

---

## 2 · PROMPT NGẮN — khi đã quen

```
Chạy quy trình trọn gói cho ZONE [Nâng mũi], ngân sách [180tr/tháng],
đích cuối [landing cho nhóm sợ đau + sợ lộ sóng].
B1 bộ từ khóa theo chân dung (khai cách xử lý bẫy TUYẾN) → B2 xếp ưu tiên + cổng WIN
→ B3 insight + câu nói thật của khách → B4 mẫu Google Ads chấm >=10/12 → B5 layout
13 section message-match với B4 + kiểm tuyến → B6 file HTML đúng khung trang +
Design System v3.0. Dừng sau B2, B4, B5. Tuân kn-rao-phap-ly.md. Bắt đầu từ B1.
```

---

## 3 · ĐƯỜNG TẮT — đã có bộ từ khóa rồi, chỉ cần từ B3

```
Đã có bộ từ khóa ở file [zones/mui.json] hoặc sheet 2 của workbook.
Bỏ B1-B2. Bắt đầu từ B3 cho cụm [S3 · Nỗi sợ & Bằng chứng], chân dung [CD1].
Chạy B3 → B4 → B5 → B6 theo đúng quy trình trọn gói, vẫn dừng ở CHỐT 2 và CHỐT 3.
```

---

## Bàn giao giữa các bước — thứ bắt buộc phải chảy xuống

Mỗi bước chỉ được dùng thứ bước trước đã sinh. Thiếu một trong các mục dưới đây là **đứt dây chuyền**:

| Từ → đến | Phải mang theo |
|---|---|
| B1 → B2 | Từ khóa đã gắn **chân dung + chặng + landing** · **cách xử lý tuyến** cho từ khóa local |
| B2 → B3 | **Cụm được chọn** + điểm cổng WIN + rào cản dự kiến |
| B3 → B4 | **Câu nói nguyên văn của khách** + rào cản chính đã chốt + bằng chứng gỡ + **có cần giữ kín không** |
| B4 → B5 | **Hook đã duyệt** + thông điệp đã hứa + CTA |
| B5 → B6 | Blueprint 13 section + copy + **dòng đối chiếu message match** + **dòng xác nhận tuyến** |

---

## Nghiệm thu cuối tuyến

**Nội dung**
- [ ] Mỗi section của landing truy được về một chân dung ở B1
- [ ] Hero lặp lại hook đã duyệt ở B4 (có dòng đối chiếu)
- [ ] Section "Gỡ 3 rào cản" gỡ đúng rào cản chốt ở B3
- [ ] Với khung A2: hero trả lời ngay, **không khoét sâu nỗi sợ**
- [ ] Micro-conversion đứng trước form booking · không xin số ở hero cho đại phẫu
- [ ] Chân dung cần giữ kín có kênh liên hệ riêng tư
- [ ] Mẫu QC đạt ≥ 10/12

**Kỹ thuật**
- [ ] Mobile-first 360–430px · body ≥15px · **input ≥16px** · vùng chạm ≥44px
- [ ] Sticky CTA đáy khớp 480px · form 2 trường + bottom sheet + honeypot
- [ ] Màu đúng v3.0 · **chữ nút cam ≥19px/800** · không amber/cyan làm chữ trên trắng
- [ ] **Khung trang** đúng mẫu `dep-ven-tron.html`: nền `#D9E0E8` · `.app` 480px · header sticky kính mờ · footer `#f1f1ef`
- [ ] Be Vietnam Pro + Lora italic chỉ cho dòng pre · không font thứ ba
- [ ] Ô ảnh tạm đúng mẫu · có bảng kê ảnh cần cấp

**Pháp lý** — một dòng không đạt là chặn phát hành
- [ ] Không từ cấm · **không hứa thời gian hồi phục cứng**
- [ ] ⚠️ **TUYẾN**: không mời đại phẫu cho viện tỉnh · địa chỉ landing đúng tuyến
- [ ] Dòng giấy phép **287/BYT-GPHĐ** nguyên văn ở footer
- [ ] Giá · ưu đãi · trả góp lấy động, không dùng số cũ
- [ ] Mọi `[CHỜ CẬP NHẬT]` đã điền hoặc đã xoá câu đó
- [ ] Pháp chế duyệt + giấy xác nhận nội dung quảng cáo trước khi chạy
