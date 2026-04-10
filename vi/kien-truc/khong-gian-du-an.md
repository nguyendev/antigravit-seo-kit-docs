# Không Gian Dự Án

Mỗi domain tạo một thư mục dự án riêng.

## Cấu trúc

```
seo-projects/{domain-slug}/
├── project.json           # Trạng thái, cấu hình, lịch sử
├── competitors.json       # Đối thủ đã cache
├── reports/               # Báo cáo markdown
├── data/                  # Dữ liệu JSON (máy đọc)
├── fixes/                 # File sửa lỗi (Phase 4)
└── screenshots/           # Ảnh chụp
```

## Domain Slug

- `example.com` → `example-com`
- `www.example.com` → `example-com` (strip www)
- `shop.example.co.uk` → `shop-example-co-uk`

## project.json

Chứa toàn bộ thông tin dự án: domain, phase, health score, settings, source context, competitors, run history.

## 💡 Mẹo

Tạo **conversation mới** trong Antigravity cho mỗi domain để tránh nhầm lẫn context.
