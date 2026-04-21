# Kế Hoạch Xây Dựng Thư Viện Kiến Thức Tử Bình Bát Tự

## Tổng quan dự án

Repo hiện có:
- **Thái Cực Âm Dương Hình Khí Mệnh Lý Học** (Vương Khánh - Thám Tác Môn) — sách đầu tiên, đã dịch sang tiếng Việt, bao gồm phần lý luận Nhân Đạo (Ngũ Hành, Thập Can, Tứ Đại Pháp Tắc), Thiên Đạo (Thái Cực Pháp) và Địa Đạo (Cách Cục Pháp)

Sẽ bổ sung dần:
- Tử Bình cổ điển (Tích Thiên Tủy, Lan Đài Diệu Bí, Tam Mệnh Thông Hội...)
- Manh Phái / Mù phái (Phái học của người mù truyền thống)
- Hoa Vũ Mệnh Lý (Hà Kiến Trung)
- Các hệ phái hiện đại khác

**Mục tiêu:** Xây dựng Obsidian vault đa hệ phái, trình bày song song không phán xét, giúp người học nắm được cả nền tảng chung lẫn sự khác biệt giữa các trường phái.

**Nguyên tắc cốt lõi khi có tranh luận giữa phái:** Trình bày song song, ghi rõ nguồn, để người học tự nhận định.

---

## Obsidian Plugins Khuyến Nghị

- **Dataview** — query notes như database (liệt kê tất cả khái niệm theo hệ phái, level, type)
- **Templater** — tạo notes mới đúng chuẩn frontmatter
- **Graph View** (core built-in) — hiển thị mạng lưới liên kết khái niệm
- **Callout blocks** — dùng để phân biệt góc nhìn hệ phái bằng màu sắc

---

## Cấu Trúc Vault `/knowledge-base/`

