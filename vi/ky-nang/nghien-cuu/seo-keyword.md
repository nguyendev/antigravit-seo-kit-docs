# seo-keyword — Nghiên Cứu Từ Khóa

## Mô Tả

Nghiên cứu từ khóa toàn diện: search volume, keyword difficulty, intent classification, keyword clustering, long-tail opportunities.

## Agent Phụ Trách

`seo-content-authority` (skill #2/6)

## Chức Năng Chính

- **Keyword research**: Phát hiện từ khóa tiềm năng
- **Intent classification**: Informational, commercial, transactional, navigational
- **Keyword clustering**: Nhóm keywords theo intent và topic
- **Difficulty analysis**: Đánh giá độ khó xếp hạng
- **Long-tail discovery**: Tìm cơ hội từ khóa dài

## Dữ Liệu Keyword

| Dữ liệu | Nguồn | Ghi chú |
|----------|-------|---------|
| Search volume | [Solann API](../../mo-rong/solann-api.md) (mặc định) | Premium Google Ads data |
| Keyword difficulty | Solann API | Competition index 0-100 |
| CPC data | Solann API | Low + high bid |
| 12-month trends | Solann API | Seasonality analysis |
| Long-tail expansion | Solann API | Autocomplete + Alphabet Soup |

> 💡 Solann API là data provider mặc định (#1). Nếu chưa cấu hình, hệ thống fall back sang HTML-only mode.

## Khi Nào Dùng

- "keyword research", "từ khóa", "search volume"
- "keyword difficulty", "keyword cluster", "intent"

## Workflow Liên Quan

- `/seo-research` — Nghiên cứu từ khóa chuyên sâu
- `/seo-strategy` — Keyword strategy trong chiến lược
