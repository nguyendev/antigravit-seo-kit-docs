# Workflows — Hệ Thống Điều Phối

Workflows là **cốt lõi** của SEO Kit. Mỗi workflow kích hoạt hàng loạt kỹ năng chuyên biệt theo thứ tự tối ưu.

## Vòng Đời SEO (Lifecycle)

```
📋 ONBOARD → 🔎 RESEARCH → 🔍 AUDIT → 🧠 STRATEGY → ⚡ EXECUTE → 📈 MONITOR → (lặp lại)
```

## 11 Workflows

### Lifecycle (7)

| Workflow | Phase | Skills | Mục Đích |
|----------|-------|--------|----------|
| [`/seo-run`](seo-run.md) | Master | — | Tự phát hiện phase, đề xuất bước tiếp |
| [`/seo-onboard`](seo-onboard.md) | Phase 1 | 4 | Khởi tạo, brand identity, personas |
| [`/seo-research`](seo-research.md) | Research | 6 | Từ khóa, audience, prompt AI, fan-out |
| [`/seo-audit`](seo-audit.md) | Phase 2 | 9 | Kiểm tra toàn diện website |
| [`/seo-strategy`](seo-strategy.md) | Phase 3 | 12 | Chiến lược, roadmap 30/60/90 |
| [`/seo-execute`](seo-execute.md) | Phase 4 | 10 | Tạo code fixes, nội dung, llms.txt |
| [`/seo-monitor`](seo-monitor.md) | Phase 5 | 8 | Giám sát, A/B test, brand sentiment |

### Deep-dive & Tiện ích (4)

| Workflow | Loại | Skills | Mục Đích |
|----------|------|--------|----------|
| [`/seo-llm-visibility`](seo-llm-visibility.md) | Deep-dive | 5 | GEO: SOV, fan-out, brand sentiment, llms.txt |
| [`/seo-social-commerce`](seo-social-commerce.md) | Deep-dive | 4 | Zalo, TikTok, Shopee Visual Search |
| [`/seo-local-suite`](seo-local-suite.md) | Deep-dive | 2 | Local SEO chuyên sâu |
| [`/seo-page`](seo-page.md) | Tiện ích | 4 | Phân tích on-page trang đơn |

## Nguyên Tắc

- **Suggest + Approve**: Workflows **KHÔNG BAO GIỜ** tự thực thi. Luôn đề xuất và chờ duyệt.
- **Deep-dive không đổi phase**: `/seo-llm-visibility`, `/seo-social-commerce`, `/seo-local-suite` ghi vào `runs[]` nhưng không cập nhật `phase`.
- **Anti-Hallucination**: Mọi output gắn tag nguồn dữ liệu (`[FETCHED]`, `[VERIFIED]`, `[INFERRED]`, `[TEMPLATE]`).