```
knowledge-base/
│
├── .obsidian/
│   └── app.json                        # Bật core plugins
│
├── _Templates/
│   ├── Khai-Niem-Template.md           # Khái niệm chung (Âm Dương, Ngũ Hành...)
│   ├── Can-Chi-Template.md             # Thiên Can / Địa Chi cụ thể
│   ├── Phuong-Phap-Template.md         # Phương pháp luận mệnh
│   ├── He-Phai-Template.md             # Tổng quan một hệ phái
│   └── Sach-Template.md                # Source book summary
│
├── 00-Tong-Quan/                       # Entry points & navigation
│   ├── Tu-Binh-Kho-Kien-Thuc.md       # MAIN MOC (master entry point)
│   ├── Lo-Trinh-Hoc.md                 # Learning roadmap (Tier 1→8)
│   ├── So-Do-He-Phai.md                # Bản đồ các hệ phái & điểm khác nhau
│   ├── MOC-Nen-Tang.md                 # Các khái niệm nền tảng chung
│   ├── MOC-Am-Duong-Ngu-Hanh.md
│   ├── MOC-Can-Chi.md
│   ├── MOC-Thap-Than.md
│   ├── MOC-Dung-Than.md                # ← điểm phân kỳ lớn nhất giữa phái
│   ├── MOC-Cach-Cuc.md
│   ├── MOC-Dai-Van-Luu-Nien.md
│   ├── MOC-Luan-Menh.md                # Ứng dụng thực tế
│   └── MOC-He-Phai.md                  # Hub tổng hợp các hệ phái
│
├── 01-Nen-Tang/                        # Tier 1-2: Kiến thức nền chung mọi phái
│   ├── Tu-Binh-La-Gi.md
│   ├── Bat-Tu-La-Gi.md                 # Tứ Trụ = 8 chữ
│   ├── Am-Duong.md
│   ├── Ngu-Hanh.md
│   ├── Sinh-Khac-Che-Hoa.md
│   ├── Thap-Thien-Can.md
│   ├── Thap-Nhi-Dia-Chi.md
│   ├── Tang-Can.md                     # Can tàng trong chi
│   ├── Ngu-Hanh-Vuong-Suy.md          # Vượng/Tướng/Hưu/Tù/Tử theo mùa
│   ├── Lap-Menh-Co-Ban.md              # Cách lập lá số Tứ Trụ
│   └── Khong-Vong.md
│
├── 02-Thap-Than/                       # Tier 3: Thập Thần — nền tảng chung
│   ├── Thap-Than-Tong-Quan.md
│   ├── Chinh-An.md
│   ├── Thiet-An.md                     # Thiên Ấn (Kiêu Thần)
│   ├── Chinh-Quan.md
│   ├── That-Sat.md
│   ├── Chinh-Tai.md
│   ├── Thiet-Tai.md                    # Thiên Tài
│   ├── Thuc-Than.md
│   ├── Thuong-Quan.md
│   ├── Ty-Kien.md
│   └── Kiep-Tai.md
│
├── 03-Can-Chi-Bien-Hoa/                # Tier 3: Can Chi biến hóa
│   ├── Thien-Can-Hop.md                # 5 hợp Can
│   ├── Dia-Chi-Luc-Hop.md
│   ├── Dia-Chi-Tam-Hop.md
│   ├── Dia-Chi-Tam-Hoi.md
│   ├── Dia-Chi-Luc-Xung.md
│   ├── Dia-Chi-Luc-Hai.md
│   ├── Dia-Chi-Luc-Pha.md
│   ├── Dia-Chi-Tu-Hinh.md
│   ├── Tuong-Sinh-Vuong-Tuong.md       # Vượng/Tướng/Hưu/Tù/Tử chi tiết
│   └── Truong-Sinh-Thap-Than.md        # Thập nhị vận trường sinh
│
├── 04-Dung-Than/                       # Tier 4: ĐIỂM PHÂN KỲ LỚN NHẤT
│   ├── Dung-Than-Tong-Quan.md          # Giải thích tại sao phái khác nhau
│   ├── PHAI-Co-Dien-Dung-Than.md       # Cổ điển: Điều hậu / Điều hầu (tiết khí)
│   ├── PHAI-Binh-Hanh-Dung-Than.md     # Bình hành: Thân vượng/nhược → chọn Dụng
│   ├── PHAI-Tham-Tac-Mon-Dung-Than.md  # Thám Tác Môn: không dùng Thân vượng/nhược
│   ├── PHAI-Manh-Phai-Dung-Than.md     # Manh Phái: Nguyệt lệnh ưu tiên
│   ├── PHAI-Hoa-Vu-Dung-Than.md        # Hoa Vũ: Thể Dụng luận
│   └── So-Sanh-Cac-Phuong-Phap.md     # Bảng so sánh tổng hợp
│
├── 05-Cach-Cuc/                        # Tier 4-5: Cách Cục
│   ├── Cach-Cuc-Tong-Quan.md
│   ├── PHAI-Co-Dien-Cach-Cuc.md        # Cổ điển: Bát chánh cách, ngoại cách
│   ├── PHAI-Tham-Tac-Mon-Cach-Cuc.md   # Thám Tác Môn: Cách Cục Pháp riêng
│   ├── Cach-Cuc-Chinh-Quan.md
│   ├── Cach-Cuc-That-Sat.md
│   ├── Cach-Cuc-Chinh-An.md
│   ├── Cach-Cuc-Thuc-Than.md
│   ├── Cach-Cuc-Thuong-Quan.md
│   ├── Cach-Cuc-Chinh-Tai.md
│   ├── Cach-Cuc-Thiet-Tai.md
│   ├── Cach-Cuc-Kien-Loc.md
│   ├── Ngoai-Cach-Tong-Quan.md         # Theo mệnh (tòng cách, hóa khí cách...)
│   └── Cach-Cuc-Vuot-Tam-Quan.md       # Tam Quan của Thám Tác Môn
│
├── 06-Thai-Cuc-Phap/                   # Tier 5: Đặc thù Thám Tác Môn
│   ├── Thai-Cuc-La-Gi.md
│   ├── Am-Duong-The-Dung.md            # Thể/Dụng luận
│   ├── Ngu-Hanh-Am-Duong-Chi-Tiet.md   # Đặc tính Mộc/Hỏa/Thổ/Kim/Thủy
│   ├── Tu-Dai-Phap-Tac.md              # Trung Hòa / Âm Dương / Cát Hung / Thái Cực
│   ├── Hinh-Phap-Khi-Phap.md           # Hình pháp vs Khí pháp
│   ├── Can-Chi-Pha-Tu.md               # Bí pháp va chạm Can Chi
│   └── Luan-Menh-Quy-Trinh.md          # Quy trình luận mệnh theo Thám Tác Môn
│
├── 07-Dai-Van-Luu-Nien/                # Tier 5-6: Đại Vận & Lưu Niên
│   ├── Dai-Van-Tong-Quan.md
│   ├── Cach-An-Dai-Van.md
│   ├── Luu-Nien-Tong-Quan.md
│   ├── Can-Chi-Luu-Van-Tuong-Tac.md    # Giao thoa Nguyên cục - Đại vận - Lưu niên
│   ├── PHAI-Co-Dien-Luu-Van.md
│   └── PHAI-Tham-Tac-Mon-Luu-Van.md
│
├── 08-Luan-Menh-Ung-Dung/              # Tier 6-7: Ứng dụng thực tế
│   ├── Quy-Trinh-Doc-La-So.md
│   ├── Phu-Quy-Ban-Tien.md
│   ├── Suc-Khoe-Benh-Tat.md
│   ├── Hon-Nhan-Tinh-Cam.md
│   ├── Su-Nghiep-Cong-Viec.md
│   ├── Luc-Than.md                     # Cha mẹ, anh em, vợ chồng, con cái
│   ├── Canh-Bao-Va-Tai-Uong.md
│   └── Vi-Du-Thuc-Te.md               # Case studies tổng hợp
│
├── 09-He-Phai/                         # Hub các hệ phái
│   ├── He-Phai-Tong-Quan.md            # Bản đồ lịch sử hệ phái Tử Bình
│   ├── Tham-Tac-Mon.md                 # Thám Tác Môn (Vương Khánh)
│   ├── Tu-Binh-Co-Dien.md              # Cổ điển (Lan Đài, Tích Thiên Tủy...)
│   ├── Manh-Phai.md                    # Manh Phái
│   ├── Hoa-Vu-Menh-Ly.md              # Hoa Vũ Mệnh Lý
│   └── [Them-he-phai-moi].md           # Placeholder cho phái mới
│
└── 10-Nguon-Sach/
    ├── Thai-Cuc-Am-Duong-Hinh-Khi.md   # Vương Khánh — cuốn đã có
    ├── [Co-Dien-Kinh-Dien].md          # Placeholder
    └── [Them-sach-moi].md              # Placeholder
```

