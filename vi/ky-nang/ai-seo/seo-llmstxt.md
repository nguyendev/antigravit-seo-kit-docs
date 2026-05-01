# seo-llmstxt — LLMs.txt Generator

## Mô Tả

Tạo và tối ưu file `llms.txt` — tiêu chuẩn cho AI bots hiểu cấu trúc website. Machine-readable site map cho AI crawlers.

## Agent Phụ Trách

`seo-ai-search` (skill #4/7)

## Chức Năng Chính

- **llms.txt generation**: Tạo file llms.txt theo chuẩn LLMO
- **llms-full.txt**: Phiên bản đầy đủ với nội dung chi tiết
- **Knowledge map**: Site-wide topic map cho AI consumption
- **Auto-update**: Cập nhật khi sitemap thay đổi
- **AI crawler optimization**: Đảm bảo AI bots parse đúng

## Scripts

| Script | Chức năng |
|--------|----------|
| `llmstxt_generator.py` | Tạo llms.txt + llms-full.txt |

## Khi Nào Dùng

- "llms.txt", "AI bot optimization", "AI indexing"
- "AI crawler access", "machine readable site map"

## Workflow Liên Quan

- `/seo-write` — Step 5 (Validate) tạo llms.txt
- `/seo-llm-visibility --focus llmstxt`
- `/seo-execute` — Tạo llms.txt trong execute phase
