# Hệ Thống Workflow

Workflows là orchestrators kích hoạt nhiều skills theo thứ tự tối ưu. SEO Kit có **12 workflows**: 10 static + 2 dynamic meta-workflows.

## Vòng Đời

```
ONBOARD → RESEARCH → AUDIT → STRATEGY → EXECUTE → MONITOR → (lặp lại)
```

## Phân Loại

### Static Workflows (10)

Agent được gán cố định cho mỗi workflow. Khi gọi `/seo-audit`, luôn load `seo-auditor`.

### Dynamic Meta-Workflows (2)

`/seo-run` và `/seo-auto-run` chọn agent dựa trên phase hiện tại của project:

| Phase | Workflow tiếp | Agent |
|-------|--------------|-------|
| *(mới)* | `/seo-onboard` | `seo-strategist` |
| `onboarded` | `/seo-research` | `seo-strategist` |
| `researched` | `/seo-audit` | `seo-auditor` |
| `audited` | `/seo-strategy` | `seo-strategist` |
| `strategized` | `/seo-execute` | `seo-migration-expert` |
| `executed` | `/seo-monitor` | `seo-data-analyst` |
| `monitoring` | re-audit cycle | `seo-auditor` |

### Cross-Agent Workflow

`/seo-execute` là workflow duy nhất kích hoạt skills từ 5 agents khác nhau (migration-expert, auditor, content-writer, growth-hacker, ai-specialist).

## Nguyên tắc

- **Suggest + Approve**: Static workflows không tự thực thi, luôn chờ duyệt
- **Autonomous mode**: `/seo-auto-run` chạy toàn bộ pipeline tự động, HALT nếu score giảm >10
- **Phase tracking**: Lifecycle workflows cập nhật `phase` trong `project.json`
- **Deep-dives không đổi phase**: `/seo-llm-visibility`, `/seo-social-commerce`, `/seo-local-suite` ghi vào `runs[]` nhưng không cập nhật `phase`
- **Anti-hallucination**: Mọi output gắn tag nguồn (`[FETCHED]`, `[VERIFIED]`, `[INFERRED]`, `[TEMPLATE]`)
