# seo-audit — Kiểm Tra Toàn Diện Website

## Mô Tả

Orchestration skill cho audit toàn diện: phối hợp tất cả skills của `seo-technical-architect` để tạo báo cáo Health Score tổng hợp.

## Agent Phụ Trách

`seo-technical-architect` (skill #2/10 — orchestrator)

## Chức Năng Chính

- **Full site audit**: Kiểm tra kỹ thuật, nội dung, schema, hình ảnh, sitemap, hreflang
- **Health Score**: Tổng điểm sức khỏe website (0-100)
- **Priority recommendations**: Xếp hạng lỗi theo severity (🔴 Critical → 🟢 Low)
- **Competitive benchmark**: So sánh với đối thủ
- **GEO readiness**: Kiểm tra sẵn sàng cho AI search
- **E-E-A-T assessment**: Đánh giá tín hiệu E-E-A-T

## Quy Trình Audit

```
1. Fetch HTML → Parse DOM
2. Technical check (CWV, SSL, robots, canonical)
3. Content check (E-E-A-T, readability, thin content)
4. Schema validation (JSON-LD, missing types)
5. Image audit (alt text, formats, CLS)
6. Sitemap & hreflang check
7. GEO readiness (AI crawler, llms.txt)
8. Source Context analysis (DNA Context)
9. Generate Health Score + Report
```

## Khi Nào Dùng

- "audit website", "kiểm tra SEO", "health score"
- "site audit", "full audit", "diagnostic"

## Workflow Liên Quan

- `/seo-audit` — Workflow chính
- `/seo-auto-run` — Tự động audit trong pipeline
