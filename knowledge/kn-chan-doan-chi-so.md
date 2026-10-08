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

**③ Đổi mẫu QC hoặc đổi loại LDP (A↔B)?**
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
