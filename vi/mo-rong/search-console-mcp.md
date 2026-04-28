# Search Console MCP

Tích hợp `search-console-mcp` — MCP server cung cấp **30+ tools** cho Google Search Console, Bing Webmaster Tools, và Google Analytics 4.

> 📌 Đây là extension **optional** (Tier 1+). Tất cả chức năng GSC cốt lõi đều có sẵn qua Python scripts. MCP bổ sung thêm SEO Intelligence, Bing, GA4, và Cross-Platform analysis.

## Tổng Quan

| Thuộc tính | Giá trị |
|-----------|---------|
| Package | `search-console-mcp` |
| Cài đặt | `npx search-console-mcp setup` |
| Auth | OAuth 2.0 Desktop Flow (tự động) |
| Credential | OS Keychain (macOS/Windows/Linux) |
| Tools | 30+ |
| Yêu cầu | Node.js 18+, Google Search Console property |

## Cài Đặt

### Bước 1: Setup OAuth

```bash
npx search-console-mcp setup
```

Lệnh này sẽ:
1. Khởi động server cục bộ
2. Mở trình duyệt → trang xác thực Google
3. Cấp quyền truy cập Search Console
4. Tự động lưu token vào OS Keychain

> 🔒 Token được lưu trong trình quản lý credentials của hệ điều hành (macOS Keychain, Windows Credential Manager, Linux Secret Service). Fallback: mã hóa AES-256-GCM.

### Bước 2: Cấu Hình Trong Antigravity

1. Mở Agent panel (sidebar)
2. Click **⋯** → **Manage MCP Servers**
3. Click **View raw config**
4. Thêm:

```json
{
  "mcpServers": {
    "search-console": {
      "command": "npx",
      "args": ["-y", "search-console-mcp"]
    }
  }
}
```

5. Save → Quay lại **Manage MCP Servers** → Click **Refresh**

### Bước 3: Thêm Bing (Tùy chọn)

```json
{
  "mcpServers": {
    "search-console": {
      "command": "npx",
      "args": ["-y", "search-console-mcp"],
      "env": {
        "BING_API_KEY": "YOUR_BING_API_KEY"
      }
    }
  }
}
```

