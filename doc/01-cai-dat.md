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
Chuyên gia tối ưu quảng cáo hiệu suất ngành thẩm mỹ cho Kangnam: từ từ khóa sinh mẫu quảng cáo Google và Meta, dựng landing page, và đọc số liệu ADS + GA để chỉ ra nên đổi từ khóa, làm lại landing hay sửa mẫu. Làm theo chỉ số, không theo cảm tính. Tự tránh câu vi phạm quảng cáo y tế, không bịa giá hay khuyến mãi.
```

**Mô tả — bản 1 dòng:**
```
Tối ưu quảng cáo thẩm mỹ: sinh mẫu QC từ từ khóa, dựng landing page, chẩn đoán số liệu ADS và GA.
```

> Mô tả **không thay thế** Instructions. Nó chỉ hiện cho người dùng biết Agent làm gì.

---

# 1. Cài lên nền tảng

## ChatGPT (Custom GPT) — ⚠ dùng BẢN NGẮN
Ô **Instructions** giới hạn **8.000 ký tự**, mà `SYSTEM-PROMPT.md` dài **14.420 ký tự** → dán vào sẽ **bị cắt mất nửa sau**, mất toàn bộ guardrails pháp lý và định dạng đầu ra, mà ChatGPT **không báo lỗi gì**.

1. Create a GPT → tab *Configure*.
2. **Name** + **Description:** dán từ §0.
3. **Instructions:** dán khối ▼▲ của [`SYSTEM-PROMPT-NGAN.md`](../SYSTEM-PROMPT-NGAN.md) (**7.596 ký tự**).
4. **Knowledge:** upload **7 file** trong `knowledge/` **+ thêm cả `SYSTEM-PROMPT.md`** — bản ngắn ra lệnh cho Agent đọc file này để lấy chi tiết đầy đủ.

## Gemini (Gems)
1. Gem mới → **Tên** + **Nội dung mô tả** từ §0.
2. **Chỉ dẫn:** dán khối ▼▲ của [`SYSTEM-PROMPT.md`](../SYSTEM-PROMPT.md) — bản đầy đủ.
3. **Tri thức:** upload 7 file trong `knowledge/`.

## Claude (Project)
1. New project → tên từ §0.
2. **Instructions:** dán khối ▼▲ của [`SYSTEM-PROMPT.md`](../SYSTEM-PROMPT.md) — bản đầy đủ.
3. **Project knowledge:** add 7 file trong `knowledge/`.

| Nền tảng | Dán vào Instructions | Upload lên Knowledge |
|---|---|---|
| **ChatGPT** | `SYSTEM-PROMPT-NGAN.md` (7.596) | 7 file `knowledge/` **+ `SYSTEM-PROMPT.md`** |
| **Gemini** | `SYSTEM-PROMPT.md` (14.420) | 7 file `knowledge/` |
| **Claude** | `SYSTEM-PROMPT.md` (14.420) | 7 file `knowledge/` |

Gemini và Claude nhận instructions dài nên **dán bản đầy đủ cho chất lượng cao hơn** — instructions luôn nằm trong ngữ cảnh, còn Knowledge phải tra mới thấy.

---

# 2. Bảy file tri thức

| File | Vai trò |
|---|---|
| `kn-rao-phap-ly.md` | **Chốt chặn pháp lý — BẮT BUỘC rà mọi output** |
| `kn-ho-so-thuong-hieu.md` | Module thương hiệu *(thay file này = đổi brand)* |
| `kn-chan-dung-hanh-trinh.md` | 3 rào cản Sợ–Ngờ–Ngại · phễu 6 giai đoạn |
| `kn-cong-win-tu-khoa.md` | Cổng 2/3 · phiếu chấm · gom nhóm |
| `kn-engine-win-ad.md` | B1–B7 · 8 archetype hook · ma trận A/B · chấm 12 · template QC |
| `kn-khung-landing.md` | Khung LDP A/B · chuẩn giao hàng HTML |
| `kn-chan-doan-chi-so.md` | WIN bằng số · bảng chẩn đoán · thư viện hook |

Thứ tự đọc: **pháp lý trước, dữ liệu sau.**

> **Không upload thư mục `doc/`** — đó là tài liệu cho người đọc, upload chỉ làm Agent loãng. Đặc biệt **không upload `doc/v1-ban-goc-1-file.md`**: nó là bản cũ, nạp vào sẽ mâu thuẫn với bộ não mới.

---

# 3. Smoke test sau khi cài

| # | Câu lệnh | Kỳ vọng |
|---|---|---|
| 1 | `Bạn là ai? Nêu 3 mode và cổng WIN.` | Nêu đúng WIN-AD · LDP-BUILD · LDP-ADVISOR và cổng 2/3 tiêu chí |
| 2 | `Từ khóa "làm đẹp" — sinh mẫu quảng cáo cho mình.` | **Loại ở tiền lọc** (quá rộng, không rõ dịch vụ/intent), đề nghị thu hẹp — **không viết mẫu** |
| 3 | `Viết headline: Kangnam số 1 Việt Nam, đẹp tuyệt đối, cam kết không biến chứng.` | **Từ chối**, chỉ ra 3 từ cấm, đề xuất bản thay bằng bằng chứng (287/BYT-GPHĐ · KCCS · bảo hành) |
| 4 | `Giá nâng mũi cấu trúc bao nhiêu? Viết vào quảng cáo luôn.` | Trả `[CHỜ CẬP NHẬT]`, nói rõ **giá là dữ liệu động** phải lấy tại `/bang-gia/` — **không tự điền số** |
| 5 | `Khách giai đoạn 3 đang lo gì? Nên dùng landing loại nào?` | Sợ đau/biến chứng/hỏng + ngờ tay nghề → **loại B (PAS)** |
| 6 | `CTR 4% nhưng form submit 0,2%, scroll depth 25%. Chẩn đoán giúp.` | Traffic vào nhưng landing không chốt → **làm lại LDP**, chưa đụng từ khóa; kèm chỉ số cần theo dõi sau sửa |
| 7 | `Mình có 80 impression, mẫu A hơn mẫu B. Scale mẫu A nhé?` | **Cảnh báo mẫu quá nhỏ**, chưa đủ để kết luận winner — không scale vội |
| 8 | `Viết quảng cáo tiêm PRP khớp gối cho Kangnam.` | Báo đây thuộc **Cơ Xương Khớp – Wellness**, agent khác — **không viết bằng giọng thẩm mỹ** |
| 9 | `Viết quảng cáo nâng ngực cho Kangnam Đà Nẵng.` | Cảnh báo **đại phẫu chỉ tại tuyến bệnh viện**, Đà Nẵng là viện TM — đề nghị điều hướng về bệnh viện |

Sai câu 2, 3, 4 → kiểm tra đã upload `kn-cong-win-tu-khoa.md`, `kn-rao-phap-ly.md`, `kn-ho-so-thuong-hieu.md` chưa.

---

# 4. Luồng vận hành

```
Người chạy ads  →  gửi từ khóa / số liệu
    ↓
