# TRI THỨC — Ads Optimize Kangnam
> File này gộp **8 module tri thức** từ `knowledge/`. Sinh tự động ngày 2026-10-22 bằng `python tools/gop-tham-khao.py`.
> ⛔ **Không sửa file này** — sửa ở bản rời trong thư mục nguồn rồi chạy lại lệnh trên.

**Cách đọc:** mỗi phần bắt đầu bằng dòng `===== tên file =====` và là **một đơn vị tri thức riêng**. Tham chiếu dạng `[[tên-file]]` trong văn bản trỏ tới **phần cùng tên ngay trong file này**, không phải file bên ngoài.

## MỤC LỤC

| # | File | Cỡ |
|---|---|---|
| 1 | `kn-chan-doan-chi-so.md` | 3.8 KB |
| 2 | `kn-chan-dung-hanh-trinh.md` | 4.8 KB |
| 3 | `kn-cong-win-tu-khoa.md` | 3.2 KB |
| 4 | `kn-engine-win-ad.md` | 6.3 KB |
| 5 | `kn-ho-so-thuong-hieu.md` | 16.6 KB |
| 6 | `kn-khung-landing.md` | 23.2 KB |
| 7 | `kn-ppl-kh-trung-tam.md` | 9.6 KB |
| 8 | `kn-rao-phap-ly.md` | 8.4 KB |


===== kn-chan-doan-chi-so.md =====

# CHẨN ĐOÁN CHỈ SỐ → QUYẾT ĐỊNH (MODE 3)
Version: 2.0 — kế thừa mục 5.3 + B8–B9 bản v1.3

## B8 · Định nghĩa WIN bằng số

Chưa có benchmark của team → **lấy control hiện tại làm mốc**.
→ Ad nào **CTR cao hơn control** VÀ **CPL thấp hơn control**, trong **cùng điều kiện** (cùng nhóm từ khóa, cùng khung giờ, cùng ngân sách tương đối) = **winner**.

**Chỉ kết luận khi đủ lượng hiển thị / chi tiêu tối thiểu.** Mẫu nhỏ thì mọi chênh lệch đều có thể là nhiễu — nói rõ *"chưa đủ dữ liệu để kết luận"* thay vì chọn bừa một winner. Đây là lỗi tốn tiền nhất trong tối ưu ads: scale một mẫu thắng nhờ may mắn.

**Số liệu cần có để chẩn đoán:**
- **ADS:** CTR · CPC · CPL · chi phí · impression · từ khóa
- **GA:** scroll depth · time-on-page · form view → submit · booking

Thiếu chỉ số nào → nói rõ **thiếu gì** và **kết luận nào chưa đưa ra được**, không suy đoán bù.

---

## Bảng triệu chứng → chẩn đoán → quyết định

| Triệu chứng số liệu | Chẩn đoán | Quyết định |
|---|---|---|
| **CTR thấp + impression cao** | Ad/hook yếu hoặc sai đối tượng | Sửa mẫu QC (MODE 1) — **chưa đụng landing** |
| **CTR cao + CVR/form thấp + scroll nông** | Traffic vào nhưng landing không chốt | **Làm lại LDP** — đổi hook hero / CTA / phần gỡ nỗi sợ |
| **CPC cao + cạnh tranh cao + CPL xấu** | Từ khóa đắt / sai intent | **Đổi hoặc thu hẹp từ khóa** — quay cổng 2/3, tìm ngách/local |
| **CVR ổn nhưng CPL vẫn cao** | Giá thầu / phân bổ ngân sách sai | **Giữ landing**, tối ưu bidding + ngân sách |
| **Form view cao, submit thấp** | Form rườm rà hoặc thiếu niềm tin tại chỗ điền | Rút gọn form + thêm trust ngay cạnh nút |
| **Nỗi đau nhóm ≠ khung landing** | Sai **loại LDP** | **Chuyển A↔B** |

**Mỗi dòng khi xuất phải kèm đủ 4 thứ:**
① ngưỡng cụ thể đang vi phạm · ② lý do dựa trên số · ③ action tiếp theo · ④ chỉ số cần theo dõi sau khi sửa (CTR · CPL · CVR).

---

## Ba quyết định của MODE 3

**① Đổi từ khóa?**
Khi intent lệch landing, hoặc CTR thấp + CPC cao + cạnh tranh cao.
→ Quay về `kn-cong-win-tu-khoa.md`, chấm lại với từ khóa hẹp hơn.

**② Làm lại LDP?**
Khi CTR ổn nhưng CVR / scroll / form thấp — người vào rồi nhưng không chốt.
→ Sửa theo thứ tự: hook hero → phần gỡ nỗi sợ → CTA → form.

**③ Đổi mẫu QC hoặc đổi khung LDP (A1↔A2)?**
Khi hook yếu, hoặc nỗi đau–khát khao không khớp khung đang dùng.
→ Quay B2–B3 của engine, hoặc đổi loại landing.

---

## B9 · Quản trị creative

- **Winner → scale**: tăng ngân sách + nhân bản sang nhóm/cơ sở tương tự.
- **Luôn giữ 1–2 challenger mới mỗi lô** — chống ad fatigue. Không có challenger thì khi winner xuống sức sẽ không có gì thay thế.
- **Lưu thư viện hook thắng theo dịch vụ** để tái sử dụng — đây là tài sản tích lũy, đừng để mất sau mỗi chiến dịch.

**Mẫu ghi thư viện hook:**
```
Dịch vụ:      Nâng mũi cấu trúc
Giai đoạn:    3 · Cân nhắc & nỗi sợ
Archetype:    5 · Nỗi sợ + trấn an
Hook:         "[nguyên văn hook thắng]"
Kết quả:      CTR __% (control __%) · CPL __ (control __)
Điều kiện:    [thời gian chạy · ngân sách · nhóm từ khóa]
```

> Luôn ghi kèm **điều kiện** — một hook thắng ở ngân sách nhỏ, nhóm hẹp chưa chắc thắng khi scale.


===== kn-chan-dung-hanh-trinh.md =====

# CHÂN DUNG KHÁCH HÀNG & PHỄU 6 GIAI ĐOẠN — Thẩm mỹ
Version: 2.2 — kế thừa mục 3.1 + 3.2 bản v1.3

## Insight nền — khách thẩm mỹ mua gì
- Khách mua **kết quả cảm xúc** (tự tin · trẻ ra · được công nhận), **không mua "ca phẫu thuật"**. Nói về quy trình trước khi nói về kết quả cảm xúc là đi sai thứ tự.
- Nhưng cảm xúc không đủ để chốt. Chốt được hay không phụ thuộc **3 rào cản**.
- Niềm tin xây bằng **bằng chứng** — giấy phép · chứng chỉ bác sĩ · ảnh/case thật · bảo hành · review. **Không xây bằng tính từ** ("đẹp nhất", "số 1").

## Ba rào cản chốt — gỡ đúng thứ tự

| Rào cản | Khách đang nghĩ gì | Bằng chứng gỡ |
|---|---|---|
| **① SỢ** | Đau không? Biến chứng không? Hỏng thì sao? | Quy trình 5 bước chuẩn y khoa · môi trường vô khuẩn · hội đồng chuyên môn giám sát · gói chăm sóc hậu phẫu |
| **② NGỜ** | Bác sĩ có thật giỏi không? Cơ sở có phép không? Có giá ẩn không? | Giấy phép KCB 287/BYT-GPHĐ · ekip bác sĩ phẫu thuật HTLX · bảng giá công khai · bảo hành minh bạch |
| **③ NGẠI** | Nghỉ bao lâu? Người nhà có biết không? | Mốc hồi phục cụ thể theo dịch vụ · tư vấn kín đáo · tái khám định kỳ |

> Mọi nội dung chốt phải gỡ **đúng rào cản của giai đoạn phễu đang nhắm**. Gỡ sai rào cản = nói lạc đề với người đang lo chuyện khác.

## Phễu 6 giai đoạn → bản đồ thông điệp

| Giai đoạn | Nhiệt | Tâm lý / nỗi đau | Dấu hiệu intent trong từ khóa | Góc thông điệp Ads | LDP nên dùng |
|---|---|---|---|---|---|
| **1 NHẬN BIẾT** | Cold | Chưa ý thức vấn đề, tò mò | "là gì" · "có nên" · "xu hướng" | Khơi gợi + giáo dục nhẹ, **chưa bán** | Content/awareness — **không chạy LDP chốt** |
| **2 TÌM HIỂU** | Warm | Đã biết vấn đề, so sánh phương pháp | "phương pháp" · "công nghệ" · "ở đâu tốt" · "bao nhiêu tiền" | So sánh + USP + định vị chuẩn Hàn / Bộ Y tế | **A1** (thiên giáo dục) |
| **3 CÂN NHẮC & NỖI SỢ ★** | Warm→Hot | Sợ đau/biến chứng/hỏng, ngờ tay nghề | "có đau không" · "bao lâu hồi phục" · "có nguy hiểm" · "bác sĩ nào" · "review" · "hỏng" | **Gỡ nỗi sợ**: an toàn Bộ Y tế · ekip bác sĩ phẫu thuật HTLX · bảo hành · ảnh thật | **A2 — AIDA trả lời trước** (xem `kn-khung-landing.md`) |
| **4 THỰC HIỆN** | Hot | Sẵn sàng, cần ưu đãi + đặt lịch | "giá [dịch vụ]" · "ưu đãi" · "đặt lịch" · "chi phí" | Ưu đãi có hạn + đặt lịch nhanh + cam kết an toàn | **A1** rút gọn, form booking nổi |
| **5 TRẢI NGHIỆM & HẬU PHẪU** | Existing | Lo hồi phục, chăm sóc đúng cách | "chăm sóc sau" · "kiêng gì" · "sưng bao lâu" | Hướng dẫn + trấn an + mời tái khám | Trang hướng dẫn/CRM — **không chạy ads chốt** |
| **6 GẮN BÓ & MỞ RỘNG** | LTV | Hài lòng → dịch vụ tiếp theo | "dịch vụ [khác]" · "khách cũ ưu đãi" | Cross-sell + loyalty + HTLX | **A1** cho dịch vụ mới |

**Giai đoạn 3 là điểm quyết định** — ngân sách và chất lượng nội dung nên dồn vào đây.
**Giai đoạn 1 và 5 không chạy LDP chốt** — ép bán ở đây là đốt ngân sách và làm hỏng niềm tin.

