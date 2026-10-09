# HỒ SƠ THƯƠNG HIỆU — KANGNAM *(module swappable)*
Version: 2.1 — kế thừa mục 3.3 bản v1.3; bổ sung cột TUYẾN và đối chiếu Design System v3.0

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
Hotline chung **0968.999.777** · email info@benhvienthammykangnam.com.vn · App **Kangnam Care**.

| Cơ sở | **TUYẾN** | Địa chỉ | Khu vực | Được mời đại phẫu? |
|---|---|---|---|---|
| Kangnam Hà Nội | **Bệnh viện** (GP 194/BYT-GPHĐ) | 190 Trường Chinh, Hà Nội | Bắc | ✅ **CÓ** |
| Kangnam Sài Gòn | **Bệnh viện** (GP 287/BYT-GPHĐ) | 666 CM Tháng 8, P. Tân Sơn Nhất, TP.HCM | Nam | ✅ **CÓ** |
| Kangnam Hà Nội (Viện TM) | Viện TM | 194 Trường Chinh, P. Kim Liên, Hà Nội | Bắc | ❌ không |
| Kangnam Hải Phòng | Viện tỉnh | 378 Tô Hiệu, P. Trần Nguyên Hãn, Hải Phòng | Bắc | ❌ không |
| Kangnam Nghệ An | Viện tỉnh | 148 Nguyễn Văn Cừ, TP. Vinh | Trung | ❌ không |
| Kangnam Đà Nẵng | Viện tỉnh | 293 Hùng Vương, P. Thanh Khê, Đà Nẵng | Trung | ❌ không |
| Kangnam Cần Thơ | Viện tỉnh | 28 Lý Tự Trọng, P. Ninh Kiều, Cần Thơ | Nam | ❌ không |
| Kangnam Thanh Hóa | Viện tỉnh | 103 Nguyễn Trãi, P. Hạc Thành, Thanh Hóa | Trung | ❌ không |

## ⚠️ TUYẾN CƠ SỞ — ràng buộc cứng

**Đại phẫu chỉ tại tuyến bệnh viện:** 190 Trường Chinh (HN) · 666 CMT8 (TP.HCM).
Viện tỉnh và viện TM làm **da/spa/tiểu phẫu + tư vấn/tái khám** — **không quảng cáo, không mời đại phẫu**.

**Từ khoá đại phẫu + tên tỉnh chỉ có viện tỉnh** (vd *"nâng ngực Đà Nẵng"*) là **bẫy**: chạy được và có người tìm thật, nhưng landing **không được mời mổ tại đó**. Hai cách xử lý hợp lệ, phải chọn một và ghi rõ:

① Đổ về landing **tư vấn/đặt khám tại viện tỉnh, phẫu thuật tại tuyến bệnh viện** — nói rõ điều đó **ngay ở hero**; hoặc
② Đưa vào **phủ định** của chiến dịch local.

Để mặc không xử lý là **vượt phạm vi giấy phép** — rủi ro pháp lý, không phải chỉ là lead kém.

**Ràng buộc này được cài ở 4 chỗ:** §4 bộ não · tiêu chí ⑥ bảng chấm WIN (vi phạm = tự động 0 điểm → loại thẳng) · bước ③ của MODE 2 (kiểm trước khi dựng) · **cổng TUYẾN trong `tools/build_keyword_workbook.py`** (chặn không build nếu `ghi_chu` chưa khai cách xử lý).

> Hotline campaign có thể khác số tổng đài (vd LP dùng 0962778866). **Địa chỉ, tuyến và phạm vi giấy phép đổi theo thời điểm — chạy local phải verify lại trước khi bật chiến dịch.**

## Trust / pháp lý — dùng làm bằng chứng gỡ nỗi sợ
- Giấy phép KCB số **287/BYT-GPHĐ** (Bộ Y tế, 03/12/2020).
- Bác sĩ chuyên khoa là **thành viên Hiệp hội Thẩm mỹ Hàn Quốc (KCCS)**.
- **Quy trình 5 bước chuẩn y khoa**, môi trường **vô khuẩn**, Hội đồng chuyên môn giám sát.
- **6 quyền lợi:** bác sĩ chuyên khoa trực tiếp khám · gói xét nghiệm tổng quát · trải nghiệm phẫu thuật đẳng cấp · gói chăm sóc hậu phẫu · tái khám định kỳ · **bảo hành minh bạch**.
- Chương trình **Hành Trình Lột Xác (HTLX)** phát trên HTV7 — nguồn case thật.

