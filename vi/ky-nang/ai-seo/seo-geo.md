# seo-geo — Tối Ưu AI Search (GEO)

## Mô Tả

Generative Engine Optimization: tối ưu cho AI search (Google AI Overviews, ChatGPT, Perplexity), AI crawler access, passage-level citability, brand mention signals.

## Agent Phụ Trách

`seo-technical-architect` (citability check) + `seo-ai-search` (GEO strategy) — **shared skill**

## Chức Năng Chính

- **AI crawler detection**: GPTBot, ClaudeBot, PerplexityBot, OAI-SearchBot
- **llms.txt detection**: Kiểm tra có file llms.txt không
- **Passage-level citability**: Tối ưu 134-167 words per passage
- **Brand mention signals**: 3x quan trọng hơn backlinks cho AI visibility
- **Platform-specific scoring**: Google AI Overviews vs ChatGPT vs Perplexity
- **SSR check**: Kiểm tra AI crawler có đọc được content không

## Scripts

| Script | Chức năng |
|--------|----------|
| `geo_auditor.py` | GEO audit toàn diện |

## Khi Nào Dùng

- "GEO", "AI search", "AI visibility", "AI overview"
- "AI crawler", "citability", "llm optimization"

## Workflow Liên Quan

- `/seo-audit` — GEO check trong audit
- `/seo-llm-visibility` — Deep-dive GEO analysis
