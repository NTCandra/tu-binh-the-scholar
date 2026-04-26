## Bối cảnh dự án
- **Repo:** `/home/user/tu-binh-the-scholar` (Obsidian vault)
- **Branch làm việc:** `claude/build-knowledge-library-IY6A2` (luôn commit + push lên branch này)
- **Mục tiêu:** Xây thư viện tri thức Tử Bình Bát Tự dạng Obsidian — tập trung vào hệ phái **Thám Tác Môn** (Vương Khánh) làm trục chính, các phái khác chỉ để so sánh
- **Ngôn ngữ:** Tiếng Việt (giữ thuật ngữ Hán-Việt + chữ Hán trong ngoặc khi cần)

## File sách cần phân tích lần này
`<TÊN_FILE_SÁCH>` — đặt ở thư mục gốc repo (ví dụ: `No7_Tân Luận Mệnh Lý Bát Tự Trung Quốc.md`, `No20_Thái Cực Âm Dương Hình Khí Lý Số_P1.md`...)
## Sách đã phân tích (KHÔNG đọc lại)
- **No6** → `Tu-Binh-Cach-Cuc-De-Nhi-Ban.md` — Cách Cục Pháp + Tài Quan Pháp (giai đoạn chuyển tiếp)
- **No13** → `Ghi-Chep-Lop-Menh-Ly-2013.md` — Ngũ Hành Chủ Đạo, Thập Can luận mệnh, lịch sử 5 phái
- **No14** → `Con-Duong-Nha-Du-Doan-Hien-Dai.md` — Tinh Khí Thần (giai đoạn sớm 2000, Khí Cơ, Quyền Sinh Khắc, Tâm Ý Công)
- **No20** → `Thai-Cuc-Am-Duong-Hinh-Khi.md` — sách lõi Thám Tác Môn (đã có khung từ phase đầu)
## Cấu trúc knowledge base (đã có)
knowledge-base/
├── 00-Tong-Quan/Lo-Trinh-Hoc.md
├── 01-Nen-Tang/ # Am-Duong, Ngu-Hanh, Thap-Thien-Can, Nguyet-Lenh, Hinh-Khi, Sinh-Khac-Che-Hoa,
│ # Chan-Than-Hu-Than, Thien-Dia-Nhan-Tam-Tai, Khi-Co, To-Chat-Bam-Sinh,
│ # Ngu-Hanh-Chu-Dao, Thuy-Hoa-Kim-Moc-Lanh-Dao-Tro-Thu, Tu-Binh-La-Gi
├── 02-Thap-Than/ # Thap-Than-Tong-Quan, Thap-Than-Ky-Hieu, Thap-Can-Luan-Menh, Thuong-Quan-Kien-Quan
├── 03-Can-Chi-Bien-Hoa/ # To-Hop-Bat-Tu, Quyen-Sinh-Khac (chưa có Hop-Hinh-Xung-Pha-Hai chuyên biệt)
├── 04-Dung-Than/ # Dung-Than-Tong-Quan, PHAI-Tham-Tac-Mon-Dung-Than
├── 05-Cach-Cuc/ # Cach-Cuc-Tong-Quan, Cach-Cuc-Vuot-Tam-Quan, Cach-Cuc-Tuong-Phap,
│ # Cach-Cuc-Dac-Biet, PHAI-Tai-Quan-Phap
├── 06-Thai-Cuc-Phap/ # Thai-Cuc-La-Gi, Tu-Dai-Phap-Tac, Lap-The, Thu-Dung
├── 07-Dai-Van-Luu-Nien/ (chưa có file nào — sách mới có thể tạo)
├── 08-Luan-Menh-Ung-Dung/Luan-Nghe-Nghiep.md
├── 09-He-Phai/ # He-Phai-Tong-Quan, Tham-Tac-Mon
├── 10-Nguon-Sach/ # Mỗi sách đã phân tích có 1 file ở đây
├── 11-Tam-Linh-Tu-Hanh/Tam-Y-Cong.md
└── _Templates/ # He-Phai, Khai-Niem, Phuong-Phap, Sach

