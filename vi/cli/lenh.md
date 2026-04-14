# Danh Sách Lệnh

## Lifecycle Workflows

| Lệnh | Phase | Mô tả |
|------|-------|-------|
| `/seo-run <domain>` | Master | Tự phát hiện phase, đề xuất bước tiếp |
| `/seo-onboard <domain>` | Phase 1 | Khởi tạo dự án, brand identity |
| `/seo-research <domain>` | Research | Từ khóa, audience, prompt patterns |
| `/seo-audit <domain>` | Phase 2 | Kiểm tra toàn diện, Health Score |
| `/seo-strategy <domain>` | Phase 3 | Chiến lược, roadmap 30/60/90 |
| `/seo-execute <domain>` | Phase 4 | Generate code fixes, content |
| `/seo-monitor <domain>` | Phase 5 | Giám sát, A/B test |

## Deep-dive Workflows

| Lệnh | Mô tả |
|------|-------|
| `/seo-auto-run <domain>` | Pipeline tự động hoàn toàn, không cần xác nhận |
| `/seo-llm-visibility <domain>` | GEO: AI SOV, fan-out, brand sentiment |
| `/seo-social-commerce <domain>` | Zalo, TikTok, Visual Search (VN market) |
| `/seo-local-suite <domain>` | Local SEO: GBP, Maps |
| `/seo-page <url>` | On-page analysis trang đơn |

## Quản Lý Cài Đặt

| Lệnh | Mô tả |
|------|-------|
| `npx antigravity-seo-kit install --key=...` | Cài đặt SEO Kit |
| `npx antigravity-seo-kit update` | Cập nhật phiên bản mới |
| `npx antigravity-seo-kit status` | Kiểm tra trạng thái |
| `npx antigravity-seo-kit devices` | Xem danh sách thiết bị |
| `npx antigravity-seo-kit devices remove <id>` | Xóa thiết bị |
| `npx antigravity-seo-kit uninstall --confirm` | Gỡ cài đặt |

## Truy Cập Trực Tiếp Kỹ Năng

Bạn có thể gọi trực tiếp bất kỳ kỹ năng nào mà không cần workflow:

```
Chạy seo-entity analysis cho example.com
```

Điều này KHÔNG ảnh hưởng project phase.