> ⚠️ **Cột "LDP nên dùng" ghi khung cho landing chạy Google Ads.** Khung chọn theo **nguồn traffic**, không theo intent: landing chạy Ads **luôn là AIDA** — `A1` khát khao hoặc `A2` **trả lời trước** (cho từ khoá nỗi sợ giai đoạn 3). **PAS chỉ dành cho SEO · GEO · social nguội.**
>
> Lý do, lý do sau nặng hơn: ① click đã trả tiền và từ khoá đã khai intent nên trì hoãn câu trả lời chỉ làm tăng bounce; ② **quảng cáo dịch vụ KCB không được gây hoang mang** nên khoét sâu nỗi sợ phẫu thuật là **rủi ro tuân thủ**.
>
> Luật đầy đủ + khung 13 section ở [`kn-khung-landing.md`](kn-khung-landing.md).

## Cách nhận diện giai đoạn từ một từ khóa lạ
1. Từ khóa có **giá / "ở đâu" / "đặt lịch" / "ưu đãi"** → giai đoạn 4.
2. Có **"có đau không" / "nguy hiểm" / "review" / "hỏng" / "bác sĩ nào"** → giai đoạn 3.
3. Có **"so sánh" / "loại nào tốt" / "công nghệ"** → giai đoạn 2.
4. Có **"là gì" / "có nên"** → giai đoạn 1.
5. Có **"sau khi" / "kiêng" / "chăm sóc"** → giai đoạn 5.
6. Không khớp nhóm nào → hỏi lại người dùng, **không đoán bừa**.


===== kn-cong-win-tu-khoa.md =====

# CỔNG WIN — Chọn & gom nhóm từ khóa (2/3 tiêu chí)
Version: 2.0 — kế thừa mục 3.4 bản v1.3

> Cổng này chạy **trước mọi việc sản xuất nội dung**. Từ khóa không qua cổng thì không viết — tiết kiệm được cả ngân sách lẫn công sức làm landing.

## Bước 0 — Tiền lọc (bắt buộc)
Từ khóa phải **đúng lĩnh vực + có bối cảnh rõ**: nêu được **dịch vụ** hoặc **địa điểm** hoặc **intent**. Lệch lĩnh vực hoặc mơ hồ hoàn toàn → **loại ngay**, không chấm tiếp.

Ví dụ loại: `làm đẹp` (quá rộng, không rõ dịch vụ) · `thẩm mỹ viện` (không intent) · `con gái đẹp` (lệch).
Ví dụ qua: `nâng mũi cấu trúc giá bao nhiêu` · `gọt hàm v-line ở đâu uy tín hà nội` · `hút mỡ bụng có nguy hiểm không`.

## Ba tiêu chí lõi — đạt ≥ 2/3 mới được sản xuất

| # | Tiêu chí | Đạt khi | Không đạt khi |
|---|---|---|---|
| ① | **Sát chuyển đổi (CR)** | Intent mua: có giá · "ở đâu" · "đặt lịch" · "ưu đãi" · tên dịch vụ cụ thể | Thông tin thuần: "là gì" · "có mấy loại" · tra cứu kiến thức |
| ② | **Cạnh tranh ít → bid thấp** | Ngách, dài, hoặc local theo cơ sở; ít đối thủ đấu giá | Từ khóa đầu ngành, ai cũng đấu, CPC cao |
| ③ | **Giá trị dịch vụ lớn ($)** | Dịch vụ biên lợi nhuận cao: nâng ngực · hút mỡ Lipo 360 · chỉnh hàm · nâng mũi cấu trúc | Dịch vụ giá thấp, khó bù chi phí quảng cáo |

## Quyết định
- **< 2/3 → KHÔNG làm nội dung.** Đổi từ khóa, hoặc thu hẹp lại (thêm dịch vụ cụ thể / thêm địa điểm / thêm intent) rồi chấm lại.
- **≥ 2/3 → chuyển MODE 1 (WIN-AD).**

**Luôn xuất phiếu chấm**, kể cả khi loại — để người duyệt thấy vì sao loại:

```
PHIẾU CỔNG WIN
Từ khóa:    "hút mỡ bụng giá bao nhiêu hà nội"
Tiền lọc:   ĐẠT (dịch vụ + địa điểm + intent giá)
① Sát CR:        ĐẠT  — có "giá", intent mua rõ
② Cạnh tranh ít: KHÔNG — từ khóa đầu ngành, nhiều đối thủ đấu
③ Giá trị lớn:   ĐẠT  — Lipo 360 thuộc nhóm biên cao
→ 2/3 · QUA CỔNG → MODE 1
Ghi chú: nên thêm biến thể local hẹp hơn để kéo CPC xuống
```

## Gom nhóm từ khóa
**1 nhóm = 1 dịch vụ × 1 giai đoạn phễu × 1 intent.**
→ 1 nhóm = **1 landing page + 1 bộ mẫu QC**.

**Không trộn nhiều intent vào 1 landing.** Người tìm "có đau không" (giai đoạn 3, đang sợ) và người tìm "giá bao nhiêu" (giai đoạn 4, sẵn sàng) cần hai trang khác nhau — gộp lại thì cả hai đều không được phục vụ đúng.

Chạy local thì thêm chiều **cơ sở**: 1 nhóm = 1 dịch vụ × 1 giai đoạn × 1 intent × 1 cơ sở. Nhớ kiểm tra **phạm vi giấy phép** của cơ sở đó — đại phẫu chỉ tuyến bệnh viện.

## Khi nào quay lại cổng này
MODE 3 chẩn đoán ra **"đổi từ khóa"** (CTR thấp + CPC cao + cạnh tranh cao, hoặc intent lệch landing) → quay về đây, chấm lại với từ khóa hẹp hơn.


===== kn-engine-win-ad.md =====

# ENGINE WIN-AD — B1→B7 & template mẫu QC
Version: 2.2 — kế thừa mục 4 (MODE 1) + 5.1 bản v1.3

Chạy tuần tự sau khi từ khóa đã **qua cổng 2/3** (`kn-cong-win-tu-khoa.md`). Đọc kết quả & lặp ở MODE 3 (B8–B9).

---

## B1 · Nghiên cứu insight từ từ khóa
Từ từ khóa, suy ra:
- **Khách là ai** — tuổi, giới, hoàn cảnh.
- **Giai đoạn phễu** — tra `kn-chan-dung-hanh-trinh.md`.
- **Nỗi đau / khát khao** — cái gì đang làm họ khó chịu, cái gì họ muốn thấy trong gương.
- **Job-to-be-done** — họ "thuê" dịch vụ này để làm gì trong đời họ.

**Bắt buộc rút 3–5 câu nói nguyên văn của khách** từ: SERP · ads đối thủ · comment · review · hỏi đáp · group Facebook · gợi ý tìm kiếm.
→ Dùng chính câu đó làm hook. **Voice of customer luôn win hơn văn marketing.**

Xuất kèm nguồn mỗi câu. Không tìm được câu thật → nói rõ **"chưa có voice of customer"**, không bịa câu nói.

---

## B2 · Chọn góc
- **Góc A — khát khao.** Dùng khi khách đã muốn đẹp, chỉ đang chọn làm gì / ở đâu.
- **Góc B — nỗi đau.** Dùng khi intent xuất phát từ khiếm khuyết/nỗi sợ.

**1 nội dung = 1 góc chính.** Trộn hai góc trong một mẫu làm loãng cả hai.

> ⚠️ **GÓC ≠ KHUNG LANDING.** Góc chỉ quyết định *mẫu quảng cáo nói về cái gì*.
> Khung landing chọn theo **nguồn traffic**: landing chạy Google Ads **luôn là AIDA**
> (`A1` khát khao / `A2` trả lời trước), **PAS chỉ cho SEO · GEO · social nguội**.
> Một mẫu QC góc B hoàn toàn có thể đổ về landing khung A2. Xem [`kn-khung-landing.md`](kn-khung-landing.md).

---

## B3 · HOOK — quyết định ~80% hiệu quả
Hook = **3 giây đầu / dòng 1 / headline**. Viết **≥ 3 hook khác archetype** cho mỗi nhóm; mỗi hook = **1 insight (B1) + 1 bằng chứng thật** (`kn-ho-so-thuong-hieu.md`).

| # | Archetype | Khung |
|---|---|---|
| 1 | Nỗi đau trực diện | "[Vấn đề]? Lý do & cách xử lý" |
| 2 | Câu hỏi chốt intent | "Đang tìm [dịch vụ] tại [địa điểm]?" |
| 3 | Bằng chứng định lượng | "[Số] ca [dịch vụ] — [kết quả thật]" |
| 4 | Phá vỡ hiểu lầm | "Tưởng [X]…? Sự thật là…" |
| 5 | Nỗi sợ + trấn an | "Sợ [đau/hỏng/biến chứng]? [Công nghệ/bác sĩ] giải quyết" |
| 6 | Khát khao + hình ảnh hóa | "[Kết quả mong muốn] sau [thời gian]" |
| 7 | FOMO ưu đãi | "[Ưu đãi] chỉ còn đến [hạn]" |
| 8 | Social proof | "[Người thật/KOL] đã [kết quả]" |

> Archetype 3 và 7 cần **số thật**. Không có số đã duyệt → đổi archetype khác, **không bịa số**.

---

## B4 · Dựng body theo tầng thông điệp
```
HOOK
 → khoét nỗi đau / khát khao
 → giải pháp + USP
 → bằng chứng (gỡ Sợ – Ngờ – Ngại)
 → ưu đãi
 → CTA + hotline
```
**Mỗi câu một nhiệm vụ.** Bằng chứng phải khớp đúng rào cản của giai đoạn phễu đang nhắm — giai đoạn 3 thì dồn bằng chứng gỡ **Sợ** và **Ngờ**, giai đoạn 4 thì dồn vào minh bạch chi phí và tốc độ đặt lịch.

---

## B5 · Xuất mẫu QC

### Google Responsive Search Ad
- **15 headline ≤ 30 ký tự** — phủ đủ 4 nhóm: `[dịch vụ + từ khóa]` · `[USP/bằng chứng]` · `[gỡ nỗi sợ]` · `[ưu đãi/CTA]`.
- **4 description ≤ 90 ký tự** — mỗi mô tả = 1 lợi ích + 1 bằng chứng + 1 CTA.
- **Path hiển thị:** `/[dich-vu]/[uu-dai]`.

### Meta Ad — 3–5 biến thể mỗi nhóm
- **Primary text:** hook (dòng 1 chạm nỗi đau/khát khao) → bằng chứng (giấy phép · ekip bác sĩ phẫu thuật HTLX · bảo hành) → CTA + hotline.
- **Headline ≤ 40 ký tự** + **Description ≤ 30 ký tự**.
- **Gợi ý visual:** mô tả bằng chữ (ảnh case thật / bác sĩ / cơ sở) — **không chèn ảnh bịa**, không mô tả ảnh kết quả không có thật.

