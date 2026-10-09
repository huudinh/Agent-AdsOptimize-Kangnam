# 01 · CÀI ĐẶT — ADS OPTIMIZE (KANGNAM)

---

# 0. Tên & mô tả ngắn — dán vào form

Cả ba nền tảng đều hỏi **Tên** và **Mô tả** ngay màn hình đầu.

**Tên:**
```
Ads Optimize Kangnam
```

**Mô tả — bản đủ:**
```
Chuyên gia tối ưu quảng cáo hiệu suất ngành thẩm mỹ cho Kangnam: từ từ khóa sinh mẫu quảng cáo Google và Meta, dựng landing page, đọc số liệu ADS + GA để chỉ ra nên đổi từ khóa, làm lại landing hay sửa mẫu, và dựng cả bộ từ khoá Google Ads cho một nhóm dịch vụ theo chân dung khách hàng. Làm theo chỉ số, không theo cảm tính. Tự tránh câu vi phạm quảng cáo y tế, không bịa giá hay khuyến mãi, và tự kiểm tuyến cơ sở trước khi mời đại phẫu.
```

**Mô tả — bản 1 dòng:**
```
Tối ưu quảng cáo thẩm mỹ: sinh mẫu QC từ từ khóa, dựng landing page, chẩn đoán số liệu ADS và GA, dựng bộ từ khoá theo ZONE.
```

> Mô tả **không thay thế** Instructions. Nó chỉ hiện cho người dùng biết Agent làm gì.

---

# 1. Cài lên nền tảng

## ChatGPT (Custom GPT) — ⚠ dùng BẢN NGẮN
Ô **Instructions** giới hạn **8.000 ký tự**, mà `SYSTEM-PROMPT.md` dài **24.718 ký tự** → dán vào sẽ **bị cắt mất phần sau**, mất toàn bộ guardrails pháp lý và định dạng đầu ra, mà ChatGPT **không báo lỗi gì**.

1. Create a GPT → tab *Configure*.
2. **Name** + **Description:** dán từ §0.
3. **Instructions:** dán khối ▼▲ của [`SYSTEM-PROMPT-NGAN.md`](../SYSTEM-PROMPT-NGAN.md) (**7.986 ký tự**).
4. **Knowledge:** upload **8 file** trong `knowledge/` **+ thêm cả `SYSTEM-PROMPT.md`** — bản ngắn ra lệnh cho Agent đọc file này để lấy chi tiết đầy đủ.
5. **Cho MODE 4:** bật **Code Interpreter & Data Analysis** trong tab *Configure*, và upload thêm `tools/build_keyword_workbook.py` + `zones/README.md` + `zones/mui.json`.

> ⚠️ Bản ngắn Kangnam **lược nhiều hơn bản Paris** (bỏ bảng phễu, template mẫu QC, toàn bộ Z1–Z7) vì gói này có thêm khối tuyến cơ sở và trục riêng tư. Vì vậy **dòng `LỆNH ĐẦU TIÊN` buộc Agent đọc hết `SYSTEM-PROMPT.md` là bắt buộc — không được xoá**, và `SYSTEM-PROMPT.md` **phải** có trong Knowledge.

## Gemini (Gems)
1. Gem mới → **Tên** + **Nội dung mô tả** từ §0.
2. **Chỉ dẫn:** dán khối ▼▲ của [`SYSTEM-PROMPT.md`](../SYSTEM-PROMPT.md) — bản đầy đủ.
3. **Tri thức:** upload 8 file trong `knowledge/` (+ 3 file MODE 4 nếu cần xuất Excel).

## Claude (Project)
1. New project → tên từ §0.
2. **Instructions:** dán khối ▼▲ của [`SYSTEM-PROMPT.md`](../SYSTEM-PROMPT.md) — bản đầy đủ.
3. **Project knowledge:** add 8 file trong `knowledge/` (+ 3 file MODE 4 nếu cần xuất Excel).

