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
| [`/seo-onboard`](seo-onboard.md) | `seo-content-authority` | Khởi tạo, brand identity, personas |
| [`/seo-research`](seo-research.md) | `seo-content-authority` | Từ khóa, audience, prompt AI, fan-out |
| [`/seo-audit`](seo-audit.md) | `seo-technical-architect` | Kiểm tra toàn diện website |
| [`/seo-strategy`](seo-strategy.md) | `seo-content-authority` | Chiến lược, roadmap 30/60/90 |
| [`/seo-execute`](seo-execute.md) | `seo-technical-architect` | Tạo code fixes, nội dung, llms.txt |
| [`/seo-monitor`](seo-monitor.md) | `seo-intelligence` | Giám sát, A/B test, brand sentiment |
| [`/seo-write`](seo-write.md) | `seo-creator` | **Content pipeline 5 bước** (research → deploy) |
| [`/seo-page`](seo-page.md) | `seo-creator` | Phân tích on-page trang đơn |
| [`/seo-llm-visibility`](seo-llm-visibility.md) | `seo-ai-search` | GEO: SOV, fan-out, brand sentiment |
| [`/seo-social-commerce`](seo-social-commerce.md) | `seo-multimedia` | Zalo, TikTok, Shopee Visual Search |
| [`/seo-local-suite`](seo-local-suite.md) | `seo-local-commerce` | Local SEO chuyên sâu |

### Dynamic Meta-Workflows (2) — Agent theo phase

| Workflow | Mô tả |
|----------|--------|
| [`/seo-run`](seo-run.md) | Interactive: hiển thị dashboard, đề xuất bước tiếp, chờ duyệt |
| [`/seo-auto-run`](seo-auto-run.md) | Autonomous: chuỗi tất cả phases còn lại tự động |

**Phase → Agent:**

| Phase hiện tại | Workflow tiếp | Agent |
|---------------|--------------|-------|
| *(mới)* | `/seo-onboard` | `seo-content-authority` |
| `greenfield` | `/seo-research` | `seo-content-authority` |
| `onboarded` | `/seo-research` hoặc `/seo-audit` | `seo-content-authority` / `seo-technical-architect` |
| `researched` | `/seo-audit` | `seo-technical-architect` |
| `audited` | `/seo-strategy` | `seo-content-authority` |
| `strategized` | `/seo-execute` | `seo-technical-architect` |
| `executed` | `/seo-monitor` | `seo-intelligence` |
| `monitoring` | re-audit cycle | `seo-technical-architect` |

### Cross-Agent Workflow: `/seo-execute`

`/seo-execute` là workflow duy nhất kích hoạt skills từ **5 agents khác nhau**:

| Skill | Agent nguồn | Điều kiện |
|-------|-------------|-----------|
| `seo-fix`, `seo-migration` | `seo-technical-architect` | Luôn chạy / `--migration` |
| `seo-schema` | `seo-technical-architect` | Luôn chạy |
| `seo-content` | `seo-content-authority` | Luôn chạy |
| `seo-video`, `seo-image-gen`, `seo-visual-search` | `seo-multimedia` | Nếu phù hợp |
| `seo-llm-signals` | `seo-ai-search` | Luôn chạy |

## Nguyên Tắc

- **Suggest + Approve**: Static workflows **KHÔNG BAO GIỜ** tự thực thi. Luôn đề xuất và chờ duyệt.
- **Deep-dive không đổi phase**: `/seo-llm-visibility`, `/seo-social-commerce`, `/seo-local-suite` ghi vào `runs[]` nhưng không cập nhật `phase`.
- **Anti-Hallucination**: Mọi output gắn tag nguồn dữ liệu (`[FETCHED]`, `[VERIFIED]`, `[INFERRED]`, `[TEMPLATE]`).
