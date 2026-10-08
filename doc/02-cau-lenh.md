# 02 · CÂU LỆNH — ADS OPTIMIZE (KANGNAM)

---

# 1. Công thức ra lệnh

```
MODE [1|2|3] — [từ khóa / cụm từ khóa / số liệu].
[dịch vụ] · [giai đoạn phễu nếu biết] · [cơ sở nếu chạy local]
```

**Bắt buộc:** mode (hoặc để Agent tự suy) + input tương ứng.
Thiếu giai đoạn phễu → Agent tự map và **nói rõ đã map vào đâu, vì sao**.

---

# 2. MODE 1 — WIN-AD

## 2.1 Một nhóm từ khóa
```
MODE 1 — từ khóa "nâng mũi cấu trúc giá bao nhiêu hà nội".
Chấm cổng WIN trước; qua cổng thì sinh mẫu Google RSA + Meta.
```

## 2.2 Lô từ khóa, lọc trước
```
MODE 1 — chấm cổng WIN cho danh sách này, chỉ báo cái nào qua/không qua
và vì sao. Chưa viết mẫu:
- hút mỡ bụng giá bao nhiêu
- thẩm mỹ viện uy tín
- gọt hàm v-line có nguy hiểm không
- cắt mí mắt là gì
- nâng ngực nội soi ở đâu tốt tphcm
```

Duyệt xong:
```
Ok, viết mẫu cho 2 từ khóa đã qua cổng.
```

## 2.3 Chỉ cần hook
```
MODE 1 — chỉ cần hook. Cho mình 6 hook khác archetype cho
"khắc phục mũi hỏng", giai đoạn 3. Ghi rõ archetype và bằng chứng dùng.
```

## 2.4 Chạy local theo cơ sở
```
MODE 1 — từ khóa "trị nám ở đâu tốt đà nẵng", chạy cho Kangnam Đà Nẵng.
Kiểm tra phạm vi giấy phép của cơ sở này trước khi viết.
```

## 2.5 Bổ sung biến thể cho lô đang chạy
```
MODE 1 — lô T1 đang chạy 3 hook, cần thêm 2 challenger mới cho vòng sau.
Giữ nguyên body và offer, chỉ đổi hook.
```

---

# 3. MODE 2 — LDP-BUILD

## 3.1 Dựng landing từ cụm từ khóa
```
MODE 2 — cụm từ khóa quanh "hút mỡ bụng Lipo 360", giai đoạn 3.
Xác định loại landing rồi dựng blueprint + copy.
```

## 3.2 Chỉ định rõ loại
```
MODE 2 — landing loại B (PAS) cho "mũi hỏng sửa lại được không".
Phần gỡ 3 rào cản viết kỹ, đây là phần quan trọng nhất.
```

## 3.3 Dựng thẳng HTML
```
MODE 2 — dựng thẳng HTML single-file cho landing nâng ngực nội soi,
giai đoạn 4. Mobile-first 480px, token Kangnam, CTA nổi.
```

## 3.4 Sửa landing đang có
```
MODE 2 — landing hiện tại CTR tốt nhưng không ai điền form.
Đề xuất sửa phần nào, theo thứ tự ưu tiên. Chưa viết lại cả trang.
```

---

# 4. MODE 3 — LDP-ADVISOR

## 4.1 Chẩn đoán đầy đủ
```
MODE 3 — số liệu 14 ngày, nhóm "nâng mũi cấu trúc HN":
ADS: impression 42.000 · CTR 2,1% · CPC 18.000đ · CPL 890.000đ · chi phí 32tr
GA: scroll depth 35% · time-on-page 28s · form view 310 · submit 22 · booking 6
Chẩn đoán và cho mình 3 quyết định.
```

## 4.2 So sánh với control
```
MODE 3 — mẫu A: CTR 2,8% CPL 740k · mẫu B (control): CTR 2,1% CPL 890k.
Impression A 9.000, B 41.000. A có phải winner không, scale được chưa?
```

## 4.3 Thiếu dữ liệu
```
MODE 3 — mình chỉ có CTR và CPC, chưa gắn GA.
Với dữ liệu này kết luận được gì, chưa kết luận được gì?
```

---

# 5. Prompt hỏi đáp (không sản xuất)

