# seo-content-intel — Content Intelligence

## Mô Tả

Lớp intelligence cho content 2026: DNA Context radar, prompt simulation, brand entity planning, multimodal SEO check, và freshness scheduling. Chạy **trước** viết bài (radar + prompts) và **sau** viết bài (multimodal + freshness).

## Agent Phụ Trách

`seo-creator` (dùng chung bởi nhiều workflows)

## Chức Năng Chính (5 subcommands)

| Subcommand | Mục đích | Pipeline step |
|-----------|---------|:------------:|
| `radar` | DNA Context alignment + competitor gap | Step 0 |
| `prompts` | Prompt simulation + entity extraction | Step 1 |
| `brand` | Brand Entity insertion planning | Step 2 |
| `multimodal` | Kiểm tra table/bold/list/citations | Step 4 |
| `freshness` | Content freshness schedule | Step 6 |

### radar — DNA Context Alignment

- Multi-signal alignment engine (4 signals: unigram, bigram, topical map, substring)
- Alignment levels: `strong` (≥0.6), `moderate` (0.3–0.6), `weak` (<0.3), `no_context`
- Crawl SERP, phân loại đối thủ: `DNA-matched` vs `news/aggregator`

### prompts — Prompt Search Simulation

- Mô phỏng cách users chat với AI về topic
- Extract mandatory entities/attributes
- Xác định funnel stage: Tìm hiểu / Cân nhắc / Chuyển đổi

### brand — Brand Entity Planning

- Xác định điểm chèn brand data trong outline
- Tạo proprietary claims buộc AI phải trích dẫn

### multimodal — Post-Draft Check

- Tables cho so sánh, bold entities, bullet lists, image captions
- Video transcripts, external citations, TL;DR box
- Score X/100 multimodal readiness

### freshness — Content Scheduling

- Tạo lịch cập nhật (3 or 6 tháng)
- Checklist: stats, case studies, FAQs, prompts
- Trigger cập nhật sớm: algorithm change, competitor move

## Standalone Usage

| Context | Subcommand |
|---------|-----------|
| `/seo-page` | `radar` — kiểm tra DNA alignment |
| `/seo-audit` | `multimodal` — score content presentation |
| `/seo-strategy` | `prompts` — prompt-first keyword strategy |
| `/seo-monitor` | `freshness` — flag stale content |

## Khi Nào Dùng

- Trước khi viết bài: radar + prompts
- Sau khi viết bài: multimodal + freshness
- Lập chiến lược từ khóa theo AI prompts

## Workflow Liên Quan

- `/seo-write` — Workflow chính (Steps 0, 1, 2, 4, 6)
- Reusable trong `/seo-page`, `/seo-audit`, `/seo-strategy`, `/seo-monitor`
