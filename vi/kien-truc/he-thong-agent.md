# Hệ Thống Agent (8 Agents)

SEO Kit sử dụng 8 AI agents chuyên biệt — mỗi agent là một "chuyên gia" tập trung vào lĩnh vực SEO cụ thể, được trang bị bộ kỹ năng riêng.

## Tổng Quan

| Agent | Chuyên môn | Skills | Workflow chính |
|-------|-----------|:------:|---------------|
| `seo-auditor` | Chẩn đoán toàn diện | 10 | `/seo-audit` |
| `seo-strategist` | Lập kế hoạch & từ khóa | 6 | `/seo-strategy`, `/seo-research` |
| `seo-content-writer` | Tạo nội dung & pipeline | 7 | `/seo-write`, `/seo-page` |
| `seo-ai-specialist` | GEO / AI visibility | 7 | `/seo-llm-visibility` |
| `seo-local-expert` | Local SEO | 3 | `/seo-local-suite` |
| `seo-growth-hacker` | Off-page & phân phối | 9 | `/seo-social-commerce` |
| `seo-data-analyst` | Analytics & giám sát | 4 | `/seo-monitor` |
| `seo-migration-expert` | Di chuyển & sửa lỗi | 2 | `/seo-execute` |

**Thống kê:** 46 skills unique / 49 with shared. 0 orphan skills. 3 shared skills.

## Agent → Skills Mapping

```
seo-auditor (10 skills)
├── seo                (core: aggregator, crawler)
├── seo-audit          (orchestration)
├── seo-technical      (SSL, headers, robots)
├── seo-content        (E-E-A-T, readability)   ⟵ shared with content-writer
├── seo-schema         (JSON-LD, validation)
├── seo-images         (alt text, formats)
├── seo-sitemap        (XML sitemap)
├── seo-hreflang       (international)
├── seo-geo            (AI readiness)           ⟵ shared with ai-specialist
└── seo-source-context (authorship)             ⟵ shared with content-writer

seo-strategist (6 skills)
├── seo-plan           (project planning)
├── seo-keyword        (keyword research)
├── seo-content-gap    (competitor gaps)
├── seo-topical-authority (cluster maps)
├── seo-audience       (personas)
└── seo-competitor-pages (rival analysis)

seo-content-writer (7 skills)
├── seo-writer         (7-step agentic pipeline)  ★ MỚI
├── seo-content        (quality scoring)          ⟵ shared with auditor
├── seo-page           (page optimization)
├── seo-source-context (authorship)               ⟵ shared with auditor
├── seo-entity         (entity SEO)
├── seo-programmatic   (content at scale)
└── seo-fan-out-generator (variations)

seo-ai-specialist (7 skills)
├── seo-geo            (GEO analysis)             ⟵ shared with auditor
├── seo-geo-monitor    (AI mention tracking)
├── seo-agentic        (agent readiness)
├── seo-llmstxt        (llms.txt)
├── seo-answer         (answer engines)
├── seo-citemet        (citation metrics)
└── seo-prompt-research (AI prompt patterns)

seo-local-expert (3 skills)
├── seo-local          (GBP, NAP, citations)
├── seo-maps           (geo-grid, map pack)
└── seo-coccoc-optimizer (Vietnam search)

seo-growth-hacker (9 skills)
├── seo-backlink       (link building)
├── seo-authority      (brand authority)
├── seo-social-zalo    (Zalo, social platforms)
├── seo-reddit-scraper (Reddit mining)
├── seo-brand-sentiment (brand monitoring)
├── seo-video          (YouTube SEO)
├── seo-video-transcript (TikTok/Shorts)
├── seo-image-gen      (AI images)
└── seo-visual-search  (Google Lens)

seo-data-analyst (4 skills)
├── seo-google         (GSC, PageSpeed, GA4)
├── seo-dataforseo     (DataForSEO API)
├── seo-logs           (server log analysis)
└── seo-test           (SEO A/B testing)

seo-migration-expert (2 skills)
├── seo-migration      (domain moves, CMS)
└── seo-fix            (bulk technical fixes)
```

## Shared Skills (3 skills — cùng tên, khác mục đích)

| Skill | Agent A (mục đích) | Agent B (mục đích) |
|-------|-------------------|-------------------|
| `seo-content` | `seo-auditor` (scoring/audit) | `seo-content-writer` (creating) |
| `seo-source-context` | `seo-auditor` (checking) | `seo-content-writer` (building) |
| `seo-geo` | `seo-auditor` (citability check) | `seo-ai-specialist` (GEO strategy) |

## Routing Tự Động

SEO Kit tự động chọn agent phù hợp dựa trên:

1. **Lệnh slash** → Agent gắn với workflow đó
2. **`@agent`** → Load agent trực tiếp
3. **Ý định** → Auto-detect từ câu hỏi
4. **Domain** → Hiển thị project state + suggest agent

Ví dụ:
- "audit site" → `seo-auditor`
- "viết bài" → `seo-content-writer` → `/seo-write`
- "appear in ChatGPT" → `seo-ai-specialist`
- "local SEO Hà Nội" → `seo-local-expert`

## Cross-Agent Workflow

`/seo-execute` là workflow duy nhất kích hoạt skills từ **5 agents**. Xem chi tiết tại [Workflows](../workflows).