---

## Thiết Kế Frontmatter (Dataview-compatible)

Mỗi note dùng YAML frontmatter nhất quán. Điểm mới so với Thái Ất: thêm field `school` để phân biệt hệ phái.

```yaml
---
title: "Dụng Thần — Thám Tác Môn"
aliases: ["用神", "Yong Shen", "Dung Than Tham Tac Mon"]
tags:
  - tu-binh
  - dung-than         # module: nen-tang | thap-than | can-chi | dung-than | cach-cuc | thai-cuc | dai-van | luan-menh | he-phai | nguon
  - phuong-phap       # type: khai-niem | phuong-phap | bien-hoa | cach-cuc | ung-dung | he-phai | nguon | moc
level: intermediate   # beginner | intermediate | advanced
school:               # all | co-dien | tham-tac-mon | manh-phai | hoa-vu | [ten-phai]
  - tham-tac-mon
divergence: high      # none | low | medium | high — mức độ khác nhau giữa các phái
related:
  - "[[Cach-Cuc-Tong-Quan]]"
  - "[[Tu-Dai-Phap-Tac]]"
sources:
  - "[[10-Nguon-Sach/Thai-Cuc-Am-Duong-Hinh-Khi]]"
chinese: "用神"
created: 2026-04-21
---
```

**Giải thích các field mới:**
- `school`: ghi `all` nếu khái niệm chung mọi phái, ghi tên phái nếu đặc thù
- `divergence`: mức độ tranh luận giữa các phái về khái niệm này (`high` = phái khác nhau hoàn toàn, cần đọc kỹ)

