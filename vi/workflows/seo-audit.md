# /seo-audit — Phase 2: Kiểm Tra Toàn Diện

## Tổng Quan

Quét chẩn đoán toàn diện website. Kích hoạt các kỹ năng chuyên biệt song song để kiểm tra sức khỏe kỹ thuật, chất lượng nội dung, schema, hình ảnh, sitemap, SEO đa ngôn ngữ, và độ sẵn sàng AI search. Tạo Health Score (0-100) và kế hoạch hành động ưu tiên.

## Cách Sử Dụng

```
/seo-audit https://example.com
```

## Kỹ Năng Kích Hoạt (tối đa 9)

| # | Kỹ năng | Vai trò | Điều kiện |
|---|---------|---------|-----------|
| 1 | `seo-technical` | Crawlability, indexability, bảo mật, CWV, JS rendering, IndexNow | Luôn |
| 2 | `seo-content` | E-E-A-T scoring, readability, thin content | Luôn |
| 3 | `seo-schema` | Schema.org detection, validation, deprecation check | Luôn |
| 4 | `seo-sitemap` | XML sitemap quality, coverage | Luôn |
| 5 | `seo-images` | Alt text, file sizes, formats, lazy loading, CLS | Luôn |
| 6 | `seo-hreflang` | Hreflang validation, SEO đa ngôn ngữ | Luôn |
| 7 | `seo-geo` | AI crawler access, citability, agentic search readiness | Luôn |
| 8 | `seo-google` | CWV field data, indexation status (PageSpeed, CrUX) | Nếu có API credentials |
| 9 | `seo-local` | GBP, NAP, citations, reviews, local schema | Nếu phát hiện local business |

## Health Score (0-100)

| Danh mục | Trọng số |
|----------|----------|
| Technical SEO | 22% |
| Content Quality | 23% |
| On-Page SEO | 20% |
| Schema / Structured Data | 10% |
| Performance (CWV) | 10% |
| AI Search Readiness | 10% |
| Images | 5% |

## Luồng Xử Lý

```
/seo-audit example.com
    │
    ▼
┌─────────────────┐
│   seo-audit      │  ← Phase workflow
└────────┬─────────┘
         │  Kích hoạt 9 kỹ năng
    ┌────┴────┬────────┬────────┬────────┬────────┬────────┬────────┬────────┐
    ▼         ▼        ▼        ▼        ▼        ▼        ▼        ▼        ▼
┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐ ┌───────┐
│tech   │ │content│ │schema │ │sitemap│ │images │ │hreflang│ │geo    │ │google │
└───┬───┘ └───┬───┘ └───┬───┘ └───┬───┘ └───┬───┘ └───┬───┘ └───┬───┘ └───┬───┘
    └─────────┴────────┴────┬───┴────────┴────────┴────────┴────────┘
                            │
                            ▼
                    ┌───────────────┐
                    │  Tổng hợp     │
                    │  Health Score │
                    └───────┬───────┘
                            │
                            ▼
                    ┌───────────────┐
                    │  Phase:       │  ← phase: "audited"
                    │  "audited"    │
                    └───────────────┘
```

## Output

```
seo-projects/{domain-slug}/
├── reports/
│   ├── audit-{date}.md
│   └── action-plan-{date}.md
└── data/
    └── audit-{date}.json
```

## Gợi Ý Tiếp

"Audit hoàn tất (Score: XX/100). Chạy `/seo-strategy` hoặc `/seo-run` để lên chiến lược nội dung & thị trường."