**Mỗi mẫu gắn nhãn:** `Nhóm từ khóa | Giai đoạn | Góc A/B | Giả thuyết test (biến gì)`.

---

## B6 · Ma trận A/B — đổi đúng 1 biến mỗi lô

| Lô | Biến đổi | Giữ nguyên | Đọc chỉ số |
|---|---|---|---|
| T1 | Hook (3 archetype) | body · offer · visual | CTR |
| T2 | Góc A↔B | hook thắng T1 | CTR + CVR |
| T3 | Bằng chứng (công nghệ / bác sĩ / case) | hook + góc thắng | CVR |
| T4 | Ưu đãi / CTA | thân thắng | CPL + Booking |
| T5 | Visual (case / bác sĩ / cơ sở) | copy thắng | CTR + CPL |

Đổi nhiều biến cùng lúc → thắng cũng **không biết nhờ cái gì**, không tái lập được.

---

## B7 · Chấm điểm WIN — ≥ 10/12 mới được duyệt
Mỗi tiêu chí **0 – 1 – 2 điểm**:

| # | Tiêu chí | 0 điểm | 2 điểm |
|---|---|---|---|
| 1 | Hook chạm trong 3 giây | Chung chung, không ai nhận ra mình | Đúng câu khách tự nói |
| 2 | Đúng intent + giai đoạn | Lệch giai đoạn phễu | Khớp đúng nỗi lo của giai đoạn |
| 3 | Bằng chứng thật | Toàn tính từ | Giấy phép/chứng chỉ/case cụ thể |
| 4 | Gỡ ≥ 1 rào cản | Không chạm Sợ–Ngờ–Ngại | Gỡ thẳng rào cản chính |
| 5 | CTA rõ 1 hành động | Mơ hồ hoặc nhiều CTA | Một hành động duy nhất, rõ |
| 6 | Tuân thủ y tế VN + Google/Meta **+ đúng tuyến cơ sở** | Có từ cấm / claim vi phạm / **mời đại phẫu ở viện tỉnh** / hứa thời gian hồi phục cứng | Sạch, đã rà `kn-rao-phap-ly.md` và đã xác nhận tuyến |

**Tổng < 10/12 → sửa rồi chấm lại. Không xuất mẫu chưa đạt.**

> ⛔ **Tiêu chí 6 bị 0 điểm = LOẠI THẲNG, bất kể tổng điểm.** Ba lỗi tự động cho 0 điểm:
> ① có từ cấm (gồm *"an toàn tuyệt đối"* · *"không biến chứng"* · *"không để lại sẹo"*);
> ② **quảng cáo/mời đại phẫu cho viện tỉnh** — vượt phạm vi giấy phép, xem `kn-ho-so-thuong-hieu.md`;
> ③ **hứa thời gian hồi phục cứng** (vd *"3 ngày là đi làm được"*) thay vì dạng khoảng + *"tùy cơ địa"*.
Tiêu chí 6 bị 0 điểm → **loại thẳng**, bất kể tổng điểm.


===== kn-ho-so-thuong-hieu.md =====

# HỒ SƠ THƯƠNG HIỆU — KANGNAM *(module swappable)*
Version: **2.3** — 2026-10-20: gỡ claim "bác sĩ thành viên KCCS" khỏi khối Trust + chuỗi bằng chứng, và gỡ "trả góp" (Kangnam không có dịch vụ này) — luật ③ và ④ ở `kn-rao-phap-ly.md`. Trước đó: v2.2 — 2026-10-16: đối chiếu trực tiếp với site production (bác sĩ · cơ sở · taxonomy). Trước đó: v2.1 bổ sung cột TUYẾN và đối chiếu Design System v3.0.

> 🔧 **Ba mục đã sửa ở v2.2 — đọc trước khi dùng lại nội dung cũ:**
> ① **Dr. Jolie Huynh đã bị loại** (trang 404, không còn trong danh sách live) — rà lại landing và mẫu quảng cáo đang chạy.
> ② **Cơ sở: 7, không phải 8** — bỏ dòng "Kangnam Hà Nội (Viện TM) 194 Trường Chinh".
> ③ **Taxonomy: 10 nhóm** — tách *Da liễu* và *Trị sắc tố*.
> Nguồn: `/doi-ngu-bac-si/` · `/chi-nhanh/` · menu chính. Chụp lại: `python ../Agent-LDP-Kangnam/tools/fetch-du-lieu.py`

> Đây là **module thương hiệu**. Đổi sang brand khác = thay file này + `kn-rao-phap-ly.md`, giữ nguyên bộ não.

## Định vị
Hệ thống **Bệnh viện Thẩm mỹ chuẩn Hàn tại Việt Nam**, nền tảng **Y khoa Quốc tế** — hệ thống bệnh viện + viện thẩm mỹ toàn quốc (Bắc – Trung – Nam).

## Nhận diện thương hiệu
**Logo** (biểu tượng + chữ "KANGNAM", chuẩn Hàn — giữ safe-area, **không đổi màu / bóp méo / thêm bóng**):
- Header: `https://benhvienthammykangnam.com.vn/wp-content/themes/SCI_Theme_v3/Module/Home/header_kn_3_0_0/images/logo-kbh.png`
- Footer (SVG, nền tối): `https://benhvienthammykangnam.com.vn/wp-content/themes/SCI_Theme_v3/Module/Home/footer_kn_3_1_0/images/logo.svg`
- Hệ sinh thái (cùng thư mục `header_kn_3_0_0/images/`): KPS `logo-kps.png` · KBS `logo-kbs.png` · KDT `logo-kdt.png` · KWN `logo-kwn.png` · KWL `logo-kwl.png`

**Màu — bộ nhận diện cấp thương hiệu:**

| Vai trò | Mã | Dùng ở |
|---|---|---|
| Primary Navy | `#003c77` | menu · điểm nhấn · heading |
| CTA | `#f6871f` | nút hành động |
| Nền | `#FFFFFF` | chủ đạo, **≥ 80% diện tích** |
| Text | `#1D2939` | thân bài |

> ⚠️ **Lệch với trang production — đọc trước khi dựng landing.**
> Trang production `dep-ven-tron.html` đang chạy `--navy #074E84` và `--cta #EF6103`, không phải `#003c77` / `#f6871f`.
> **Dựng landing thì dùng token production** ở [`kn-khung-landing.md`](kn-khung-landing.md) (Design System Kangnam v3.0) để trang mới khớp trang đang chạy.
> Bảng trên vẫn là bộ nhận diện cho **ấn phẩm cấp thương hiệu** (profile, brochure, biển hiệu).
> Chênh lệch này **cần brand/pháp chế chốt một lần** — xem *Việc còn treo* ở [`doc/CHANGELOG.md`](../doc/CHANGELOG.md).

**Font:** Be Vietnam Pro (production dùng thêm **Lora italic** cho dòng "pre" của tiêu đề section).

**Giọng:** chuyên nghiệp – y khoa nhưng ấm, "chuẩn Hàn", tận tâm. **Không** dùng từ cấm / so sánh tuyệt đối.

## Cơ sở
Hotline chung **0968.999.777** · email **benhvienthammy@kangnam.com.vn** · App **Kangnam Care** · Zalo OA.
Pháp nhân chịu trách nhiệm nội dung: **Công ty TNHH Bệnh viện Thẩm mỹ Kangnam Sài Gòn**.

> **Tổng: 7 cơ sở tại 7 tỉnh thành — 2 bệnh viện thẩm mỹ + 5 viện thẩm mỹ.** *(nguồn `/chi-nhanh/`, đối chiếu 2026-10-16)*

| Cơ sở | **TUYẾN** | Địa chỉ | Khu vực | Được mời đại phẫu? |
|---|---|---|---|---|
| Kangnam Hà Nội | **Bệnh viện** (GP 194/BYT-GPHĐ) | 190 Trường Chinh, Hà Nội | Bắc | ✅ **CÓ** |
| Kangnam Sài Gòn | **Bệnh viện** (GP 287/BYT-GPHĐ) | 666 CM Tháng 8, P. Tân Sơn Nhất, TP.HCM | Nam | ✅ **CÓ** |
| Kangnam Hải Phòng | Viện thẩm mỹ | 378 Tô Hiệu, P. Trần Nguyên Hãn, TP. Hải Phòng | Bắc | ❌ không |
| Kangnam Nghệ An | Viện thẩm mỹ | 148 Nguyễn Văn Cừ, TP. Vinh | Trung | ❌ không |
| Kangnam Đà Nẵng | Viện thẩm mỹ | 293 Hùng Vương, P. Thanh Khê, Đà Nẵng | Trung | ❌ không |
| Kangnam Cần Thơ | Viện thẩm mỹ | 28 Lý Tự Trọng, P. Ninh Kiều, TP. Cần Thơ | Nam | ❌ không |
| Kangnam Thanh Hóa | Viện thẩm mỹ | 103 Nguyễn Trãi, P. Hạc Thành, Thanh Hóa | Trung | ❌ không |

> 🔧 **Sửa 2026-10-16:** bảng cũ có thêm dòng *"Kangnam Hà Nội (Viện TM) — 194 Trường Chinh, P. Kim Liên"* → **không có trên `/chi-nhanh/`, đã bỏ khỏi bảng này**. Lưu ý `194` cũng là **số giấy phép** của bệnh viện Hà Nội (bệnh viện ở số **190**), nên dòng cũ dễ gây nhầm.
> ⚠️ **Chưa khẳng định cơ sở này đã đóng.** Các file brand khác gọi địa chỉ 194 Trường Chinh là *"Viện Trẻ hoá & Điều trị da công nghệ cao"* — có thể là **pháp nhân khác**, không phải một cơ sở Kangnam. Tương tự với *218 Nguyễn Trãi (SG CS2)* và *chi nhánh Bình Dương*. **Chỉ dùng 7 cơ sở ở bảng trên cho nội dung local**; ba địa chỉ kia chỉ dùng sau khi Pháp chế xác nhận — nêu sai pháp nhân là rào **R3**.

## ⚠️ TUYẾN CƠ SỞ — ràng buộc cứng

**Đại phẫu chỉ tại tuyến bệnh viện:** 190 Trường Chinh (HN) · 666 CMT8 (TP.HCM).
**5 viện thẩm mỹ** (Hải Phòng · Nghệ An · Đà Nẵng · Cần Thơ · Thanh Hóa) làm **da/spa/tiểu phẫu + tư vấn/tái khám** — **không quảng cáo, không mời đại phẫu**.

