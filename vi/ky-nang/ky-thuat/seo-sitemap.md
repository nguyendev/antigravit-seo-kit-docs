# seo-sitemap — Sitemap Analysis

## Mô Tả

Phân tích và kiểm tra XML sitemap: cấu trúc, URLs, lastmod, priority, coverage so với site thực tế.

## Agent Phụ Trách

`seo-auditor` (skill #7/10)

## Chức Năng Chính

- Phân tích XML sitemap (sitemap.xml, sitemap index)
- So sánh URLs trong sitemap vs URLs thực tế
- Kiểm tra lastmod accuracy
- Phát hiện orphan pages (không có trong sitemap)
- Kiểm tra sitemap size limits (50K URLs, 50MB)
- Tạo sitemap mới nếu thiếu

## Khi Nào Dùng

- "sitemap", "xml sitemap", "sitemap analysis"
- "sitemap audit", "sitemap generation"

## Workflow Liên Quan

- `/seo-audit` — Kiểm tra sitemap trong audit toàn diện
