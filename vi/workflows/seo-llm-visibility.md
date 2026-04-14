# /seo-llm-visibility — Tối Ưu AI Search

## Mục Đích

Deep-dive workflow cho GEO (Generative Engine Optimization). Đo lường Share of Voice (SOV) trong AI search, dự đoán RAG queries, tối ưu cho AI citations.

> 📌 Đây là deep-dive workflow — KHÔNG thay đổi phase dự án.

## Cú Pháp

```
/seo-llm-visibility <domain> [--focus sov|fanout|sentiment|llmstxt|citemet|all]
```

## Agent Phụ Trách

`seo-ai-specialist` — 6 kỹ năng GEO/AI

## Kỹ Năng Kích Hoạt (5)

| # | Kỹ năng | Vai trò | Điều kiện |
|---|---------|---------|-----------|
| 1 | `seo-geo-monitor` | Đo SOV và Citability | Luôn chạy |
| 2 | `seo-brand-sentiment` | Phát hiện sentiment bias trong AI | Luôn chạy |
| 3 | `seo-fan-out-generator` | Dự đoán RAG sub-queries | Luôn chạy |
| 4 | `seo-llmstxt` | Tạo llms.txt cho AI bots | `--focus llmstxt` hoặc `all` |
| 5 | `seo-citemet` | Tích hợp AI Share Buttons | `--focus citemet` hoặc `all` |

## Các Bước

1. Load project context (semantic anchor, competitors)
2. Đo baseline visibility trên ChatGPT, Claude, Gemini, Perplexity
3. Dự đoán AI intent qua fan-out prediction
4. Phát hiện brand sentiment bias
5. Tạo llms.txt (nếu yêu cầu)
6. Tích hợp CiteMET buttons (nếu yêu cầu)
7. Verification checkpoint
8. Lưu báo cáo + đề xuất bước tiếp

## Kết Quả

```
seo-projects/{domain-slug}/
├── reports/geo-visibility-{date}.md
└── data/geo-visibility-{date}.json
```

## Gợi Ý Tiếp

- SOV thấp → `/seo-strategy --focus ai`
- Sentiment tiêu cực → Ưu tiên xử lý uy tín thương hiệu
- OK → Giám sát định kỳ với `/seo-monitor --focus geo`
