# Hệ Thống Workflow

## Cấu Trúc Workflow

```
.agent/workflows/seo-{name}.md
```

Mỗi workflow là file markdown với YAML frontmatter:

```yaml
---
description: "Mô tả ngắn gọn workflow"
---

# /seo-{name} <domain> [options]

## Purpose
## Skills Activated
## Steps
## Output
```

## State Machine

Workflows quản lý state qua `project.json`:

```json
{
  "domain": "example.com",
  "phase": "audited",
  "health_score": 72,
  "phase_history": [
    {"phase": "onboarded", "date": "2025-03-01", "run_id": "r001"},
    {"phase": "audited", "date": "2025-03-02", "run_id": "r002"}
  ],
  "runs": [...]
}
```

## Suggest + Approve

Workflows **KHÔNG BAO GIỜ** tự thực thi. Luồng:

1. AI phân tích trạng thái hiện tại
2. Hiển thị dashboard
3. Đề xuất bước tiếp theo
4. **Chờ duyệt** từ người dùng
5. Thực thi sau khi được duyệt

## Danh Sách

| Workflow | File | Phase |
|----------|------|-------|
| `/seo-run` | `seo-run.md` | Master |
| `/seo-onboard` | `seo-onboard.md` | Phase 1 |
| `/seo-research` | `seo-research.md` | Research |
| `/seo-audit` | `seo-audit.md` | Phase 2 |
| `/seo-strategy` | `seo-strategy.md` | Phase 3 |
| `/seo-execute` | `seo-execute.md` | Phase 4 |
| `/seo-monitor` | `seo-monitor.md` | Phase 5 |
| `/seo-local-suite` | `seo-local-suite.md` | Đặc biệt |
| `/seo-page` | `seo-page.md` | Tiện ích |
