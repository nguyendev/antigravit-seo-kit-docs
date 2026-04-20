# seo-fan-out-generator — RAG Sub-queries

## Mô Tả

Phân tách queries thành RAG sub-queries: dự đoán cách AI retrieval systems decompose câu hỏi, tìm content gaps cho AI search.

## Agent Phụ Trách

`seo-content-writer` (skill #7/7)

## Chức Năng Chính

- **Fan-out decomposition**: Tách query chính thành sub-queries
- **RAG prediction**: Dự đoán retrieval paths của AI
- **AI content gaps**: Phát hiện sub-topics AI không tìm thấy
- **Zero-click intent mapping**: Map intent cho câu hỏi không cần click
- **Query tree generation**: Tạo cây queries phân cấp

## Scripts

| Script | Chức năng |
|--------|----------|
| `fan_out_generator.py` | Query decomposition engine |

## Khi Nào Dùng

- "RAG queries", "sub-queries", "fan out"
- "AI content gaps", "query decomposition"

## Workflow Liên Quan

- `/seo-write` — Step 1 (Research) fan-out analysis
- `/seo-llm-visibility` — Fan-out prediction