---

## Mẫu Note — Khái Niệm Chung (Nền Tảng)

```markdown
# Thập Thần Tổng Quan

## Tóm tắt
> [!summary] 1 câu
> Thập Thần là 10 mối quan hệ giữa Nhật Can và các Can Chi khác trong lá số, đại diện cho thuộc tính xã hội của con người.

## Nội dung chính
...

## Quan điểm các hệ phái
> [!note] Chung mọi phái
> Định nghĩa Thập Thần và cách tính là giống nhau ở tất cả các phái.

## Ví dụ / Minh họa
...

## Liên kết
### Phụ thuộc vào
- [[Am-Duong]] - cần hiểu Âm Dương trước
- [[Ngu-Hanh]] - nền tảng Ngũ Hành

### Dẫn đến
- [[Dung-Than-Tong-Quan]] - sau khi biết Thập Thần → học cách chọn Dụng Thần
- [[Cach-Cuc-Tong-Quan]]

### Liên quan
- [[Thap-Thien-Can]], [[Thap-Nhi-Dia-Chi]]
```

---

## Mẫu Note — Điểm Phân Kỳ Giữa Hệ Phái

```markdown
# Dụng Thần — Tổng Quan

## Tóm tắt
> [!summary] 1 câu
> Dụng Thần là yếu tố trung tâm nhất trong luận mệnh Tử Bình, nhưng cách xác định Dụng Thần là điểm khác nhau lớn nhất giữa các hệ phái.

> [!warning] Điểm phân kỳ cao
> Các hệ phái có cách xác định Dụng Thần hoàn toàn khác nhau. Hãy đọc từng phái trước khi so sánh.

## Định nghĩa chung
Dụng Thần là Can/Chi trong lá số đóng vai trò điều tiết, cân bằng, hoặc phát huy sức mạnh tổng thể của bát tự.

## Quan điểm các hệ phái

> [!note] 🏛️ Tử Bình Cổ Điển
> Dụng Thần được xác định dựa trên **Nguyệt lệnh** (tiết khí tháng sinh) là ưu tiên đầu tiên. Phương pháp "Điều Hậu" điều chỉnh theo mùa (hàn/ấm). Tiếp đó mới xét Thân vượng/nhược để chọn Dụng bổ sung.
> — Nguồn: [[10-Nguon-Sach/Tich-Thien-Tuy]], [[10-Nguon-Sach/Lan-Dai-Dieu-Bi]]

> [!tip] ⚖️ Phái Bình Hành (truyền thống phổ biến)
> Trước tiên xét **Thân vượng hay nhược**: nếu Thân vượng → dùng Tài/Quan/Thực Thương để tiết; nếu Thân nhược → dùng Ấn/Tỷ Kiếp để phù.
> — Đây là phương pháp phổ biến nhất trong sách giáo khoa Tử Bình thế kỷ 20.

> [!example] 🔬 Thám Tác Môn (Vương Khánh)
> **Bác bỏ hoàn toàn** khái niệm Thân vượng/nhược làm tiêu chí chọn Dụng Thần. Thay vào đó: xét **Âm Dương cân bằng** (Thái Cực Pháp) và **khí chủ trời đất** (Cách Cục Pháp). Dụng Thần là yếu tố giúp Âm Dương hòa hợp thành Thái Cực.
> — Nguồn: [[10-Nguon-Sach/Thai-Cuc-Am-Duong-Hinh-Khi]]

> [!abstract] 🎯 Manh Phái
> *(Chờ bổ sung khi có sách)*

> [!quote] 🌸 Hoa Vũ Mệnh Lý
> *(Chờ bổ sung khi có sách)*

## So sánh trực tiếp
| Tiêu chí | Cổ điển | Bình Hành | Thám Tác Môn |
|---|---|---|---|
| Bước đầu tiên | Nguyệt lệnh | Thân vượng/nhược | Âm Dương cân bằng |
| Vai trò Thân | Quan trọng | Trung tâm | Không phải tiêu chí |
| Cách Cục | Từ Nguyệt lệnh | Thân + Thập Thần | Khí chủ trời đất |

## Liên kết
### Phụ thuộc vào
- [[Thap-Than-Tong-Quan]]
- [[Ngu-Hanh-Vuong-Suy]]

### Dẫn đến
- [[PHAI-Tham-Tac-Mon-Dung-Than]]
- [[PHAI-Co-Dien-Dung-Than]]
- [[Cach-Cuc-Tong-Quan]]
```

