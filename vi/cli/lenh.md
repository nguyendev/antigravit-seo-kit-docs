# Danh Sách Lệnh

## Lifecycle Workflows (Static — Agent cố định)

| Lệnh | Agent | Mô tả |
|------|-------|-------|
| `/seo-onboard <domain>` | `seo-content-authority` | Khởi tạo dự án, brand identity |
| `/seo-research <domain>` | `seo-content-authority` | Từ khóa, audience, prompt patterns |
| `/seo-audit <domain>` | `seo-technical-architect` | Kiểm tra toàn diện, Health Score |
| `/seo-strategy <domain>` | `seo-content-authority` | Chiến lược, roadmap 30/60/90 |
| `/seo-execute <domain>` | `seo-technical-architect` | Generate code fixes, content |
| `/seo-monitor <domain>` | `seo-intelligence` | Giám sát, A/B test |
| `/seo-write <keyword>` | `seo-creator` | **Content pipeline 7 bước** (radar → deploy) |
| `/seo-page <url>` | `seo-creator` | On-page analysis trang đơn |
| `/seo-llm-visibility <domain>` | `seo-ai-search` | GEO: AI SOV, fan-out, brand sentiment |
| `/seo-social-commerce <domain>` | `seo-multimedia` | Zalo, TikTok, Visual Search (VN market) |
| `/seo-local-suite <domain>` | `seo-local-commerce` | Local SEO: GBP, Maps |

## Web Development Workflows (SEO-Driven)

Khác với nhóm `/seo-*` chuyên dùng để phân tích và tối ưu, nhóm `/web-*` dùng để lập trình và xây dựng website theo tư tưởng "Code để Rank".

| Lệnh | Agent | Mô tả |
|------|-------|-------|
| `/web-create` | `web-orchestrator` | Khởi tạo ứng dụng mới từ đầu |
| `/web-enhance` | `web-orchestrator` | Nâng cấp hoặc thêm tính năng mới |
| `/web-ui-design` | `web-frontend-specialist` | Tạo hoặc thiết kế lại UI/UX chuẩn Web Vitals |
| `/web-deploy` | `devops-engineer` | Triển khai an toàn lên Production (5-phase rollout) |
| `/web-test` | `qa-automation-engineer` | Viết & chạy test tự động (Playwright/Jest) |
| `/web-preview` | N/A | Chạy dev server để xem trước giao diện |
| `/web-debug` | `debugger` | Bật chế độ tìm diệt bug chuyên sâu |
| `/web-plan` | `project-planner` | Lên kế hoạch cấu trúc và hệ thống cho dự án web |
| `/web-brainstorm` | N/A | Thảo luận và nghiên cứu giải pháp lập trình |
| `/web-status` | N/A | Xem tiến độ hiện tại của dự án Web |
| `/web-orchestrate` | `web-orchestrator` | Gọi nhiều agent cùng làm một task phức tạp |

## Shared & Verification Scripts

Các script chạy ngoài luồng dùng để kiểm tra dự án (dành cho cả SEO và Web):

| Script | Thư mục | Mục đích |
|--------|---------|----------|
| `verify_all.py` | `.agent/scripts/` | Chạy toàn bộ suite kiểm tra (Master Script) |
| `checklist.py` | `.agent/scripts/` | Kiểm tra Priority: Security, Lint, Schema, UX |
| `security_scan.py` | `.agent/skills/vulnerability-scanner/`| Quét bảo mật dự án trước khi deploy |
| `lighthouse_audit.py` | `.agent/skills/performance-profiling/`| Quét Core Web Vitals |
| `webmcp_audit.py` | `.agent/skills/seo-agentic/` | Chấm điểm mức độ sẵn sàng cho AI Agent |

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
