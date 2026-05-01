# seo-citemet — Citation Metrics (CiteMET)

## Mô Tả

Tạo CiteMET — nút chia sẻ cho AI: AI share button, prompt payload, "Share to ChatGPT", AI memory injection cho content.

## Agent Phụ Trách

`seo-ai-search` (skill #6/7)

## Chức Năng Chính

- **CiteMET generation**: Tạo citemet markup cho pages
- **AI share button**: Nút "Share to ChatGPT/Claude"
- **Prompt payload**: Pre-built prompts kích hoạt AI trích dẫn
- **AI memory injection**: Structured data cho AI to remember
- **Passage-level citation**: Markup cho individual passages

## Scripts

| Script | Chức năng |
|--------|----------|
| `citemet_generator.py` | Tạo CiteMET markup |

## Khi Nào Dùng

- "citemet", "AI share button", "share to ChatGPT"
- "AI memory injection", "cite button"

## Workflow Liên Quan

- `/seo-write` — Step 5 (Validate) tạo CiteMET
- `/seo-execute` — CiteMET generation
