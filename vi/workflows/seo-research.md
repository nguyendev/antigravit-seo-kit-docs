# /seo-research — Nghiên Cứu

Nghiên cứu từ khóa, audience, prompt AI, fan-out queries, content gap.

## Cách sử dụng

```
/seo-research yourdomain.com --seed "từ khóa 1, từ khóa 2" --focus all
```

## Kỹ Năng Kích Hoạt (6)

| Kỹ năng | Vai trò |
|---------|---------|
| `seo-audience` | Personas, journey mapping, community mining |
| `seo-keyword` | Seed expansion, volume/difficulty, intent, clustering |
| `seo-prompt-research` | AI query patterns, multi-turn chains |
| `seo-fan-out-generator` | Dự đoán sub-queries RAG của LLM (10-20 hidden queries) |
| `seo-content-gap` | Cross-reference vs đối thủ |
| `seo-dataforseo` | Live data enrichment (v2+) |

## Tương thích Greenfield

Research hoạt động với domain chưa publish — sử dụng `project.json` thay vì crawl data.

## Kết quả

- Keywords JSON, Clusters JSON, Prompt patterns JSON
- Audience personas + Fan-out queries
- Phase: `researched`
