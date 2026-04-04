# Kỹ Năng (Skills)

SEO Kit bao gồm **35 kỹ năng chuyên biệt**, mỗi kỹ năng là một file `SKILL.md` với YAML frontmatter định nghĩa khả năng và hướng dẫn. Các kỹ năng được tổ chức thành 7 nhóm.

## 7 Nhóm Kỹ Năng

| Nhóm | Kỹ năng | Mô tả |
|------|---------|-------|
| [Technical SEO](ky-thuat) | 5 | Crawlability, CWV, sitemap, images, hreflang |
| [Content SEO](noi-dung) | 4 | E-E-A-T, content gap, topical authority, entity |
| [AI & GEO](ai-seo) | 5 | GEO, AI answer, geo-monitor, agentic, prompt research |
| [Nghiên Cứu](nghien-cuu) | 4 | Keyword, audience, source context, competitors |
| [Off-Page](off-page) | 3 | Backlink, authority, local SEO |
| [Thực Thi](thuc-thi) | 5 | Fix, schema, migration, programmatic, video |
| [Giám Sát](giam-sat) | 4 | Test, logs, Google APIs, Maps |

**Tổng: 30 kỹ năng chính** + 5 bổ sung (seo orchestrator, dataforseo, image-gen, plan, source-context)

## Cách Hoạt Động

Mỗi skill có cấu trúc:

```yaml
---
name: skill-name
description: >
  Khi nào sử dụng skill này. Keywords kích hoạt và use cases cụ thể.
---

# Tên Skill

Hướng dẫn và tài liệu...
```

## Truy Cập Trực Tiếp

Gọi bất kỳ skill nào trực tiếp:

```
"Run seo-entity for example.com"
```

Không cần đi qua workflow. Truy cập trực tiếp KHÔNG thay đổi phase dự án.
