# /seo-page — Phân Tích Trang Đơn

## Tổng Quan

Phân tích chuyên sâu MỘT trang web. Đây là tiện ích độc lập, **KHÔNG** ảnh hưởng giai đoạn vòng đời dự án. Sử dụng khi cần kiểm tra nhanh một URL cụ thể mà không cần chạy audit toàn site.

## Cách Sử Dụng

```
/seo-page https://example.com/about
```

## Kỹ Năng Kích Hoạt (4)

| # | Kỹ năng | Vai trò |
|---|---------|---------|
| 1 | `seo-page` | On-page SEO elements, title, meta, headings, URL, internal links |
| 2 | `seo-content` | E-E-A-T scoring, readability, word count, keyword optimization |
| 3 | `seo-schema` | Schema detection, validation, generation cho trang này |
| 4 | `seo-geo` | AI citability score, passage extractability |

## Các Bước Thực Hiện

1. **Load domain project**
2. **Fetch URL** và phân tích HTML source
3. **On-page SEO analysis**:
   - Title tag, meta description, heading hierarchy
   - URL structure, internal links, anchor text
   - Canonical, meta robots, Open Graph, Twitter Card
4. **Content quality assessment**: E-E-A-T signals, readability metrics
5. **Schema validation**: Detect, validate, recommend missing schema
6. **AI citability check**: Score citability, passage extractability
7. **Flag potential CWV issues**
8. **Page Score Card**: Binary checks ("✅ Has H1" / "❌ Missing alt text")

## Output

```
seo-projects/{domain-slug}/reports/page-{slug}-{date}.md
```

## Lưu Ý

Workflow này **KHÔNG** cập nhật project `phase`. Là tiện ích cho phân tích page-level nhanh tại bất kỳ thời điểm nào trong vòng đời SEO.