## Quy trình cần làm
### Bước 1: Đọc sách mới
- Sách rất dài (1500-2800 dòng/file). Đọc theo chunk **250 dòng** để tránh lỗi token.
- Dùng TodoWrite để track tiến độ đọc.
### Bước 2: Phân tích & xác định concept mới
Trong khi đọc, ghi nhận:
- **Khái niệm KHÔNG có** trong knowledge base hiện tại → tạo file mới
- **Khái niệm ĐÃ có** nhưng có insight bổ sung → enrich file hiện có
- **Giai đoạn của Vương Khánh** (sớm/chuyển tiếp/hoàn thiện) → ghi rõ trong source note nếu có khác biệt với phái Thám Tác Môn trưởng thành
### Bước 3: Tạo source note
Luôn tạo `10-Nguon-Sach/<Ten-Sach-Khong-Dau>.md` đầu tiên, gồm:
- Thông tin sách (tác giả, năm, ISBN, tên file)
- Tóm tắt nội dung
- Cấu trúc chương
- Đóng góp độc đáo
- Hạn chế / so sánh với Thám Tác Môn trưởng thành (nếu là giai đoạn sớm)
- Liên kết đến concept files
### Bước 4: Tạo concept files mới (5-7 files thường đủ)
Ưu tiên các concept **độc đáo nhất** của sách. Mỗi file follow template chung:
```yaml
---
title: "<Tên>"
aliases: ["<chữ Hán>", "<bản Việt không dấu>", "<English>"]
tags: [tu-binh, <category>, tham-tac-mon]
level: beginner|intermediate|advanced
school: tham-tac-mon|all
divergence: none|low|medium|high
related: ["[[...]]"]
sources: ["[[10-Nguon-Sach/<sach>]]"]
chinese: "<chữ Hán>"
created: 2026-04-22
---
Bước 5: Enrich files hiện có
Cập nhật 09-He-Phai/Tham-Tac-Mon.md (mục Sách nguồn)
Cập nhật 00-Tong-Quan/Lo-Trinh-Hoc.md (lộ trình + bảng nguồn)
Cập nhật source list trong các file concept liên quan
Nếu là giai đoạn lịch sử mới → bổ sung 09-He-Phai/He-Phai-Tong-Quan.md
Bước 6: Commit & push
git add knowledge-base/
git commit -m "feat: làm giàu knowledge base từ phân tích <No>X (<Tên ngắn>)
<...mô tả các file mới + file enrich + lưu ý>"
git push -u origin claude/build-knowledge-library-IY6A2
Quy ước viết file
Callouts hệ phái (luôn dùng ở mục "Quan điểm các hệ phái"):

> [!example] 🔬 Thám Tác Môn — quan điểm Vương Khánh
> [!tip] ⚖️ Phái Bình Hành — phái phổ biến (Thân vượng/nhược)
> [!note] 🏛️ Phái Cổ Điển — Tử Bình Chân Thuyên / Từ Vĩ Cương
> [!note] 🎯 Manh Phái — Đoạn Kiến Nghiệp
> [!success] ✅ Chung mọi phái — điểm chung
Callout cảnh báo: > [!warning] cho điểm phân kỳ cao, > [!important] cho framework cốt lõi, > [!tip] cho công thức ứng dụng.

Wiki link nội bộ: [[01-Nen-Tang/Am-Duong]] (path từ root knowledge-base, không có .md)

Cấu trúc 1 concept file:

Frontmatter
# Title
## Tóm tắt (1 câu trong > [!summary])
## Nội dung chính (chia I, II, III...)
## Quan điểm các hệ phái
## Liên kết (Phụ thuộc vào / Dẫn đến / Liên quan)
Tránh: không tạo file con quá nhỏ; không emoji thừa; giữ giọng học thuật + ví dụ thực chiến từ sách.

Lưu ý đặc biệt
Vương Khánh có 4 giai đoạn: No7 (sớm nhất, gần Đại Pháp Sinh Khắc) → No14 (2000, Tinh Khí Thần, vẫn Thân vượng/nhược) → No6 (chuyển tiếp, Cách Cục Pháp) → No20/No13 (trưởng thành, bác bỏ Thân vượng/nhược). Khi phân tích sách mới, xác định giai đoạn và ghi chú nếu có mâu thuẫn với khung Thám Tác Môn trưởng thành.
Không tự ý tạo PR; chỉ commit + push branch. User sẽ tạo PR sau.
Báo cáo cuối cùng kèm danh sách file mới + file enrich + commit hash.