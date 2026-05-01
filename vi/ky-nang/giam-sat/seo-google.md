# seo-google — Google APIs (GSC, PageSpeed, GA4)

## Mô Tả

Tích hợp Google APIs: Search Console, PageSpeed Insights, CrUX, Indexing API, GA4. Provider dữ liệu chính cho giám sát SEO.

## Agent Phụ Trách

`seo-intelligence` (skill #1/4)

## Chức Năng Chính

- **Google Search Console**: Query performance, indexing status, manual actions
- **PageSpeed Insights**: Core Web Vitals (LCP, INP, CLS)
- **CrUX data**: Chrome UX Report — real user metrics
- **Indexing API**: Submit URLs cho instant indexing
- **GA4 integration**: Organic traffic, conversions, user behavior

## Credential Tiers

| Tier | Phát hiện | Lệnh khả dụng |
|------|-----------|---------------|
| **0** (API Key) | `api_key` | `pagespeed`, `crux`, `youtube`, `nlp` |
| **1** (OAuth/SA) | + OAuth token | Tier 0 + `gsc`, `inspect`, `sitemaps`, `index` |
| **1+** (MCP) | + `search-console-mcp` | Tier 1 + **30+ MCP tools** |
| **2** (Full) | + `ga4_property_id` | Tier 1 + `ga4`, `ga4-pages` |

## MCP Mode (Tier 1+)

Khi cài `search-console-mcp`, bạn được bổ sung **30+ tools** không có trong scripts:

| Nhóm | Tools | Ví dụ |
|------|:-----:|-------|
| SEO Intelligence | 6 | `detect_cannibalization`, `seo_quick_wins`, `seo_lost_queries` |
| Bing | 7 | `bing_analytics_query`, `bing_index_now` |
| GA4 | 6 | `analytics_page_performance`, `analytics_realtime` |
| Cross-Platform | 5 | `compare_engines`, `opportunity_matrix` |

> **Quy tắc:** Tag MCP data là `[VERIFIED:GSC-MCP]`, script data là `[VERIFIED:GSC-Script]`.

Xem [hướng dẫn cài đặt Search Console MCP](../../mo-rong/search-console-mcp.md).

## Khi Nào Dùng

- "Google Search Console", "GSC", "PageSpeed"
- "CrUX", "indexing API", "GA4", "Google API"
- "Bing", "cannibalization", "quick wins" (cần MCP)

## Workflow Liên Quan

- `/seo-monitor` — Giám sát metrics định kỳ
- `/seo-audit` — PageSpeed/CWV trong audit
- `/seo-strategy` — Quick wins, opportunities

## Lưu Ý

> Cần Google API credentials. Xem hướng dẫn setup tại phần cài đặt.
> MCP là optional — tất cả chức năng GSC cốt lõi hoạt động qua Python scripts.
