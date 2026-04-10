# Dự Án Đầu Tiên

Hướng dẫn setup và chạy phân tích SEO cho domain đầu tiên.

## Trước Khi Bắt Đầu

- ✅ Đã cài đặt Antigravity ([hướng dẫn](cai-dat.md))
- ✅ Đã cài đặt SEO Kit với license key
- ✅ Có domain muốn phân tích

## Bước 1: Chạy Lệnh Master

Trong khung chat của Antigravity, gõ:

```
/seo-run yourdomain.com
```

SEO Kit sẽ phát hiện đây là dự án mới (🆕) và đề xuất chạy `/seo-onboard`.

## Bước 2: Onboarding

Chấp nhận đề xuất. SEO Kit sẽ:

1. **Pre-scan** domain tự động (kiểm tra ngôn ngữ, CMS, loại doanh nghiệp)
2. **Hỏi 5-7 câu hỏi** để xác nhận thông tin:
   - Loại doanh nghiệp (SaaS / E-commerce / Local / Publisher / Agency)
   - Core topic (Semantic Anchor)
   - Mục tiêu SEO (traffic / leads / sales / AI visibility)
   - CMS / Platform
   - Thị trường mục tiêu
   - Đối thủ (URLs)
   - Timeline (ngắn / trung / dài hạn)

> 💡 AI sẽ gợi ý câu trả lời dựa trên pre-scan. Bạn chỉ cần xác nhận hoặc sửa lại.

3. Sau khi bạn trả lời, SEO Kit tự động:
   - Tạo thư mục `seo-projects/yourdomain-com/`
   - Phân tích Source Context (brand identity, E-E-A-T)
   - Xây dựng audience personas
   - Kiểm tra Google API credentials
   - Tạo báo cáo onboarding

## Bước 3: Tiếp Tục Vòng Đời

Sau onboarding, chạy lại:

```
/seo-run yourdomain.com
```

SEO Kit sẽ hiển thị dashboard trạng thái và đề xuất bước tiếp theo (thường là `/seo-research` hoặc `/seo-audit`).

## Cấu Trúc Thư Mục Dự Án

Mỗi domain tạo một thư mục riêng:

```
seo-projects/yourdomain-com/
├── project.json           ← Trạng thái, cấu hình, lịch sử
├── competitors.json       ← Đối thủ đã cache
├── reports/               ← Báo cáo markdown
├── data/                  ← Dữ liệu JSON máy đọc
├── fixes/                 ← File sửa lỗi (Phase 4)
└── screenshots/           ← Ảnh chụp
```

## 💡 Mẹo: Mỗi Dự Án = Một Conversation Mới

**Khuyến nghị**: Tạo một **conversation (chat) mới** trong Antigravity cho mỗi domain/dự án SEO.

Lý do:
- Mỗi dự án antigravity seo kit sẽ tự động tạo thư mục `seo-projects/domain-slug/` riêng biệt
- Conversation mới giúp AI tập trung vào context của domain đó
- Tránh nhầm lẫn dữ liệu giữa các domain
- Dễ quản lý lịch sử phân tích

**Cách làm**: Trong Antigravity, nhấn **"New Conversation"** (hoặc phím tắt Ctrl+Shift+L) trước khi bắt đầu phân tích domain mới.

## Bước Tiếp Theo

- [Workflows](../workflows) — Hiểu vòng đời 5 giai đoạn
- [CLI](../cli/lenh.md) — Xem danh sách lệnh
- [Kỹ Năng](../ky-nang) — Khám phá 44 kỹ năng
