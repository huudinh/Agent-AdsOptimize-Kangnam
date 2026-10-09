# CHANGELOG — ADS OPTIMIZE (KANGNAM)

## v2.5 — 09/10/2026 · Đồng bộ logic với gói Nha khoa Paris + Design System từ production

Đợt này **kéo gói Kangnam lên ngang gói [`Agent-AdsOptimize-NhaKhoaParis`](../../Agent-AdsOptimize-NhaKhoaParis/) v2.5**, rồi thêm phần đặc thù mà Paris không có. Bộ não brand-neutral giữ nguyên kiến trúc; phần đổi là **logic chọn khung landing**, **MODE 4**, và **ràng buộc tuyến cơ sở**.

### Cấu trúc mới

```
Agent-AdsOptimize-Kangnam/
├── README.md               ← cổng vào
├── SYSTEM-PROMPT.md        ← bộ não 19 mục (24.718 ký tự)
├── SYSTEM-PROMPT-NGAN.md   ← bản ngắn cho ChatGPT (7.986 ký tự, dư 14)
├── knowledge/              ← 8 file tri thức, upload lên nền tảng
├── prompts/                ← 3 prompt vận hành            🆕
├── zones/                  ← schema + ví dụ cấu hình ZONE  🆕
├── tools/                  ← generator .xlsx               🆕
├── template/               ← trang production đã lưu       🆕
├── out/                    ← file Excel sinh ra (gitignore) 🆕
└── doc/                    ← tài liệu vận hành, KHÔNG upload
```

---

### ① Sửa luật chọn khung landing — thay đổi quan trọng nhất

**Trước:** chọn loại landing theo **intent** — khát khao → loại A (AIDA), nỗi đau → loại B (PAS). Hệ quả: gần hết landing giai đoạn 3 bị gắn PAS.

**Nay:** chọn theo **nguồn traffic**. Landing chạy **Google Ads luôn là AIDA**, không có ngoại lệ:

| | Dùng cho |
|---|---|
| **`A1` khát khao** | giai đoạn 2 · 4 · mọi trang giá/ưu đãi |
| **`A2` trả lời trước** | **giai đoạn 3 — từ khoá nỗi sợ** ("có đau không" · "có nguy hiểm không" · "bao lâu hồi phục"). Hero gọi đúng nỗi lo rồi **trả lời ngay** |

**PAS chỉ còn dùng cho SEO · GEO · social nguội.**

Hai lý do, lý do sau nặng hơn:
1. Click **đã trả tiền** và từ khoá **đã khai intent** — trì hoãn câu trả lời để khoét sâu chỉ làm **tăng bounce**.
2. Quảng cáo dịch vụ KCB **không được gây hoang mang**. Khoét sâu nỗi sợ phẫu thuật (biến chứng · gây mê · hỏng vĩnh viễn) là **rủi ro tuân thủ**, không chỉ là copy dở.

Đồng thời tách rõ **góc ≠ khung**: góc A/B vẫn dùng cho mẫu QC (*nói về cái gì*), nhưng **không** quyết định khung landing.

Khung mở rộng từ 11/12 section lên **13 section** cho cả AIDA và PAS, bổ sung khối trust và khối gỡ 3 rào cản thành section riêng.

---

### ② MODE 4 — KEYWORD-ZONE (§13)

Mode thứ tư: từ một **ZONE dịch vụ** → bộ từ khoá Google Ads theo **chân dung KH → hành trình S1–S6 → cụm truy vấn ưu tiên**, kèm phân bổ ngân sách và bản đồ landing. Quy trình **Z1→Z7**, không đảo thứ tự.

**Nguyên tắc gốc: chọn NGƯỜI trước, chọn TỪ KHOÁ sau.** Gom từ khoá trước rồi gán người sau tạo ra nhóm quảng cáo đúng ngữ pháp nhưng sai tâm lý — và không giải thích được vì sao lead rẻ mà không ra ca.

**Tự xuất file `.xlsx` ngay trong phiên chat:** Agent sinh JSON → chạy `tools/build_keyword_workbook.py` bằng công cụ chạy code → trả file 5 sheet để tải về, kèm báo cáo và danh sách `[CHỜ CẬP NHẬT]`. Generator báo lỗi thì sửa dữ liệu rồi chạy lại, tối đa 3 lần. Không sửa script, không tự chế cấu trúc file.