| Mục đích | Prompt |
|---|---|
| Chấm từ khóa | `Từ khóa "cắt mí giá rẻ" được mấy điểm cổng WIN? Có nên làm không?` |
| Chọn giai đoạn | `"gọt hàm bao lâu hồi phục" thuộc giai đoạn mấy, dùng landing loại gì?` |
| Kiểm tra câu chữ | `Headline này có vi phạm gì không: "Nâng mũi đẹp vĩnh viễn, cam kết không biến chứng"?` |
| Chọn bằng chứng | `Giai đoạn 3 dịch vụ nâng ngực nên dùng bằng chứng nào mạnh nhất?` |
| Thiết kế test | `Mình muốn biết hook hay offer tạo ra khác biệt. Thiết kế lô test giúp.` |
| Giải thích chỉ số | `CPL cao mà CVR ổn nghĩa là gì? Sửa ở đâu?` |
| Gợi ý visual | `Landing nâng mũi nên dùng hình gì để không vi phạm policy Meta?` |

---

# 6. Prompt tinh chỉnh

```
15 headline đang thiên về ưu đãi quá. Cân lại: 4 dịch vụ+từ khóa, 4 USP,
4 gỡ nỗi sợ, 3 CTA.
```
```
Hook số 2 nghe như văn quảng cáo. Viết lại bằng đúng câu khách tự nói.
```
```
Mẫu Meta đang dài quá cho feed. Rút primary text còn 3 dòng, giữ bằng chứng.
```
```
Bỏ hết chỗ nào có số liệu chưa duyệt, thay bằng [CHỜ CẬP NHẬT].
```
```
Chuyển landing này từ loại A sang loại B, giữ nguyên phần bác sĩ và giá.
```

---

# 7. Những gì Agent sẽ TỪ CHỐI hoặc CẢNH BÁO

| Yêu cầu | Phản hồi của Agent |
|---|---|
| "Viết Kangnam số 1 / tốt nhất Việt Nam" | Từ chối; nêu từ cấm; đề xuất USP đo được (287/BYT-GPHĐ · KCCS · bảo hành) |
| "Ghi cam kết không biến chứng / đẹp tuyệt đối" | Từ chối; đề xuất ngôn ngữ xác suất + bằng chứng + dấu `*` |
| "Điền đại giá vào cho có" | Từ chối; `[CHỜ CẬP NHẬT]`; nhắc giá là dữ liệu động lấy tại `/bang-gia/` |
| "Lấy giá lần trước bạn viết ấy" | Từ chối; số cũ có thể đã sai — bắt buộc lấy mới |
| "Bịa số ca cho hook mạnh hơn" | Từ chối; đổi sang archetype khác không cần số |
| "Thêm tên bác sĩ X cho uy tín" | Kiểm tra danh sách bác sĩ; không có → `[CHỜ CẬP NHẬT]` |
| "Viết review khách cho sinh động" | Từ chối bịa review; hỏi có review thật đã duyệt chưa |
| "Dùng ảnh before-after này" | Hỏi đã duyệt pháp lý + có giấy đồng ý chưa; chưa có → không dùng |
| "Tạo ảnh mô phỏng kết quả" | Từ chối; không tạo ảnh kết quả giả |
| "So sánh trực diện với [tên đối thủ]" | Từ chối nêu tên hạ thấp; đề xuất bộ tiêu chí khách quan |
| "Từ khóa này mình thích, cứ viết đi" (chưa qua cổng) | Cảnh báo < 2/3 tiêu chí, nêu rõ thiếu tiêu chí nào; đề nghị thu hẹp từ khóa |
| "Xuất luôn, khỏi chấm điểm" | Cảnh báo chưa chấm WIN 12 điểm; mẫu < 10/12 không nên chạy |
| "Scale mẫu này đi" (mẫu nhỏ) | Cảnh báo chưa đủ hiển thị/chi tiêu để kết luận winner |
| "Quảng cáo nâng ngực cho viện tỉnh" | Cảnh báo đại phẫu chỉ tuyến bệnh viện; đề nghị điều hướng |
| "Viết quảng cáo tiêm PRP khớp gối" | Báo thuộc Cơ Xương Khớp – Wellness, dùng agent CXK-CPW |
| "Gửi ảnh hồ sơ bệnh án khách để viết case" | Từ chối; không nạp dữ liệu bệnh nhân lên công cụ công cộng |
