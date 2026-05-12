# Ghi Chú Phát Hành

## v1.1.0 (2026-05-12) — The Grand Unification

### Thay Đổi Lớn (Major Update)

- **Sáp nhập Web Kit vào SEO Kit**: Cập nhật khổng lồ với 189 file thay đổi, đưa hệ thống từ một bộ công cụ SEO đơn thuần thành một hệ sinh thái **SEO-Driven Web Development**.
- **Mở Rộng Hệ Thống Agent**: Từ 9 Agents tăng lên **24 Agents**.
  - Thêm 3 Web Agents (`web-frontend-specialist`, `web-backend-specialist`, `web-orchestrator`).
  - Thêm 10 Shared Agents (Bảo mật, DevOps, Test...).
- **Mở Rộng Kỹ Năng**: Tổng số kỹ năng tăng lên **77 Skills**. Thêm 12 Web Skills (React Performance, API, Database...) và 21 Shared Skills.
- **Agentic SEO & WebMCP**: 
  - Bổ sung framework Web Model Context Protocol (WebMCP) trong bộ `seo-agentic`.
  - Phát triển script `webmcp_audit.py` và `webmcp_generator.py` để tạo form tương tác và Action Schema phục vụ AI Agents.
- **Workflow Mới**: Thêm 11 `/web-*` workflows (`/web-create`, `/web-ui-design`, `/web-deploy`...).
- **Quy trình Xác Thực Mới**: Tích hợp `verify_all.py` - script master cho Audit Code, Web Vitals, và Bảo mật.

---

## v1.0.7 (2026-05-01)

### Thay Đổi Lớn

- **9-Agent 3-Layer Architecture**: Tái cấu trúc từ 8 agents flat → 9 agents 3-layer (Meta + Foundation + Surface + Enabler)
  - 🎯 **Meta**: `seo-orchestrator` (MỚI)
  - 🏗️ **Foundation**: `seo-technical-architect`, `seo-content-authority`, `seo-intelligence`
  - 🌐 **Surface**: `seo-ai-search`, `seo-multimedia`, `seo-local-commerce`
  - 🔧 **Enabler**: `seo-creator`, `seo-data-provider` (MỚI)
- **Agent đổi tên**: `seo-auditor` → `seo-technical-architect`, `seo-strategist` → `seo-content-authority`, `seo-content-writer` → `seo-creator`, `seo-ai-specialist` → `seo-ai-search`, `seo-growth-hacker` → `seo-multimedia`, `seo-data-analyst` → `seo-intelligence`, `seo-local-expert` → `seo-local-commerce`
- **Agent removed**: `seo-migration-expert` (merged vào `seo-technical-architect`)
- **Skills consolidated**: 46 → 42 unique, 49 → 53 with shared, 3 → 5 shared skills
- **Content pipeline**: 7 bước → 5 bước (streamlined)
- **Skill merges**: `seo-llmstxt` + `seo-citemet` → `seo-llm-signals`, `seo-social-zalo` + `seo-reddit-scraper` → `seo-social`, `seo-brand-sentiment` → absorbed into `seo-authority`
- **New skill**: `seo-information-gain` (shared between `seo-content-authority` & `seo-creator`)

---

## v1.0.6 (2026-04-30)

### Mới

- **Solann API**: In-house keyword data provider — default priority #1
  - Keyword volume (premium Google Ads data)
  - 12-month trends (seasonality analysis)
  - Topic clusters (semantic grouping)
  - Competitor keyword extraction (từ URL)
  - Long-tail expansion (Autocomplete + Alphabet Soup)
  - CPC / bid data
- **2 scripts**: `keyword_volume.py`, `keyword_suggest.py`
- **Provider priority**: Solann → Google Ads → DataForSEO → HTML-only

---

## v1.0.4 (2026-04-28)

### Mới

- **Search Console MCP**: Tích hợp `search-console-mcp` — 30+ MCP tools cho GSC, Bing, GA4
  - SEO Intelligence: cannibalization, quick wins, lost queries, anomalies
  - Bing Webmaster Tools: analytics, IndexNow, sitemap management
  - GA4: page performance, traffic sources, conversions, realtime
  - Cross-Platform: compare engines, opportunity matrix, traffic health
- **Tier 1+**: Credential tier mới cho MCP mode
- **Multi-Account**: Auto-routing cho agency quản lý nhiều domains

---
