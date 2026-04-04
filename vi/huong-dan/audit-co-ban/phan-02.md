# Phần 2: Chạy Audit

## Mục Tiêu

Thực hiện kiểm tra toàn diện website với tối đa 9 kỹ năng chuyên biệt song song.

## Bước 1: Khởi chạy audit

```
/seo-audit yourdomain.com
```

## Bước 2: Theo dõi quá trình

SEO Kit kích hoạt các kỹ năng phân tích:
- ✅ Technical SEO (crawlability, CWV, security)
- ✅ Content Quality (E-E-A-T scoring)
- ✅ Schema Markup (JSON-LD, deprecation)
- ✅ Sitemap (coverage, quality)
- ✅ Images (alt text, sizes, formats)
- ✅ Hreflang (international SEO)
- ✅ GEO (AI search readiness)
- 🔑 Google APIs (nếu có credentials)
- 📍 Local SEO (nếu phát hiện local business)

## Bước 3: Chờ kết quả

Audit toàn diện có thể mất vài phút tùy kích thước website. Kết quả bao gồm:
- **Health Score**: Điểm tổng hợp 0-100
- **Action Plan**: Danh sách ưu tiên Critical → High → Medium → Low

## Kết Quả

```
seo-projects/yourdomain-com/
├── reports/audit-{date}.md          ← Báo cáo chi tiết
├── reports/action-plan-{date}.md    ← Kế hoạch hành động
└── data/audit-{date}.json           ← Dữ liệu máy đọc
```

## Tiếp Theo

→ [Phần 3: Đọc Kết Quả](phan-03.md)