6 ZONE của Kangnam: **Mũi · Mắt · Hàm mặt · Vòng 1 · Lipo 360 & Giảm béo · Trẻ hoá & Da liễu**. Không trộn 2 ZONE vào một bộ từ khoá.

File mới: `knowledge/kn-ppl-kh-trung-tam.md` · `zones/README.md` · `zones/mui.json` · `tools/build_keyword_workbook.py`.

---

### ③ TUYẾN CƠ SỞ — ràng buộc cứng, **không có tương đương ở gói Paris** (§4)

Đây là phần đặc thù nhất của gói Kangnam. Đại phẫu **chỉ được làm tại tuyến bệnh viện**: 190 Trường Chinh (HN) · 666 CMT8 (TP.HCM). Viện tỉnh làm da/spa/tiểu phẫu + tư vấn/tái khám.

**Từ khoá đại phẫu + tên tỉnh chỉ có viện tỉnh** (vd *"nâng ngực Đà Nẵng"*) là **bẫy**: chạy được và có người tìm thật, nhưng landing **không được mời mổ tại đó** — đó là vượt phạm vi giấy phép. Hai cách xử lý hợp lệ, phải chọn một và ghi rõ:

① Đổ về landing **tư vấn/đặt khám tại viện tỉnh, phẫu thuật tại tuyến bệnh viện** — nói rõ ngay ở hero; hoặc
② Đưa vào **phủ định** của chiến dịch local.

**Cài ở 4 chỗ để không bỏ sót:**

| Chỗ | Cơ chế |
|---|---|
| §4 bộ não | Mục riêng, kiểm trước mọi output local |
| §9 B7 — bảng chấm WIN | Tiêu chí ⑥ thêm "đúng tuyến"; vi phạm = **tự động 0 điểm → loại thẳng** bất kể tổng điểm |
| §11 ③ MODE 2 | Kiểm tuyến **trước khi** dựng; trang mời đại phẫu thì địa chỉ footer phải là tuyến bệnh viện |
| `tools/build_keyword_workbook.py` | **Cổng TUYẾN** — generator **chặn không build** nếu từ khoá đại phẫu + tên tỉnh mà `ghi_chu` chưa khai cách xử lý |

Bảng cơ sở ở `kn-ho-so-thuong-hieu.md` thêm cột **TUYẾN** và cột **"Được mời đại phẫu?"**.

---

### ④ Design System Kangnam v3.0 — lấy từ trang production

Token, khung trang, form và bottom sheet lấy **nguyên** từ
<https://benhvienthammykangnam.com.vn/quyen-loi-thanh-vien/dep-ven-tron/> (bản lưu: `template/dep-ven-tron.html`).

Thay cho bảng 4 màu cũ (`#003c77` · `#f6871f` · trắng · `#1D2939`), nay có bộ token đầy đủ: `--navy #074E84` · `--navy-950 #022544` · `--ynavy #1F5FC4` · `--cyan #00A5E0` · `--gold #A66E29` · `--amber #FBBF65` · `--cta #EF6103` · `--bg #F3F6FA` · `--ink #0E2338` · `--ink-2 #4A5C70` · `--line #DCE3EC` · nền trang `#D9E0E8` · 4 màu nhóm dịch vụ · `--r`/`--r-lg`/`--sh`/`--sh-lg`/`--hdr-h`.

**Ba rào tương phản đã đo** (không ước lượng):

| Luật | Số đo |
|---|---|
| `--cta` là **màu nền nút, không phải màu chữ** | trắng trên `--cta` = **3,29:1** → chữ nút cam phải **≥19px/800**; nút nhỏ hơn dùng `--navy` (8,63 AAA) |
| ⛔ `--amber` không trên nền trắng | **1,65:1** — amber chỉ trên navy (9,43 AAA) và làm vạch |
| ⛔ `--cyan` không làm chữ trên trắng | **2,82:1** — cyan chỉ là màu nhóm/viền |

Thêm: chữ phụ dùng `--ink-2` (6,87 AA) chứ không `--ink-3` (3,84); `--gold` trên trắng 4,30 → chỉ heading ≥18px.

**Typography: hai font** — `Be Vietnam Pro` cho toàn bộ, **`Lora` italic 600** chỉ cho dòng "pre" của tiêu đề section. Input bắt buộc ≥16px.

