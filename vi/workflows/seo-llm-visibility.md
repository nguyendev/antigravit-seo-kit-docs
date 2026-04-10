# /seo-llm-visibility — GEO: AI Search Visibility

Workflow deep-dive chuyên về Generative Engine Optimization. Đo AI SOV, dự đoán RAG queries, phát hiện brand sentiment bias.

## Cách sử dụng

```
/seo-llm-visibility yourdomain.com --focus all
```

## Kỹ Năng Kích Hoạt (5)

| Kỹ năng | Vai trò |
|---------|---------|
| `seo-geo-monitor` | Đo Share of Voice (SOV) trên ChatGPT, Claude, Gemini, Perplexity |
| `seo-brand-sentiment` | Phát hiện negative sentiment, LLM bias |
| `seo-fan-out-generator` | Dự đoán RAG sub-queries |
| `seo-llmstxt` | Generate `/llms.txt` cho AI bots |
| `seo-citemet` | AI Share Buttons (inject vào AI memory) |

> **Deep-dive**: Workflow này KHÔNG thay đổi project `phase`. Ghi vào `runs[]` với `type: "geo-visibility"`.

## Khi nào sử dụng

- Muốn biết AI Search engines có biết brand của bạn không
- Kiểm tra brand bị bias tiêu cực trong AI outputs
- Chuẩn bị nội dung cho AI citation
