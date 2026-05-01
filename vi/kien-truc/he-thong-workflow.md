# Hệ Thống Workflow

Workflows là orchestrators kích hoạt nhiều skills theo thứ tự tối ưu. SEO Kit có **13 workflows**: 11 static + 2 dynamic meta-workflows.

## Vòng Đời

```
ONBOARD → RESEARCH → AUDIT → STRATEGY → EXECUTE → MONITOR → (lặp lại)
```

## Phân Loại

### Static Workflows (11)

Agent được gán cố định cho mỗi workflow. Khi gọi `/seo-audit`, luôn load `seo-technical-architect`.

### Dynamic Meta-Workflows (2)

`/seo-run` và `/seo-auto-run` chọn agent dựa trên phase hiện tại của project:

| Phase | Workflow tiếp | Agent |
|-------|--------------|-------|
| *(mới)* | `/seo-onboard` | `seo-content-authority` |
| `onboarded` | `/seo-research` | `seo-content-authority` |
| `researched` | `/seo-audit` | `seo-technical-architect` |
| `audited` | `/seo-strategy` | `seo-content-authority` |
| `strategized` | `/seo-execute` | `seo-technical-architect` |
| `executed` | `/seo-monitor` | `seo-intelligence` |
| `monitoring` | re-audit cycle | `seo-technical-architect` |

### Cross-Agent Workflow

`/seo-execute` là workflow duy nhất kích hoạt skills từ nhiều agents khác nhau (`seo-technical-architect`, `seo-content-authority`, `seo-multimedia`, `seo-ai-search`).

## Nguyên tắc

- **Suggest + Approve**: Static workflows không tự thực thi, luôn chờ duyệt
- **Autonomous mode**: `/seo-auto-run` chạy toàn bộ pipeline tự động, HALT nếu score giảm >10
- **Phase tracking**: Lifecycle workflows cập nhật `phase` trong `project.json`
- **Deep-dives không đổi phase**: `/seo-llm-visibility`, `/seo-social-commerce`, `/seo-local-suite` ghi vào `runs[]` nhưng không cập nhật `phase`
- **Anti-hallucination**: Mọi output gắn tag nguồn (`[FETCHED]`, `[VERIFIED]`, `[INFERRED]`, `[TEMPLATE]`)