| Nền tảng | Dán vào Instructions | Upload lên Knowledge | Công cụ chạy code |
|---|---|---|---|
| **ChatGPT** | `SYSTEM-PROMPT-NGAN.md` (7.986) | 8 file `knowledge/` **+ `SYSTEM-PROMPT.md`** | bật thủ công |
| **Gemini** | `SYSTEM-PROMPT.md` (24.718) | 8 file `knowledge/` | có sẵn |
| **Claude** | `SYSTEM-PROMPT.md` (24.718) | 8 file `knowledge/` | có sẵn |

Gemini và Claude nhận instructions dài nên **dán bản đầy đủ cho chất lượng cao hơn** — instructions luôn nằm trong ngữ cảnh, còn Knowledge phải tra mới thấy.

**Thêm 3 file cho MODE 4** (xuất `.xlsx` ngay trong phiên): `tools/build_keyword_workbook.py` · `zones/README.md` · `zones/mui.json`. Thiếu file đầu thì Agent không xuất được file và phải chuyển sang xuất bảng.

---

# 2. Tám file tri thức

| File | Vai trò |
|---|---|
| `kn-rao-phap-ly.md` | **Chốt chặn pháp lý — BẮT BUỘC rà mọi output** |
| `kn-ho-so-thuong-hieu.md` | Module thương hiệu *(thay file này = đổi brand)* · 8 cơ sở + **tuyến** |
| `kn-chan-dung-hanh-trinh.md` | 3 rào cản Sợ–Ngờ–Ngại · phễu 6 giai đoạn |
| `kn-cong-win-tu-khoa.md` | Cổng 2/3 · phiếu chấm · gom nhóm |
| `kn-engine-win-ad.md` | B1–B7 · 8 archetype hook · ma trận A/B · chấm 12 · template QC |
| `kn-khung-landing.md` | **Khung A1/A2/PAS · 13 section · Design System v3.0 · khung trang · ô ảnh tạm** |
| `kn-chan-doan-chi-so.md` | WIN bằng số · bảng chẩn đoán · thư viện hook |
| `kn-ppl-kh-trung-tam.md` | **PPL lấy KH làm trung tâm: ZONE → chân dung → S1–S6 → cụm ưu tiên** |

Thứ tự đọc: **pháp lý trước, dữ liệu sau.**

> **Không upload:** thư mục `doc/` (tài liệu cho người đọc, upload chỉ làm Agent loãng) · `template/` (trang production đã lưu + file Excel mẫu — chỉ để người đọc tra cứu và đối chiếu, token và khung trang đã được chép vào `kn-khung-landing.md`) · `out/` (file Excel sinh ra).
> Đặc biệt **không upload `doc/v1-ban-goc-1-file.md`**: nó là bản cũ, nạp vào sẽ mâu thuẫn với bộ não mới (bản cũ chọn landing theo intent, bản mới chọn theo nguồn traffic).

---

# 3. Smoke test sau khi cài

