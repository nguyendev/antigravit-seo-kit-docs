# seo-schema — Schema Markup & Structured Data

## Mô Tả

Tạo và kiểm tra Schema.org markup: JSON-LD generation, rich snippet targeting, schema validation, Schema.org v29.4+ compliance.

## Agent Phụ Trách

`seo-technical-architect` (skill #5/10)

## Chức Năng Chính

- **Schema generation**: Tạo JSON-LD cho Article, FAQPage, HowTo, Product, etc.
- **Schema validation**: Kiểm tra syntax và compliance
- **Rich snippet targeting**: Tối ưu cho rich results
- **Missing schema detection**: Phát hiện schema cần thêm
- **Schema.org v29.4+**: Hỗ trợ phiên bản mới nhất

## Scripts

| Script | Chức năng |
|--------|----------|
| `schema_auditor.py` | Schema audit + generation |

## Khi Nào Dùng

- "schema markup", "structured data", "JSON-LD"
- "rich snippet", "schema.org", "schema generation"

## Workflow Liên Quan

- `/seo-audit` — Schema check trong audit
- `/seo-write` — Schema generation trong Step 2 (Outline)
- `/seo-execute` — Schema fixes
