# seo-technical — Kiểm Tra Kỹ Thuật

## Tổng Quan

Phân tích kỹ thuật SEO toàn diện trên 9 danh mục. Được kích hoạt tự động trong `/seo-audit`.

## 9 Danh Mục Kiểm Tra

| # | Danh mục | Nội dung |
|---|----------|----------|
| 1 | Crawlability | robots.txt, meta robots, canonical, redirect chains |
| 2 | Indexability | Noindex, canonicalization, pagination |
| 3 | Security | HTTPS, HSTS, mixed content, CSP |
| 4 | Core Web Vitals | LCP (<2.5s), INP (<200ms), CLS (<0.1) |
| 5 | Mobile | Viewport, touch targets, font sizes |
| 6 | JS Rendering | CSR/SSR detection, hydration issues |
| 7 | URL Structure | Length, special characters, parameters |
| 8 | HTTP Headers | Status codes, redirects, caching |
| 9 | IndexNow | Protocol support, API submission |

## Sử dụng trực tiếp

```
"Run seo-technical analysis for example.com"
```

## Trong workflow

Tự động kích hoạt trong `/seo-audit` (luôn chạy).
