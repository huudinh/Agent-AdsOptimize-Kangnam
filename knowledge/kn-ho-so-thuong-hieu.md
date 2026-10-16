# HỒ SƠ THƯƠNG HIỆU — KANGNAM *(module swappable)*
Version: **2.2** — 2026-10-16: đối chiếu trực tiếp với site production (bác sĩ · cơ sở · taxonomy). Trước đó: v2.1 bổ sung cột TUYẾN và đối chiếu Design System v3.0.

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
- Bác sĩ có **chứng chỉ hành nghề (CCHN)** — số CCHN từng người ở bảng mục *Bác sĩ*; nhiều bác sĩ là **thành viên Hiệp hội Thẩm mỹ Hàn Quốc (KCCS)** và các hiệp hội quốc tế (VSAPS · ASPS · ISAPS…) — nêu theo từng người, không nêu chung chung.
- **Phòng mổ vô khuẩn + khu hậu phẫu riêng** tại tuyến bệnh viện *(nguyên văn `/chi-nhanh/`)*.
- **Quy trình 5 bước chuẩn y khoa**, môi trường **vô khuẩn**, Hội đồng chuyên môn giám sát.
- **6 quyền lợi:** bác sĩ chuyên khoa trực tiếp khám · gói xét nghiệm tổng quát · trải nghiệm phẫu thuật đẳng cấp · gói chăm sóc hậu phẫu · tái khám định kỳ · **bảo hành minh bạch**.
- Chương trình **Hành Trình Lột Xác (HTLX)** phát trên HTV7 — nguồn case thật.

**Ưu tiên dùng bằng chứng theo thứ tự:** giấy phép Bộ Y tế → KCCS → quy trình 5 bước + vô khuẩn → bảo hành minh bạch → case HTLX.

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

**KHÔNG bịa. KHÔNG dùng số cũ.** Không truy cập được → để `[CHỜ CẬP NHẬT]` và báo người dùng. Áp cho cả: % ưu đãi · số suất · hạn chương trình · giá trả góp.

## Ranh giới với thương hiệu anh em
Yêu cầu về **cơ xương khớp / bảo tồn khớp / PRP khớp** thuộc **Cơ Xương Khớp – Wellness** — thương hiệu phân biệt riêng, có agent riêng (CXK-CPW). Báo người dùng chuyển agent, **không viết bằng giọng thẩm mỹ**.

**Nha khoa (KDT)** — niềng răng · bọc răng sứ · cấy Implant · dán mặt sứ — thuộc sub-brand **Kangnam Dental**. Vẫn trong hệ sinh thái nên **được phép cross-sell ở chặng S6**, nhưng rào cản chốt của nha khoa khác hẳn (NGỜ về vật liệu nặng nhất, thay vì SỢ về kết quả thấy bằng mắt). Vì vậy: **gợi ý được, nhưng không dựng bộ từ khoá hay landing nha khoa bằng bộ não này** — nghiệp vụ nha khoa có agent riêng (tham chiếu: [`Agent-AdsOptimize-NhaKhoaParis`](../../Agent-AdsOptimize-NhaKhoaParis/)).

**Nha khoa KHÔNG phải một ZONE của MODE 4.** Màu nhóm `--g-nk` trong Design System chỉ dùng khi hiển thị danh mục toàn hệ sinh thái.
