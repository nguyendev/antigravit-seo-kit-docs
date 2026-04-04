# Hệ Thống Kỹ Năng (Skills)

## Cấu Trúc Một Skill

```
.agent/skills/seo-{name}/
├── SKILL.md              ← File chính (YAML frontmatter + instructions)
├── references/           ← Tài liệu tham khảo (load khi cần)
│   └── *.md
├── scripts/              ← Python automation scripts
│   └── *.py
└── schema/               ← JSON-LD templates (nếu có)
    └── *.json
```

## SKILL.md Format

```yaml
---
name: seo-{name}
description: >
  Khi nào sử dụng skill này.
  Keywords kích hoạt và use cases.
---

# Hướng dẫn chi tiết
```

## Nguyên Tắc

1. **Progressive Disclosure**: SKILL.md ngắn gọn. Reference files tải bổ sung khi cần thiết.
2. **Self-Contained**: Mỗi skill có thể chạy độc lập, không phụ thuộc skill khác.
3. **Composable**: Workflows compose nhiều skills lại với nhau.
4. **Anti-Hallucination**: Mọi output phải tag nguồn dữ liệu (`[FETCHED]`, `[VERIFIED]`, `[INFERRED]`, `[TEMPLATE]`).

## Truy Cập

- **Qua workflow**: Tự động kích hoạt bởi lifecycle workflows
- **Trực tiếp**: "Run seo-entity for example.com" (không đổi phase)
