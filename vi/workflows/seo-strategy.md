# /seo-strategy — Phase 3: Chiến Lược

## Tổng Quan

Dựa trên kết quả audit Phase 2, đi sâu vào bối cảnh cạnh tranh và hệ sinh thái nội dung. Xác định khoảng trống, mapping topical authority, phân tích entity, và tạo roadmap 30/60/90 ngày ưu tiên.

## Cách Sử Dụng

```
/seo-strategy example.com competitor1.com competitor2.com --focus all
```

### Tham số

| Tham số | Mô tả |
|---------|-------|
| `competitor1`, `competitor2` | Domain đối thủ (tùy chọn, tự phát hiện nếu có MCP) |
| `--focus` | `content`, `authority`, `ai`, `backlink`, hoặc `all` |

## Điều Kiện Tiên Quyết

- **Khuyến nghị**: Chạy `/seo-audit` trước (Phase 2) cho dữ liệu chẩn đoán
- **Tùy chọn**: Dữ liệu `/seo-research` enriches keyword gaps
- Không có audit data → cảnh báo nhưng cho phép chạy

## Kỹ Năng Kích Hoạt (tối đa 10)

| # | Kỹ năng | Vai trò | Điều kiện |
|---|---------|---------|-----------|
| 1 | `seo-content-gap` | Keywords thiếu, cannibalization, topical gaps vs đối thủ | Luôn |
| 2 | `seo-topical-authority` | Internal link graph, content clusters, pillar gaps | Luôn |
| 3 | `seo-entity` | Entity NER, salience, Knowledge Graph readiness | Luôn |
| 4 | `seo-authority` | Cross-platform presence, topical depth | Luôn |
| 5 | `seo-competitor-pages` | Phân tích trang đối thủ, comparison templates | Luôn |
| 6 | `seo-backlink` | Backlink profile, toxic links, competitor link gap | Luôn |
| 7 | `seo-answer` | AI answer eligibility, passage scoring | Luôn |
| 8 | `seo-agentic` | Action schema, API discoverability, A2A readiness | Luôn |
| 9 | `seo-programmatic` | Cơ hội programmatic SEO, template strategies | Nếu phù hợp |
| 10 | `seo-plan` | Tổng hợp thành roadmap 30/60/90 ngày | Luôn |

## Các Bước Thực Hiện

1. Load domain project
2. Phát hiện MCP providers (Ahrefs, Semrush, DataForSEO)
3. Xử lý đối thủ (từ input, cached, auto-discover, hoặc hỏi user)
4. Cross-reference research data (nếu có)
5. Chạy content gap analysis
6. Chạy topical authority analysis
7. Chạy entity analysis
8. Chạy authority mapping
9. Chạy competitor page analysis
10. Chạy backlink analysis
11. Chạy AI answer readiness
12. Chạy agentic SEO audit
13. Đánh giá cơ hội pSEO
14. **Tổng hợp roadmap 30/60/90 ngày** (ưu tiên impact × effort)
15. Lưu outputs, set `phase: "strategized"`

## Output

```
seo-projects/{domain-slug}/
├── reports/
│   ├── strategy-{date}.md
│   └── roadmap-{date}.md
└── data/
    ├── content-gap-{date}.json
    ├── cluster-map-{date}.json
    └── backlink-{date}.json
```
