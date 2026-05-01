# Hệ Thống Agent (9 Agents — 3-Layer Architecture)

SEO Kit sử dụng 9 AI agents chuyên biệt, tổ chức thành **3 tầng** + 1 meta-orchestrator. Mỗi agent là một "chuyên gia" tập trung vào lĩnh vực SEO cụ thể, được trang bị bộ kỹ năng riêng.

## Kiến Trúc 3-Layer

```
🎯 META: seo-orchestrator
│
├── 🏗️ FOUNDATION (WHAT to do — SEO disciplines)
│   ├── seo-technical-architect   → Infrastructure, audit, migration, fixes
│   ├── seo-content-authority     → Strategy, content, E-E-A-T, authority
│   └── seo-intelligence          → Data analytics, monitoring, attribution
│
├── 🌐 SURFACE (WHERE to rank — search surfaces)
│   ├── seo-ai-search             → GEO, AI Overviews, ChatGPT, agentic web
│   ├── seo-multimedia            → Video, social, image, visual search
│   └── seo-local-commerce        → Local, maps, CốcCốc, e-commerce
│
└── 🔧 ENABLER (HOW to execute — cross-cutting)
    ├── seo-creator               → Content pipeline, page optimization, pSEO
    └── seo-data-provider         → Unified data access (Solann, Google, DataForSEO)
```

## Tổng Quan

| Layer | Agent | Chuyên môn | Skills | Workflow chính |
|:-----:|-------|-----------|:------:|---------------|
| 🎯 Meta | `seo-orchestrator` | Lifecycle & coordination | meta | `/seo-run`, `/seo-auto-run` |
| 🏗️ Foundation | `seo-technical-architect` | Infrastructure & diagnostics | 9 | `/seo-audit` |
| 🏗️ Foundation | `seo-content-authority` | Strategy & authority | 12 | `/seo-strategy`, `/seo-research`, `/seo-onboard` |
| 🏗️ Foundation | `seo-intelligence` | Analytics & monitoring | 5 | `/seo-monitor` |
| 🌐 Surface | `seo-ai-search` | AI/GEO visibility | 6 | `/seo-llm-visibility` |
| 🌐 Surface | `seo-multimedia` | Video, social, visual | 4 | `/seo-social-commerce` |
| 🌐 Surface | `seo-local-commerce` | Local & commerce | 3 | `/seo-local-suite` |
| 🔧 Enabler | `seo-creator` | Content execution | 4 | `/seo-write`, `/seo-page` |
| 🔧 Enabler | `seo-data-provider` | Data access layer | 3 | *(enabler — no primary)* |

**Thống kê:** 42 skills unique / 53 with shared. 0 orphan skills. 5 shared skills.

## Agent → Skills Mapping