Site tự phát biểu luật này, dùng được nguyên văn làm copy:
> *"Kangnam Hà Nội và Kangnam Sài Gòn [thực hiện được phẫu thuật lớn]. Các viện thẩm mỹ tập trung dịch vụ da, spa, tiểu phẫu trong phạm vi giấy phép, cùng vai trò tư vấn và tái khám."*
> *"Tái khám và chăm sóc hậu phẫu tại chi nhánh Kangnam gần nhà nhất, không bắt buộc quay lại đúng nơi đã phẫu thuật."*

**Từ khoá đại phẫu + tên tỉnh chỉ có viện thẩm mỹ** (vd *"nâng ngực Đà Nẵng"*) là **bẫy**: chạy được và có người tìm thật, nhưng landing **không được mời mổ tại đó**. Hai cách xử lý hợp lệ, phải chọn một và ghi rõ:

① Đổ về landing **tư vấn/đặt khám tại viện thẩm mỹ, phẫu thuật tại tuyến bệnh viện** — nói rõ điều đó **ngay ở hero**; hoặc
② Đưa vào **phủ định** của chiến dịch local.

Để mặc không xử lý là **vượt phạm vi giấy phép** — rủi ro pháp lý, không phải chỉ là lead kém.

**Ràng buộc này được cài ở 4 chỗ:** §4 bộ não · tiêu chí ⑥ bảng chấm WIN (vi phạm = tự động 0 điểm → loại thẳng) · bước ③ của MODE 2 (kiểm trước khi dựng) · **cổng TUYẾN trong `tools/build_keyword_workbook.py`** (chặn không build nếu `ghi_chu` chưa khai cách xử lý).

> Hotline campaign có thể khác số tổng đài (vd LP dùng 0962778866). **Địa chỉ, tuyến và phạm vi giấy phép đổi theo thời điểm — chạy local phải verify lại trước khi bật chiến dịch.**

## Trust / pháp lý — dùng làm bằng chứng gỡ nỗi sợ
- Giấy phép KCB **287/BYT-GPHĐ** (Bộ Y tế, 03/12/2020 — **Sài Gòn**) và **194/BYT-GPHĐ** (**Hà Nội**). Footer phải ghi **đúng số của cơ sở mà nội dung đang nhắm**.
- Bác sĩ có **chứng chỉ hành nghề (CCHN)** — số CCHN từng người ở bảng mục *Bác sĩ*. Đây là bằng chứng tay nghề **duy nhất** được dùng ở mức cá nhân, và phải nêu kèm **tên + chuyên khoa + cơ sở**.
- ⛔ **Không dùng claim hội – hiệp hội** (KCCS · Hiệp hội Thẩm mỹ Hàn Quốc · VSAPS · ASPS · ISAPS…) trong bất kỳ đầu ra nào — tư cách hội là của từng người, không phải của thương hiệu. Luật ③ ở [`kn-rao-phap-ly.md`](kn-rao-phap-ly.md).
- **Phòng mổ vô khuẩn + khu hậu phẫu riêng** tại tuyến bệnh viện *(nguyên văn `/chi-nhanh/`)*.
- **Quy trình 5 bước chuẩn y khoa**, môi trường **vô khuẩn**, Hội đồng chuyên môn giám sát.
- **6 quyền lợi:** bác sĩ chuyên khoa trực tiếp khám · gói xét nghiệm tổng quát · trải nghiệm phẫu thuật đẳng cấp · gói chăm sóc hậu phẫu · tái khám định kỳ · **bảo hành minh bạch**.
- Chương trình **Hành Trình Lột Xác (HTLX)** phát trên HTV7 — hai công dụng: **ekip bác sĩ phẫu thuật HTLX** là bằng chứng tay nghề ở mức ekip (thay cho claim hội – hiệp hội đã gỡ), và là nguồn **case thật** đã phát sóng. Chỉ dùng cho ngữ cảnh **ekip mổ**; nói về bác sĩ khám/tư vấn thì viết "bác sĩ chuyên khoa trực tiếp khám".

**Ưu tiên dùng bằng chứng theo thứ tự:** giấy phép Bộ Y tế → ekip bác sĩ phẫu thuật HTLX → hội đồng chuyên môn + quy trình 5 bước vô khuẩn → bảo hành minh bạch → case thật HTLX.

## Bác sĩ — **nguồn duy nhất: `/doi-ngu-bac-si/`**
Danh sách nằm trong khối `<script type="application/json" id="kn-doctors-data">` của trang đó, kèm **CCHN · chuyên khoa · cơ sở · cờ `verified` · số năm · số ca · ảnh**. Bản chụp **2026-10-16: 16 bác sĩ + Dr. Richard Huy giới thiệu riêng**.

| Bác sĩ | CCHN | Chuyên khoa | Cơ sở | `status` | KN | Số ca |
|---|---|---|---|---|---|---|
| **Dr. Richard Huy** (Võ Tiến Huy) | 000303/HNO-CCHN | Chỉnh hình hàm mặt · nâng mũi sụn sườn · nâng ngực · ca khó | HN + SG | *(trang riêng)* | 20 | — |
| **Dr. Victor Vu** | 000220/QNI-CCHN | Hàm mặt | HÀ NỘI | ✅ verified | 18 | ~14.250 |
| **Dr. Harvey Nguyen** | 028305/HNO-CCHN | Nâng mũi · cắt mí | SÀI GÒN | ✅ verified | 20 | 15.000 |
| **Dr. Jason Nguyen** | 030179/HNO-CCHN | Nâng mũi · tiểu phẫu | SÀI GÒN | ✅ verified | 10 | >4.000 |
| **Dr. Louis Truong** | 035619/BYT-CCHN | Nâng mũi · cắt mí | HÀ NỘI | ✅ verified | 10 | 10.000 |
| **Dr. Nicolas Hung** | — | Nâng mũi · cắt mí | HÀ NỘI | ✅ verified | 10 | 3.000 |
| **Dr. Alex Han** | — | Hàm mặt | HÀ NỘI | ✅ verified | 10 | 9.250 |
| **Dr. Felix Tran** | — | Ngực · vóc dáng | SÀI GÒN | ✅ verified | 20 | 10.000 |
| **Dr. Daniel Nguyen** | 032533/HNO-CCHN | Cấy mỡ · khuôn mặt | HÀ NỘI | ✅ verified | 10 | ~8.000 |
| **Dr. Alice Tran** | 039379/HNO-CCHN | Da liễu | SÀI GÒN | ✅ verified | 5 | >4.000 |
| **Đỗ Minh Vương** | 037801/HNO-CCHN | Da liễu | HÀ NỘI | ✅ verified | 8 | ~6.000 |
| Dr. Edward Nguyen | 005169/TNG-CCHN | Hàm mặt | SÀI GÒN | ⚠️ trống | 10 | >7.000 |
| Dr. Henry Nguyen | 028062/HNO-CCHN | Nâng mũi · cắt mí | HÀ NỘI | ⚠️ trống | 12 | >13.000 |
| Dr. Galvin Nguyen | 038579/HNO-CCHN | Ngực · vóc dáng | HÀ NỘI | ⚠️ trống | 10 | ~14.000 |
| Dr. Lucas Hoang | 009496/HNO-CCHN | Ngực · vóc dáng | SÀI GÒN | ⚠️ trống | 15 | >20.000 |
| Dr. Mark Nguyen | 036718/HNO-CCHN | Cấy mỡ · khuôn mặt | SÀI GÒN | ⚠️ trống | 10 | 15.000 |
| Dr. Frankie Vu | — | Nâng mũi · cắt mí | SÀI GÒN | ⚠️ trống | 10 | 10.000 |

**Ba cổng trước khi gắn tên vào bất kỳ nội dung nào:**
① Có trong **danh sách live** không — *trang hồ sơ còn sống **không** đồng nghĩa được dùng.*
② **Đúng chuyên khoa VÀ đúng cơ sở** của nội dung — bác sĩ Sài Gòn không gắn vào landing/ads Hà Nội, dù tên đúng.
③ `status: verified` **và** có số CCHN. Thiếu → chọn bác sĩ khác cùng chuyên khoa cùng cơ sở, hoặc `[CHỜ CẬP NHẬT]` và **ẩn khối** — ⛔ không hiển thị bác sĩ kèm ghi chú cảnh báo.

> 🔧 **Sửa 2026-10-16 — quan trọng:** danh sách cũ ghi *"Dr. Jolie Huynh"*. Trang `/doi-ngu-bac-si/jolie-huynh/` nay trả **404** và tên này **không còn trong danh sách live** → **đã loại**. Hai slug khác cũng 404: `bac-si-dr-hong-vu`, `le-thi-thuy`. ⛔ Không dùng ba tên này ở bất kỳ đâu; rà lại landing và mẫu quảng cáo đang chạy.
> ⚠️ **4 bác sĩ chưa có CCHN** trong dữ liệu (Alex Han · Nicolas Hung · Felix Tran · Frankie Vu) và **6 bác sĩ `status` trống** → xác minh với Chuyên môn/Pháp chế trước khi dùng.
> Số ca và số năm: chép **đúng** số trên site, gắn `*` + *"Hiệu quả phụ thuộc cơ địa mỗi người"*. ⛔ Không làm tròn lên.
> Chụp lại danh sách bất cứ lúc nào: `python ../Agent-LDP-Kangnam/tools/fetch-du-lieu.py --chi bac_si`

## Taxonomy dịch vụ — dùng để gom nhóm từ khóa & chọn landing

| Nhóm | Dịch vụ |
|---|---|
| **Mắt** | tạo mắt 2 mí · mở khóe · trẻ hóa mắt · khắc phục sụp mí |
| **Mũi** | nâng mũi thẩm mỹ · thu nhỏ cánh mũi · mài gồ/chỉnh xương · khắc phục mũi hỏng |
| **Hàm mặt** | chỉnh hàm hô · chỉnh hàm móm · gọt góc hàm V-line · hạ gò má · tạo má lúm · tạo hình môi |
| **Vòng 1** | nâng ngực · treo sa trễ |
| **Lipo 360 – Mỡ – Mông** | giảm mỡ · tạo hình thành bụng · cấy mỡ |
| **Trẻ hóa da** | tiêm trẻ hóa · căng da · trẻ hóa công nghệ cao · căng chỉ |
| **Da liễu** | trị mụn · trị sẹo |
| **Trị sắc tố** | trị nám tàn nhang · trị bớt sắc tố · xóa xăm |
| **Clinic** | triệt lông · tắm trắng · phun xăm · điêu khắc |
| **Nha khoa** | niềng răng · bọc răng sứ · cấy Implant · dán mặt sứ |

