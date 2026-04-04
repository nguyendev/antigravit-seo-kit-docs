# /seo-research — Nghiên Cứu SEO Toàn Diện

## Tổng Quan

Nghiên cứu SEO toàn diện kết hợp phân tích đối tượng, khám phá từ khóa, phân tích mẫu prompt AI, và xác định khoảng trống nội dung. Có thể chạy độc lập hoặc chuẩn bị cho Phase 3 (`/seo-strategy`).

## Cách Sử Dụng

```
/seo-research example.com --seed "seo tools,seo audit" --focus all
```

### Tham số

| Tham số | Mô tả | Mặc định |
|---------|-------|----------|
| `--seed` | Từ khóa hạt giống, phân cách bằng dấu phẩy | Tự trích xuất từ homepage |
| `--focus` | Lĩnh vực tập trung: `keyword`, `audience`, `prompt`, `all` | `all` |

## Kỹ Năng Kích Hoạt (tối đa 5)

| # | Kỹ năng | Vai trò | Điều kiện |
|---|---------|---------|-----------|
| 1 | `seo-audience` | Định nghĩa persona, journey mapping, community mining | Luôn |
| 2 | `seo-keyword` | Mở rộng seed, volume/difficulty, intent, clustering | Luôn |
| 3 | `seo-prompt-research` | Mẫu query AI, conversational mining, prompt chains | `--focus prompt` hoặc `all` |
| 4 | `seo-content-gap` | Cross-reference từ khóa vs competitor coverage | Luôn |
| 5 | `seo-dataforseo` | Enrichment dữ liệu trực tiếp (volume, difficulty, SERP) | Nếu MCP khả dụng |

## Các Bước Thực Hiện

1. **Load domain project** — Nếu có project → load project.json; nếu mới → tạo minimal
2. **Phát hiện MCP providers** — Kiểm tra DataForSEO, Ahrefs, Semrush
3. **Xử lý seed keywords**: Từ `--seed`, từ industry trong project.json, hoặc từ homepage meta tags
4. **Phân tích audience** → 2-4 personas + journey maps
5. **Nghiên cứu từ khóa** → 500+ keywords, phân loại intent, clustering
6. **Nghiên cứu prompt** (nếu focus bao gồm) → Mẫu prompt AI, multi-turn chains
7. **Phân tích content gap** → Cross-reference keywords vs nội dung hiện có
8. **Verification checkpoint** (anti-hallucination):
   - Trình bày draft personas: "Draft personas dưới đây. Chính xác không?"
   - Trình bày top 20 keywords: "Xác nhận?"
   - Tag: `[FETCHED]`, `[VERIFIED]`, `[INFERRED]`, hoặc `[TEMPLATE]`
9. **Tổng hợp** → Keyword targeting plan, map keywords → personas → journey stages
10. **Lưu outputs** và cập nhật `phase: "researched"`

## Output

```
seo-projects/{domain-slug}/
├── reports/research-{date}.md
└── data/
    ├── audience-{date}.json
    ├── keywords-{date}.json
    ├── clusters-{date}.json
    └── prompt-patterns-{date}.json
```
