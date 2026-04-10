# Tích Hợp MCP

SEO Kit sử dụng MCP (Model Context Protocol) để kết nối dữ liệu bên ngoài.

## Data Providers

| Provider | Dữ liệu |
|----------|---------|
| DataForSEO | SERP, keywords, backlinks, on-page |
| Ahrefs | DR, backlinks, content gap |
| Semrush | Keyword gap, toxic links |

## Tier System

| Tier | Nguồn | Mô tả |
|------|-------|-------|
| 0 | HTML-only | Mặc định, không cần API |
| 1 | + Google APIs | GSC, CrUX, PageSpeed |
| 2 | + DataForSEO | Live SERP data |
| 3 | + Ahrefs/Semrush | Full backlink data |