```
seo-technical-architect (9 skills) — 🏗️ Foundation
├── seo                (core: aggregator, crawler)
├── seo-audit          (orchestration)
├── seo-technical      (SSL, headers, robots)
├── seo-content        (E-E-A-T, scoring)        ⟵ shared with content-authority
├── seo-schema         (JSON-LD, validation)
├── seo-images         (alt text, formats)
├── seo-sitemap        (XML sitemap)
├── seo-hreflang       (international)
├── seo-migration      (domain moves, CMS)
└── seo-fix            (bulk technical fixes)

seo-content-authority (12 skills) — 🏗️ Foundation
├── seo-plan           (project planning)
├── seo-keyword        (keyword research)
├── seo-solann         (keyword volume, trends)   ⟵ shared with intelligence, data-provider
├── seo-content-gap    (competitor gaps)
├── seo-topical-authority (cluster maps)
├── seo-audience       (personas)
├── seo-competitor-pages (rival analysis)
├── seo-content        (quality + E-E-A-T)        ⟵ shared with technical-architect
├── seo-entity         (entity SEO)
├── seo-backlink       (link building)
├── seo-authority      (brand authority + sentiment)
└── seo-information-gain (comparative IG)          ⟵ shared with creator

seo-intelligence (5 skills) — 🏗️ Foundation
├── seo-solann         (keyword volume, trends)   ⟵ shared with content-authority, data-provider
├── seo-google         (GSC, PageSpeed, GA4)      ⟵ shared with data-provider
├── seo-dataforseo     (DataForSEO API)           ⟵ shared with data-provider
├── seo-logs           (server log analysis)
└── seo-test           (SEO A/B testing)

seo-ai-search (6 skills) — 🌐 Surface
├── seo-geo            (GEO analysis)
├── seo-geo-monitor    (AI mention tracking)
├── seo-agentic        (agent readiness)
├── seo-llm-signals    (llms.txt + CiteMET)
├── seo-answer         (answer engines)
└── seo-prompt-research (AI prompt patterns)

seo-multimedia (4 skills) — 🌐 Surface
├── seo-social         (Zalo + Reddit/Quora)
├── seo-video          (YouTube + TikTok/Shorts)
├── seo-image-gen      (AI images)
└── seo-visual-search  (Google Lens)

seo-local-commerce (3 skills) — 🌐 Surface
├── seo-local          (GBP, NAP, citations)
├── seo-maps           (geo-grid, map pack)
└── seo-coccoc-optimizer (Vietnam search)

seo-creator (4 skills) — 🔧 Enabler
├── seo-writer         (5-step agentic pipeline)
├── seo-page           (page optimization)
├── seo-programmatic   (content at scale + fan-out)
└── seo-information-gain (comparative IG)          ⟵ shared with content-authority

seo-data-provider (3 skills) — 🔧 Enabler
├── seo-solann         (keyword volume, trends)   ⟵ shared with content-authority, intelligence
├── seo-google         (GSC, PageSpeed, GA4)      ⟵ shared with intelligence
└── seo-dataforseo     (DataForSEO API)           ⟵ shared with intelligence
```

## Shared Skills (5 skills — cùng tên, khác mục đích)

| Skill | Agents | Mục đích |
|-------|--------|---------|
| `seo-content` | `seo-technical-architect` (scoring) | `seo-content-authority` (strategy) |
| `seo-solann` | `seo-content-authority` (strategy volume) | `seo-intelligence` (monitoring) | `seo-data-provider` (data access) |
| `seo-google` | `seo-intelligence` (analytics) | `seo-data-provider` (data access) |
| `seo-dataforseo` | `seo-intelligence` (analysis) | `seo-data-provider` (data access) |
| `seo-information-gain` | `seo-content-authority` (pre-creation IG strategy) | `seo-creator` (post-creation IG validation) |

## Routing Tự Động

SEO Kit tự động chọn agent phù hợp dựa trên:

1. **Lệnh slash** → Agent gắn với workflow đó
2. **`@agent`** → Load agent trực tiếp
3. **Ý định** → Auto-detect từ câu hỏi
4. **Domain** → Hiển thị project state + suggest agent

Ví dụ:
- "audit site" → `seo-technical-architect`
- "viết bài" → `seo-creator` → `/seo-write`
- "appear in ChatGPT" → `seo-ai-search`
- "local SEO Hà Nội" → `seo-local-commerce`
- "keyword volume" → `seo-content-authority` (via `seo-data-provider`)

## Cross-Agent Workflow

`/seo-execute` kích hoạt skills từ **nhiều agents**:

| Skill | Source Agent | Điều kiện |
|-------|-------------|----------|
| `seo-fix`, `seo-migration` | `seo-technical-architect` | Luôn chạy / `--migration` |
| `seo-schema` | `seo-technical-architect` | Luôn chạy |
| `seo-content` | `seo-content-authority` | Luôn chạy |
| `seo-video`, `seo-image-gen`, `seo-visual-search` | `seo-multimedia` | Nếu phù hợp |
| `seo-llm-signals` | `seo-ai-search` | Luôn chạy |

Xem chi tiết tại [Workflows](../workflows).