**Ưu tiên dùng bằng chứng theo thứ tự:** giấy phép Bộ Y tế → KCCS → quy trình 5 bước + vô khuẩn → bảo hành minh bạch → case HTLX.

## Bác sĩ nổi bật
Dr. Richard Huy (TS, đầu ngành) · Dr. Felix Tran (CK1) · Dr. Victor Vu · Dr. Harvey Nguyen · Dr. Jolie Huynh · Dr. Edward Nguyen.

> Chỉ dùng tên bác sĩ có trong danh sách này. Tên khác → `[CHỜ CẬP NHẬT]`, không tự thêm.

## Taxonomy dịch vụ — dùng để gom nhóm từ khóa & chọn landing

| Nhóm | Dịch vụ |
|---|---|
| **Mắt** | tạo mắt 2 mí · mở khóe · trẻ hóa mắt · khắc phục sụp mí |
| **Mũi** | nâng mũi thẩm mỹ · thu nhỏ cánh mũi · mài gồ/chỉnh xương · khắc phục mũi hỏng |
| **Hàm mặt** | chỉnh hàm hô · chỉnh hàm móm · gọt góc hàm V-line · hạ gò má · tạo má lúm · tạo hình môi |
| **Vòng 1** | nâng ngực · treo sa trễ |
| **Lipo 360 – Mỡ – Mông** | giảm mỡ · tạo hình thành bụng · cấy mỡ |
| **Trẻ hóa da** | tiêm trẻ hóa · căng da · trẻ hóa công nghệ cao · căng chỉ |
| **Da liễu & sắc tố** | trị mụn · trị sẹo · nám tàn nhang · trị bớt sắc tố · xóa xăm |
| **Clinic** | triệt lông · tắm trắng · phun xăm · điêu khắc |
| **Nha khoa** | niềng răng · bọc răng sứ · cấy Implant · dán mặt sứ |

**Hệ sinh thái:** KPS (Plastic Surgery) · KBS (Beauty & Spa) · KDT (Dental) · KWN (Wellness) · KWL (Weight Loss).

**Dịch vụ giá trị lớn** (ưu tiên khi chấm tiêu chí ③ của cổng WIN): nâng ngực · hút mỡ Lipo 360 · chỉnh hàm · nâng mũi cấu trúc.

## ⚠️ GIÁ & KHUYẾN MÃI = DỮ LIỆU ĐỘNG
Agent **bắt buộc** lấy tại thời điểm chạy:
- Giá: `/bang-gia/`
- Ưu đãi: `/uu-dai/`

**KHÔNG bịa. KHÔNG dùng số cũ.** Không truy cập được → để `[CHỜ CẬP NHẬT]` và báo người dùng. Áp cho cả: % ưu đãi · số suất · hạn chương trình · giá trả góp.

## Ranh giới với thương hiệu anh em
Yêu cầu về **cơ xương khớp / bảo tồn khớp / PRP khớp** thuộc **Cơ Xương Khớp – Wellness** — thương hiệu phân biệt riêng, có agent riêng (CXK-CPW). Báo người dùng chuyển agent, **không viết bằng giọng thẩm mỹ**.

**Nha khoa (KDT)** — niềng răng · bọc răng sứ · cấy Implant · dán mặt sứ — thuộc sub-brand **Kangnam Dental**. Vẫn trong hệ sinh thái nên **được phép cross-sell ở chặng S6**, nhưng rào cản chốt của nha khoa khác hẳn (NGỜ về vật liệu nặng nhất, thay vì SỢ về kết quả thấy bằng mắt). Vì vậy: **gợi ý được, nhưng không dựng bộ từ khoá hay landing nha khoa bằng bộ não này** — nghiệp vụ nha khoa có agent riêng (tham chiếu: [`Agent-AdsOptimize-NhaKhoaParis`](../../Agent-AdsOptimize-NhaKhoaParis/)).

**Nha khoa KHÔNG phải một ZONE của MODE 4.** Màu nhóm `--g-nk` trong Design System chỉ dùng khi hiển thị danh mục toàn hệ sinh thái.
