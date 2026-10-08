# 🎯 ADS OPTIMIZE — Tối ưu quảng cáo hiệu suất (Kangnam)

> Version 2.0 · AI **sinh mẫu quảng cáo win · dựng landing page · chẩn đoán số liệu ADS + GA** cho **Hệ thống Bệnh viện Thẩm mỹ Kangnam** — làm theo chỉ số, không làm theo cảm tính.

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

---

## Ba chế độ

| Mode | Làm gì | Input tối thiểu | Đầu ra |
|---|---|---|---|
| **1 · WIN-AD** | Từ từ khóa → mẫu QC Google RSA + Meta | danh sách từ khóa + dịch vụ | 15 headline + 4 description + 3–5 biến thể Meta + bảng chấm WIN + kế hoạch test |
| **2 · LDP-BUILD** | Từ từ khóa → landing loại A hoặc B | cụm từ khóa + dịch vụ | blueprint section-by-section + copy, hoặc HTML single-file |
| **3 · LDP-ADVISOR** | Đọc ADS + GA → chẩn đoán | CTR·CPC·CPL·impression + scroll·form·booking | điểm nghẽn + 3 quyết định kèm ngưỡng và action |

Mở phiên Agent luôn hỏi chạy mode nào. Không nói thì nó tự suy từ input và báo lại.

---

## Cổng WIN 2/3 — chạy trước mọi nội dung

**Tiền lọc:** từ khóa phải đúng lĩnh vực + có bối cảnh rõ. Lệch → loại.

| # | Tiêu chí | Đạt khi |
|---|---|---|
| ① | **Sát chuyển đổi** | Intent mua: giá · "ở đâu" · đặt lịch — không phải thông tin thuần |
| ② | **Cạnh tranh ít → bid thấp** | Ngách, dài, hoặc local theo cơ sở |
| ③ | **Giá trị dịch vụ lớn** | Nâng ngực · Lipo 360 · chỉnh hàm · nâng mũi cấu trúc |

**< 2/3 → KHÔNG làm nội dung.** Đổi hoặc thu hẹp từ khóa rồi chấm lại.
**Gom nhóm:** 1 nhóm = 1 dịch vụ × 1 giai đoạn phễu × 1 intent = 1 landing + 1 bộ QC. **Không trộn intent vào một landing.**

---

## Phễu 6 giai đoạn

| Giai đoạn | Dấu hiệu từ khóa | Góc thông điệp | LDP |
|---|---|---|---|
| 1 **NHẬN BIẾT** | "là gì" · "có nên" | Giáo dục nhẹ, **chưa bán** | Không chạy LDP chốt |
| 2 **TÌM HIỂU** | "ở đâu tốt" · "bao nhiêu tiền" | So sánh + USP chuẩn Hàn | A hoặc B |
| 3 **CÂN NHẮC & NỖI SỢ** ★ | "có đau không" · "review" · "hỏng" | **Gỡ nỗi sợ**: Bộ Y tế · KCCS · bảo hành | **Loại B (PAS)** |
| 4 **THỰC HIỆN** | "giá" · "ưu đãi" · "đặt lịch" | Ưu đãi có hạn + đặt lịch nhanh | **Loại A** rút gọn |
| 5 **HẬU PHẪU** | "chăm sóc sau" · "kiêng gì" | Hướng dẫn + trấn an | Trang CRM |
| 6 **GẮN BÓ** | "khách cũ ưu đãi" | Cross-sell + HTLX | **Loại A** |

**Giai đoạn 3 là điểm quyết định** — dồn ngân sách và chất lượng nội dung vào đây.

---

## Hai cổng chặn không được bỏ qua

**① Cổng WIN 2/3** — từ khóa chưa đạt 2/3 thì không sản xuất nội dung.
**② Chấm điểm WIN ≥ 10/12** — mẫu QC chưa đạt thì không xuất. 6 tiêu chí: hook chạm 3 giây · đúng intent + giai đoạn · bằng chứng thật · gỡ ≥1 rào cản · CTA rõ 1 hành động · tuân thủ y tế VN + Google/Meta. **Tiêu chí tuân thủ bị 0 điểm → loại thẳng** bất kể tổng điểm.

---

## Quick start (4 bước)

1. Tạo 1 Project / GPT / Gem mới. Tên và mô tả ngắn: xem [`doc/01-cai-dat.md` §0](doc/01-cai-dat.md).
2. **Instructions:** dán khối ▼▲ trong [`SYSTEM-PROMPT.md`](SYSTEM-PROMPT.md) — riêng **ChatGPT** dùng [`SYSTEM-PROMPT-NGAN.md`](SYSTEM-PROMPT-NGAN.md).
3. **Knowledge:** upload 7 file `.md` trong [`knowledge/`](knowledge/).
4. Gọi mode: `MODE 1` · `MODE 2` · `MODE 3` — hoặc cứ nói bằng lời thường, Agent tự suy.

