# /seo-auto-run — Tự Động Hoàn Toàn

## Mục Đích

Pipeline SEO tự động hoàn toàn. Khác với `/seo-run` (hỏi xác nhận từng bước), `/seo-auto-run` chuỗi toàn bộ vòng đời trong một lần chạy. Agent tự phát hiện phase hiện tại và thực thi TẤT CẢ phases còn lại.

**Đây là tính năng cốt lõi của Agentic SEO**: thiết lập, chạy, xem kết quả.

## Cú Pháp

```
/seo-auto-run <domain> [--phases <from>-<to>] [--fix-apply] [--report-format markdown|json]
```

| Tham số | Bắt buộc | Mô tả |
|---------|:--------:|-------|
| `domain` | ✅ | Domain mục tiêu |
| `--phases` | ❌ | Giới hạn phạm vi: `audit-execute`, `research-strategy` |
| `--fix-apply` | ❌ | Tự động áp dụng fixes vào workspace |
| `--report-format` | ❌ | Định dạng output: `markdown` (mặc định) hoặc `json` |

## Agent Phụ Trách

`seo-data-analyst` — Kỹ năng: seo-google, seo-dataforseo, seo-logs, seo-test

## Quy Tắc An Toàn

1. **KHÔNG sửa production files** nếu thiếu `--fix-apply`
2. **Ghi nhật ký mọi quyết định** vào `data/auto-run-{date}.json`
3. **DỪNG** nếu Health Score giảm >10 điểm giữa các phase
4. **Giới hạn 30 phút** — nếu vượt, lưu tiến trình và báo cáo

## So Sánh Với /seo-run

| Khía cạnh | `/seo-run` | `/seo-auto-run` |
|-----------|-----------|-----------------|
| Xác nhận | Hỏi từng phase | Hoàn toàn tự động |
| Phạm vi | Phase tiếp theo | Tất cả phases còn lại |
| Decision log | Không | Bắt buộc |
| Báo cáo | Từng phase | Tổng hợp |
| Safety halt | Không | Score drop >10 = DỪNG |

## Kết Quả

```
seo-projects/{domain-slug}/
├── reports/auto-run-{date}.md    ← Báo cáo tổng hợp
└── data/auto-run-{date}.json     ← Decision log
```