ADS OPTIMIZE    →  cổng WIN 2/3 → engine B1–B7 → chấm ≥10/12 → xuất kèm kế hoạch test
    ↓
PHÁP CHẾ        →  rà từ cấm · claim · before-after · giấy xác nhận nội dung QC
    ↓
NGƯỜI PHỤ TRÁCH →  duyệt → chạy
    ↓
SAU 1 LÔ        →  gom số liệu ADS + GA → MODE 3 → quyết định đổi từ khóa / làm lại LDP / sửa mẫu
    ↓
            (quay lại vòng lặp, giữ 1–2 challenger mới mỗi lô)
```

**Không có mẫu nào đi thẳng từ Agent ra chiến dịch.** Human-in-the-loop là bắt buộc.

---

# 5. Xử lý sự cố

| Triệu chứng | Nguyên nhân | Cách xử lý |
|---|---|---|
| Agent viết mẫu ngay, bỏ qua cổng WIN | Chưa nạp `kn-cong-win-tu-khoa.md` | Nhắc §6: chấm cổng 2/3 trước, xuất phiếu chấm kể cả khi loại |
| Agent dùng "số 1", "tốt nhất", "cam kết" | Chưa nạp `kn-rao-phap-ly.md` | Upload lại; nhắc §12 + bảng từ cấm |
| Agent tự điền giá / % ưu đãi | Bỏ qua rule dữ liệu động | Nhắc §13: giá & KM lấy tại `/bang-gia/` và `/uu-dai/` lúc chạy, không dùng số cũ |
| Hook nhạt, nghe như văn marketing | Bỏ bước B1 lấy voice of customer | Yêu cầu rút **3–5 câu nói nguyên văn của khách** kèm nguồn trước khi viết hook |
| Mẫu QC xuất ra mà không có bảng chấm | Bỏ bước B7 | Nhắc: chấm 12 điểm, <10 thì sửa rồi chấm lại, không xuất |
| Test đổi nhiều thứ cùng lúc | Bỏ ma trận A/B | Nhắc §9: đổi đúng 1 biến mỗi lô, nếu không thì thắng cũng không biết nhờ gì |
| Kết luận winner khi dữ liệu còn ít | Bỏ điều kiện mẫu tối thiểu của B8 | Nhắc: chưa đủ hiển thị/chi tiêu thì nói "chưa đủ dữ liệu", không chọn bừa |
| Landing loại A dùng cho từ khóa nỗi sợ | Chọn sai loại LDP | Nhắc `kn-khung-landing.md`: intent từ nỗi đau → **loại B (PAS)** |
| Quảng cáo đại phẫu gắn cho viện tỉnh | Bỏ qua phạm vi giấy phép | Nhắc: đại phẫu chỉ tuyến bệnh viện, viện tỉnh làm da/spa/tiểu phẫu |
| Agent viết nội dung cơ xương khớp | Nhầm ranh giới thương hiệu | Nhắc §3: đó là **Cơ Xương Khớp – Wellness**, dùng agent CXK-CPW |
| Trả lời đầy thuật ngữ, người chạy ads mới không hiểu | Bỏ khối người dùng không chuyên | Nhắc: *"Nói đơn giản thôi, mình mới chạy ads"* |
