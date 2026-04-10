# Hệ Thống Kỹ Năng

Mỗi kỹ năng là một thư mục trong `.agent/skills/` chứa SKILL.md và scripts.

## Cấu trúc

```
.agent/skills/seo-{name}/
├── SKILL.md           # Hướng dẫn chi tiết cho AI
├── scripts/           # Python scripts thực thi
└── assets/            # Templates, data mẫu
```

## Cách hoạt động

1. Workflow đọc `SKILL.md` để hiểu kỹ năng
2. AI agent thực thi theo instructions
3. Scripts hỗ trợ tính toán và phân tích
4. Kết quả lưu vào domain project folder
