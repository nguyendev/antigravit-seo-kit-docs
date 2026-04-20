# Workflows — Hệ Thống Điều Phối

Workflows là **cốt lõi** của SEO Kit. Mỗi workflow kích hoạt hàng loạt kỹ năng chuyên biệt theo thứ tự tối ưu.

## Vòng Đời SEO (Lifecycle)

```
📋 ONBOARD → 🔎 RESEARCH → 🔍 AUDIT → 🧠 STRATEGY → ⚡ EXECUTE → 📈 MONITOR → (lặp lại)
```

## 13 Workflows

### Static Workflows (11) — Agent cố định

| Workflow | Agent | Mục Đích |
|----------|-------|----------|
| [`/seo-onboard`](seo-onboard.md) | `seo-strategist` | Khởi tạo, brand identity, personas |
| [`/seo-research`](seo-research.md) | `seo-strategist` | Từ khóa, audience, prompt AI, fan-out |
| [`/seo-audit`](seo-audit.md) | `seo-auditor` | Kiểm tra toàn diện website |
| [`/seo-strategy`](seo-strategy.md) | `seo-strategist` | Chiến lược, roadmap 30/60/90 |
| [`/seo-execute`](seo-execute.md) | `seo-migration-expert` | Tạo code fixes, nội dung, llms.txt |
| [`/seo-monitor`](seo-monitor.md) | `seo-data-analyst` | Giám sát, A/B test, brand sentiment |
| [`/seo-write`](seo-write.md) | `seo-content-writer` | **Content pipeline 7 bước** (radar → deploy) |
| [`/seo-page`](seo-page.md) | `seo-content-writer` | Phân tích on-page trang đơn |
| [`/seo-llm-visibility`](seo-llm-visibility.md) | `seo-ai-specialist` | GEO: SOV, fan-out, brand sentiment |
| [`/seo-social-commerce`](seo-social-commerce.md) | `seo-growth-hacker` | Zalo, TikTok, Shopee Visual Search |
| [`/seo-local-suite`](seo-local-suite.md) | `seo-local-expert` | Local SEO chuyên sâu |

### Dynamic Meta-Workflows (2) — Agent theo phase

| Workflow | Mô tả |
|----------|--------|
| [`/seo-run`](seo-run.md) | Interactive: hiển thị dashboard, đề xuất bước tiếp, chờ duyệt |
| [`/seo-auto-run`](seo-auto-run.md) | Autonomous: chuỗi tất cả phases còn lại tự động |

**Phase → Agent:**

| Phase hiện tại | Workflow tiếp | Agent |
|---------------|--------------|-------|
| *(mới)* | `/seo-onboard` | `seo-strategist` |
| `greenfield` | `/seo-research` | `seo-strategist` |
| `onboarded` | `/seo-research` hoặc `/seo-audit` | `seo-strategist` / `seo-auditor` |
| `researched` | `/seo-audit` | `seo-auditor` |
| `audited` | `/seo-strategy` | `seo-strategist` |
| `strategized` | `/seo-execute` | `seo-migration-expert` |
| `executed` | `/seo-monitor` | `seo-data-analyst` |
| `monitoring` | re-audit cycle | `seo-auditor` |

### Cross-Agent Workflow: `/seo-execute`

`/seo-execute` là workflow duy nhất kích hoạt skills từ **5 agents khác nhau**:

| Skill | Agent nguồn | Điều kiện |
|-------|-------------|-----------|
| `seo-fix`, `seo-migration` | `seo-migration-expert` | Luôn chạy / `--migration` |
| `seo-schema` | `seo-auditor` | Luôn chạy |
| `seo-content` | `seo-content-writer` | Luôn chạy |
| `seo-video`, `seo-video-transcript`, `seo-image-gen`, `seo-visual-search` | `seo-growth-hacker` | Nếu phù hợp |
| `seo-llmstxt`, `seo-citemet` | `seo-ai-specialist` | Luôn chạy |

## Nguyên Tắc

- **Suggest + Approve**: Static workflows **KHÔNG BAO GIỜ** tự thực thi. Luôn đề xuất và chờ duyệt.
- **Deep-dive không đổi phase**: `/seo-llm-visibility`, `/seo-social-commerce`, `/seo-local-suite` ghi vào `runs[]` nhưng không cập nhật `phase`.
- **Anti-Hallucination**: Mọi output gắn tag nguồn dữ liệu (`[FETCHED]`, `[VERIFIED]`, `[INFERRED]`, `[TEMPLATE]`).
