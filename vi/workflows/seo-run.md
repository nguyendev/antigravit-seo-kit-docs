# /seo-run — Master Orchestrator

Lệnh duy nhất bạn cần nhớ. Tự phát hiện giai đoạn hiện tại và đề xuất bước tiếp.

## Cách sử dụng

```
/seo-run yourdomain.com
```

## State Machine

| Trạng thái | Đề xuất |
|------------|---------|
| Chưa có project | → `/seo-onboard` |
| `greenfield` (domain chưa live) | → `/seo-research` hoặc `/seo-strategy` |
| `onboarded` | → `/seo-research` (hoặc `/seo-audit` nếu bỏ qua) |
| `researched` | → `/seo-audit` |
| `audited` | → `/seo-strategy` |
| `strategized` | → `/seo-execute` |
| `executed` | → `/seo-monitor` |
| `monitoring` | → Dashboard + đề xuất re-audit |

## Routing Thông Minh (2026)

Nếu user đề cập **AI Search / ChatGPT / GEO** → route sang `/seo-llm-visibility`.

Nếu user đề cập **Zalo / TikTok / Shopee** → route sang `/seo-social-commerce`.

## Quy tắc

- **KHÔNG BAO GIỜ** tự chạy phase mà chưa được duyệt
- Luôn hiển thị dashboard trạng thái trước khi đề xuất
- User có thể nhảy sang phase bất kỳ bằng lệnh trực tiếp