> 🔧 **Sửa 2026-10-16:** bản cũ gộp *"Da liễu & sắc tố"* thành một nhóm. Menu chính của site **tách đôi** → **10 nhóm**, đúng như bảng trên.
> **Tên nhóm trên menu site** (dùng khi viết nội dung hiển thị, R2): *Dịch vụ Mắt · Dịch vụ Mũi · Hàm Mặt · Thẩm mỹ Vòng 1 · Lipo 360 – Mỡ – Mông · Trẻ Hóa Da · Da Liễu · Trị Sắc Tố · **Kangnam Clinic** · Nha Khoa*. Tên trong bảng trên là tên rút gọn để **gom từ khoá**; tên khách hay gọi (*"gọt hàm V-line"*) chỉ dùng trong từ khoá và khi trích lời khách, **không** dùng ở phần nêu dịch vụ.
> **Bảng giá gom theo 8 nhóm** (khác taxonomy dịch vụ): Mắt · Mũi · Khuôn mặt · Thẩm mỹ vòng 1 · Lipo 360 – Mỡ & Mông · Trẻ hóa da · Da liễu · Spa.

**Hệ sinh thái:** KPS (Plastic Surgery) · KBS (Beauty & Spa) · KDT (Dental) · KWN (Wellness) · KWL (Weight Loss).

**Dịch vụ giá trị lớn** (ưu tiên khi chấm tiêu chí ③ của cổng WIN): nâng ngực · hút mỡ Lipo 360 · chỉnh hàm · nâng mũi cấu trúc.

## ⚠️ GIÁ & KHUYẾN MÃI = DỮ LIỆU ĐỘNG
Agent **bắt buộc** lấy tại thời điểm chạy:
- Giá: `/bang-gia/`
- Ưu đãi: `/uu-dai/`

**KHÔNG bịa. KHÔNG dùng số cũ.** Không truy cập được → để `[CHỜ CẬP NHẬT]` và báo người dùng. Áp cho cả: % ưu đãi · số suất · hạn chương trình.

⛔ **Kangnam KHÔNG có dịch vụ trả góp** — không phải dữ liệu động, mà là **không có**. Không viết "trả góp / trả chậm / góp 0%" vào nội dung; từ khoá dạng này đưa vào phủ định. Trục NGẠI chi phí gỡ bằng **giá minh bạch + ưu đãi đang chạy + cam kết không phát sinh**. Luật ④ ở [`kn-rao-phap-ly.md`](kn-rao-phap-ly.md).

## Ranh giới với thương hiệu anh em
Yêu cầu về **cơ xương khớp / bảo tồn khớp / PRP khớp** thuộc **Cơ Xương Khớp – Wellness** — thương hiệu phân biệt riêng, có agent riêng (CXK-CPW). Báo người dùng chuyển agent, **không viết bằng giọng thẩm mỹ**.

**Nha khoa (KDT)** — niềng răng · bọc răng sứ · cấy Implant · dán mặt sứ — thuộc sub-brand **Kangnam Dental**. Vẫn trong hệ sinh thái nên **được phép cross-sell ở chặng S6**, nhưng rào cản chốt của nha khoa khác hẳn (NGỜ về vật liệu nặng nhất, thay vì SỢ về kết quả thấy bằng mắt). Vì vậy: **gợi ý được, nhưng không dựng bộ từ khoá hay landing nha khoa bằng bộ não này** — nghiệp vụ nha khoa có agent riêng (tham chiếu: [`Agent-AdsOptimize-NhaKhoaParis`](../../Agent-AdsOptimize-NhaKhoaParis/)).

**Nha khoa KHÔNG phải một ZONE của MODE 4.** Màu nhóm `--g-nk` trong Design System chỉ dùng khi hiển thị danh mục toàn hệ sinh thái.


===== kn-khung-landing.md =====

# KHUNG LANDING PAGE & DESIGN SYSTEM KANGNAM v3.0
Version: 3.1 — kế thừa mục 5.2 + MODE 2 bản v1.3; token và khung trang lấy từ trang production

## Chọn khung landing — theo NGUỒN TRAFFIC trước, rồi mới tới intent

| | **Google Ads** (search trả phí) | **SEO · GEO · social nguội** |
|---|---|---|
| **Khung** | **AIDA** | **PAS** — Vấn đề → Khoét sâu → Giải pháp |
| **Vì sao** | Click **đã trả tiền** và từ khoá **đã khai intent** → vào thẳng message match, bằng chứng, CTA | Người đọc không tìm gì cả, **chưa thấy mình có vấn đề** → phải dựng nhận biết trước khi nói giải pháp |

**Mọi landing chạy từ Google Ads mặc định là AIDA.** Hai biến thể, khác nhau ở *thứ tự*, không khác nhau ở *góc*:

| | **A1 — khát khao** | **A2 — trả lời trước** |
|---|---|---|
| **Dùng cho** | Giai đoạn 2 · 4 · mọi trang giá/ưu đãi: nâng mũi đẹp tự nhiên · cắt mí · V-line · trẻ hoá da | **Giai đoạn 3 — từ khoá nỗi sợ**: "nâng ngực có đau không" · "gọt hàm có nguy hiểm không" · "hút mỡ bao lâu hồi phục" · "mũi hỏng sửa được không" |
| **Hero** | Kết quả khát khao + CTA | **Gọi đúng nỗi lo, rồi TRẢ LỜI NGAY** ngay dưới hero |
| **Thứ tự** | Chú ý → quan tâm → khát khao → hành động | Nỗi lo → **câu trả lời** → bằng chứng gỡ Sợ–Ngờ–Ngại → ưu đãi → CTA |

⛔ **Không khoét sâu nỗi sợ trên landing chạy Ads.** Hai lý do, lý do sau nặng hơn:
1. Click đã trả tiền và câu hỏi đã nêu rõ trong từ khoá — trì hoãn câu trả lời để khoét sâu chỉ làm **tăng bounce**.
2. Quảng cáo dịch vụ KCB **không được gây hoang mang**. Khoét sâu nỗi sợ phẫu thuật (biến chứng · gây mê · hỏng vĩnh viễn) là **rủi ro tuân thủ**, không chỉ là copy dở.

**PAS dùng ở đâu:** bài SEO · nội dung GEO (câu trả lời trong AI/chatbot) · post Facebook/TikTok nguội — nơi người đọc chưa chủ động tìm nên phải dựng nhận biết vấn đề trước.

Chọn sai khung là nguyên nhân phổ biến nhất của **CTR ổn nhưng không ai điền form**.

> **Góc ≠ khung.** Góc A (khát khao) / B (nỗi đau) vẫn dùng để chọn *nói về cái gì* trong mẫu quảng cáo (§8 B2 của bộ não). Nó **không** quyết định khung landing. Một mẫu QC góc B hoàn toàn có thể đổ về landing khung A2.

---

## AIDA (13 section) — khung mặc định cho mọi landing chạy Ads

Dưới đây là thứ tự của **A1**. Với **A2** (từ khoá nỗi sợ), giữ nguyên 13 section nhưng **đảo đầu trang**: hero gọi tên nỗi lo → section 2 là **câu trả lời thẳng** cho đúng nỗi lo đó → rồi mới tới trust và phần còn lại. Khối gỡ 3 rào cản (Sợ–Ngờ–Ngại) đẩy lên **ngay sau câu trả lời**.

1. **Hero (70–90vh)** — headline kết quả khát khao + subheadline + CTA chính + CTA phụ (gọi) + trust badge
2. **Trust** — giấy phép Bộ Y tế + hội đồng chuyên môn + **ekip bác sĩ phẫu thuật HTLX trên HTV7** + báo chí
3. **Dịch vụ & công nghệ** — card: icon – tên – mô tả – CTA
4. **Vì sao chọn Kangnam** — **6 quyền lợi** · chuẩn Hàn · bệnh viện chuyên khoa · bảo hành minh bạch
5. **Quy trình 5 bước chuẩn y khoa** — vô khuẩn · hội đồng chuyên môn giám sát
6. **Đội ngũ bác sĩ** (tên thật từ hồ sơ thương hiệu)
7. **Gỡ 3 rào cản (Sợ–Ngờ–Ngại)** ★ — gỡ **đúng** rào cản của chân dung được gán, không gỡ chung chung cả ba
8. **Chi phí / ưu đãi** `[động]` — ⛔ không có trả góp
9. **Review khách**
10. **Before–After thật** (đã duyệt pháp lý) — chia tab theo chân dung
11. **FAQ** — ưu tiên câu xử lý nỗi sợ
12. **Micro-conversion → Booking CTA + form**
13. **Footer** — logo · giấy phép · hotline · hệ thống cơ sở · social

---

## PAS (13 section) — chỉ cho SEO · GEO · social nguội

> **Không dùng khung này cho landing chạy Google Ads.** Xem luật ở đầu file.

1. **Hero** — gọi đúng **Vấn đề/nỗi đau** (mũi hỏng · sụp mí · hô móm · béo bụng sau sinh) + hứa hẹn giải pháp + CTA
2. **Khoét sâu** — hệ quả nếu không xử lý. Chỉ được khoét sâu ở đây, và vẫn **không gây hoang mang** — nêu hệ quả có thật, không vẽ thảm hoạ
3. **Giải pháp** — phương pháp Kangnam giải quyết đúng vấn đề đó
4. **Gỡ 3 rào cản (Sợ–Ngờ–Ngại)** ★ — giấy phép Bộ Y tế · ekip bác sĩ phẫu thuật HTLX · quy trình 5 bước + vô khuẩn · bảo hành minh bạch · gói chăm sóc hậu phẫu
5. **Bằng chứng** — case thật **đúng vấn đề đó** + HTLX
6. **Bác sĩ** (tên thật)
7. **Quy trình an toàn**
8. **Chi phí / ưu đãi** `[động]` — ⛔ không có trả góp
9. **Review người từng gặp đúng vấn đề đó**
10. **Before–After**
11. **FAQ xử lý nỗi sợ**
12. **Micro-conversion → Booking CTA + form**
13. **Footer**

> Section 4 là trái tim của khung này. Làm hời hợt ở đây thì cả trang mất tác dụng.

---

## Micro-conversion — hạ rào cản trước khi xin số

Khách giai đoạn 3 chưa sẵn sàng để lại số điện thoại cho một ca đại phẫu, nhưng sẵn sàng làm một việc nhỏ. **Đặt một bước trung gian trước form booking.**

Ba micro-conversion của Kangnam, xếp theo mức rào cản từ thấp lên cao:

