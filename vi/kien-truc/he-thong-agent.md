# Hệ Thống Agent (8 Agents)

SEO Kit sử dụng 8 AI agents chuyên biệt — mỗi agent là một "chuyên gia" tập trung vào lĩnh vực SEO cụ thể, được trang bị bộ kỹ năng riêng.

## Danh Sách Agents

| Agent | Chuyên môn | Kỹ năng | Workflow chính |
|-------|-----------|---------|---------------|
| `seo-auditor` | Chẩn đoán toàn diện | 9 skills + 9 scripts | `/seo-audit` |
| `seo-strategist` | Lập kế hoạch & từ khóa | 6 skills | `/seo-strategy`, `/seo-research` |
| `seo-content-writer` | Tạo nội dung | 6 skills | `/seo-page`, `/seo-run` |
| `seo-ai-specialist` | GEO / AI visibility | 6 skills | `/seo-llm-visibility` |
| `seo-local-expert` | Local SEO | 3 skills | `/seo-local-suite` |
| `seo-growth-hacker` | Off-page & phân phối | 8 skills | `/seo-social-commerce` |
| `seo-data-analyst` | Analytics & giám sát | 4 skills | `/seo-monitor`, `/seo-auto-run` |
| `seo-migration-expert` | Di chuyển & sửa lỗi | 2 skills | `/seo-execute` |

## Agent → Skills Mapping

```
seo-auditor
├── seo-audit, seo-technical, seo-content, seo-schema
├── seo-images, seo-sitemap, seo-hreflang
├── seo-geo, seo-source-context

seo-strategist
├── seo-plan, seo-keyword, seo-content-gap
├── seo-topical-authority, seo-audience, seo-competitor-pages

seo-content-writer
├── seo-content, seo-page, seo-source-context
├── seo-entity, seo-programmatic, seo-fan-out-generator

seo-ai-specialist
├── seo-geo, seo-geo-monitor, seo-agentic
├── seo-llmstxt, seo-answer, seo-citemet

seo-local-expert
├── seo-local, seo-maps, seo-coccoc-optimizer

seo-growth-hacker
├── seo-backlink, seo-social-zalo, seo-reddit-scraper
├── seo-brand-sentiment, seo-video, seo-video-transcript
├── seo-image-gen, seo-visual-search

seo-data-analyst
├── seo-google, seo-dataforseo, seo-logs, seo-test

seo-migration-expert
├── seo-migration, seo-fix
```

## Routing Tự Động

SEO Kit tự động chọn agent phù hợp dựa trên:

1. **Lệnh slash** → Agent gắn với workflow đó
2. **`@agent`** → Load agent trực tiếp
3. **Ý định** → Auto-detect từ câu hỏi của bạn
4. **Domain** → Hiển thị project state + suggest agent

Ví dụ:
- "audit site" → `seo-auditor`
- "keyword strategy" → `seo-strategist`
- "appear in ChatGPT" → `seo-ai-specialist`
- "local SEO Hà Nội" → `seo-local-expert`

## Triết Lý Từng Agent

| Agent | Triết lý |
|-------|---------|
| `seo-auditor` | "Đo lường mọi thứ. Không giả định." |
| `seo-strategist` | "Chiến lược không có dữ liệu là đoán. Dữ liệu không có chiến lược là nhiễu." |
| `seo-content-writer` | "Viết cho người, cấu trúc cho máy." |
| `seo-ai-specialist` | "Được trích dẫn là ranking #1 mới." |
| `seo-local-expert` | "Local SEO: đúng người, đúng nơi, đúng lúc." |
| `seo-growth-hacker` | "Nội dung là lửa. Phân phối là xăng." |
| `seo-data-analyst` | "Không có dữ liệu, bạn chỉ là người có ý kiến." |
| `seo-migration-expert` | "Migration không có kế hoạch = migration sang trang 2." |
