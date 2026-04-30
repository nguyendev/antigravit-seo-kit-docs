# Tích Hợp MCP

SEO Kit sử dụng MCP (Model Context Protocol) để kết nối dữ liệu bên ngoài.

## Data Providers

| Provider | Dữ liệu | Loại | Ưu tiên |
|----------|---------|------|:-------:|
| [Solann API](../mo-rong/solann-api.md) | Keyword volume, trends, CPC, competitor keywords | In-house API | #1 |
| [Search Console MCP](../mo-rong/search-console-mcp.md) | GSC, Bing, GA4, SEO Intelligence — 30+ tools | MCP Server | #2 |
| [DataForSEO](../mo-rong/dataforseo.md) | SERP, keywords, backlinks, on-page | Extension | #3 |
| [Ahrefs](../mo-rong/ahrefs.md) | DR, backlinks, content gap | MCP Server | #4 |
| [Semrush](../mo-rong/semrush.md) | Keyword gap, toxic links | MCP Remote | #4 |

## Tier System

| Tier | Nguồn | Mô tả |
|------|-------|-------|
| 0 | HTML-only | Mặc định, không cần API |
| 1 | + Google APIs | GSC, CrUX, PageSpeed (qua scripts) |
| 1+ | + Search Console MCP | SEO Intelligence, Bing, GA4, Cross-Platform |
| 2 | + DataForSEO | Live SERP data |
| 3 | + Ahrefs/Semrush | Full backlink data |

## Search Console MCP (Tier 1+)

Extension quan trọng nhất — bổ sung **30+ tools** không có trong scripts:

- **SEO Intelligence**: Cannibalization, Quick Wins, Lost Queries, Anomalies
- **Bing**: Search analytics, IndexNow, Sitemap management
- **GA4**: Page performance, Traffic sources, Conversions, Realtime
- **Cross-Platform**: Compare Engines, Opportunity Matrix, Traffic Health

Xem [hướng dẫn cài đặt chi tiết](../mo-rong/search-console-mcp.md).

## Quy Tắc Tag Dữ Liệu

| Tag | Nguồn |
|-----|-------|
| `[VERIFIED:Solann]` | Dữ liệu từ Solann API |
| `[VERIFIED:GSC-MCP]` | Dữ liệu từ search-console-mcp |
| `[VERIFIED:GSC-Script]` | Dữ liệu từ Python scripts |
| `[VERIFIED:DataForSEO]` | Dữ liệu từ DataForSEO API |
