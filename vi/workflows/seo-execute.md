# /seo-execute — Phase 4: Thực Thi

## Tổng Quan

Chuyển đổi kết quả audit và chiến lược thành sản phẩm sẵn dùng: code fixes, schema markup, redirect maps, content briefs, và video SEO assets. Mọi thứ developer hoặc team nội dung cần để triển khai kế hoạch SEO.

## Cách Sử Dụng

```
/seo-execute example.com --categories meta,schema,robots,redirects
```

### Tham số

| Tham số | Mô tả |
|---------|-------|
| `--categories` | Loại fix cần tạo: `meta`, `schema`, `robots`, `redirects`, `content`, `video` |
| `--migration` | Bật chế độ migration (redirect mapping, pre/post plans) |

## Điều Kiện Tiên Quyết

- **Bắt buộc**: Dữ liệu audit từ Phase 2 (`data/audit-{date}.json`)
- **Khuyến nghị**: Chiến lược từ Phase 3 cho content brief generation
- Không có audit data → lỗi: "Chạy `/seo-audit` trước."

## Kỹ Năng Kích Hoạt (tối đa 6)

| # | Kỹ năng | Vai trò | Điều kiện |
|---|---------|---------|-----------|
| 1 | `seo-fix` | Tự tạo meta tags, schema JSON-LD, robots.txt, redirects | Luôn |
| 2 | `seo-schema` | Tạo schema mới cho trang thiếu structured data | Luôn |
| 3 | `seo-content` | Content briefs và hướng dẫn tối ưu | Luôn |
| 4 | `seo-migration` | Redirect mapping, kế hoạch pre/post migration | Nếu có `--migration` |
| 5 | `seo-video` | VideoObject schema, video sitemap generation | Nếu phát hiện video |
| 6 | `seo-image-gen` | AI-generated SEO image assets | Nếu extension khả dụng |

## Output

```
seo-projects/{domain-slug}/
├── fixes/{date}/              ← Tất cả file sửa lỗi
│   ├── meta-tags.html
│   ├── schema-jsonld/
│   ├── robots.txt
│   └── redirects.csv
└── reports/
    └── execution-{date}.md
```

## Gợi Ý Tiếp

"Fixes đã tạo. Review files trong `fixes/{date}/`. Chạy `/seo-monitor` hoặc `/seo-run` để theo dõi tác động."