> Lấy API key tại: [Bing Webmaster Tools Settings](https://www.bing.com/webmasters/settings/api). Mỗi user có key riêng.

### Bước 4: Thêm GA4 (Tùy chọn)

```bash
npx search-console-mcp setup --engine=ga4
```

Wizard sẽ:
1. Yêu cầu đường dẫn Service Account JSON
2. Liệt kê GA4 properties khả dụng
3. Chọn property phù hợp

> ⚠️ GA4 yêu cầu **Service Account** (không dùng OAuth). Email SA phải được thêm làm **Viewer** trong GA4 Admin → Property Access Management.

Config đầy đủ (GSC + Bing + GA4):

```json
{
  "mcpServers": {
    "search-console": {
      "command": "npx",
      "args": ["-y", "search-console-mcp"],
      "env": {
        "GOOGLE_APPLICATION_CREDENTIALS": "C:\\Users\\YOU\\.config\\seo-kit\\service_account.json",
        "BING_API_KEY": "YOUR_BING_API_KEY"
      }
    }
  }
}
```

## Xác Nhận Cài Đặt

```bash
npx search-console-mcp accounts list
```

Kết quả mẫu:

```
✓ Google: seo@yourcompany.com (3 properties)
✓ Google: personal@gmail.com (2 properties)
✓ Bing: bing-user@outlook.com (1 site)
✓ GA4: seo-kit@project.iam.gserviceaccount.com (1 property)
```

## Danh Sách 30+ MCP Tools

### Google Search Console (7 tools)

| Tool | Chức năng | Workflow |
|------|----------|---------|
| `query_analytics` | Search analytics: clicks, impressions, CTR, position | `/seo-audit`, `/seo-monitor` |
| `compare_periods` | So sánh 2 khoảng thời gian | `/seo-monitor` |
| `analytics_time_series` | Xu hướng hàng ngày, phát hiện ngày bắt đầu giảm | `/seo-monitor` |
| `analytics_drop_attribution` | Tương quan drop với Core Update | `/seo-monitor` |
| `inspect_url` | Trạng thái index URL | `/seo-audit` |
| `inspection_batch` | Batch inspection (tối đa 5/lần) | `/seo-audit` |
| `get_pagespeed` | PageSpeed + Core Web Vitals | `/seo-audit` |

### SEO Intelligence (6 tools) — chỉ có qua MCP

| Tool | Chức năng | Workflow |
|------|----------|---------|
| `seo_opportunities` | Impressions cao, CTR thấp → fix title/meta | `/seo-strategy` |
| `detect_cannibalization` | Phát hiện nhiều trang cạnh tranh cùng keyword | `/seo-audit` |
| `seo_quick_wins` | Striking distance keywords (vị trí 4-10) | `/seo-strategy` |
| `detect_anomalies` | Phát hiện bất thường thống kê (Z-score) | `/seo-monitor` |
| `seo_lost_queries` | Keywords đang mất thứ hạng | `/seo-monitor` |
| `seo_brand_vs_nonbrand` | Phân tách brand vs organic growth | `/seo-strategy` |

### Bing Webmaster Tools (7 tools) — chỉ có qua MCP

| Tool | Chức năng | Workflow |
|------|----------|---------|
| `bing_analytics_query` | Bing search performance | `/seo-audit` |
| `bing_analytics_compare_periods` | So sánh xu hướng Bing | `/seo-monitor` |
| `bing_analytics_detect_anomalies` | Phát hiện bất thường Bing | `/seo-monitor` |
| `bing_url_info` | Trạng thái index URL trên Bing | `/seo-audit` |
| `bing_index_now` | Instant indexing (IndexNow) | `/seo-execute` |
| `bing_sitemaps_list` | Danh sách sitemaps | `/seo-execute` |
| `bing_sitemaps_submit` | Submit sitemap | `/seo-execute` |

### Google Analytics 4 (6 tools)

| Tool | Chức năng | Workflow |
|------|----------|---------|
| `analytics_page_performance` | Sessions, engagement rate theo trang | `/seo-audit` |
| `analytics_traffic_sources` | Phân tích Channel/Source/Medium | `/seo-audit` |
| `analytics_organic_landing_pages` | Trang đích organic traffic | `/seo-strategy` |
| `analytics_conversion_funnel` | Trang chuyển đổi cao nhất | `/seo-strategy` |
| `analytics_user_behavior` | Thiết bị, quốc gia, engagement | `/seo-audit` |
| `analytics_realtime` | Active users thời gian thực | `/seo-monitor` |

### Cross-Platform Intelligence (5 tools) — chỉ có qua MCP

| Tool | Chức năng | Workflow |
|------|----------|---------|
| `opportunity_matrix` | GSC + GA4 combined opportunities | `/seo-strategy` |
| `traffic_health_check` | Health check đa nguồn tự động | `/seo-monitor` |
| `page_analysis` | Deep page analysis (GSC + GA4) | `/seo-audit` |
| `compare_engines` | So sánh Google vs Bing | `/seo-monitor` |
| `sites_health_check` | Dashboard tất cả properties | `/seo-monitor` |

## Script vs MCP — Khi Nào Dùng Cái Nào?

| Nhu cầu | Dùng | Lý do |
|---------|------|-------|
| GSC analytics (>1000 rows) | Script `gsc_query.py` | Batch processing, quick-win detect |
| Trend analysis + drop attribution | MCP `analytics_time_series` | Không có trong scripts |
| Phát hiện cannibalization | MCP `detect_cannibalization` | Thuật toán riêng |
| Quick wins (striking distance) | MCP `seo_quick_wins` | Không có trong scripts |
| Bing analytics/indexing | MCP `bing_*` | Không có Bing scripts |
| GA4 đầy đủ | MCP `analytics_*` | Nhiều tools hơn `ga4_report.py` |
| GA4 cơ bản | Script `ga4_report.py` | Không cần setup MCP |
| URL inspection (batch lớn) | Script `gsc_inspect.py` | Không giới hạn 5 URL |
| URL inspection (nhanh) | MCP `inspect_url` | Nhanh hơn, ít setup |
| CrUX History (25 tuần) | Script `crux_history.py` | MCP không có |
| Indexing API (Google) | Script `indexing_notify.py` | MCP chỉ có Bing IndexNow |
| YouTube, NLP, Knowledge Graph | Scripts only | MCP không hỗ trợ |

> **Quy tắc tag dữ liệu:** MCP data → `[VERIFIED:GSC-MCP]`, Script data → `[VERIFIED:GSC-Script]`. Cả hai đều là nguồn xác thực.

## Multi-Account

### Thêm Tài Khoản

```bash
# Chạy setup cho mỗi tài khoản Google
npx search-console-mcp setup
```

Mỗi lần chạy sẽ mở trình duyệt cho tài khoản Google mới. Server **tự động chọn** tài khoản đúng dựa trên `siteUrl` bạn truy vấn.

### Quản Lý Tài Khoản

```bash
# Liệt kê tài khoản
npx search-console-mcp accounts list

# Đăng xuất tài khoản mặc định
npx search-console-mcp logout

# Đăng xuất tài khoản cụ thể
npx search-console-mcp logout user@gmail.com
```

### Agency Workflow

Sau khi login + config Bing:

```
Account: seo@agency.com
  Google: sc-domain:client-a.com, sc-domain:client-b.com
  Bing: client-a.com, client-b.com
  GA4: properties/123456789 (client-a.com)
```

Truy vấn trực tiếp bất kỳ property nào — auto-routing tự chọn tài khoản đúng.

### Thêm Domain Mới

1. Verify domain trong Google Search Console
2. (Tùy chọn) Thêm vào Bing Webmaster Tools
3. MCP tự phát hiện — không cần thay đổi config

## Biến Môi Trường

| Biến | Bắt buộc | Mô tả |
|------|:--------:|-------|
| `BING_API_KEY` | ❌ | API key Bing Webmaster Tools |
| `GOOGLE_APPLICATION_CREDENTIALS` | ❌ | Đường dẫn Service Account JSON (cho GA4) |

> Không cần `GSC_OAUTH_*` — OAuth được quản lý tự động bởi `npx search-console-mcp setup` và lưu trong OS Keychain.

## Xử Lý Sự Cố

| Vấn đề | Giải pháp |
|--------|-----------|
| `npx` không tìm thấy | Cài Node.js 18+ từ [nodejs.org](https://nodejs.org) |
| OAuth popup không mở | Kiểm tra firewall. Chạy `npx search-console-mcp setup` trong terminal |
| `403 Forbidden` | Tài khoản Google chưa có quyền. Kiểm tra GSC Settings → Users |
| Bing tools không hoạt động | Kiểm tra `BING_API_KEY` trong `mcp_config.json` env |
| GA4 tools không hoạt động | Chạy `npx search-console-mcp setup --engine=ga4`. Thêm SA email làm Viewer trong GA4 |
| MCP server không hiển thị | Restart IDE sau khi sửa `mcp_config.json`. Kiểm tra Agent panel |
| Token hết hạn | Chạy `npx search-console-mcp setup` lại. Hoặc `logout` → re-setup |

## Rate Limits

| API | Per-Minute | Per-Day | Auth |
|-----|-----------|---------|------|
| GSC Search Analytics | 1,200 QPM/site | 30M QPD | OAuth (MCP) |
| GSC URL Inspection | 600 QPM | 2,000 QPD/site | OAuth (MCP) |
| Bing Analytics | Theo Bing quota | — | API Key |
| GA4 Data API | 10 concurrent | ~25K tokens/day | Service Account |

## Kỹ Năng Liên Quan

| Kỹ năng | Vai trò |
|---------|---------|
| [seo-google](../ky-nang/giam-sat/seo-google.md) | Skill chính sử dụng MCP tools |
| [seo-dataforseo](dataforseo.md) | SERP data bổ sung |
| [seo-technical](../ky-nang/ky-thuat/seo-technical.md) | CWV thresholds |
