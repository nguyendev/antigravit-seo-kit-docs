# Hệ Thống Agent (8 Agents)

SEO Kit sử dụng 8 AI agents chuyên biệt — mỗi agent là một "chuyên gia" tập trung vào lĩnh vực SEO cụ thể, được trang bị bộ kỹ năng riêng.

## Danh Sách Agents

| Agent | Chuyên môn | Kỹ năng | Workflow chính |
|-------|-----------|---------|---------------|
| `seo-auditor` | Chẩn đoán toàn diện | 10 skills | `/seo-audit` |
| `seo-strategist` | Lập kế hoạch & từ khóa | 6 skills | `/seo-strategy`, `/seo-research` |
| `seo-content-writer` | Tạo nội dung | 6 skills | `/seo-page`, `/seo-run` |
| `seo-ai-specialist` | GEO / AI visibility | 7 skills | `/seo-llm-visibility` |
| `seo-local-expert` | Local SEO | 3 skills | `/seo-local-suite` |
| `seo-growth-hacker` | Off-page & phân phối | 9 skills | `/seo-social-commerce` |
| `seo-data-analyst` | Analytics & giám sát | 4 skills | `/seo-monitor`, `/seo-auto-run` |
| `seo-migration-expert` | Di chuyển & sửa lỗi | 2 skills | `/seo-execute` |

## Agent → Skills Mapping

```
seo-auditor (10 skills)
├── seo                (core: aggregator, crawler)
├── seo-audit          (orchestration)
├── seo-technical      (SSL, headers, robots)
├── seo-content        (E-E-A-T, readability)  ⟵ shared with content-writer
├── seo-schema         (JSON-LD, validation)
├── seo-images         (alt text, formats)
├── seo-sitemap        (XML sitemap)
├── seo-hreflang       (international)
├── seo-geo            (AI readiness)          ⟵ shared with ai-specialist
└── seo-source-context (authorship)            ⟵ shared with content-writer

seo-strategist (6 skills)
├── seo-plan           (project planning)
├── seo-keyword        (keyword research)
├── seo-content-gap    (competitor gaps)
├── seo-topical-authority (cluster maps)
├── seo-audience       (personas)
└── seo-competitor-pages (rival analysis)

seo-content-writer (6 skills)
├── seo-content        (quality scoring)       ⟵ shared with auditor
├── seo-page           (page optimization)
├── seo-source-context (authorship)            ⟵ shared with auditor
├── seo-entity         (entity SEO)
├── seo-programmatic   (content at scale)
└── seo-fan-out-generator (variations)

seo-ai-specialist (7 skills)
├── seo-geo            (GEO analysis)          ⟵ shared with auditor
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

## Shared Skills (3)

3 skills được chia sẻ giữa agents — cùng skill nhưng **mục đích khác nhau**:

| Skill | Agent A (mục đích) | Agent B (mục đích) |
|-------|---------------------|---------------------|
| `seo-content` | `seo-auditor` (chấm điểm) | `seo-content-writer` (tạo mới) |
| `seo-source-context` | `seo-auditor` (kiểm tra) | `seo-content-writer` (xây dựng) |
| `seo-geo` | `seo-auditor` (citability check) | `seo-ai-specialist` (GEO strategy) |

> 📊 Tổng: 44 unique skills / 47 with shared assignments / 0 orphan skills

## Routing Tự Động

SEO Kit tự động chọn agent phù hợp theo thứ tự ưu tiên:

```
User Request
    │
    ├─ Lệnh /command? ─────→ Execute workflow → Agent cố định
    │       └─ Meta (/seo-run, /seo-auto-run) → Agent theo phase
    │
    ├─ @agent? ────────────→ Load agent trực tiếp
    │
    ├─ Skill cụ thể? ─────→ Load skill (không qua agent)
    │
    ├─ Ý định → AI search? → seo-ai-specialist
    │         → Audit?      → seo-auditor
    │         → Keywords?   → seo-strategist
    │
    └─ Domain detected? ──→ Hiển thị project state + suggest agent
```

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