---

## Mẫu Note — Hệ Phái

```markdown
# Thám Tác Môn (探索者门)

## Tóm tắt
> [!summary]
> Hệ phái Tử Bình hiện đại do Vương Khánh (bút danh Thám Tác Giả) sáng lập, lấy Âm Dương Thái Cực làm cốt lõi, bác bỏ phương pháp Thân vượng/nhược truyền thống.

## Người sáng lập
**Vương Khánh** (王庆), bút danh Thám Tác Giả, hiệu Cốc Tử Tiên Sinh, quê Chiết Giang.

## Ba phương pháp chính
1. **Thái Cực Pháp** — luận Thiên mệnh, xuất phát từ Ngũ Hành, xem Âm Dương cân bằng
2. **Cách Cục Pháp** — luận Địa mệnh, xuất phát từ Thập Thần, xem khí chủ trời đất
3. **Hình Tượng Pháp** — luận Nhân mệnh, thủ tượng từ Can Chi

## Tư tưởng cốt lõi
- Nguồn gốc từ "Đạo Đức Kinh" và "Dịch Kinh"
- Âm Dương là linh hồn của Bát Tự, Thái Cực là cơ sở phán đoán cát hung
- Hình là vật chứa của Khí; phải kết hợp cả Hình pháp lẫn Khí pháp

## Điểm khác biệt với cổ điển
| | Cổ điển | Thám Tác Môn |
|---|---|---|
| Thân vượng/nhược | Tiêu chí trung tâm | Không dùng |
| Dụng Thần | Từ Nguyệt lệnh + Thân | Từ Âm Dương cân bằng |
| Cách Cục | Bát chánh cách | Khí chủ trời đất |

## Sách nguồn
- [[10-Nguon-Sach/Thai-Cuc-Am-Duong-Hinh-Khi]] ← hiện có

## Liên kết
- [[Thai-Cuc-La-Gi]]
- [[Tu-Dai-Phap-Tac]]
- [[Cach-Cuc-Tong-Quan]]
```

---

## Sơ Đồ Lộ Trình Học (8 Tầng)

