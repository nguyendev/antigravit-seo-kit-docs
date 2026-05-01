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
| **Unique skills** | 42 |
| **With shared** | 53 (5 skills chia sẻ giữa agents) |
| **Orphan skills** | 0 ✅ |
| **Skills with scripts** | 40 / 42 |
| **Executable scripts** | 78 |
| **Instruction-only** | 6 (`seo-audit`, `seo-competitor-pages`, `seo-dataforseo`, `seo-local`, `seo-maps`, `seo-plan`) |
| **Agent:Skill ratio** | 1:5.1 |

## Shared Skills (5)

5 skills được chia sẻ giữa agents — cùng skill nhưng mục đích khác nhau:

| Skill | Agents | Mục đích |
|-------|--------|---------|
| `seo-content` | `seo-technical-architect` (scoring) | `seo-content-authority` (strategy) |
| `seo-solann` | `seo-content-authority` (strategy volume) | `seo-intelligence` (monitoring) | `seo-data-provider` (data access) |
| `seo-google` | `seo-intelligence` (analytics) | `seo-data-provider` (data access) |
| `seo-dataforseo` | `seo-intelligence` (analysis) | `seo-data-provider` (data access) |
| `seo-information-gain` | `seo-content-authority` (pre-creation IG strategy) | `seo-creator` (post-creation IG validation) |

## Cách Hoạt Động

1. Workflow đọc `SKILL.md` để hiểu kỹ năng
2. AI agent thực thi theo instructions
3. Scripts hỗ trợ tính toán và phân tích
4. Kết quả lưu vào domain project folder

## Xem Thêm

- [42 kỹ năng chi tiết](../ky-nang/index.md)
- [Hệ thống Agent](he-thong-agent.md) — mapping skills → agents
