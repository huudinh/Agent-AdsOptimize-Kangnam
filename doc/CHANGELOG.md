# CHANGELOG — ADS OPTIMIZE (KANGNAM)

## v2.0 — 08/10/2026 · Tái cấu trúc từ 1 file thành gói chuẩn

Nội dung chuyên môn của bản `v1.3` **giữ nguyên**, chỉ tách cấu trúc theo chuẩn gói đã dùng cho [`Agent-CoXuongKhop`](../../Agent-CoXuongKhop/) và [`Agent-KN-CPW`](../../Agent-KN-CPW/) — để mọi agent trong hệ dùng chung một khuôn.

**Vì sao tách:** bản v1.3 là một file 21 KB chứa lẫn bộ não, dữ liệu thương hiệu và tài liệu vận hành. Dán cả file vào Instructions thì vượt giới hạn nền tảng; muốn đổi brand thì phải sửa giữa file; muốn sửa một số liệu thương hiệu thì phải mở cả bộ não ra tìm.

**Cấu trúc mới**

```
Agent-AdsOptimize-Kangnam/
├── README.md               ← cổng vào
├── SYSTEM-PROMPT.md        ← bộ não 17 mục, khối ▼▲ (14.420 ký tự)
├── SYSTEM-PROMPT-NGAN.md   ← bản ngắn cho ChatGPT (7.596 ký tự)
├── knowledge/              ← 7 file tri thức, upload lên nền tảng
└── doc/                    ← tài liệu vận hành, KHÔNG upload
```

**Bản gốc v1.3 → mục nguồn**

| Mục bản v1.3 | Đi về đâu |
|---|---|
| 0 · Phiếu thiết kế 6 ô | `README.md` (bảng 3 mode + ranh giới) |
| 1 · ROLE · 2 · MISSION | `SYSTEM-PROMPT.md` §1 |
| 3.1 insight + 3.2 phễu | `knowledge/kn-chan-dung-hanh-trinh.md` + tóm tắt ở §7 |
| **3.3 module thương hiệu** | `knowledge/kn-ho-so-thuong-hieu.md` *(swappable)* |
| 3.4 cổng 2/3 | `knowledge/kn-cong-win-tu-khoa.md` + tóm tắt ở §6 |
| 4 · MODE 1 (B1–B7) + 5.1 template QC | `knowledge/kn-engine-win-ad.md` + tóm tắt ở §8–§9 |
| 4 · MODE 2 + 5.2 khung LDP | `knowledge/kn-khung-landing.md` + tóm tắt ở §10 |
| 4 · MODE 3 (B8–B9) + 5.3 chẩn đoán | `knowledge/kn-chan-doan-chi-so.md` + tóm tắt ở §11 |
| 6 · RULES | `knowledge/kn-rao-phap-ly.md` + tóm tắt ở §12, §16 |
| 7 · SELF-CHECK · 8 · KÍCH HOẠT | `SYSTEM-PROMPT.md` §17 và §5 |

Bản gốc giữ nguyên tại `doc/v1-ban-goc-1-file.md` để đối chiếu — **không dùng để cài**.

**Bộ não viết lại thành 17 mục.** Giữ đủ lõi cũ, bổ sung các mục khuôn CXK-CPW còn thiếu:

| Mục | Nguồn |
|---|---|
| §1 Role & Mission · §5 Ba chế độ · §6 Cổng WIN · §7 Phễu · §8–§9 Engine · §10 LDP · §11 Advisor · §12 Guardrails · §17 Tự kiểm | có ở v1.3, giữ nguyên lõi |
| **§2 Bảng tri thức** — 7 file, thứ tự đọc pháp lý trước | **MỚI** |
| **§3 Định danh thương hiệu** + **ranh giới hệ sinh thái** | **MỚI** |
| **§4 Nguyên tắc tối thượng** — bằng chứng thay tính từ + phép thử | **MỚI** |
| **§13 Giá & KM là dữ liệu động** — tách thành mục riêng, có luật cấm dùng số cũ đã nhớ | nâng từ ghi chú trong 3.3 |
| **§14 Định dạng đầu ra** — 6 phần cho MODE 1, nêu rõ thứ tự | **MỚI** |
| **§15 Khi thiếu dữ liệu + người dùng không chuyên** | **MỚI** |
| **§16 Rules 11 điều** | mở rộng từ mục 6 |

