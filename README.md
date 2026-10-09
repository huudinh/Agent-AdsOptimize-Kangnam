# 🎯 ADS OPTIMIZE — Tối ưu quảng cáo hiệu suất (Kangnam)

> Version 2.5 · AI **sinh mẫu quảng cáo win · dựng landing page · chẩn đoán số liệu ADS + GA · dựng bộ từ khoá theo ZONE** cho **Hệ thống Bệnh viện Thẩm mỹ Kangnam** — làm theo chỉ số, không làm theo cảm tính.

Theo công thức HCI **R·M·K·W·O**. Kiến trúc **BRAIN brand-neutral** ([`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md)) + **MODULE thương hiệu tách riêng** ([`knowledge/kn-ho-so-thuong-hieu.md`](knowledge/kn-ho-so-thuong-hieu.md)) → đổi brand chỉ cần thay module, không sửa bộ não.

Agent anh em dùng chung bộ não: [`Agent-AdsOptimize-NhaKhoaParis`](../Agent-AdsOptimize-NhaKhoaParis/) (nha khoa).

---

## Nguyên tắc tối thượng

> **Niềm tin xây bằng BẰNG CHỨNG, không bằng TÍNH TỪ.**

Khách mua thẩm mỹ mua **kết quả cảm xúc** — nhưng chỉ xuống tiền khi gỡ được **3 rào cản: Sợ → Ngờ → Ngại**.

```
❌ "Kangnam — thẩm mỹ viện số 1 Việt Nam, đẹp tuyệt đối, không biến chứng"
✅ "Giấy phép KCB 287/BYT-GPHĐ · bác sĩ thành viên Hiệp hội Thẩm mỹ Hàn Quốc (KCCS)
   · quy trình 5 bước chuẩn y khoa · bảo hành minh bạch"
```

**Phép thử trước khi xuất:** *"Câu này là bằng chứng kiểm chứng được, hay chỉ là tính từ?"*

**Thứ tự dùng bằng chứng:** giấy phép KCB Bộ Y tế → **KCCS** → hội đồng chuyên môn + **quy trình 5 bước vô khuẩn** → **bảo hành minh bạch** → case **HTLX (HTV7)**.
Ở thẩm mỹ, kết quả hỏng **nhìn thấy bằng mắt và nằm trên mặt** — nên bằng chứng về *an toàn và tay nghề* thắng bằng chứng về *vật liệu*. (Ngược với nha khoa, nơi rào cản NGỜ về vật liệu nặng nhất.)

---

## ⚠️ TUYẾN CƠ SỞ — ràng buộc cứng của gói này

**Đại phẫu chỉ tại tuyến bệnh viện:** 190 Trường Chinh (HN) · 666 CMT8 (TP.HCM).
Viện tỉnh (Hải Phòng · Nghệ An · Đà Nẵng · Cần Thơ · Thanh Hóa) chỉ làm **da/spa/tiểu phẫu + tư vấn/tái khám**.

**Từ khoá đại phẫu + tên tỉnh chỉ có viện tỉnh** (vd *"nâng ngực Đà Nẵng"*) là **bẫy**: chạy được và có người tìm thật, nhưng landing **không được mời mổ tại đó**. Hai cách xử lý hợp lệ, phải chọn một và ghi rõ:

① Đổ về landing **tư vấn/đặt khám tại viện tỉnh, phẫu thuật tại tuyến bệnh viện** — nói rõ điều đó trên trang; hoặc
② Đưa vào **phủ định** của chiến dịch local.

Để mặc không xử lý là **rủi ro pháp lý**, không phải chỉ là lead kém. Ràng buộc này được cài ở 3 chỗ: §4 bộ não · tiêu chí ⑥ của bảng chấm WIN (vi phạm = tự động 0 điểm → loại thẳng) · và **cổng TUYẾN trong generator** (chặn không build nếu `ghi_chu` chưa khai cách xử lý).

---

## Bốn chế độ

| Mode | Làm gì | Input tối thiểu | Đầu ra |
|---|---|---|---|
| **1 · WIN-AD** | Từ từ khóa → mẫu QC Google RSA + Meta | danh sách từ khóa + dịch vụ | 15 headline + 4 description + 3–5 biến thể Meta + bảng chấm WIN + kế hoạch test |
| **2 · LDP-BUILD** | Từ từ khóa → landing khung A1/A2 | cụm từ khóa + dịch vụ | blueprint 13 section + copy, hoặc HTML single-file + bảng kê ảnh cần cấp |
| **3 · LDP-ADVISOR** | Đọc ADS + GA → chẩn đoán | CTR·CPC·CPL·impression + scroll·form·booking | điểm nghẽn + 3 quyết định kèm ngưỡng và action |
| **4 · KEYWORD-ZONE** | Từ 1 ZONE → bộ từ khoá theo chân dung + hành trình | tên ZONE + ngân sách/tháng | **file `.xlsx` 5 sheet** + báo cáo + danh sách `[CHỜ CẬP NHẬT]` |

Mở phiên Agent luôn hỏi chạy mode nào. Không nói thì nó tự suy từ input và báo lại.

---

## Chọn khung landing — theo NGUỒN TRAFFIC, không theo intent

Đây là thay đổi logic quan trọng nhất của bản 2.5:

| | **Google Ads** (search trả phí) | **SEO · GEO · social nguội** |
|---|---|---|
| **Khung** | **AIDA** — không có ngoại lệ | **PAS** |
| **Vì sao** | Click **đã trả tiền** và từ khoá **đã khai intent** → vào thẳng message match, bằng chứng, CTA | Người đọc chưa thấy mình có vấn đề → phải dựng nhận biết trước |

**Hai biến thể AIDA**, khác nhau ở *thứ tự*, không khác nhau ở *góc*:

- **`A1` khát khao** — giai đoạn 2 · 4 · mọi trang giá/ưu đãi.
- **`A2` trả lời trước** — từ khoá nỗi sợ giai đoạn 3 (*"nâng ngực có đau không"* · *"gọt hàm có nguy hiểm không"* · *"hút mỡ bao lâu hồi phục"*). Hero gọi đúng nỗi lo rồi **trả lời ngay**.

⛔ **Không khoét sâu nỗi sợ trên landing chạy Ads.** Hai lý do, lý do sau nặng hơn: trì hoãn câu trả lời làm **tăng bounce**; và quảng cáo dịch vụ KCB **không được gây hoang mang** nên khoét sâu nỗi sợ phẫu thuật là **rủi ro tuân thủ**.

**Góc ≠ khung.** Góc A/B vẫn dùng để chọn *nói về cái gì* trong mẫu QC — nó không quyết định khung landing.

---

## Micro-conversion — hạ rào cản trước khi xin số

Khách giai đoạn 3 chưa sẵn sàng để lại số cho một ca đại phẫu. **Đặt một bước trung gian trước form:**

| Micro-conversion | Dùng cho |
|---|---|
| **Chọn dịch vụ quan tâm** — bottom sheet có dot màu nhóm (mẫu ở trang production) | mọi chặng, nằm trong form |
| **Chọn mức ưu đãi / voucher** | giai đoạn 4 |
| **Đặt khám miễn phí với bác sĩ chuyên khoa** — không phải đặt lịch mổ | **giai đoạn 3 ★** |

⛔ Không bắt điền số ngay ở hero cho ca đại phẫu.

**Trục riêng tư — đặc thù thẩm mỹ.** Rào cản NGẠI ở ngành này có trục *"không muốn người thân biết"* (rõ nhất ở khách nam và khách nữ lần đầu). Mọi landing phải có **kênh liên hệ riêng tư song song form** (Zalo/chat) hoặc dòng cam kết bảo mật dưới nút submit. Thiếu trục này là bỏ mất một phần lead của giai đoạn 3.

---

## Bộ nhận diện & khung trang (Design System Kangnam v3.0)

Token, khung trang, form và bottom sheet lấy **nguyên** từ trang production
<https://benhvienthammykangnam.com.vn/quyen-loi-thanh-vien/dep-ven-tron/> (bản lưu: [`template/dep-ven-tron.html`](template/)).

> ⚠️ **Trang mẫu dùng để lấy gì — và KHÔNG lấy gì.** Đây là trang **quyền lợi thành viên** (`noindex`, chỉ cho khách đã nhận thông báo), chỉ có 3 section.
> ✅ Lấy: token màu · khung trang · header/footer · form + bottom sheet · nhịp trình bày mobile.
> ❌ **Không lấy cấu trúc nội dung** — thứ tự section lấy từ khung **13 mục** ở `kn-khung-landing.md`.

**Token lõi**

```css
--navy:#074E84; --navy-900:#04365E; --navy-950:#022544; --ynavy:#1F5FC4; --cyan:#00A5E0;
--gold:#A66E29;  --amber:#FBBF65;   --terra:#D77927;
--cta:#EF6103;   --cta-press:#CF5300;
--bg:#F3F6FA;    --surface:#FFFFFF;
--ink:#0E2338;   --ink-2:#4A5C70;   --ink-3:#6E7E90;  --line:#DCE3EC;
--r-sm:8px; --r:14px; --r-lg:20px; --hdr-h:56px;
/* nền trang #D9E0E8 · khối form .reg #1B4182 · footer #f1f1ef chữ #254770 */
```

Tỷ lệ **80% trắng/`--bg` · 15% navy · 5% cam** — không nền toàn navy.

**Ba rào tương phản WCAG** (đã đo, không phải ước lượng)

| Luật | Số đo |
|---|---|
| **`--cta` là màu NỀN NÚT, không phải màu chữ** | Trắng trên `--cta` = **3,29:1** → chữ trên nút cam phải **≥19px/800** (ngưỡng large-text AA). Nút nhỏ hơn dùng `--navy` (trắng trên navy = 8,63 AAA) |
| ⛔ **`--amber` không đặt trên nền trắng** | **1,65:1**. Amber chỉ dùng trên navy (9,43 AAA) và làm vạch trang trí |
| ⛔ **`--cyan` không làm chữ trên trắng** | **2,82:1**. Cyan chỉ là màu nhóm dịch vụ / viền |

Thêm: chữ phụ dùng `--ink-2` (6,87 AA), **không** dùng `--ink-3` (3,84 trên `--bg`). `--gold` trên trắng 4,30 → chỉ heading ≥18px, đúng như `.sec-head .pre` của production.

**Hai font** — `Be Vietnam Pro` 400/500/700/800 cho toàn bộ body/nút/form/heading; **`Lora` italic 600** chỉ cho dòng "pre" của tiêu đề section và câu nhấn. Input bắt buộc ≥16px (nhỏ hơn làm iOS tự zoom). Không nạp font thứ ba.

**Khung trang**

```
body #D9E0E8
└── .app  max-width 480px, nền --bg, box-shadow, overflow-x clip
    ├── .hdr   sticky, kính mờ (blur 10px), logo + 1 CTA cam pill
    ├── <main>
    │   ├── .hero       ảnh full-width, fetchpriority="high", CTA trong màn đầu
    │   ├── <section>   .wrap padding-inline 16px
    │   │               .sec-head = .pre (Lora vàng) + .main (26/800 navy) + .bar (amber)
    │   │               card .gcard nền trắng, radius --r-lg, border-top 4px màu nhóm
    │   └── .reg        nền #1B4182, card .fcard trắng + bottom sheet chọn dịch vụ
    └── .foot  nền #f1f1ef, chữ #254770
                logo · DÒNG GIẤY PHÉP 287/BYT-GPHĐ NGUYÊN VĂN · hotline pill gradient
                · danh sách cơ sở · social · logo Bộ Công Thương
+ sticky CTA đáy (khớp max-width 480px) + popup CTA
```

Giữ nguyên phần accessibility của production: `:focus-visible` viền amber · khối `prefers-reduced-motion` · honeypot trong form · `aria-live` cho trạng thái submit · màn cảm ơn dạng `.view` riêng.

**Luật ô ảnh tạm.** Chưa có ảnh thật đã duyệt → **không** dùng ảnh stock/AI, **không** trỏ `<img>` tới URL không tồn tại. Dựng khối viền đứt `2px dashed var(--line)` nền `#E8EFFB`, giữ đúng `aspect-ratio`, bên trong ghi **tỉ lệ + nội dung ảnh cần cấp + điều kiện pháp lý**. Cuối mỗi landing kèm **BẢNG KÊ ẢNH CẦN CẤP** (section · tỉ lệ · nội dung · ai duyệt) — thiếu bảng này thì trang coi như chưa giao xong.

---

## Cổng WIN 2/3 — chạy trước mọi nội dung

**Tiền lọc:** từ khóa phải đúng lĩnh vực + có bối cảnh rõ. Lệch → loại.

| # | Tiêu chí | Đạt khi |
|---|---|---|
| ① | **Sát chuyển đổi** | Intent mua: giá · "ở đâu" · đặt lịch · trả góp — không phải thông tin thuần |
| ② | **Cạnh tranh ít → bid thấp** | Ngách, dài, hoặc local theo cơ sở |
| ③ | **Giá trị dịch vụ lớn** | Nâng ngực · Lipo 360 · chỉnh hàm · gọt V-line · nâng mũi cấu trúc |

**< 2/3 → KHÔNG làm nội dung.** Đổi hoặc thu hẹp từ khóa rồi chấm lại. Từ khóa đầu ngành gần như luôn trượt ② — thu hẹp bằng **nỗi sợ · "sửa lại/khắc phục" · địa điểm · tình huống** (trước cưới · sau sinh · họp lớp).

**Gom nhóm:** 1 nhóm = 1 dịch vụ × 1 giai đoạn phễu × 1 intent (× cơ sở nếu local) = 1 landing + 1 bộ QC. **Không trộn intent vào một landing.**

---

## Phễu 6 giai đoạn

| Giai đoạn | Dấu hiệu từ khóa | Góc thông điệp | LDP |
|---|---|---|---|
| 1 **NHẬN BIẾT** | "là gì" · "có nên" | Giáo dục nhẹ, **chưa bán** | Không chạy LDP chốt |
| 2 **TÌM HIỂU** | "ở đâu tốt" · "bao nhiêu tiền" | So sánh + USP chuẩn Hàn | **A1** |
| 3 **CÂN NHẮC & NỖI SỢ** ★ | "có đau không" · "có nguy hiểm" · "bao lâu hồi phục" · "review" · "hỏng" | **Gỡ nỗi sợ**: Bộ Y tế · KCCS · quy trình 5 bước · bảo hành | **A2 — trả lời trước** |
| 4 **THỰC HIỆN** | "giá" · "ưu đãi" · "đặt lịch" · "trả góp" | Ưu đãi + trả góp + cam kết an toàn | **A1** rút gọn, form nổi |
| 5 **HẬU PHẪU** | "chăm sóc sau" · "kiêng gì" · "sưng bao lâu" | Hướng dẫn + trấn an | Trang CRM |
| 6 **GẮN BÓ** | "khách cũ ưu đãi" · "dịch vụ khác" | Cross-sell + HTLX | **A1** |

**Giai đoạn 3 là điểm quyết định** — dồn ngân sách và chất lượng nội dung vào đây. Giai đoạn 1 và 5 **không chạy LDP chốt**.

---

## Hai cổng chặn không được bỏ qua

**① Cổng WIN 2/3** — từ khóa chưa đạt 2/3 thì không sản xuất nội dung.
**② Chấm điểm WIN ≥ 10/12** — mẫu QC chưa đạt thì không xuất. 6 tiêu chí: hook chạm 3 giây · đúng intent + giai đoạn · bằng chứng thật · gỡ ≥1 rào cản · CTA rõ 1 hành động · **tuân thủ y tế VN + Google/Meta + đúng tuyến cơ sở**. **Tiêu chí tuân thủ bị 0 điểm → loại thẳng** bất kể tổng điểm; quảng cáo đại phẫu cho viện tỉnh là tự động 0 điểm.

---

## Quick start (5 bước)

1. Tạo 1 Project / GPT / Gem mới. Tên và mô tả ngắn: xem [`doc/01-cai-dat.md` §0](doc/01-cai-dat.md).
2. **Instructions:** dán khối ▼▲ trong [`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md) — riêng **ChatGPT** dùng [`SYSTEM-PROMPT-NGAN.md`](SYSTEM-PROMPT-NGAN.md).
3. **Knowledge:** upload **8 file `.md`** trong [`knowledge/`](knowledge/).
4. **Cho MODE 4** (xuất Excel): bật công cụ chạy code (ChatGPT → *Code Interpreter*) và upload thêm [`tools/build_keyword_workbook.py`](tools/) + [`zones/README.md`](zones/) + [`zones/mui.json`](zones/).
5. Gọi mode: `MODE 1` · `MODE 2` · `MODE 3` · `MODE 4` — hoặc cứ nói bằng lời thường, Agent tự suy.

**Câu lệnh mẫu:**
```
MODE 1 — từ khóa "nâng mũi cấu trúc giá bao nhiêu hà nội". Chấm cổng WIN trước,
qua cổng thì sinh mẫu Google RSA + Meta.
```
```
MODE 4 — dựng bộ từ khoá cho ZONE "Hút mỡ Lipo 360", ngân sách 150tr/tháng,
xuất file Excel cho tôi tải về.
```

Bộ câu lệnh đầy đủ: [`doc/02-cau-lenh.md`](doc/02-cau-lenh.md) · prompt cho người chưa quen thuật ngữ ads: [`doc/04-prompt-nguoi-moi.md`](doc/04-prompt-nguoi-moi.md).

---

## Tài liệu

| File | Nội dung | Trạng thái |
|---|---|---|
| [SYSTEM-PROMPT.md](SYSTEM-PROMPT.md) | Bộ não — 19 mục · **24.718 ký tự** | ✅ |
| [SYSTEM-PROMPT-NGAN.md](SYSTEM-PROMPT-NGAN.md) | Bản ngắn **7.986 ký tự** (dư 14) — chỉ cho **ChatGPT** (ô Instructions giới hạn 8.000) | ✅ |
| [knowledge/kn-rao-phap-ly.md](knowledge/kn-rao-phap-ly.md) | Từ cấm → từ đúng · luật ảnh · HITL · policy Google/Meta | ✅ |
| [knowledge/kn-ho-so-thuong-hieu.md](knowledge/kn-ho-so-thuong-hieu.md) | Định vị · nhận diện · 8 cơ sở + **tuyến** · trust · bác sĩ · taxonomy *(module swappable)* | ✅ |
| [knowledge/kn-chan-dung-hanh-trinh.md](knowledge/kn-chan-dung-hanh-trinh.md) | Insight · 3 rào cản · phễu 6 giai đoạn | ✅ |
| [knowledge/kn-cong-win-tu-khoa.md](knowledge/kn-cong-win-tu-khoa.md) | Cổng 2/3 · phiếu chấm · gom nhóm | ✅ |
| [knowledge/kn-engine-win-ad.md](knowledge/kn-engine-win-ad.md) | B1–B7 · 8 archetype hook · ma trận A/B · chấm điểm 12 · template QC | ✅ |
| [knowledge/kn-khung-landing.md](knowledge/kn-khung-landing.md) | **Khung A1/A2/PAS · 13 section · Design System v3.0 · khung trang · ô ảnh tạm** | ✅ |
| [knowledge/kn-chan-doan-chi-so.md](knowledge/kn-chan-doan-chi-so.md) | Định nghĩa WIN bằng số · bảng chẩn đoán · thư viện hook | ✅ |
| [knowledge/kn-ppl-kh-trung-tam.md](knowledge/kn-ppl-kh-trung-tam.md) | **PPL lấy KH làm trung tâm: ZONE → chân dung → S1–S6 → cụm ưu tiên** | ✅ |
| [prompts/prompt-sinh-bo-tu-khoa-zone.md](prompts/) | MODE 4 — 1 prompt chính ra thẳng `.xlsx` + 3 phụ + 1 dự phòng | ✅ |
| [prompts/prompt-build-landing-page.md](prompts/) | MODE 2 — dựng landing, 5 prompt + checklist giao hàng | ✅ |
| [prompts/prompt-quy-trinh-tron-goi.md](prompts/) | Dây chuyền 6 bước MODE 4 → 1 → 2, 3 chốt dừng | ✅ |
| [zones/README.md](zones/README.md) | Schema JSON 17 khối + **cổng kiểm tra (gồm cổng TUYẾN)** | ✅ |
| [zones/mui.json](zones/) | Ví dụ hoàn chỉnh — 7 chân dung · 10 chiến dịch · 11 landing · 66 từ khoá | ✅ |
| [tools/build_keyword_workbook.py](tools/) | Generator `.xlsx` 5 sheet · 6 cổng kiểm tra | ✅ |
| [template/KN … Nâng mũi.xlsx](template/) | **File Excel mẫu** — bộ từ khoá ZONE Mũi đã dựng xong, đủ 5 sheet có công thức (36 KB) | 📦 |
| [template/dep-ven-tron.html](template/) | Trang production đã lưu — nguồn của Design System v3.0 | 📦 |
| [doc/01-cai-dat.md](doc/01-cai-dat.md) | Tên & mô tả · cài 3 nền tảng · smoke test · xử lý sự cố | ✅ |
| [doc/02-cau-lenh.md](doc/02-cau-lenh.md) | Câu lệnh 4 mode · prompt mẫu · điều Agent sẽ từ chối | ✅ |
| [doc/03-output-mau.md](doc/03-output-mau.md) | Output mẫu đủ 4 mode · dấu hiệu đúng/sai | ✅ |
| [doc/04-prompt-nguoi-moi.md](doc/04-prompt-nguoi-moi.md) | Prompt cho người không chuyên ads | ✅ |
| [doc/CHANGELOG.md](doc/CHANGELOG.md) | Lịch sử · việc còn treo | ✅ |
| [doc/v1-ban-goc-1-file.md](doc/v1-ban-goc-1-file.md) | Bản gốc v1.3 một file — lưu để đối chiếu, **không dùng để cài** | 📦 |

> **Quy ước:** version ghi trong header từng file, **KHÔNG** gắn version vào tên file.
> **Không upload** lên Knowledge: `doc/` · `template/` · `out/`.

---

## ⚠️ Giá & khuyến mãi là dữ liệu động

Agent **bắt buộc** lấy giá tại `/bang-gia/` và ưu đãi tại `/uu-dai/` **ở thời điểm chạy**. **Không bịa, không dùng số cũ đã nhớ.** Không truy cập được → để `[CHỜ CẬP NHẬT]` và báo người dùng.

Áp cho cả: % ưu đãi · số suất · hạn chương trình · **điều kiện và lãi suất trả góp**.

---

## Ranh giới

Không cam kết kết quả y khoa ("đẹp tuyệt đối · khỏi 100% · không biến chứng · an toàn tuyệt đối · số 1 · tốt nhất · vĩnh viễn · không để lại sẹo") · **không hứa thời gian hồi phục cứng** · không chẩn đoán/kê đơn/báo giá ca cụ thể · không bịa giá · khuyến mãi · số ca · % · giải thưởng · tên bác sĩ · review · không tạo ảnh kết quả giả · không dùng before–after chưa duyệt pháp lý · không chèn ảnh stock/AI thay ô ảnh tạm · không nêu tên hạ thấp đối thủ · không nạp CCCD/hồ sơ bệnh án/ảnh khách lên công cụ công cộng.

**Đại phẫu chỉ tại tuyến bệnh viện** (190 Trường Chinh HN · 666 CMT8 SG). Viện tỉnh làm da/spa/tiểu phẫu + tư vấn/tái khám — **không quảng cáo đại phẫu cho viện tỉnh**.

**Yêu cầu về cơ xương khớp / bảo tồn khớp** thuộc thương hiệu riêng **Cơ Xương Khớp – Wellness**, có agent riêng [`Agent-CoXuongKhop`](../Agent-CoXuongKhop/) — không viết bằng giọng thẩm mỹ.

Mọi mẫu QC / landing / tư vấn là **bản đề xuất**, phải qua người duyệt trước khi chạy. Nội dung quảng cáo dịch vụ KCB cần **giấy xác nhận nội dung quảng cáo** của cơ quan y tế trước khi phát hành.