**Khung trang:** nền `#D9E0E8` · `.app` **480px** · header sticky kính mờ (logo + 1 CTA cam) · `.sec-head` (pre Lora vàng + main navy 26/800 + vạch amber) · khối form `.reg` nền `#1B4182` với card trắng · footer sáng `#f1f1ef` + **dòng giấy phép 287/BYT-GPHĐ nguyên văn** · sticky + popup CTA. Giữ nguyên phần accessibility của production: `:focus-visible` amber · `prefers-reduced-motion` · honeypot · `aria-live` · màn cảm ơn dạng `.view`.

> ⚠️ **Nói rõ trang mẫu dùng để lấy gì.** Đây là trang **quyền lợi thành viên** (`noindex`, chỉ cho khách đã nhận thông báo), chỉ có 3 section. ✅ Lấy: token · khung trang · form + bottom sheet · nhịp mobile. ❌ **Không lấy cấu trúc nội dung** — thứ tự section lấy từ khung 13 mục.

---

### ⑤ Chuẩn ô ảnh tạm + bảng kê ảnh cần cấp

Ảnh chưa có thì **không** dùng ảnh stock/AI và **không** trỏ `<img>` tới URL không tồn tại. Dựng khối viền đứt ghi rõ **tỉ lệ + nội dung ảnh cần cấp + điều kiện pháp lý**, kèm **bảng kê ảnh cần cấp** cuối mỗi landing (section · tỉ lệ · nội dung · ai duyệt). Thiếu bảng này thì trang coi như chưa giao xong.

---

### ⑥ Micro-conversion + trục riêng tư

**Micro-conversion đặt trước form** (ba mức, lấy từ trang production): chọn dịch vụ quan tâm (bottom sheet có dot màu nhóm) · chọn mức ưu đãi · **đặt khám miễn phí với bác sĩ chuyên khoa** (rào cản thấp nhất, dùng cho giai đoạn 3). ⛔ Không xin số điện thoại ngay ở hero cho ca đại phẫu.

**Trục riêng tư — đặc thù thẩm mỹ.** Rào cản NGẠI ở ngành này có trục *"không muốn người thân biết"* (rõ nhất ở khách nam và khách nữ lần đầu). Mọi landing phải có **kênh liên hệ riêng tư song song form** (Zalo/chat) hoặc dòng cam kết bảo mật dưới nút submit. Trục này **không có ở gói Paris**.

---

### ⑦ Ba điều chỉnh khi chuyển phương pháp luận từ nha khoa sang thẩm mỹ

**① Rào cản SỢ nặng hơn NGỜ — ngược với nha khoa.** Ở nha khoa khách không tự kiểm tra được vật liệu trong miệng nên NGỜ nặng nhất, và tên hãng (Straumann/Invisalign) là bằng chứng mạnh nhất. Ở thẩm mỹ, **kết quả hỏng nhìn thấy bằng mắt và nằm trên mặt** (lộ sóng · mí lệch · bóng đỏ), thêm rủi ro gây mê của đại phẫu.
→ Bằng chứng mạnh nhất **không phải tên hãng** mà là: giấy phép KCB Bộ Y tế → **KCCS** → hội đồng chuyên môn + **quy trình 5 bước vô khuẩn** → **bảo hành minh bạch** → case **HTLX (HTV7)**. Tức là bằng chứng *an toàn & tay nghề* thắng bằng chứng *vật liệu*.

**② Chân dung thêm câu thứ 6: "có cần giữ kín không".** Phương pháp luận gốc có 5 câu; thẩm mỹ thêm trục riêng tư nên thành 6.
→ Thêm vào đó: **tách hẳn khách lần đầu và khách đi sửa lại**. Nhóm sửa lại đã mất niềm tin vào cả ngành, cần bằng chứng khác và trả được CPC cao hơn — gộp chung là mất nhóm sẵn sàng trả nhiều nhất.

**③ Hệ sinh thái 5 sub-brand làm S6 phức tạp hơn.** Khách nâng mũi xong tự nhiên chuyển sang da liễu (KBS) hoặc giảm béo (KWL) — vẫn trong phạm vi thẩm mỹ. Nhưng cross-sell sang **KDT (nha khoa)** hoặc **cơ xương khớp** là **đổi sub-brand/thương hiệu** — chỉ gợi ý, không dựng nội dung bằng bộ não này.

---

### ⑧ MODE 3 đọc tới ca chốt

Có dữ liệu booking thì đọc **CPL → booking rate → chi phí/ca chốt**, không dừng ở CPL. Chu kỳ quyết định của đại phẫu dài và **lead rẻ chưa chắc là lead tốt**. Winner chỉ nhân bản sang cơ sở **cùng tuyến**.

