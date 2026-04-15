# Hệ Thống Kỹ Năng

Mỗi kỹ năng là một thư mục trong `.agent/skills/` chứa SKILL.md và scripts.

## Cấu trúc

```
.agent/skills/seo-{name}/
├── SKILL.md           # Hướng dẫn chi tiết cho AI
├── scripts/           # Python scripts thực thi
└── assets/            # Templates, data mẫu
```

## Thống Kê

| Metric | Giá trị |
|--------|---------|
| **Unique skills** | 44 |
| **With shared** | 47 (3 skills chia sẻ giữa agents) |
| **Orphan skills** | 0 ✅ |
| **Agent:Skill ratio** | 1:5.5 |

## Shared Skills (3)

3 skills được chia sẻ giữa 2 agents — cùng skill nhưng mục đích khác nhau:

| Skill | Agent A | Agent B |
|-------|---------|---------|
| `seo-content` | `seo-auditor` (chấm điểm) | `seo-content-writer` (tạo mới) |
| `seo-source-context` | `seo-auditor` (kiểm tra) | `seo-content-writer` (xây dựng) |
| `seo-geo` | `seo-auditor` (citability check) | `seo-ai-specialist` (GEO strategy) |

## Cách Hoạt Động

1. Workflow đọc `SKILL.md` để hiểu kỹ năng
2. AI agent thực thi theo instructions
3. Scripts hỗ trợ tính toán và phân tích
4. Kết quả lưu vào domain project folder

## Xem Thêm

- [44 kỹ năng chi tiết](../ky-nang/index.md)
- [Hệ thống Agent](he-thong-agent.md) — mapping skills → agents