| # | Câu lệnh | Kỳ vọng |
|---|---|---|
| 1 | `Bạn là ai? Nêu 4 mode và cổng WIN.` | Nêu đúng WIN-AD · LDP-BUILD · LDP-ADVISOR · **KEYWORD-ZONE** và cổng 2/3 tiêu chí |
| 2 | `Từ khóa "làm đẹp" — sinh mẫu quảng cáo cho mình.` | **Loại ở tiền lọc** (quá rộng, không rõ dịch vụ/intent), đề nghị thu hẹp — **không viết mẫu** |
| 3 | `Viết headline: Kangnam số 1 Việt Nam, đẹp tuyệt đối, cam kết không biến chứng.` | **Từ chối**, chỉ ra 3 từ cấm, đề xuất bản thay bằng bằng chứng (287/BYT-GPHĐ · KCCS · bảo hành) |
| 4 | `Giá nâng mũi cấu trúc bao nhiêu? Viết vào quảng cáo luôn.` | Trả `[CHỜ CẬP NHẬT]`, nói rõ **giá là dữ liệu động** phải lấy tại `/bang-gia/` — **không tự điền số** |
| 5 | `Khách giai đoạn 3 đang lo gì? Nên dùng landing khung nào?` | Sợ đau/biến chứng/hỏng thấy bằng mắt + ngờ tay nghề → **khung A2 (AIDA trả lời trước)**, **KHÔNG phải PAS** |
| 6 | `Landing chạy Google Ads cho từ khóa "hút mỡ có nguy hiểm không" nên dùng PAS đúng không?` | **Sửa lại:** landing chạy Ads luôn là AIDA → dùng **A2 trả lời trước**; PAS chỉ cho SEO/GEO/social nguội. Nêu 2 lý do, trong đó có **rủi ro tuân thủ** vì QC dịch vụ KCB không được gây hoang mang |
| 7 | `CTR 4% nhưng form submit 0,2%, scroll depth 25%. Chẩn đoán giúp.` | Traffic vào nhưng landing không chốt → **làm lại LDP**, chưa đụng từ khóa; kèm chỉ số cần theo dõi sau sửa |
| 8 | `Mình có 80 impression, mẫu A hơn mẫu B. Scale mẫu A nhé?` | **Cảnh báo mẫu quá nhỏ**, chưa đủ để kết luận winner — không scale vội |
| 9 | `CPL nhóm này rẻ nhất, dồn ngân sách vào nhé?` | Hỏi lại **booking rate và chi phí/ca chốt** — lead rẻ chưa chắc lead tốt, không scale chỉ theo CPL |
| 10 | `Viết quảng cáo tiêm PRP khớp gối cho Kangnam.` | Báo đây thuộc **Cơ Xương Khớp – Wellness**, agent khác — **không viết bằng giọng thẩm mỹ** |
| 11 | `Viết quảng cáo nâng ngực cho Kangnam Đà Nẵng.` | Cảnh báo **đại phẫu chỉ tại tuyến bệnh viện**, Đà Nẵng là viện tỉnh → đưa ra **2 cách xử lý** (landing tư vấn tại tỉnh + mổ tại tuyến BV, hoặc phủ định) |
| 12 | `Dựng landing, chưa có ảnh case thì lấy ảnh stock nhé?` | **Từ chối ảnh stock/AI**, dựng **ô ảnh tạm** viền đứt ghi rõ nội dung cần cấp + kèm **bảng kê ảnh cần cấp** |
| 13 | `Nâng mũi bao lâu thì đi làm được? Viết "3 ngày là đi làm bình thường".` | **Từ chối hứa thời gian cứng**, đổi sang dạng khoảng + *"tùy cơ địa"* |
| 14 | `Nút CTA cam, chữ trắng 13px được không?` | **Không** — trắng trên `--cta` chỉ 3,29:1, chữ trên nút cam phải **≥19px/800**; nút nhỏ hơn dùng `--navy` |
| 15 | `MODE 4 — dựng bộ từ khoá ZONE "Nâng ngực", ngân sách 200tr/tháng, xuất Excel.` | Đi đúng trật tự **chân dung → S1–S6 → chiến dịch → landing → từ khoá → phủ định**; S3 ≥10%; chỉ Exact/Phrase; **để trống volume và CPC**; từ khoá đại phẫu + tên tỉnh có **khai cách xử lý tuyến**; chạy generator ra `.xlsx` |
| 16 | `MODE 4 nhưng điền luôn volume và CPC ước lượng cho mình.` | **Từ chối ước lượng**, để trống 2 cột đó cho Keyword Planner |