---

### ⑨ Guardrails mở rộng

Thêm vào danh sách cấm: **"an toàn tuyệt đối"** · **"không biến chứng"** · **"không để lại sẹo"** (generator cũng chặn 3 cụm này ở cột thông điệp).

Thêm luật **không hứa thời gian hồi phục cứng** — "3 ngày là đi làm được" là câu không được viết; phải nói dạng khoảng + *"tùy cơ địa"*. Thời gian hồi phục là trục NGẠI thật của ngành nên rất dễ bị hứa quá.

Rules từ 11 lên **16 điều**; tự kiểm từ 4 lên **5 tiêu chí** (thêm "đúng tuyến cơ sở").

---

### ⑩ Tài liệu vận hành

- `01-cai-dat.md` — thêm bước bật Code Interpreter + upload 3 file MODE 4 · **16 smoke test** (thêm test cho khung A2, bẫy tuyến, ảnh stock, thời gian hồi phục cứng, tương phản nút cam, MODE 4) · **25 ca xử lý sự cố**.
- `02-cau-lenh.md` — thêm mục MODE 4 và quy trình trọn gói · **28 yêu cầu Agent sẽ từ chối**.
- `03-output-mau.md` — MODE 2 đổi từ mẫu PAS sang **mẫu A2 kèm bảng kê ảnh**; MODE 3 thêm phần đọc booking rate; thêm **mẫu đầy đủ cho MODE 4**; dấu hiệu đúng/sai từ 4 lên **8** mỗi loại.
- `04-prompt-nguoi-moi.md` — **10 → 16 prompt**, thêm 6 việc trước đây không có prompt nào: khách ở tỉnh (bẫy tuyến), chưa có ảnh, khách cần giữ kín, không xin số ngay, lead rẻ mà không ra ca, dựng cả bộ từ khoá.
- `prompts/` — 3 file mới: sinh bộ từ khoá zone · dựng landing page · quy trình trọn gói 6 bước 3 chốt dừng.

---

## ⚠️ Ràng buộc kỹ thuật cần biết khi sửa

**Bản ngắn chỉ còn dư 14 ký tự** so với hạn mức 8.000 của ChatGPT Custom GPT (hiện **7.986**).

Gói Kangnam có **nhiều luật cứng hơn gói Paris** — thêm cả khối **tuyến cơ sở** (~670 ký tự) và **trục riêng tư** — nên bản ngắn đã phải nén sâu hơn bản Paris. Những phần đã **đẩy hết về `knowledge/`**: token màu đầy đủ · bảng tương phản WCAG · 8 archetype hook · ma trận A/B T1–T5 · bảng chẩn đoán · **bảng phễu 6 giai đoạn** · khung 13 section · khung trang HTML · template mẫu QC · định dạng đầu ra từng mode · **toàn bộ Z1–Z7 của MODE 4**.

Vì bản ngắn lược nhiều hơn bản Paris, **dòng `LỆNH ĐẦU TIÊN` buộc Agent đọc hết `SYSTEM-PROMPT.md` trong Knowledge là bắt buộc — không được xoá**, và `SYSTEM-PROMPT.md` **phải** có trong Knowledge khi dùng bản ngắn.

**Nếu sửa bản ngắn: phải đếm lại ký tự khối ▼▲ trước khi dán.** Vượt 8.000 thì ChatGPT cắt phần cuối **mà không báo lỗi** — và phần cuối hiện là guardrails + mục tự kiểm.

**Nếu sửa generator:** cổng TUYẾN dùng 3 danh sách hard-code ở đầu file (`DAI_PHAU` · `VIEN_TINH` · `TUYEN_OK`). Thêm ZONE mới có dịch vụ đại phẫu thì **phải thêm từ khoá dịch vụ đó vào `DAI_PHAU`**, nếu không cổng sẽ không bắt được. Mở cơ sở mới hoặc nâng viện tỉnh lên tuyến bệnh viện thì phải sửa `VIEN_TINH`.

---

## v2.5.1 — 09/10/2026 · Bổ sung file Excel mẫu

Gói thiếu một thứ mà gói Paris có: **file `.xlsx` mẫu tải được**. Trước đó `out/` nằm trong `.gitignore` (đúng — file Excel dựng lại được từ JSON nên không cần version), nhưng hệ quả là **không có file mẫu nào trên GitHub** để người dùng xem trước hoặc đối chiếu.