```
Tier 1 — Nền tảng vũ trụ quan (mọi phái giống nhau)
  Âm Dương → Ngũ Hành → Sinh Khắc Chế Hóa

Tier 2 — Công cụ cơ bản (mọi phái giống nhau)
  Thập Thiên Can → Thập Nhị Địa Chi → Tàng Can → Khổng Vong
  Ngũ Hành vượng suy theo mùa → Lập lá số Tứ Trụ

Tier 3 — Thập Thần & Biến hóa (mọi phái giống nhau)
  10 Thập Thần → Can Chi Hợp/Xung/Hình/Hại/Phá
  Thập nhị vận Trường Sinh

Tier 4 — ĐIỂM PHÂN KỲ: Dụng Thần
  Đọc So-Sanh-Cac-Phuong-Phap.md trước
  → Chọn hệ phái muốn học sâu
  → PHAI-Co-Dien / PHAI-Tham-Tac-Mon / PHAI-Manh-Phai / PHAI-Hoa-Vu

Tier 5 — Cách Cục (có dị biệt nhỏ giữa phái)
  Bát chánh cách cổ điển ↔ Cách Cục Pháp Thám Tác Môn
  Ngoại cách / Tòng cách / Hóa khí cách

Tier 5b — Thái Cực Pháp (đặc thù Thám Tác Môn)
  Thái Cực là gì → Thể Dụng → Tứ Đại Pháp Tắc → Can Chi Phá Tự

Tier 6 — Đại Vận & Lưu Niên
  Cách an vận → Tương tác Nguyên cục/Đại vận/Lưu niên

Tier 7 — Ứng dụng luận mệnh thực tế
  Phú quý bần tiện → Sức khỏe → Hôn nhân → Sự nghiệp → Lục Thân

Tier 8 — Tích hợp đa phái
  Đọc cùng một lá số theo nhiều phái → so sánh kết quả
```

---

## Callout Convention (Phân Biệt Hệ Phái Bằng Màu)

```markdown
> [!note] 🏛️ Tử Bình Cổ Điển
> Nội dung theo Cổ điển (Tích Thiên Tủy, Lan Đài Diệu Bí, Tam Mệnh Thông Hội)

> [!tip] ⚖️ Phái Bình Hành
> Nội dung theo phái Bình Hành phổ biến (sách giáo khoa thế kỷ 20)

> [!example] 🔬 Thám Tác Môn
> Nội dung theo Thám Tác Môn (Vương Khánh)

> [!abstract] 🎯 Manh Phái
> Nội dung theo Manh Phái

> [!quote] 🌸 Hoa Vũ Mệnh Lý
> Nội dung theo Hoa Vũ (Hà Kiến Trung)

> [!warning] ⚠️ Điểm tranh luận
> Đây là điểm các phái bất đồng — đọc kỹ từng góc nhìn

> [!success] ✅ Chung mọi phái
> Đây là điểm tất cả phái đồng thuận
```

---

## Các Bước Triển Khai (Theo Thứ Tự)

### Bước 1: Khởi tạo vault structure
- Tạo thư mục `/knowledge-base/` và tất cả subdirectories
- Tạo `.obsidian/app.json`
- Tạo 5 template files trong `_Templates/`

### Bước 2: Tạo Source Book note (10-Nguon-Sach/)
- `Thai-Cuc-Am-Duong-Hinh-Khi.md` — tóm tắt đầy đủ cuốn của Vương Khánh: mục lục, 3 phương pháp, phạm vi, đặc điểm phái
- Placeholder notes cho sách sẽ thêm sau

### Bước 3: Tạo Hệ Phái notes (09-He-Phai/)
- `He-Phai-Tong-Quan.md` — bản đồ lịch sử Tử Bình
- `Tham-Tac-Mon.md` — từ sách đã có
- Placeholder cho các phái chưa có sách

### Bước 4: Tạo Master MOC + Learning Roadmap (00-Tong-Quan/)
- `Tu-Binh-Kho-Kien-Thuc.md` — entry point chính
- `Lo-Trinh-Hoc.md` — lộ trình 8 tầng
- `So-Do-He-Phai.md` — bản đồ các phái và điểm khác nhau
- 8 MOC con

### Bước 5: Tạo Foundation Notes (01-Nen-Tang/) — 11 notes
- Âm Dương, Ngũ Hành, Sinh Khắc, Can Chi, Tàng Can, Vượng Suy, Lập lá số...
- Tất cả có `school: all` vì mọi phái đồng thuận

