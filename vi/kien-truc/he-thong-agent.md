# Hệ Thống Agent (24 Agents — Multi-Domain Architecture)

Antigravity SEO Kit v1.1.0 đã được nâng cấp thành hệ sinh thái **SEO-Driven Web Development**, phá bỏ ranh giới giữa lập trình và SEO. Hệ thống hiện sử dụng **24 AI agents** chuyên biệt, tổ chức thành **3 Domains (Miền hoạt động)** chính.

## 1. Phân Tích & Chiến Lược SEO (SEO Domain)

Bao gồm 9 Agents tổ chức thành **3-Layer Architecture** (Foundation + Surface + Enabler).

| Layer | Agent | Chuyên môn | Skills | Workflow chính |
|:-----:|-------|-----------|:------:|---------------|
| 🎯 Meta | `seo-orchestrator` | Lifecycle & coordination | meta | `/seo-run`, `/seo-auto-run` |
| 🏗️ Foundation | `seo-technical-architect` | Infrastructure & diagnostics | 9 | `/seo-audit` |
| 🏗️ Foundation | `seo-content-authority` | Strategy & authority | 12 | `/seo-strategy`, `/seo-research` |
| 🏗️ Foundation | `seo-intelligence` | Analytics & monitoring | 5 | `/seo-monitor` |
| 🌐 Surface | `seo-ai-search` | AI/GEO visibility, WebMCP | 7 | `/seo-llm-visibility` |
| 🌐 Surface | `seo-multimedia` | Video, social, visual | 4 | `/seo-social-commerce` |
| 🌐 Surface | `seo-local-commerce` | Local & commerce | 3 | `/seo-local-suite` |
| 🔧 Enabler | `seo-creator` | Content execution, IG | 5 | `/seo-write`, `/seo-page` |
| 🔧 Enabler | `seo-data-provider` | Data access layer | 3 | *(enabler)* |

## 2. Xây Dựng Web Chuẩn SEO (Web Development Domain)

Code website như một công cụ để thống trị SERP và các AI Answer Engines.

| Layer | Agent | Chuyên môn | Khái quát công việc | Workflow chính |
|:-----:|-------|-----------|--------------------|---------------|
| 🎯 Meta | `web-orchestrator` | Điều phối lập trình web | Phân tích yêu cầu, gọi các chuyên gia lập trình | `/web-orchestrate` |
| 💻 Core | `web-frontend-specialist` | UI/UX, Core Web Vitals | React, Tailwind, hiệu năng, DOM Rendering | `/web-ui-design`, `/web-enhance` |
| ⚙️ Core | `web-backend-specialist` | API, Database, Server | API Schema, WebMCP Endpoint, Database | `/web-create` |

## 3. Kỹ Năng Nền Tảng (Shared Domain)

Các Agent dùng chung giúp kiểm soát chất lượng, bảo mật, gỡ lỗi và quản lý hệ thống.

| Agent | Chuyên môn | Khái quát công việc |
|-------|-----------|--------------------|
| `debugger` | Gỡ lỗi hệ thống | Phân tích root-cause, sửa lỗi chuyên sâu |
| `security-auditor` | Đánh giá bảo mật | Quét lỗ hổng (OWASP), bảo vệ dữ liệu |
| `devops-engineer` | Vận hành & Triển khai | Server management, Docker, Deploy pipelines |
| `performance-optimizer` | Tối ưu hiệu năng | Phân tích Bundle, Lighthouse audit |
| `project-planner` | Lập kế hoạch dự án | Phân chia công việc, dependency graph |
| `explorer-agent` | Phân tích Source Code | Mapping codebase, tìm kiếm tệp tin |
| `documentation-writer`| Viết tài liệu | Sinh docs API, code comments |
| `qa-automation-engineer`| Tự động hóa kiểm thử| Playwright, E2E |
| `test-engineer` | Kỹ sư kiểm thử | Unit tests, Integration tests |
| `code-archaeologist` | Quản lý Legacy Code | Đọc hiểu mã nguồn cũ, refactoring |

## Tính Tích Hợp (The Grand Unification)

Khi bạn sử dụng `/seo-execute`, hệ thống không chỉ sửa các thẻ meta, mà `seo-orchestrator` có thể gọi `web-frontend-specialist` để tinh chỉnh cấu trúc DOM React nhằm cải thiện CLS (Cumulative Layout Shift) hoặc LCP (Largest Contentful Paint). 
Tương tự, khi dùng `/web-create`, `web-backend-specialist` sẽ tự động tuân thủ cấu trúc API Discoverability được quy định bởi `seo-ai-search` để hỗ trợ WebMCP.