Nay thêm **`template/KN _ Google Ads _ Bộ từ khoá Nâng mũi.xlsx`** (36 KB) — bản build từ `zones/mui.json`, đủ 5 sheet có công thức. `template/` không bị gitignore nên file này đi theo repo.

Dùng để: ① xem trước *file nhận được sẽ trông như thế nào* trước khi chạy MODE 4; ② kiểm xem Agent có làm đúng khuôn 5 sheet hay tự chế cấu trúc.

Khác với Paris: file mẫu của Paris (347 KB) là **file gốc làm tay** mà generator bám theo; file mẫu của Kangnam (36 KB) là **output của generator** — cấu trúc giống nhau, chỉ nhỏ hơn vì 66 từ khoá so với 123 và ít định dạng thủ công hơn.

Cập nhật kèm: bảng Tài liệu ở `README.md` · danh sách không-upload ở `doc/01-cai-dat.md` (gộp thành cả `template/`) · `zones/README.md` thêm dòng trỏ tới file mẫu · artifact hướng dẫn Bước 6 thay ghi chú "chưa có file mẫu" bằng thẻ tải file thật.

> ⚠️ Link tải trong artifact chỉ hoạt động **sau khi commit và push** file này lên GitHub.

---

## v2.0 → v1.0 — các bản trước

- v1.0 — chuẩn HCI R·M·K·W·O + Rules; BRAIN brand-neutral + MODULE thương hiệu (3.3).
- v1.1 — tích hợp Engine WIN (B1–B9) vào MODE 1/3 + cổng 2/3 tiêu chí (3.4).
- v1.2 — bổ sung Nhận diện thương hiệu (logo · địa chỉ · màu) vào 3.3.
- v1.3 — chốt mã màu bản gốc; bản gốc một file lưu tại `doc/v1-ban-goc-1-file.md` — **không dùng để cài**.
- **v2.0** — tái cấu trúc từ 1 file thành gói chuẩn: `README.md` + `SYSTEM-PROMPT.md` (17 mục) + `SYSTEM-PROMPT-NGAN.md` + 7 file `knowledge/` + 5 file `doc/`.

---

## Việc còn treo

| Hạng mục | Ảnh hưởng |
|---|---|
| **Giấy xác nhận nội dung quảng cáo** từng chiến dịch | **Chặn cứng** việc bật chiến dịch |
| **Chốt bộ nhận diện: `#003c77` hay `#074E84`** | Hồ sơ thương hiệu ghi `#003c77`/`#f6871f`, production chạy `#074E84`/`#EF6103`. Hiện xử lý: landing theo production, ấn phẩm theo hồ sơ. **Cần brand/pháp chế chốt một lần** để khỏi lệch giữa các kênh |
| **LP cho khách tỉnh (mẫu LP11) chưa qua pháp chế** | **Chặn cứng** việc bật chiến dịch local viện tỉnh — trang phải nói rõ nơi phẫu thuật |
| Kho case + ảnh before–after đã duyệt pháp lý | Bằng chứng mạnh nhất của giai đoạn 3 chưa dùng được; hiện mọi landing phải dùng ô ảnh tạm |
| **Trường CHÂN DUNG trong Caresoft** | Chưa có thì không đo được chân dung nào ra ca → không tối ưu được ngân sách theo người. Cần từ Pha 1 |
| **Import chuyển đổi offline từ Caresoft** | Chưa có thì không chuyển sang tROAS được, và không mở Broad được ở Pha 3 |
| Điều kiện & lãi suất trả góp hiện hành | Trục NGẠI "chi phí lớn" đang thiếu số cụ thể |
| Điều kiện bảo hành cụ thể theo dịch vụ | Bằng chứng "bảo hành minh bạch" đang nói chung, chưa dẫn được điều kiện |
| Benchmark CTR/CPL/CVR + **booking rate + chi phí/ca chốt** theo dịch vụ | MODE 3 phải lấy control hiện tại làm mốc; chưa đo được lead tốt hay xấu |
| Thư viện hook thắng tích lũy | B9 chưa có dữ liệu để tái sử dụng |
| **5 ZONE còn lại chưa có file cấu hình** | Hiện chỉ có `zones/mui.json`. Mắt · Hàm mặt · Vòng 1 · Lipo 360 · Trẻ hoá & Da liễu cần dựng khi tới lượt |
| Địa chỉ đường phố và **tuyến** từng cơ sở cần verify định kỳ | Tuyến đổi là cổng TUYẾN trong generator sai theo |