**Ràng buộc mới làm rõ trong bản này**
- **Ranh giới hệ sinh thái:** yêu cầu về **cơ xương khớp / bảo tồn khớp** thuộc thương hiệu riêng **Cơ Xương Khớp – Wellness** (agent CXK-CPW) — Agent phải báo người dùng, **không viết bằng giọng thẩm mỹ**. Bản v1.3 không có ranh giới này nên dễ lấn.
- **Phạm vi giấy phép theo cơ sở:** đại phẫu chỉ tuyến bệnh viện; **không quảng cáo đại phẫu cho viện tỉnh**. Trước chỉ là ghi chú dưới bảng địa chỉ, nay thành luật trong §3 + smoke test 9.
- **Không dùng số giá/KM cũ đã nhớ** (Rule 4) — bản cũ chỉ cấm "bịa", chưa cấm rõ việc tái dùng số đã lấy ở phiên trước.
- **Tiêu chí tuân thủ bị 0 điểm → loại thẳng** bất kể tổng điểm WIN.

**Tài liệu vận hành mới (`doc/`)**
- `01-cai-dat.md` — tên & mô tả cho form · cài 3 nền tảng + bảng dán gì/upload gì · **9 smoke test** · luồng vận hành có pháp chế · **11 ca xử lý sự cố**.
- `02-cau-lenh.md` — câu lệnh cho cả 3 mode · prompt hỏi đáp · prompt tinh chỉnh · **16 yêu cầu Agent sẽ từ chối/cảnh báo**.
- `03-output-mau.md` — output mẫu đủ 7 phần cho MODE 1 (phiếu cổng WIN → voice of customer → RSA → Meta → bảng chấm → kế hoạch test → ghi chú duyệt), trích MODE 2 và MODE 3 · 4 dấu hiệu đúng / 4 dấu hiệu sai.
- `04-prompt-nguoi-moi.md` — 10 prompt cho người chưa quen thuật ngữ ads.

---

## v1.3 — bản gốc một file

- v1.0 — chuẩn HCI R·M·K·W·O + Rules; kiến trúc BRAIN brand-neutral + MODULE thương hiệu tách riêng (mục 3.3).
- v1.1 — tích hợp Engine tạo nội dung WIN (B1–B9) vào MODE 1/3 + cổng 2/3 tiêu chí (mục 3.4).
- v1.2 — bổ sung Nhận diện thương hiệu (logo · địa chỉ · màu) vào mục 3.3.
- v1.3 — chốt mã màu chính xác: primary `#003c77`, CTA `#f6871f`.

---

## Việc còn treo

| Hạng mục | Ảnh hưởng |
|---|---|
| **Giấy xác nhận nội dung quảng cáo** từng chiến dịch | **Chặn cứng** việc bật chiến dịch — mọi mẫu chỉ nằm ở trạng thái chờ |
| Kho case + ảnh before–after đã có giấy đồng ý và duyệt pháp lý | Bằng chứng mạnh nhất của giai đoạn 3 đang không dùng được |
| Phạm vi giấy phép chi tiết từng cơ sở (làm được gì / không làm gì) | Chạy local chưa chắc đúng; hiện chỉ có luật chung "đại phẫu = tuyến bệnh viện" |
| Benchmark CTR/CPL/CVR theo dịch vụ của team | MODE 3 đang phải lấy control hiện tại làm mốc thay vì chuẩn ngành |
| Thư viện hook thắng tích lũy | B9 chưa có dữ liệu để tái sử dụng — mỗi chiến dịch vẫn bắt đầu lại từ đầu |
| Số liệu công bố được (số ca · % hài lòng · giải thưởng) | Archetype 3 (bằng chứng định lượng) và 7 (FOMO) đang khó dùng |
