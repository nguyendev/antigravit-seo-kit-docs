# Audit Đầu Tiên

Hướng dẫn nhanh để chạy audit SEO đầu tiên sau khi cài đặt SEO Kit.

## Bước 1: Khởi tạo dự án

```
/seo-run example.com
```

SEO Kit sẽ phát hiện đây là dự án mới và đề xuất chạy `/seo-onboard`.

## Bước 2: Onboarding

```
/seo-onboard example.com
```

Workflow này kích hoạt 4 kỹ năng:
1. **seo-google**: Kiểm tra API credentials (GSC, GA4, PageSpeed)
2. **seo-source-context**: Phân tích thương hiệu, credibility score
3. **seo-audience**: Xây dựng personas đối tượng mục tiêu
4. **seo-plan**: Phát hiện ngành, đối thủ cạnh tranh

## Bước 3: Chạy audit

```
/seo-audit example.com
```

Audit toàn diện kích hoạt tới 9 kỹ năng song song:
- Technical SEO (crawlability, Core Web Vitals)
- Content Quality (E-E-A-T scoring)
- Schema Markup
- Sitemap
- Images
- Hreflang
- AI Search Readiness (GEO)

## Bước 4: Đọc kết quả

Kết quả được lưu tại:
```
seo-projects/example-com/reports/audit-{date}.md
seo-projects/example-com/reports/action-plan-{date}.md
seo-projects/example-com/data/audit-{date}.json
```

### Health Score

Điểm SEO tổng hợp (0-100) dựa trên 7 danh mục:

| Danh mục | Trọng số |
|----------|----------|
| Technical SEO | 22% |
| Content Quality | 23% |
| On-Page SEO | 20% |
| Schema / Structured Data | 10% |
| Performance (CWV) | 10% |
| AI Search Readiness | 10% |
| Images | 5% |

## Bước Tiếp Theo

Sau khi có audit, bạn có thể:
- Chạy `/seo-strategy` để lên chiến lược dựa trên kết quả audit
- Chạy `/seo-run example.com` để xem dashboard và nhận gợi ý tự động
- Gọi kỹ năng trực tiếp: "Run seo-entity for example.com"
