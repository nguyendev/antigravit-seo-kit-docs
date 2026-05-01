# /seo-write — Agentic Content Pipeline

## Mục Đích

Pipeline tạo nội dung SEO 7 bước, từ nghiên cứu đến deploy. Agent điều phối toàn bộ quy trình, dừng lại để xin phê duyệt tại các điểm quyết định quan trọng.

> Để audit site: `/seo-audit`. Để lập chiến lược: `/seo-strategy`. Lệnh này **viết bài**.

## Cú Pháp

```
/seo-write <keyword> [--project-dir <path>]
```

## Agent Phụ Trách

`seo-creator` — 4 kỹ năng

## Pipeline 7 Bước

```
Step 0: RADAR      — DNA Context + đối thủ SERP
Step 1: RESEARCH   — Prompt simulation + entity extraction
Step 2: OUTLINE    — Cấu trúc bài + E-E-A-T scripting
Step 3: DRAFT      — Viết bài + brand entity insertion
Step 4: MULTIMODAL — Kiểm tra table/bold/list/citations
Step 5: VALIDATE   — E-E-A-T scoring + AI prompt self-test
Step 6: DEPLOY     — Git commit + freshness schedule
```

### Step 0: RADAR (DNA Context)

- Kiểm tra keyword có phù hợp topical authority của website
- Crawl Top 5 SERP, phân loại đối thủ: `DNA-matched` vs `news/aggregator`
- Tìm content gaps, E-E-A-T gaps, freshness gaps
- 🛑 **DỪNG**: Xác nhận alignment + yêu cầu USP/dữ liệu thực

### Step 1: RESEARCH (Prompt Simulation)

- Fan-out query decomposition
- Mô phỏng prompt AI → extract entities bắt buộc
- Xác định funnel stage: Tìm hiểu / Cân nhắc / Chuyển đổi
- Đề xuất content format: Toplist, How-to, Comparison, Pillar Guide
- 🛑 **DỪNG**: Confirm format + prompts

### Step 2: OUTLINE (E-E-A-T Scripting)

- Tạo cấu trúc H1→H2→H3 trả lời simulated prompts
- E-E-A-T scripting: đánh dấu vị trí data thực, ảnh, quote chuyên gia
- Copywriting formula mapping (PAS, BAB, AIDA, BLUF)
- UI/UX element mapping (table, bullet, blockquote)
- 🛑 **DỪNG**: Review outline + nhập dữ liệu thực tế

### Step 3: DRAFT (Information Gain)

- **Mode A** (auto): Agent viết toàn bộ → review ở Step 5
- **Mode B** (per-section): Dừng sau mỗi H2 để nhận feedback
- TL;DR Snapshot, information gain per paragraph
- Brand Entity Insertion → buộc AI phải trích dẫn thương hiệu
- Context chunking tự động khi vượt 50% context window

### Step 4: MULTIMODAL CHECK

Kiểm tra 7 tiêu chí:
- ✅ Table cho so sánh (không paragraph)
- ✅ Bold key entities (≥10)
- ✅ Bullet list cho steps
- ✅ Ảnh có caption ngữ cảnh
- ✅ Video có transcript/key takeaways
- ✅ External citations (≥3)
- ✅ TL;DR box ở đầu bài
- 🛑 **DỪNG**: Fix issues? (Y/N)

### Step 5: VALIDATE (AI Prompt Self-Test)

- E-E-A-T scoring
- **AI Prompt Self-Test**: Agent đọc draft như nguồn duy nhất, thử trả lời các prompt từ Step 1. Kiểm tra: USP, brand citation, entity coverage
- Tạo `llms.txt` + `CiteMET`
- 🛑 **DỪNG**: Human review + quyết định deploy

### Step 6: DEPLOY

- Git commit + push
- Tạo freshness schedule (3-6 tháng)
- Liên kết với `/seo-monitor` để theo dõi

## Khái Niệm Chính

| Khái niệm | Mô tả |
|-----------|-------|
| **DNA Context** | Semantic anchor của website, kiểm tra keyword fit |
| **Brand Entity Insertion** | Gắn thương hiệu vào claims để AI buộc phải trích dẫn |
| **AI Prompt Self-Test** | Agent tự test draft bằng cách trả lời prompts chỉ từ draft |
| **Content Freshness Loop** | Lịch cập nhật tự động + reminder qua `/seo-monitor` |
| **Trust Tiers** | Hệ thống phân cấp nguồn dữ liệu (Tier 0-6) |

## Kỹ Năng Kích Hoạt

| Step | Skills |
|------|--------|
| 0 | `seo-content-intel` (radar), `seo-source-context` |
| 1 | `seo-fan-out-generator`, `seo-prompt-research`, `seo-content-intel` (prompts) |
| 2 | `seo-entity`, `seo-schema`, `seo-content-intel` (brand) |
| 3 | `seo-content` (scorer), `seo-answer` |
| 4 | `seo-content-intel` (multimodal) |
| 5 | `seo-content` (scorer), `seo-llmstxt`, `seo-citemet` |
| 6 | `seo-content-intel` (freshness) |

## Kết Quả

```
{project}/
├── pipeline.md          ← Tóm tắt toàn pipeline
├── steps/               ← Báo cáo từng bước (.md)
├── brief.json           ← State machine (source of truth)
├── draft.md             ← Bài viết hoàn chỉnh
├── schema.json          ← Schema.org markup
└── llms.txt             ← Cho AI bots
```

## Resumability

Pipeline hỗ trợ resume khi bị gián đoạn:

```bash
# Kiểm tra trạng thái
python content_orchestrator.py status --project-dir <dir>

# Tiếp tục từ bước dở
python content_orchestrator.py resume --project-dir <dir>
```