| Micro-conversion | Nguồn | Dùng cho chặng |
|---|---|---|
| **Chọn dịch vụ quan tâm** — bottom sheet nhóm dịch vụ có màu (mẫu ở trang production) | `template/dep-ven-tron.html` | mọi chặng, đứng ngay trong form |
| **Chọn mức ưu đãi / voucher** — khách tự chọn quyền lợi rồi mới điền số | `template/dep-ven-tron.html` | giai đoạn 4 |
| **Đặt khám miễn phí với bác sĩ chuyên khoa** — không phải đặt lịch mổ | 6 quyền lợi | **giai đoạn 3 ★** |

**Luật đặt vị trí:** micro-conversion đứng **trước** form booking — sau section "Gỡ 3 rào cản" (khung A2 · PAS) hoặc sau section "Dịch vụ" (khung A1).

⛔ **Không** bắt khách điền số ngay ở hero cho ca đại phẫu. Hero chỉ cần CTA cuộn xuống hoặc nút gọi.

> **Trục riêng tư — đặc thù thẩm mỹ.** Rào cản NGẠI của ngành này có trục *"không muốn người thân biết"*. Mọi landing phải có **kênh liên hệ riêng tư song song form**: nút Zalo/chat, hoặc dòng cam kết bảo mật ngay dưới nút submit (mẫu `.privacy` ở trang production). Thiếu trục này là bỏ mất một phần lead của giai đoạn 3.

---

## Quy tắc chung
- **CTA lặp sau mỗi 2–3 section** + **Sticky CTA mobile** + **Popup CTA**.
- Giá và ưu đãi luôn là dữ liệu động — lấy tại `/bang-gia/` và `/uu-dai/` lúc chạy. ⛔ **Kangnam không có trả góp** — không dựng section hay dòng nào về trả góp.
- Mọi con số gắn dấu `*` + dòng *"Hiệu quả phụ thuộc cơ địa mỗi người"*.
- Before–after chỉ dùng case đã duyệt pháp lý.
- **Chưa có ảnh thật → dựng ô ảnh tạm** theo mẫu ngay dưới, **không dùng ảnh stock/AI**.
- ⚠️ **Tuyến cơ sở quyết định được quảng cáo gì.** Đại phẫu chỉ tại tuyến bệnh viện (190 Trường Chinh HN · 666 CMT8 SG). Landing local của viện tỉnh **không được** mời đại phẫu — chỉ da/spa/tiểu phẫu + tư vấn/tái khám. Kiểm tra lại trước khi gắn địa chỉ vào footer.

---

## Ô ảnh tạm — bắt buộc khi chưa có ảnh thật

**Không bao giờ** chèn ảnh stock, ảnh AI, hay `<img>` trỏ tới URL không tồn tại. Chưa có ảnh thật đã duyệt → dựng **ô ảnh tạm** đúng mẫu dưới đây. Ô này vừa giữ đúng bố cục, vừa là phiếu đặt hàng cho người cấp ảnh.

```css
.ph{display:grid;place-content:center;gap:6px;text-align:center;margin:0;padding:16px;
    aspect-ratio:var(--ar,16/9);background:#E8EFFB;border:2px dashed var(--line,#DCE3EC);
    border-radius:var(--r,14px);color:var(--ink-2,#4A5C70);font-size:14px;line-height:1.45}
.ph b{display:block;font-weight:700;color:var(--navy,#074E84)}
```

```html
<figure class="ph" style="--ar:16/9">
  <b>Ảnh 16:9</b>
  Case nâng mũi cấu trúc trước–sau · phục vụ CD1 · cần giấy đồng ý KH + pháp chế duyệt
</figure>
```

**Dòng mô tả phải nói rõ ảnh đó LÀ GÌ**, không viết chung chung "ảnh minh hoạ". Tối thiểu gồm: nội dung · chân dung hoặc section nó phục vụ · điều kiện pháp lý nếu là case thật.

| Vị trí | `--ar` | Ghi chú |
|---|---|---|
| Hero | `4/5` mobile · `16/9` desktop | Ảnh duy nhất được tải ngay, không lazy-load |
| Before–after | `1/1` | Cặp 2 ô cạnh nhau hoặc tab/swipe |
| Chân dung bác sĩ | `3/4` | Chỉ bác sĩ có trong hồ sơ thương hiệu |
| Công nghệ · thiết bị · phòng mổ · cơ sở | `16/9` | Ảnh thật của hệ thống |
| Case HTLX | `16/9` | Ảnh/clip đã phát sóng, ghi rõ số phát sóng |
| Icon | `1/1` | 48px, một bộ icon duy nhất |

**Cuối mỗi landing page phải kèm BẢNG KÊ ẢNH CẦN CẤP** — liệt kê từng ô tạm: section · tỉ lệ · nội dung cần · ai duyệt. Không có bảng này thì trang coi như chưa giao xong.

---

## Design System Kangnam v3.0 — chuẩn giao hàng HTML

**Trang mẫu chuẩn: `https://benhvienthammykangnam.com.vn/quyen-loi-thanh-vien/dep-ven-tron/`**
(bản lưu: `template/dep-ven-tron.html`). Token, khung trang, form và bottom sheet dưới đây lấy **nguyên** từ trang đó — không tự chế biến thể mới.

> ⚠️ **Trang mẫu dùng để lấy GÌ và KHÔNG lấy gì.**
> Đây là trang **quyền lợi thành viên** (`noindex`, chỉ dành cho khách đã nhận thông báo), chỉ có 3 section.
> ✅ Lấy: token màu · khung trang · header/footer · form + bottom sheet chọn dịch vụ · sticky/shimmer CTA · nhịp trình bày mobile.
> ❌ **Không lấy cấu trúc nội dung** — 3 section của nó không phải khung landing chạy Ads. Thứ tự section lấy từ khung 13 mục ở trên.

### Token màu

```css
:root{
  --navy:#074E84; --navy-900:#04365E; --navy-950:#022544;
  --ynavy:#1F5FC4; --cyan:#00A5E0;
  --gold:#A66E29;  --amber:#FBBF65;  --terra:#D77927;
  --cta:#EF6103;   --cta-press:#CF5300;
  --bg:#F3F6FA;    --surface:#FFFFFF;
  --ink:#0E2338;   --ink-2:#4A5C70;  --ink-3:#6E7E90;
  --line:#DCE3EC;  --ok:#1E8E5A;     --err:#C62828; --err-t:#FDECEC;
  /* màu nhóm dịch vụ — dùng cho chip, viền card, dot trong dropdown */
  --g-spa:#00A5E0;  --g-spa-t:#E2F5FC;    /* Beauty & Spa  */
  --g-pttm:#1F5FC4; --g-pttm-t:#E8EFFB;   /* Phẫu thuật TM */
  --g-nk:#A66E29;   --g-nk-t:#FCF1DF;     /* Nha khoa      */
  --g-oth:#6E7E90;  --g-oth-t:#EEF1F5;    /* Khác          */
  --r-sm:8px; --r:14px; --r-lg:20px;
  --sh:0 2px 10px rgba(7,78,132,.08);
  --sh-lg:0 10px 30px rgba(2,37,68,.16);
  --hdr-h:56px;
}
```

> ⚠️ **Lệch với bộ nhận diện cũ.** `kn-ho-so-thuong-hieu.md` ghi Primary Navy `#003c77` và CTA cam `#f6871f`. Production đang chạy `#074E84` và `#EF6103`.
> **Dựng landing thì dùng token production ở trên** — để trang mới khớp trang đang chạy. Bộ nhận diện cấp thương hiệu (profile, ấn phẩm) vẫn theo file hồ sơ. Chênh lệch này cần pháp chế/brand chốt một lần, xem *Việc còn treo* ở `doc/CHANGELOG.md`.

| Luật | |
|---|---|
| **Tỷ lệ** | 80% trắng/`--bg` · 15% navy · 5% cam CTA. **Không nền toàn navy** |
| **Nền trang** | `#D9E0E8` — xám xanh, để khối `--bg` ở giữa nổi lên như một thẻ |
| **`--cta` là màu NỀN NÚT, không phải màu chữ** | Chữ trắng trên `--cta` chỉ đạt **3,29:1** → chữ trên nút cam phải **≥19px/800** (ngưỡng large-text AA). Nút nhỏ hơn thì đổi sang `--navy` (trắng trên navy = 8,63 AAA) |
| ⛔ **Cấm** | `--amber` trên nền trắng (**1,65:1**) — amber **chỉ** dùng trên navy (9,43 AAA) và làm vạch trang trí · `--cyan` làm chữ trên trắng (**2,82:1**) — cyan chỉ là màu nhóm/viền · `--ink-3` cho chữ nhỏ (3,84 trên `--bg`) — chữ phụ dùng `--ink-2` (6,87 AA) |
| **An toàn** | `--navy` trên trắng 8,63 AAA · `--ink` trên `--bg` 14,72 AAA · `--gold` trên trắng 4,30 → **chỉ heading ≥18px** (đúng như `.sec-head .pre` của production) · `--err` trên trắng 5,62 AA |

### Khung trang — nền, container, header, footer, sticky

Mọi LDP dùng **đúng bộ khung này**, chỉ thay phần `<section>` ở giữa.

