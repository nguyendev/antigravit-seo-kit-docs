# Danh Sách Lệnh

## Lifecycle Workflows (Static — Agent cố định)

| Lệnh | Agent | Mô tả |
|------|-------|-------|
| `/seo-onboard <domain>` | `seo-strategist` | Khởi tạo dự án, brand identity |
| `/seo-research <domain>` | `seo-strategist` | Từ khóa, audience, prompt patterns |
| `/seo-audit <domain>` | `seo-auditor` | Kiểm tra toàn diện, Health Score |
| `/seo-strategy <domain>` | `seo-strategist` | Chiến lược, roadmap 30/60/90 |
| `/seo-execute <domain>` | `seo-migration-expert` | Generate code fixes, content |
| `/seo-monitor <domain>` | `seo-data-analyst` | Giám sát, A/B test |
| `/seo-write <keyword>` | `seo-content-writer` | **Content pipeline 7 bước** (radar → deploy) |
| `/seo-page <url>` | `seo-content-writer` | On-page analysis trang đơn |
| `/seo-llm-visibility <domain>` | `seo-ai-specialist` | GEO: AI SOV, fan-out, brand sentiment |
| `/seo-social-commerce <domain>` | `seo-growth-hacker` | Zalo, TikTok, Visual Search (VN market) |
| `/seo-local-suite <domain>` | `seo-local-expert` | Local SEO: GBP, Maps |

## Dynamic Meta-Workflows (Agent theo phase)

| Lệnh | Mô tả |
|------|-------|
| `/seo-run <domain>` | Interactive: tự phát hiện phase, đề xuất bước tiếp, chờ duyệt |
| `/seo-auto-run <domain>` | Autonomous: chuỗi tất cả phases tự động, không cần xác nhận |

## Quản Lý Cài Đặt

| Lệnh | Mô tả |
|------|-------|
| `npx antigravity-seo-kit install --key=...` | Cài đặt SEO Kit |
| `npx antigravity-seo-kit update` | Cập nhật phiên bản mới |
| `npx antigravity-seo-kit status` | Kiểm tra trạng thái |
| `npx antigravity-seo-kit devices` | Xem danh sách thiết bị |
| `npx antigravity-seo-kit devices remove <id>` | Xóa thiết bị |
| `npx antigravity-seo-kit uninstall --confirm` | Gỡ cài đặt |
| `npx antigravity-seo-kit --version` | Xem phiên bản CLI |
| `npx antigravity-seo-kit --help` | Hiển thị trợ giúp |

## Truy Cập Trực Tiếp Kỹ Năng

Bạn có thể gọi trực tiếp bất kỳ kỹ năng nào mà không cần workflow:

```
Chạy seo-entity analysis cho example.com
```

Điều này KHÔNG ảnh hưởng project phase.
