# Quy Tắc Vận Hành (7 Rules)

SEO Kit có 7 quy tắc luôn-bật, đảm bảo chất lượng đầu ra và an toàn dữ liệu.

## Danh Sách Quy Tắc

| Rule | Mục đích | Phạm vi |
|------|---------|---------|
| `seo-auto-routing` | Tự phát hiện domain, chọn agent, phân biệt skill | Luôn bật |
| `seo-anti-hallucination` | Cấm bịa dữ liệu, bắt buộc tag nguồn | Luôn bật |
| `seo-domain-project` | Cấu trúc thư mục dự án, state machine | Luôn bật |
| `seo-output-convention` | Tiêu chuẩn format báo cáo | Luôn bật |
| `seo-report-format` | Template báo cáo audit | Khi audit |
| `seo-provider-priority` | Thứ tự ưu tiên nguồn dữ liệu | Khi truy vấn data |
| `seo-agent-security` | An toàn API key, kiểm soát truy cập | Luôn bật |

## Chi Tiết

### seo-anti-hallucination — Chống Bịa Dữ Liệu

Quy tắc quan trọng nhất. Mọi dữ liệu phải được tag nguồn:

| Tag | Ý nghĩa |
|-----|---------|
| `[FETCHED]` | Lấy trực tiếp từ website/API |
| `[VERIFIED]` | Xác nhận qua script tự động |
| `[INFERRED]` | AI suy luận (có thể sai) |
| `[TEMPLATE]` | Từ industry template (cần xác nhận) |

**TUYỆT ĐỐI KHÔNG** bịa search volume, traffic, rankings, hoặc điểm số.

### seo-auto-routing — Tự Động Chọn Agent

Khi bạn gõ tin nhắn, SEO Kit tự phát hiện:
1. Domain → load project tương ứng
2. Ý định → chọn agent phù hợp
3. Kỹ năng → load skill bundle

### seo-domain-project — Cấu Trúc Dự Án

Quản lý state machine cho vòng đời 5 giai đoạn. Mỗi domain có workspace riêng với `project.json` chứa phase, score, và lịch sử.

### seo-provider-priority — Ưu Tiên Dữ Liệu

```
DataForSEO > Ahrefs > Semrush > Google APIs > HTML phân tích > Không có (template)
```

### seo-agent-security — An Toàn

- API keys không được ghi vào báo cáo
- Credentials lưu ngoài project folder
- Scripts không gọi API ngoài danh sách cho phép