```css
*{box-sizing:border-box} html{scroll-behavior:smooth;-webkit-text-size-adjust:100%}
body{margin:0;font:400 15px/1.55 var(--f);color:var(--ink);background:#D9E0E8}
img{max-width:100%}
:focus-visible{outline:3px solid var(--amber);outline-offset:2px;border-radius:6px}
@media (prefers-reduced-motion:reduce){
  html{scroll-behavior:auto} *{transition:none!important;animation:none!important}}

/* container: thẻ khổ điện thoại, căn giữa trên nền xám xanh */
.app{max-width:480px;margin:0 auto;background:var(--bg);min-height:100vh;
  box-shadow:0 0 0 1px rgba(0,0,0,.04),0 20px 60px rgba(0,0,0,.12);
  padding-bottom:env(safe-area-inset-bottom,0px);position:relative;overflow-x:clip}
.wrap{padding-inline:16px}
section{position:relative}

/* header: sticky, kính mờ, logo + 1 CTA cam */
.hdr{position:sticky;top:0;z-index:60;display:flex;align-items:center;
  justify-content:space-between;gap:10px;min-height:var(--hdr-h);padding:9px 14px;
  padding-top:calc(9px + env(safe-area-inset-top,0px));
  background:rgba(243,246,250,.86);backdrop-filter:blur(10px);
  -webkit-backdrop-filter:blur(10px);border-bottom:1px solid rgba(220,227,236,.75)}
.hdr__logo img{max-height:34px;width:auto;display:block}
.hdr__cta{flex-shrink:0;display:inline-flex;align-items:center;gap:6px;
  background:var(--cta);color:#fff;font-weight:800;font-size:12.5px;
  padding:10px 15px;border-radius:999px;border:0;white-space:nowrap;
  box-shadow:0 4px 12px rgba(239,97,3,.3)}

/* tiêu đề section: pre serif vàng + main navy + vạch amber */
.sec-head{text-align:center;margin-bottom:20px}
.sec-head .pre{display:block;font:italic 600 18px/1.3 var(--f2);color:var(--gold)}
.sec-head .main{display:block;font-size:26px;font-weight:800;color:var(--navy);
  letter-spacing:-.2px;margin-top:2px}
.sec-head .bar{display:block;width:48px;height:3px;border-radius:3px;
  background:var(--amber);margin:12px auto 0}

/* nút */
.btn{display:flex;align-items:center;justify-content:center;gap:8px;min-height:52px;
  width:100%;border:0;border-radius:999px;padding:12px 22px;font-weight:800;
  letter-spacing:.3px;text-decoration:none;transition:transform .12s,background-color .15s}
.btn-cta{background:var(--cta);color:#fff;font-size:19px;text-transform:uppercase;
  box-shadow:0 6px 18px rgba(239,97,3,.38)}          /* 19px/800 — ngưỡng tương phản */
.btn-cta:hover{background:var(--cta-press)}
.btn-cta:active{transform:scale(.98);background:var(--cta-press)}
.btn-outline{background:#fff;color:var(--navy);box-shadow:inset 0 0 0 1.5px var(--navy);
  font-size:15px;min-height:46px;font-weight:700}

/* card nhóm dịch vụ: viền trên theo màu nhóm */
.gcard{background:var(--surface);border-radius:var(--r-lg);box-shadow:var(--sh);
  overflow:hidden;border-top:4px solid var(--gc)}
.gcard[data-g="spa"]{--gc:var(--g-spa);--gct:var(--g-spa-t)}
.gcard[data-g="pttm"]{--gc:var(--g-pttm);--gct:var(--g-pttm-t)}
.gcard[data-g="nk"]{--gc:var(--g-nk);--gct:var(--g-nk-t)}

/* footer */
.foot{position:relative;background:#f1f1ef;color:#254770;padding:26px 14px 30px;
  text-align:center}
.ft__license{font-size:12.5px;font-style:italic;line-height:1.55;margin-top:8px}
.ft__hot{display:flex;align-items:center;justify-content:center;gap:12px;max-width:270px;
  margin:18px auto 0;padding:10px 22px;border-radius:55px;
  background:linear-gradient(90deg,#fec465 0%,#c28710 100%);color:#fff;
  font-weight:700;text-decoration:none}
.ft__hot-num{display:block;font-size:24px;font-weight:800}
.ft__branches-title{font-size:14px;font-weight:700;margin-bottom:5px}
.ft__branches-list{font-size:13px;line-height:1.85}
```

```html
<body>
<div class="app" id="app">

  <header class="hdr">
    <div class="hdr__logo"><a href="/" aria-label="Bệnh viện Thẩm mỹ Kangnam">
      <img src="LOGO.png" alt="Bệnh viện Thẩm mỹ Kangnam" width="275" height="34"></a></div>
    <button class="hdr__cta" type="button" data-goform>ĐẶT LỊCH NGAY</button>
  </header>

  <main>
    <section class="hero"><!-- ảnh hero full-width, fetchpriority="high" + CTA --></section>

    <!-- ===== phần thay đổi theo từng LDP: các <section> theo khung 13 mục ===== -->
    <section class="offers wrap">
      <h2 class="sec-head">
        <span class="pre">Lý do chọn Kangnam</span>
        <span class="main">BỆNH VIỆN CHUYÊN KHOA</span>
        <span class="bar" aria-hidden="true"></span>
      </h2>
      …
    </section>
    <!-- ===== hết phần thay đổi ===== -->

    <section class="reg" id="dang-ky"><!-- micro-conversion + form --></section>
  </main>

  <footer class="foot">
    <div class="ft__logo"><img src="LOGO-FT.svg" alt="Bệnh viện Thẩm mỹ Kangnam"
      width="192" height="114" loading="lazy"></div>
    <p class="ft__license"><i>Giấy phép hoạt động khám chữa bệnh số 287/BYT-GPHĐ do<br>
      Bộ Y tế cấp ngày 03/12/2020</i></p>
    <a href="tel:0968999777" class="ft__hot">
      <span class="ft__hot-txt">
        <span class="ft__hot-label">Hotline</span>
        <span class="ft__hot-num">0968999777</span></span></a>
    <div class="ft__branches">
      <div class="ft__branches-title">Hệ thống bệnh viện và Viện thẩm mỹ trên toàn quốc</div>
      <p class="ft__branches-list">Hà Nội - TP.HCM 1 - TP.HCM 2 - Hải Phòng
        - Nghệ An - Đà Nẵng - Cần Thơ - Thanh Hóa</p>
    </div>
    <div class="ft__socials"><!-- FB · YouTube · Instagram · TikTok · logo Bộ Công Thương --></div>
  </footer>

</div>
</body>
```

**Luật khung trang**
- `.app` là **480px** (không phải 460px) — khớp production. `.sticky-bar` nếu dùng phải cùng `max-width:480px`, nếu không sẽ lệch trên desktop.
- Header **sticky, kính mờ**, chỉ chứa **logo + 1 CTA cam**. Không nhồi menu, không nhồi 3 nút.
- `--hdr-h:56px` dùng cho `scroll-margin-top` của mọi section có anchor — bỏ đi là CTA cuộn tới chỗ bị header che.
- Footer là **khối sáng `#f1f1ef`**, không phải navy. Chữ `#254770` (8,39 AAA).
- **Dòng giấy phép KCB `287/BYT-GPHĐ` trong footer là bắt buộc**, chép đúng nguyên văn, không rút gọn.
- Logo Bộ Công Thương + 4 kênh social: giữ đủ, đây là tín hiệu tin cậy.
- Form đặt trong `.reg` nền navy đậm (`#1B4182`, trắng trên nền này = 9,88 AAA), card form trắng nổi lên bằng `--sh-lg`.
- Có **`:focus-visible` viền amber** và khối `prefers-reduced-motion` — giữ nguyên, đây là phần accessibility của production.

### Form & bottom sheet — chép mẫu, đừng dựng lại

Trang production đã giải xong bài form mobile. Lấy nguyên:

- `.input` / `.select-btn`: `min-height:50px` · `border:1.5px solid var(--line)` · `border-radius:12px` · **`font:500 16px`** (nhỏ hơn 16px là iOS tự zoom khi chạm) · focus `border-color:var(--ynavy)` + `box-shadow:0 0 0 3px rgba(31,95,196,.18)`.
- Lỗi: `.field.bad` → viền `--err` + nền `--err-t`, kèm `.err` 13px/600 có icon. `aria-describedby` trỏ tới ô lỗi.
- **Chọn dịch vụ = bottom sheet**, không phải `<select>` — mỗi dòng có **dot màu nhóm** (`--g-spa` / `--g-pttm` / `--g-nk` / `--g-oth`). Đây chính là micro-conversion.
- **Honeypot** `input[name=email]` ẩn ngoài màn hình + `aria-hidden` — chống bot, giữ nguyên.
- `aria-live="polite"` cho vùng thông báo trạng thái submit, và `.spin` trong nút khi đang gửi.
- `.privacy` 12px dưới nút submit: *"Thông tin của bạn chỉ dùng để BVTM Kangnam liên hệ xác nhận…"* — đây là trục **riêng tư**, không được bỏ.
- Checkbox đồng ý dữ liệu cá nhân + popup chính sách: **bắt buộc**, không phải tuỳ chọn.
- Màn **cảm ơn** là một `.view` riêng che toàn trang, không phải alert.

### Typography — hai font