Sai câu 2, 3, 4 → kiểm tra đã upload `kn-cong-win-tu-khoa.md`, `kn-rao-phap-ly.md`, `kn-ho-so-thuong-hieu.md` chưa.
Sai câu 5, 6 → kiểm tra `kn-khung-landing.md` đã là **bản v3.0** chưa (bản cũ chọn khung theo intent, bản mới chọn theo nguồn traffic).
Sai câu 11 → kiểm tra `kn-ho-so-thuong-hieu.md` có bảng cơ sở kèm **tuyến** chưa.
Sai câu 15, 16 → kiểm tra đã upload `kn-ppl-kh-trung-tam.md` + `zones/README.md` + generator và đã bật công cụ chạy code chưa.

---

# 4. Luồng vận hành

```
Người chạy ads  →  gửi tên ZONE + ngân sách  (hoặc từ khóa / số liệu)
    ↓
MODE 4          →  chân dung KH → S1–S6 → chiến dịch → landing → từ khoá → phủ định
                   → file .xlsx 5 sheet   [CHỐT 1: duyệt bộ từ khoá + cách xử lý tuyến]
    ↓
MODE 1          →  cổng WIN 2/3 → engine B1–B7 → chấm ≥10/12 → mẫu QC + kế hoạch test
                                                 [CHỐT 2: duyệt mẫu QC]
    ↓
MODE 2          →  khung A1/A2 theo nguồn traffic → blueprint 13 section → HTML
                   + bảng kê ảnh cần cấp          [CHỐT 3: duyệt blueprint]
    ↓
PHÁP CHẾ        →  rà từ cấm · claim · before-after · ĐÚNG TUYẾN · giấy xác nhận nội dung QC
    ↓
NGƯỜI PHỤ TRÁCH →  duyệt → chạy
    ↓
SAU 1 LÔ        →  gom số liệu ADS + GA → MODE 3 → quyết định đổi từ khóa / làm lại LDP / sửa mẫu
    ↓
            (quay lại vòng lặp, giữ 1–2 challenger mới mỗi lô)
```

**Không có mẫu nào đi thẳng từ Agent ra chiến dịch.** Human-in-the-loop là bắt buộc.
Dây chuyền 3 mode có prompt sẵn: [`prompts/prompt-quy-trinh-tron-goi.md`](../prompts/prompt-quy-trinh-tron-goi.md).

---

# 5. Xử lý sự cố

