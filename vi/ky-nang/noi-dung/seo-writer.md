# seo-writer — Content Pipeline 7 Bước

## Mô Tả

Pipeline tạo nội dung SEO hoàn chỉnh, từ nghiên cứu DNA Context đến deploy. Sử dụng shared state qua `brief.json` với Trust Tier conflict resolution và dual-layer markdown output.

## Agent Phụ Trách

`seo-creator`

## Chức Năng Chính

- **7-step pipeline**: RADAR → RESEARCH → OUTLINE → DRAFT → MULTIMODAL → VALIDATE → DEPLOY
- **DNA Context alignment**: Kiểm tra keyword phù hợp topical authority
- **Brand Entity Insertion**: Gắn thương hiệu vào claims để buộc AI trích dẫn
- **AI Prompt Self-Test**: Agent tự test draft bằng simulated prompts
- **Content Freshness Loop**: Lịch cập nhật tự động
- **Draft Mode A/B**: Auto hoặc per-section với human feedback
- **Copywriting formula mapping**: PAS, BAB, AIDA, BLUF per H2
- **Context chunking**: Tự động split khi vượt 50% context window

## Scripts

| Script | Chức năng |
|--------|----------|
| `content_orchestrator.py` | State machine chính |
| `brief_manager.py` | CRUD cho brief.json |
| `conflict_resolver.py` | Trust Tier conflict resolution |
| `context_chunker.py` | Split/buffer/assemble nội dung dài |
| `content_validator.py` | E-E-A-T scoring + fact-checking |

## Khi Nào Dùng

- "Viết bài về X"
- "Tạo content cho Y"
- "Write article about Z"
- Cần pipeline tạo nội dung end-to-end

## Workflow Liên Quan

- `/seo-write` — Workflow chính
- Phụ thuộc: `seo-content-intel`, `seo-source-context`, `seo-entity`, `seo-schema`, `seo-fan-out-generator`, `seo-prompt-research`, `seo-content`, `seo-answer`, `seo-llmstxt`, `seo-citemet`