| Vai trò | Font | Weight |
|---|---|---|
| Toàn bộ body, nút, form, heading chính | **Be Vietnam Pro** (`--f`) | 400 · 500 · 700 · 800 |
| Dòng "pre" của tiêu đề section, câu nhấn cảm xúc (`--f2`) | **Lora** *italic* | 600 |

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Be+Vietnam+Pro:wght@400;500;700;800&family=Lora:ital,wght@1,600&display=swap" rel="stylesheet">
```

```css
--f:'Be Vietnam Pro',system-ui,-apple-system,'Segoe UI',Roboto,Arial,sans-serif;
--f2:'Lora',Georgia,'Times New Roman',serif;
```

- Body **15px/1.55** là mặc định production; **input bắt buộc 16px**.
- `h1,h2,h3{line-height:1.2}` · `.sec-head .main` 26px/800 · `.sec-head .pre` Lora italic 18px.
- Lora **chỉ** dùng cho dòng pre và câu nhấn — không dùng cho đoạn văn.
- **Không nạp font thứ ba.** Cần nhấn thì đổi weight.

### Layout
- Card radius **20px** (`--r-lg`) · input/ô nhỏ **14px** (`--r`) · chip **8px** (`--r-sm`) · button **999px**
- Shadow chỉ hai cấp: `--sh` cho card, `--sh-lg` cho khối nổi (form, popup). **Không chồng shadow.**
- `section` padding **44px 0 36px**, nội dung trong `.wrap` (`padding-inline:16px`)
- Mobile-first, single-file HTML, khung thiết kế **360–430px**, container 480px

### Phong cách
Y khoa cao cấp chuẩn Hàn — sạch, nhiều khoảng trắng, navy làm nền tin cậy, cam chỉ dành cho hành động.

**Không:** nền tối toàn trang · quá 3 màu chính · gradient/neon mạnh · nhiều style icon lẫn lộn · card nhiều shadow · animation rối. (Hiệu ứng `shimmer` trên CTA header là ngoại lệ duy nhất đã có trên production.)

---

## Luồng làm việc MODE 2
1. Nhận cụm từ khóa + dịch vụ → **xác định nguồn traffic trước**, rồi chốt khung `A1` / `A2` / `PAS` và **nói rõ vì sao**.
2. Lấy USP / trust / bác sĩ / 6 quyền lợi từ `kn-ho-so-thuong-hieu.md`; giá & KM lấy động (không có trả góp).
3. **Kiểm tuyến cơ sở**: landing có mời đại phẫu không? Nếu có thì địa chỉ trong footer phải là tuyến bệnh viện.
4. **Mặc định hỏi:** *"Xuất copy-deck trước, hay dựng thẳng HTML?"*
5. Dựng HTML thì tuân Design System v3.0 ở trên, kèm **bảng kê ảnh cần cấp** cuối trang.


===== kn-ppl-kh-trung-tam.md =====

# PHƯƠNG PHÁP LUẬN — MARKETING LẤY KHÁCH HÀNG LÀM TRUNG TÂM
Version: 1.1 — áp dụng cho việc dựng bộ từ khoá Google Ads theo ZONE

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
→ Bằng chứng mạnh nhất **không phải tên hãng** mà là: **giấy phép bệnh viện của Bộ Y tế → ekip bác sĩ phẫu thuật HTLX → hội đồng chuyên môn + quy trình 5 bước vô khuẩn → bảo hành minh bạch → case thật HTLX**.
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


===== kn-rao-phap-ly.md =====

# RÀO PHÁP LÝ — Quảng cáo y tế & thẩm mỹ (Kangnam)
Version: 2.2
Áp cho MỌI output. Agent tự rà trước khi xuất; nội dung chạm ranh → gắn cờ ⚠️ chờ người duyệt.

## Nguyên tắc nền
- Thẩm mỹ là **dịch vụ khám chữa bệnh** — nội dung quảng cáo chịu quản lý của pháp luật quảng cáo y tế VN, **cộng thêm** chính sách hạn chế của Google Ads và Meta với ngành làm đẹp/phẫu thuật.
- Mọi phát ngôn y khoa (cơ chế · hiệu quả · chỉ định · an toàn) phải là **lời bác sĩ hoặc chữ đã được bác sĩ duyệt**.
- Mọi con số (số ca · % · tỷ lệ hài lòng · giải thưởng · năm kinh nghiệm) phải có nguồn thật trong hồ sơ thương hiệu hoặc trên site. **Không nguồn → không đăng.**
- Nội dung quảng cáo dịch vụ KCB cần **giấy xác nhận nội dung quảng cáo** của cơ quan y tế trước khi phát hành. Chưa có → gắn ⚠️, không bật chiến dịch.

## Bảng từ CẤM → từ ĐÚNG

| Cấm | Thay bằng |
|---|---|
| đẹp tuyệt đối / hoàn hảo 100% | kết quả hài hòa với gương mặt, bác sĩ tư vấn theo từng cơ địa* |
| khỏi 100% / chắc chắn thành công | tỷ lệ cải thiện cao khi thực hiện đúng chỉ định* |
| không biến chứng / an toàn tuyệt đối | quy trình 5 bước chuẩn y khoa, môi trường vô khuẩn, hội đồng chuyên môn giám sát |
| không đau | giảm đau theo phác đồ, gây tê/gây mê do bác sĩ chỉ định |
| số 1 / tốt nhất / duy nhất / hàng đầu | (bỏ) hoặc nêu USP đo được: giấy phép KCB, ekip bác sĩ phẫu thuật HTLX, bảo hành |
| vĩnh viễn / trọn đời | duy trì lâu dài, có chế độ bảo hành minh bạch |
| cam kết kết quả như hình | kết quả tùy cơ địa, bác sĩ đánh giá riêng từng trường hợp* |
| rẻ nhất thị trường | chi phí minh bạch, công khai tại bảng giá |
| **không để lại sẹo** | vị trí đường mổ được chọn để hạn chế sẹo, chăm sóc theo hướng dẫn* |
| **"3 ngày là đi làm được"** và mọi mốc thời gian hồi phục CỨNG | mốc hồi phục dạng **khoảng** (vd 7–14 ngày) + **"tùy cơ địa mỗi người"** |
| **"chính hãng"** gắn cho vật liệu không có hồ sơ | nêu đúng tên vật liệu/thiết bị có trong hồ sơ thương hiệu, hoặc bỏ |
| **"bác sĩ thành viên KCCS / Hiệp hội Thẩm mỹ Hàn Quốc"** và mọi claim hội–hiệp hội (VSAPS · ASPS · ISAPS…) | **ekip bác sĩ phẫu thuật HTLX (HTV7)** · **bác sĩ có CCHN** — nêu đúng tên người, đúng cơ sở *(luật ③)* |
| **"trả góp" · "trả chậm" · "góp 0%"** | (bỏ hẳn) — Kangnam không có dịch vụ này; gỡ trục chi phí bằng **giá minh bạch + ưu đãi đang chạy + không phát sinh** *(luật ④)* |

Mọi con số và cam kết mức độ đều phải gắn dấu `*` dẫn **"Hiệu quả phụ thuộc cơ địa mỗi người"**.

## Hình ảnh / video
- **Before–After:** chỉ dùng case **thật đã được duyệt**, có giấy đồng ý của khách hàng, và phải **xác minh tính pháp lý trước khi chạy**. Nhiều định dạng before-after bị Google/Meta hạn chế với ngành thẩm mỹ — kiểm tra chính sách nền tảng trước.
- **Không tạo ảnh kết quả giả**, không dùng ảnh stock/AI mô phỏng kết quả rồi trình bày như case thật.
- Tránh cận cảnh thao tác phẫu thuật · máu · vết mổ gây sợ (vi phạm policy nền tảng + phản tác dụng).
- Ảnh bác sĩ, cơ sở, thiết bị: chỉ dùng ảnh thật của hệ thống.

## Không được làm
- **Không chẩn đoán** tình trạng của khách qua ảnh/mô tả, **không kê đơn**, **không báo giá ca cụ thể** — chỉ tư vấn định hướng rồi mời thăm khám.
- **Không nêu tên hạ thấp đối thủ.** So sánh bằng bộ tiêu chí khách quan để khách tự đánh giá.
- **Không gắn sai pháp nhân / sai phạm vi giấy phép** của cơ sở. Đại phẫu chỉ tại tuyến bệnh viện; viện tỉnh làm da/spa/tiểu phẫu + tư vấn/tái khám.
- **Không nạp** CCCD · hồ sơ bệnh án · ảnh khách hàng lên công cụ công cộng.

## Human-in-the-loop — bắt buộc duyệt trước khi chạy
Mẫu QC có số liệu y khoa · nội dung so sánh phương pháp · mọi caption ads · nội dung có phát ngôn bác sĩ · before–after · landing page trước khi publish.

## 🔶 Cần xác nhận trước khi bật chiến dịch
- Số **giấy xác nhận nội dung quảng cáo** của từng nội dung/chiến dịch: `[CHỜ CẬP NHẬT]`
- Danh sách case + ảnh đã có giấy đồng ý sử dụng hình ảnh: `[CHỜ CẬP NHẬT]`
- Phạm vi giấy phép chi tiết từng cơ sở (làm được gì / không làm gì): `[CHỜ CẬP NHẬT]`

---

## Bốn luật riêng của gói Kangnam

**① KHÔNG hứa thời gian hồi phục cứng.** Thời gian hồi phục là trục **NGẠI** thật của ngành ("nghỉ bao lâu mới đi làm được") nên rất dễ bị hứa quá. Luôn nói dạng **khoảng** và kèm *"tùy cơ địa mỗi người"*. Câu như *"3 ngày là đi làm bình thường"* là **không được viết**.

**② KHÔNG quảng cáo đại phẫu cho viện tỉnh.** Đại phẫu chỉ được làm tại **tuyến bệnh viện** (190 Trường Chinh HN · 666 CMT8 SG). Viện tỉnh làm da/spa/tiểu phẫu + tư vấn/tái khám.

Từ khoá **đại phẫu + tên tỉnh chỉ có viện tỉnh** (vd *"nâng ngực Đà Nẵng"*) phải xử lý theo một trong hai cách: ① đổ về landing tư vấn/đặt khám tại viện tỉnh + **phẫu thuật tại tuyến bệnh viện**, nói rõ trên trang; hoặc ② đưa vào **phủ định** của chiến dịch local.

Đây là **vượt phạm vi giấy phép**, không phải chuyện hiệu suất quảng cáo. Chi tiết ở [`kn-ho-so-thuong-hieu.md`](kn-ho-so-thuong-hieu.md) và §4 của bộ não.

**③ KHÔNG dùng claim hội – hiệp hội làm bằng chứng.** Cấm viết *"bác sĩ thành viên KCCS"*, *"thành viên Hiệp hội Thẩm mỹ Hàn Quốc"*, và tương tự với VSAPS · ASPS · ISAPS… ở **mọi** đầu ra: headline · description · primary text · landing · bộ từ khoá · thông điệp ZONE.

*Vì sao:* tư cách hội là của **từng cá nhân**, không phải của ekip hay của thương hiệu — viết ở mức nhóm quảng cáo là claim **không kiểm chứng được**, lại nằm đúng vùng *"bằng chứng gỡ NGỜ"* nên sai là hỏng cả cụm.

*Thay bằng (theo thứ tự ưu tiên):* **giấy phép KCB Bộ Y tế** → **ekip bác sĩ phẫu thuật HTLX (HTV7)** → **hội đồng chuyên môn + quy trình 5 bước vô khuẩn** → **bảo hành minh bạch** → **case thật HTLX**. Cần nói về tay nghề một người cụ thể thì nêu **tên + CCHN + chuyên khoa + cơ sở** theo bảng bác sĩ ở [`kn-ho-so-thuong-hieu.md`](kn-ho-so-thuong-hieu.md), qua đủ **3 cổng bác sĩ**.

*Lưu ý ngữ cảnh:* chỗ đang nói về **bác sĩ khám / tư vấn** (không phải ekip mổ) thì **bỏ hẳn claim**, viết *"bác sĩ chuyên khoa trực tiếp khám"* — **không** gắn HTLX vào, vì HTLX là **ekip phẫu thuật**.

**④ KHÔNG quảng cáo trả góp.** **Kangnam không có dịch vụ trả góp.** Không viết *"trả góp"* · *"trả chậm"* · *"góp 0%"* · *"0 đồng trước"* vào bất kỳ đầu ra nào. Từ khoá chứa *"trả góp"* → đưa vào **phủ định toàn tài khoản**, không dựng nhóm quảng cáo.

*Vì sao:* đây là **hứa một dịch vụ không tồn tại** — sai sự thật với khách, đồng thời kéo lead không đủ ngân sách làm đội chi phí/ca chốt. Trục **NGẠI chi phí** gỡ bằng **giá minh bạch (`/bang-gia/`) + ưu đãi đang chạy (`/uu-dai/`) + cam kết không phát sinh**.

**Cổng tự động:** `tools/build_keyword_workbook.py` **chặn build** nếu zone JSON còn `KCCS` / `hiệp hội thẩm mỹ hàn quốc`, hoặc còn `trả góp` trong từ khoá / thông điệp (phủ định thì được).