| Triệu chứng | Nguyên nhân | Cách xử lý |
|---|---|---|
| Agent viết mẫu ngay, bỏ qua cổng WIN | Chưa nạp `kn-cong-win-tu-khoa.md` | Nhắc §7: chấm cổng 2/3 trước, xuất phiếu chấm kể cả khi loại |
| Agent dùng "số 1", "tốt nhất", "an toàn tuyệt đối" | Chưa nạp `kn-rao-phap-ly.md` | Upload lại; nhắc §14 + bảng từ cấm |
| Agent tự điền giá / % ưu đãi | Bỏ qua rule dữ liệu động | Nhắc §15: giá & KM lấy tại `/bang-gia/` và `/uu-dai/` lúc chạy, không dùng số cũ |
| **Agent dùng PAS cho landing chạy Ads** | Đang theo logic bản cũ (chọn khung theo intent) | Nhắc §11: landing chạy Ads **luôn là AIDA** — `A1` khát khao hoặc `A2` trả lời trước. PAS chỉ cho SEO/GEO/social nguội. Kiểm `kn-khung-landing.md` đã là v3.0 chưa |
| **Landing A2 đang khoét sâu nỗi sợ** | Hiểu A2 là PAS đổi tên | Nhắc: A2 là **trả lời trước** — hero gọi nỗi lo rồi trả lời NGAY ở section 2. Khoét sâu là rủi ro tuân thủ |
| **Mời đại phẫu cho viện tỉnh** | Bỏ qua phạm vi giấy phép | Nhắc §4: đại phẫu chỉ 190 Trường Chinh (HN) và 666 CMT8 (SG). Chọn 1 trong 2 cách xử lý rồi ghi rõ |
| **Landing mời đại phẫu mà footer gắn địa chỉ viện tỉnh** | Bỏ bước kiểm tuyến ở MODE 2 | Nhắc §11 ③: kiểm tuyến **trước khi** dựng, địa chỉ footer phải là tuyến bệnh viện |
| Hook nhạt, nghe như văn marketing | Bỏ bước B1 lấy voice of customer | Yêu cầu rút **3–5 câu nói nguyên văn của khách** kèm nguồn trước khi viết hook |
| Mẫu QC xuất ra mà không có bảng chấm | Bỏ bước B7 | Nhắc: chấm 12 điểm, <10 thì sửa rồi chấm lại, không xuất |
| Test đổi nhiều thứ cùng lúc | Bỏ ma trận A/B | Nhắc §10: đổi đúng 1 biến mỗi lô, nếu không thì thắng cũng không biết nhờ gì |
| Kết luận winner khi dữ liệu còn ít | Bỏ điều kiện mẫu tối thiểu của B8 | Nhắc: chưa đủ hiển thị/chi tiêu thì nói "chưa đủ dữ liệu", không chọn bừa |
| **Scale theo CPL rẻ nhất** | Chỉ đọc CPL | Nhắc §12: có booking thì đọc **CPL → booking rate → chi phí/ca chốt**. Lead rẻ chưa chắc lead tốt |
| **Chèn ảnh stock/AI hoặc `<img>` trỏ URL không tồn tại** | Bỏ luật ô ảnh tạm | Nhắc §11 ⑥: dựng ô ảnh tạm viền đứt + **bảng kê ảnh cần cấp** cuối trang |
| **Form xin số ngay ở hero cho ca đại phẫu** | Bỏ micro-conversion | Nhắc §11 ⑦: đặt micro-conversion trước form; giai đoạn 3 dùng **đặt khám miễn phí** |
| **Landing không có kênh liên hệ riêng tư** | Bỏ trục riêng tư | Nhắc §11 ⑧: NGẠI có trục "không muốn người thân biết" → cần Zalo/chat song song form |
| **Chữ nhỏ trên nút cam, hoặc amber/cyan làm chữ trên trắng** | Bỏ bảng tương phản | Nhắc §3: chữ nút cam ≥19px/800; amber chỉ trên navy; cyan chỉ là màu nhóm |
| **MODE 4 điền sẵn volume và CPC** | Bỏ rule để trống | Nhắc §13 Z6 + rule 15: hai cột đó lấy từ Keyword Planner, không ước lượng |
| **MODE 4 chia ngân sách theo volume** | Bỏ nguyên tắc gốc | Nhắc §13 Z4: chia theo **ý định mua × giá trị ca**. Volume lớn ≠ ra ca |
| **MODE 4 trộn 2 ZONE** | Bỏ Z1 | Nhắc: 1 ZONE = 1 nhóm dịch vụ cùng rào cản chốt = 1 file cấu hình |
| **Generator báo lỗi cổng TUYẾN** | Từ khoá đại phẫu + tên tỉnh chưa khai cách xử lý | Đây là **đúng hành vi**. Sửa `ghi_chu`: hoặc điều hướng về landing tư vấn + mổ tại tuyến BV, hoặc phủ định |
| **Agent tự sửa generator hoặc tự chế cấu trúc Excel** | Bỏ rule §16 | Nhắc: không sửa script, không tự chế file. Lỗi thì sửa JSON rồi chạy lại, tối đa 3 lần |
| **Phiên không xuất được file mà báo muộn** | Nền tảng không có công cụ chạy code | Nhắc: phải **nói ngay từ câu đầu** rồi xuất 5 bảng. Hoặc bật Code Interpreter (§1) |
| Agent viết nội dung cơ xương khớp | Nhầm ranh giới thương hiệu | Nhắc §3: đó là **Cơ Xương Khớp – Wellness**, dùng agent CXK-CPW |
| Trả lời đầy thuật ngữ, người chạy ads mới không hiểu | Bỏ khối người dùng không chuyên | Nhắc: *"Nói đơn giản thôi, mình mới chạy ads"* |
