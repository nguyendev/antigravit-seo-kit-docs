# Danh Sách Lệnh CLI

## Quản Lý Cài Đặt

```bash
# Cài đặt SEO Kit với license key
npx ag-seo-kit install --key=SK-XXXX-XXXX-XXXX

# Cập nhật lên phiên bản mới nhất
npx ag-seo-kit update

# Kiểm tra trạng thái cài đặt
npx ag-seo-kit status

# Gỡ cài đặt
npx ag-seo-kit uninstall --confirm
```

## Quản Lý Thiết Bị

```bash
# Xem danh sách thiết bị đã kích hoạt
npx ag-seo-kit devices

# Xóa thiết bị để giải phóng slot
npx ag-seo-kit devices remove <deviceId>
```

## SEO Workflows (trong Antigravity)

Các lệnh này chạy bên trong nền tảng Google Antigravity:

| Lệnh | Giai Đoạn | Mục Đích |
|------|-----------|----------|
| `/seo-run <domain>` | Master | Tự phát hiện phase, đề xuất bước tiếp |
| `/seo-onboard <domain>` | Phase 1 | Khởi tạo dự án |
| `/seo-research <domain>` | Research | Nghiên cứu từ khóa, audience, prompts |
| `/seo-audit <domain>` | Phase 2 | Kiểm tra toàn diện website |
| `/seo-strategy <domain>` | Phase 3 | Chiến lược nội dung & thị trường |
| `/seo-execute <domain>` | Phase 4 | Tạo bản sửa lỗi |
| `/seo-monitor <domain>` | Phase 5 | Giám sát & đo lường |
| `/seo-local-suite <domain>` | Đặc biệt | Local SEO chuyên sâu |
| `/seo-page <url>` | Tiện ích | Phân tích trang đơn |

## Truy Cập Kỹ Năng Trực Tiếp

```
"Run seo-entity analysis for example.com"
"Check seo-backlink for competitor.com"
"Analyze seo-schema for https://example.com/about"
```

Truy cập trực tiếp KHÔNG thay đổi phase dự án.
