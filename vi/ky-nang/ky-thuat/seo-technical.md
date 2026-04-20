# seo-technical — Kiểm Tra Kỹ Thuật

## Mô Tả

Kiểm tra toàn diện khía cạnh kỹ thuật của website: tốc độ tải trang, Core Web Vitals, crawlability, indexability, robots.txt, canonical, SSL, headers.

## Agent Phụ Trách

`seo-auditor` (skill #3/10)

## Chức Năng Chính

- **Core Web Vitals**: LCP (<2.5s), INP (<200ms), CLS (<0.1)
- **LCP Subparts**: TTFB, resource load delay, load time, render delay
- **Crawlability**: Robots.txt, meta robots, X-Robots-Tag
- **Indexability**: Canonical tags, noindex, redirect chains
- **SSL/Security**: HTTPS, mixed content, HSTS
- **Server headers**: Cache-Control, Content-Encoding, CSP
- **Rendering**: SSR vs CSR detection, Soft Navigations API

## Scripts

| Script | Chức năng |
|--------|----------|
| `technical_auditor.py` | Audit kỹ thuật toàn diện |

## Khi Nào Dùng

- "kiểm tra kỹ thuật", "technical SEO", "page speed"
- "core web vitals", "robots.txt", "canonical"

## Workflow Liên Quan

- `/seo-audit` — Audit toàn diện (bao gồm technical)