### Bước 6: Tạo Thập Thần notes (02-Thap-Than/) — 11 notes
- Tổng quan + 10 Thập Thần riêng lẻ
- Ghi chú điểm phái nào đặt nặng Thập Thần hơn

### Bước 7: Tạo Can Chi Biến Hóa notes (03-Can-Chi-Bien-Hoa/) — 10 notes
- Hợp/Xung/Hình/Hại/Phá/Trường Sinh

### Bước 8: Tạo Dụng Thần notes (04-Dung-Than/) — 7 notes ← TRỌNG TÂM
- `Dung-Than-Tong-Quan.md` — giải thích tại sao phái khác nhau
- 1 note per phái, dùng callout convention
- `So-Sanh-Cac-Phuong-Phap.md` — bảng so sánh

### Bước 9: Tạo Cách Cục notes (05-Cach-Cuc/) — 14 notes
- Overview + 8 chánh cách + Ngoại cách + Thám Tác Môn Tam Quan

### Bước 10: Tạo Thái Cực Pháp notes (06-Thai-Cuc-Phap/) — 7 notes
- Đặc thù Thám Tác Môn từ sách đã có

### Bước 11: Tạo Đại Vận & Lưu Niên notes (07-Dai-Van-Luu-Nien/) — 6 notes

### Bước 12: Tạo Ứng Dụng notes (08-Luan-Menh-Ung-Dung/) — 8 notes
- Case studies từ sách Vương Khánh làm điểm khởi đầu

### Bước 13: Cập nhật tất cả MOC files với links đầy đủ

---

## Workflow Khi Thêm Sách Mới

Khi thêm sách của hệ phái mới hoặc cùng hệ phái:

1. Claude đọc toàn bộ sách mới
2. Xác định hệ phái → tạo/cập nhật note trong `09-He-Phai/`
3. Tạo Source Book note trong `10-Nguon-Sach/`
4. **Với khái niệm mới chưa có note** → tạo note mới, ghi `school: [ten-phai]`
5. **Với khái niệm đã có note** → thêm callout block cho hệ phái mới vào note đó
6. **Với điểm phân kỳ** → cập nhật `04-Dung-Than/So-Sanh-Cac-Phuong-Phap.md` và bảng so sánh trong note liên quan
7. Cập nhật `00-Tong-Quan/So-Do-He-Phai.md`
8. Cập nhật các MOC liên quan

---

## Xác Minh (Verification)

Sau khi hoàn thành, kiểm tra:

- Mở `/knowledge-base/` làm Obsidian vault
- Mở `00-Tong-Quan/Tu-Binh-Kho-Kien-Thuc.md` — phải thấy links đến tất cả khu vực
- Bật Graph View — phải thấy mạng lưới liên kết, các note hệ phái cluster rõ ràng
- Cài Dataview → chạy query:
  ```
  TABLE school, level, divergence FROM "knowledge-base"
  WHERE divergence = "high"
  SORT level
  ```
  Phải hiện đủ các điểm phân kỳ cao giữa phái
- Dùng `Lo-Trinh-Hoc.md` làm lộ trình, click từng tier kiểm tra tính liên tục

---

## Files Nguồn Cần Đọc Khi Triển Khai

**Sách đã có:**
- `No20_Thái Cực Âm Dương Hình Khí Lý Số_P1.md` (trong project knowledge) — đọc toàn bộ

**Sách sẽ bổ sung (placeholder):**
- Tích Thiên Tủy (积天髓) — Tử Bình cổ điển
- Lan Đài Diệu Bí (兰台妙秘) — cổ điển
- Tam Mệnh Thông Hội (三命通会) — cổ điển
- Manh Phái tài liệu
- Hoa Vũ Mệnh Lý (Hà Kiến Trung)

**Template hiện tại:**
- `sample_plan.md` — tham khảo cấu trúc từ dự án Thái Ất