**Câu lệnh mẫu:**
```
MODE 1 — từ khóa "nâng mũi cấu trúc giá bao nhiêu hà nội". Chấm cổng WIN trước,
qua cổng thì sinh mẫu Google RSA + Meta.
```

---

## Tài liệu

| File | Nội dung | Trạng thái |
|---|---|---|
| [SYSTEM-PROMPT.md](SYSTEM-PROMPT.md) | Bộ não — 17 mục · **14.420 ký tự** | ✅ |
| [SYSTEM-PROMPT-NGAN.md](SYSTEM-PROMPT-NGAN.md) | Bản ngắn **7.596 ký tự** — chỉ cho **ChatGPT** (ô Instructions giới hạn 8.000) | ✅ |
| [knowledge/kn-rao-phap-ly.md](knowledge/kn-rao-phap-ly.md) | Từ cấm → từ đúng · luật ảnh · HITL · policy Google/Meta | ✅ |
| [knowledge/kn-ho-so-thuong-hieu.md](knowledge/kn-ho-so-thuong-hieu.md) | Định vị · nhận diện · 8 cơ sở · trust · bác sĩ · taxonomy *(module swappable)* | ✅ |
| [knowledge/kn-chan-dung-hanh-trinh.md](knowledge/kn-chan-dung-hanh-trinh.md) | Insight · 3 rào cản · phễu 6 giai đoạn | ✅ |
| [knowledge/kn-cong-win-tu-khoa.md](knowledge/kn-cong-win-tu-khoa.md) | Cổng 2/3 · phiếu chấm · gom nhóm | ✅ |
| [knowledge/kn-engine-win-ad.md](knowledge/kn-engine-win-ad.md) | B1–B7 · 8 archetype hook · ma trận A/B · chấm điểm 12 · template QC | ✅ |
| [knowledge/kn-khung-landing.md](knowledge/kn-khung-landing.md) | Khung LDP A/B · chuẩn giao hàng HTML · token màu | ✅ |
| [knowledge/kn-chan-doan-chi-so.md](knowledge/kn-chan-doan-chi-so.md) | Định nghĩa WIN bằng số · bảng chẩn đoán · thư viện hook | ✅ |
| [doc/01-cai-dat.md](doc/01-cai-dat.md) | Tên & mô tả · cài 3 nền tảng · smoke test · xử lý sự cố | ✅ |
| [doc/02-cau-lenh.md](doc/02-cau-lenh.md) | Câu lệnh 3 mode · prompt mẫu · điều Agent sẽ từ chối | ✅ |
| [doc/03-output-mau.md](doc/03-output-mau.md) | Output mẫu đủ 3 mode · dấu hiệu đúng/sai | ✅ |
| [doc/04-prompt-nguoi-moi.md](doc/04-prompt-nguoi-moi.md) | 10 prompt cho người không chuyên ads | ✅ |
| [doc/CHANGELOG.md](doc/CHANGELOG.md) | Lịch sử · việc còn treo | ✅ |
| [doc/v1-ban-goc-1-file.md](doc/v1-ban-goc-1-file.md) | Bản gốc v1.3 một file — lưu để đối chiếu, **không dùng để cài** | 📦 |

> **Quy ước:** version ghi trong header từng file, **KHÔNG** gắn version vào tên file.

---

## ⚠️ Giá & khuyến mãi là dữ liệu động

Agent **bắt buộc** lấy giá tại `/bang-gia/` và ưu đãi tại `/uu-dai/` **ở thời điểm chạy**. **Không bịa, không dùng số cũ đã nhớ.** Không truy cập được → để `[CHỜ CẬP NHẬT]` và báo người dùng.

Áp cho cả: % ưu đãi · số suất · hạn chương trình · giá trả góp.

---

## Ranh giới

Không cam kết kết quả y khoa ("đẹp tuyệt đối · khỏi 100% · không biến chứng · an toàn tuyệt đối · số 1 · tốt nhất · vĩnh viễn") · không chẩn đoán/kê đơn/báo giá ca cụ thể · không bịa giá · khuyến mãi · số ca · % · giải thưởng · tên bác sĩ · review · không tạo ảnh kết quả giả · không dùng before–after chưa duyệt pháp lý · không nêu tên hạ thấp đối thủ · không nạp CCCD/hồ sơ bệnh án/ảnh khách lên công cụ công cộng.

**Đại phẫu chỉ tại tuyến bệnh viện** (190 Trường Chinh HN · 666 CMT8 SG). Viện tỉnh làm da/spa/tiểu phẫu + tư vấn/tái khám — **không quảng cáo đại phẫu cho viện tỉnh**.

**Yêu cầu về cơ xương khớp / bảo tồn khớp** thuộc thương hiệu riêng **Cơ Xương Khớp – Wellness**, có agent riêng [`Agent-CoXuongKhop`](../Agent-CoXuongKhop/) — không viết bằng giọng thẩm mỹ.

Mọi mẫu QC / landing / tư vấn là **bản đề xuất**, phải qua người duyệt trước khi chạy.
"# Agent-AdsOptimize-Kangnam" 
