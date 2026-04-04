# DataForSEO Extension

Extension mạnh nhất với 22 lệnh MCP, cung cấp dữ liệu SERP trực tiếp, từ khóa, backlinks, on-page analysis, và AI visibility.

## 22 Lệnh

### SERP (4 lệnh)
- `serps_google_organic` — Kết quả tìm kiếm organic
- `serps_google_maps` — Kết quả Google Maps
- `serps_ai_overview` — Google AI Overviews
- `serps_chatgpt_search` — ChatGPT search results

### Từ Khóa (5 lệnh)
- `kw_keyword_suggestions` — Gợi ý từ khóa
- `kw_related_keywords` — Từ khóa liên quan
- `kw_search_volume` — Volume tìm kiếm
- `kw_search_intent` — Search intent classification
- `kw_keyword_difficulty` — Độ khó từ khóa

### Backlinks (4 lệnh)
- `bl_summary` — Tổng quan backlink profile
- `bl_backlinks` — Danh sách backlinks chi tiết
- `bl_referring_domains` — Referring domains
- `bl_competitors` — Backlink competitors

### On-Page (5 lệnh)
- `onpage_crawl_start` — Bắt đầu crawl
- `onpage_crawl_status` — Trạng thái crawl
- `onpage_pages` — Danh sách trang
- `onpage_summary` — Tổng quan on-page
- `onpage_duplicate_content` — Phát hiện nội dung trùng lặp

### AI/GEO (2 lệnh)
- `ai_overview_presence` — Kiểm tra AI Overview presence
- `ai_chatgpt_mentions` — ChatGPT mention tracking

### Khác (2 lệnh)
- `domain_whois` — WHOIS lookup
- `serps_featured_snippet` — Featured snippet data

## Cấu Hình

```json
{
  "mcpServers": {
    "dataforseo": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-dataforseo"],
      "env": {
        "DATAFORSEO_LOGIN": "your_login",
        "DATAFORSEO_PASSWORD": "your_password"
      }
    }
  }
}
```
