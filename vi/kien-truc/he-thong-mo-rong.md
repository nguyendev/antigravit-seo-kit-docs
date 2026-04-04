# Hệ Thống Mở Rộng

Hướng dẫn xây dựng extension mới cho SEO Kit.

## Cấu Trúc Extension

```
extensions/{name}/
├── SKILL.md            ← Skill definition
├── mcp-config.json     ← MCP server configuration
├── scripts/            ← Python scripts (nếu có)
└── references/         ← Documentation
```

## Bước Tạo Extension

1. **Tạo thư mục** trong `extensions/`
2. **Viết SKILL.md** với YAML frontmatter
3. **Đăng ký MCP server** trong config
4. **Viết scripts** nếu cần xử lý dữ liệu
5. **Test** với một domain thực tế
6. **Đăng ký** trong `extensions/index.json`

## Provider Priority

Extension mới sẽ cần đăng ký priority level. Xem `.agent/rules/provider-priority.md`.
