# /seo-monitor — Phase 5: Giám Sát

## Tổng Quan

Theo dõi tác động của các thay đổi SEO theo thời gian. So sánh metrics trước/sau, giám sát AI search visibility, phân tích crawl patterns, và cảnh báo regression. Phase này tạo vòng phản hồi quay lại Phase 2 (re-audit) khi cần.

## Cách Sử Dụng

```
/seo-monitor example.com --focus experiments
```

### Tham số

| Tham số | Mô tả |
|---------|-------|
| `--focus` | `experiments`, `geo`, `logs`, `traffic`, `backlinks`, `migration` |

## Kỹ Năng Kích Hoạt (tối đa 6)

| # | Kỹ năng | Vai trò | Điều kiện |
|---|---------|---------|-----------|
| 1 | `seo-test` | A/B test tracking, experiment baseline/measurement | Luôn |
| 2 | `seo-geo-monitor` | AI citability scoring, competitive GEO, platform comparison | Luôn |
| 3 | `seo-logs` | Server log analysis, crawl budget, AI bot monitoring | Nếu có log file |
| 4 | `seo-google` | GSC traffic trends, CWV changes, indexation status | Nếu có API credentials |
| 5 | `seo-backlink` | Backlink growth/loss, toxic links mới | Nếu MCP khả dụng |
| 6 | `seo-migration` | Post-migration health check, redirect chains | Nếu đang migration |

## Anti-Hallucination Checkpoint

- Xác minh baseline data TỒN TẠI trong `project.json` trước khi so sánh
- Không có baseline → ghi "Không có baseline. Đây là lần đo đầu tiên."
- KHÔNG BAO GIỜ bịa dữ liệu so sánh lịch sử
- Tag metrics: `[VERIFIED]` (từ GSC/MCP) hoặc `[FETCHED]` (từ crawl)

## So Sánh Baseline

- Load audit score trước đó từ `project.json.runs[]`
- Tính delta: hiện tại vs baseline
- Cảnh báo regression (score giảm > 5 điểm)

## Auto-Suggest Loop

| Tình huống | Gợi ý |
|-----------|-------|
| Score cải thiện | "Tiến triển tốt! Tiếp tục giám sát hoặc `/seo-strategy` tìm cơ hội mới." |
| Score giảm | "⚠️ Regression. Khuyến nghị chạy `/seo-audit` để chẩn đoán." |
| >30 ngày từ audit cuối | "Đã lâu rồi. Cân nhắc chạy `/seo-audit` mới." |

## Output

```
seo-projects/{domain-slug}/
├── reports/monitor-{date}.md
└── data/monitor-{date}.json
```
