Repo thai-at-the-scholar hiện chứa 2 cuốn sách dịch từ tiếng Trung:

- **Thái Ất Nhập Môn Giản Giới** (5 files, ~641 dòng) - giới thiệu nền tảng
- **Thái Ất Thần Số Dự Trắc Tuyệt Học** (37 files, ~3906 dòng) - chuyên sâu phương pháp

Mục tiêu: tạo một Obsidian vault tại /knowledge-base/ tổng hợp kiến thức từ 2 cuốn này thành các notes có cấu trúc, hỗ trợ người học từ tổng quan đến chi tiết. Sẽ có thêm sách mới được load vào repo dần dần, workflow sẽ là Claude đọc + phân tích + tạo/cập nhật notes thủ công.

**Obsidian Plugins Khuyến Nghị**

Vì người dùng mới với Obsidian, tôi sẽ thiết kế vault tương thích với:

- **Dataview** - query notes như database, tạo bảng động từ frontmatter (ví dụ: "liệt kê tất cả 16 thần", "hiện các phương pháp cấp intermediate")
- **Templater** - tạo notes mới đúng chuẩn frontmatter khi thêm sách mới
- **Graph View** (core, built-in) - hiển thị mạng lưới liên kết giữa các khái niệm

**Cấu trúc Vault /knowledge-base/**

knowledge-base/

├── .obsidian/

│ └── app.json # Bật core plugins: graph, templates, search

├── \_Templates/

│ ├── Khai-Niem-Template.md # Generic concept note

│ ├── Than-Template.md # Spirit/entity note

│ ├── Cung-Template.md # Palace note

│ ├── Phuong-Phap-Template.md # Calculation method note

│ └── Sach-Template.md # Source book summary note

├── 00-Tong-Quan/ # Entry points & navigation

│ ├── Thai-At-Kho-Kien-Thuc.md # MAIN MOC (master entry point)

│ ├── Lo-Trinh-Hoc.md # Learning roadmap (Tier 1→7)

│ ├── MOC-Nen-Tang.md

│ ├── MOC-Cac-Than.md

│ ├── MOC-Cac-Cung.md

│ ├── MOC-Phep-Tinh.md

│ ├── MOC-Cach-Cuc.md

│ └── MOC-Ung-Dung.md

├── 01-Nen-Tang/ # Tier 1-2: Prerequisites + Framework

│ ├── Thai-At-La-Gi.md

│ ├── Tam-Thuc.md

│ ├── Ngu-Nguyen-Luc-Ky.md

│ ├── Cuu-Cung.md

│ ├── Am-Duong-So.md

│ └── Chu-Ky-Thoi-Gian.md

├── 02-Cac-Than/ # Tier 3: 16 spirits + star entities

│ ├── Thap-Luc-Than-Tong-Quan.md # Overview of all 16 spirits

│ ├── Thai-At-Than.md # Primary star

│ ├── Van-Xuong.md

│ ├── Thuy-Kich.md

│ ├── Dinh-Muc.md

│ ├── Cac-Tuong-Si.md # Generals (Chủ/Khách/Định Đại Tướng)

│ ├── Tam-Co.md # Quân Cơ, Thần Cơ, Dân Cơ

│ ├── Ngu-Phuc.md

│ ├── Dai-Du-Tieu-Du.md

│ ├── Tu-Than.md

│ ├── Thien-At-Dia-At.md

│ └── Thai-Tue.md

├── 03-Cac-Cung/ # Tier 3: Nine Palaces

│ ├── Cuu-Cung-Tong-Quan.md

│ ├── Cung-1-Khon.md

│ ├── Cung-2-Ly.md

│ ├── Cung-3-Can.md

│ ├── Cung-4-Chan.md

│ ├── Cung-5-Trung.md

│ ├── Cung-6-Doai.md

│ ├── Cung-7-Khon-B.md

│ ├── Cung-8-Kham.md

│ └── Cung-9-Ton.md

├── 04-Phep-Tinh/ # Tier 4-5: Calculations & Numbers

│ ├── Tich-Nien.md

│ ├── Tinh-Vi-Thai-At.md

│ ├── Tu-Ke-Toan.md # Niên/Nguyệt/Nhật/Thời Kế overview

│ ├── Tuan-Ky-Nam.md

│ ├── Tuan-Ky-Thang.md

│ ├── Tuan-Ky-Ngay.md

│ ├── Tuan-Ky-Gio.md

│ ├── Thien-Muc-Khach-Muc.md

│ ├── So-Chu-Khach-Dinh.md

│ ├── Phan-Loai-So.md # Number classification (Hòa, Trọng Dương, etc.)

│ └── Bat-Mon.md

├── 05-Cach-Cuc/ # Tier 4: Pattern types

│ ├── Cach-Cuc-Tong-Quan.md

│ ├── Yem-Cach.md

│ ├── Bach-Cach.md

│ ├── Kich-Cach.md

│ ├── De-Hiep-Cach.md

│ ├── Cach-Bien-Cach.md

│ ├── Doi-Cach.md

│ ├── Quan-Cach.md

│ ├── Tu-Cach.md

│ ├── Tu-Quach-Co-Cach.md

│ └── Tu-Quach-Du-Cach.md

├── 06-Ung-Dung/ # Tier 6-7: Applied divination

│ ├── Doc-Que-Co-Ban.md

│ ├── Phan-Doan-Thanh-Bai.md

│ ├── Tinh-Thoi-Gian-Ket-Qua.md

│ └── Lich-Su-Kiem-Chung.md # Yuan dynasty case studies

└── 07-Nguon-Sach/

├── Thai-At-Nhap-Mon.md

└── Thai-At-Than-So.md

**Thiết kế Frontmatter (Dataview-compatible)**

Mỗi note dùng YAML frontmatter nhất quán:

yaml

\---

title: "Thái Ất Là Gì"

aliases: \["太乙", "Taiyi", "Thai At Star"\]

tags:

\- thai-at

\- nen-tang # hoặc: cac-than | cac-cung | phep-tinh | cach-cuc | ung-dung

\- khai-niem # hoặc: than | cung | phuong-phap | cach-cuc | ung-dung | nguon

level: beginner # beginner | intermediate | advanced

type: concept # concept | entity | method | pattern | application | source | moc

related:

\- "\[\[Tam-Thuc\]\]"

\- "\[\[Ngu-Nguyen-Luc-Ky\]\]"

sources:

\- "\[\[07-Nguon-Sach/Thai-At-Nhap-Mon\]\]"

chinese: "太乙"

created: 2026-04-19

\---

**Mẫu note (Concept note):**

markdown

**\# Thái Ất Là Gì**

**\## Tóm tắt**

\> \[!summary\] 1 câu

\> Thái Ất là ngôi sao chủ đạo trong hệ thống Tam Thức...

**\## Nội dung chính**

...

**\## Ví dụ / Minh họa**

...

**\## Liên kết**

**\### Phụ thuộc vào**

\- \[\[Am-Duong-So\]\] - cần hiểu Âm Dương trước

**\### Dẫn đến**

\- \[\[Tinh-Vi-Thai-At\]\] - biết Thai At là gì → học cách tính vị trí

**\### Liên quan**

\- \[\[Van-Xuong\]\], \[\[Thuy-Kich\]\]

**Các bước triển khai (theo thứ tự)**

**Bước 1: Khởi tạo vault structure**

- Tạo thư mục /knowledge-base/ và tất cả subdirectories
- Tạo .obsidian/app.json (bật graph view, templates)
- Tạo 5 template files trong \_Templates/

**Bước 2: Tạo 2 Source Book notes (07-Nguon-Sach/)**

- Tóm tắt từng cuốn: mục lục, nội dung chính, phạm vi
- Đây là "nguồn gốc" được link từ mọi note khác

**Bước 3: Tạo Master MOC + Learning Roadmap (00-Tong-Quan/)**

- Thai-At-Kho-Kien-Thuc.md - entry point, link đến tất cả MOC con
- Lo-Trinh-Hoc.md - lộ trình học 7 tầng từ beginner → expert
- 6 MOC con (Nền tảng, Thần, Cung, Phép tính, Cách cục, Ứng dụng)

**Bước 4: Tạo Foundation Notes (01-Nen-Tang/) - 6 notes**

- Thai-At-La-Gi, Tam-Thuc, Ngu-Nguyen-Luc-Ky, Cuu-Cung, Am-Duong-So, Chu-Ky-Thoi-Gian

**Bước 5: Tạo Spirit Notes (02-Cac-Than/) - 12 notes**

- Thập Lục Thần overview + từng nhóm thần (Tam Sơ, Tướng Sĩ, Tam Cơ, etc.)

**Bước 6: Tạo Palace Notes (03-Cac-Cung/) - 10 notes**

- Overview + 9 individual palaces với vị trí, quái, thuộc tính, thần trú

**Bước 7: Tạo Calculation Method Notes (04-Phep-Tinh/) - 11 notes**

- Từ Tích Niên → Tứ Kế Toán → Thiên Mục/Khách Mục → Phân loại Số

**Bước 8: Tạo Pattern Notes (05-Cach-Cuc/) - 11 notes**

- Overview + 10 cách cục với điều kiện, ý nghĩa, ví dụ

**Bước 9: Tạo Application Notes (06-Ung-Dung/) - 4 notes**

- Từ đọc quẻ cơ bản đến case studies lịch sử (Yuan Dynasty floods)

**Bước 10: Cập nhật tất cả MOC files với links đầy đủ**

**Workflow cho sách mới (tương lai)**

Khi user thêm sách mới vào repo:

- Claude đọc toàn bộ nội dung sách mới
- Xác định khái niệm mới (chưa có note) → tạo note mới
- Xác định khái niệm đã có → bổ sung thông tin/góc nhìn mới vào note hiện tại
- Tạo Source Book note mới trong 07-Nguon-Sach/
- Cập nhật các MOC liên quan

**Xác minh (Verification)**

Sau khi hoàn thành, kiểm tra bằng cách:

- Mở /knowledge-base/ làm Obsidian vault
- Mở 00-Tong-Quan/Thai-At-Kho-Kien-Thuc.md - phải thấy links đến tất cả khu vực
- Bật Graph View - phải thấy mạng lưới liên kết giữa notes
- Cài Dataview → chạy query TABLE level, type FROM "knowledge-base" SORT level - phải hiện đủ metadata
- Dùng Lo-Trinh-Hoc.md làm lộ trình, click qua từng link kiểm tra tính liên tục của nội dung

**Files nguồn cần đọc khi triển khai**

**Sách 1:**

- 太乙入门简介 Thái Ất Nhập Môn Giản Giới/Thái Ất Nhập Môn Giản Giới_P1.md → P5.md

**Sách 2:**

- 太乙神数 Thái Ất Thần Sổ/Thái Ất Thần Số_P1.md → P36.md (đọc toàn bộ)

**Template hiện tại:**

- translation_template.md - tham khảo cấu trúc frontmatter hiện có