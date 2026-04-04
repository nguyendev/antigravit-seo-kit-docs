# Kiến Trúc

Antigravity SEO Kit tuân theo kiến trúc Agent Skills tiêu chuẩn mở gồm 3 lớp:

```
┌─────────────────────────────────────────┐
│         DIRECTIVE LAYER                  │
│  agent.md, GEMINI.md                    │
│  Quy tắc, hành vi, routing             │
├─────────────────────────────────────────┤
│         ORCHESTRATION LAYER              │
│  workflows/ (seo-run, seo-audit, ...)   │
│  Điều phối các kỹ năng                  │
├─────────────────────────────────────────┤
│         EXECUTION LAYER                  │
│  skills/ (seo-technical, seo-geo, ...)  │
│  Kỹ năng chuyên biệt + scripts         │
└─────────────────────────────────────────┘
```

## Tài Liệu Chi Tiết

| Chủ đề | Mô tả |
|--------|-------|
| [Hệ thống kỹ năng](he-thong-ky-nang.md) | Cách skills hoạt động, cấu trúc SKILL.md |
| [Hệ thống workflow](he-thong-workflow.md) | Cách workflows điều phối skills |
| [Không gian dự án](khong-gian-du-an.md) | Domain workspaces, project.json |
| [Tích hợp MCP](tich-hop-mcp.md) | Model Context Protocol, extensions |
| [Hệ thống mở rộng](he-thong-mo-rong.md) | Cách xây dựng extension mới |
