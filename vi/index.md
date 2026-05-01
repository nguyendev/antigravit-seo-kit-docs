```json
//[doc-seo]
{
    "Description": "Tài liệu Antigravity SEO Kit — bộ công cụ AI SEO chuyên nghiệp với 9 agents (3-layer architecture), 42 kỹ năng, 13 workflows, và vòng đời 5 giai đoạn cho Google Antigravity."
}
```

Antigravity SEO Kit cung cấp **9 AI agents** tổ chức thành **3-layer architecture** (Foundation + Surface + Enabler), **42 kỹ năng phân tích SEO**, và **13 workflows tự động** (11 static + 2 dynamic), tổ chức thành **vòng đời 5 giai đoạn**. Được xây dựng cho nền tảng [Google Antigravity](https://antigravity.google/download).

## Tại Sao Chọn Antigravity SEO Kit?

- **Agentic SEO**: AI agent tự phân tích, đề xuất, và tạo bản sửa lỗi. Bạn chỉ cần duyệt và áp dụng.
- **Agentic Content Pipeline**: `/seo-write` — viết bài 5 bước tự động từ research đến deploy.
- **Vòng đời toàn diện**: Từ onboarding đến monitoring, mỗi giai đoạn xây dựng trên kết quả trước.
- **Một lệnh duy nhất**: `/seo-run domain.com` tự động phát hiện giai đoạn và đề xuất bước tiếp.
- **GEO & AI Search**: Tối ưu cho ChatGPT, Gemini, Perplexity, Cốc Cốc AI — không chỉ Google.
- **Vietnam-Ready**: Zalo OA, Cốc Cốc, TikTok, Shopee Lens — built-in cho thị trường Việt Nam.

## Bắt Đầu Nhanh

```bash
npx antigravity-seo-kit install --key=SK-XXXX-XXXX-XXXX
```

> Mua license key tại: [antigravityseokit.solann.io](https://antigravityseokit.solann.io/)

Xem [Hướng dẫn cài đặt chi tiết](bat-dau/cai-dat.md) nếu bạn mới bắt đầu.

## Vòng Đời SEO

```
📋 ONBOARD → 🔎 RESEARCH → 🔍 AUDIT → 🧠 STRATEGY → ⚡ EXECUTE → 📈 MONITOR → (lặp lại)
```

Đọc thêm tại [Workflows](workflows).

### 13 Workflows (11 Static + 2 Dynamic)

**Static Workflows (11):**

| Workflow | Agent | Mục Đích |
|----------|-------|----------|
| [`/seo-onboard`](workflows/seo-onboard.md) | `seo-content-authority` | Khởi tạo dự án, brand identity, personas |
| [`/seo-research`](workflows/seo-research.md) | `seo-content-authority` | Từ khóa, audience, prompt AI, content gap |
| [`/seo-audit`](workflows/seo-audit.md) | `seo-technical-architect` | Kiểm tra toàn diện website |
| [`/seo-strategy`](workflows/seo-strategy.md) | `seo-content-authority` | Chiến lược nội dung & thị trường |
| [`/seo-execute`](workflows/seo-execute.md) | `seo-technical-architect` | Tạo bản sửa lỗi & nội dung |
| [`/seo-monitor`](workflows/seo-monitor.md) | `seo-intelligence` | Theo dõi & đo lường |
| [`/seo-write`](workflows/seo-write.md) | `seo-creator` | **Content pipeline 5 bước** |
| [`/seo-page`](workflows/seo-page.md) | `seo-creator` | Phân tích trang đơn |
| [`/seo-llm-visibility`](workflows/seo-llm-visibility.md) | `seo-ai-search` | GEO: AI SOV, fan-out, brand sentiment |
| [`/seo-social-commerce`](workflows/seo-social-commerce.md) | `seo-multimedia` | Zalo, TikTok, Visual Search |
| [`/seo-local-suite`](workflows/seo-local-suite.md) | `seo-local-commerce` | Local SEO chuyên sâu |

**Dynamic Meta-Workflows (2):**

| Workflow | Mô tả |
|----------|--------|
| [`/seo-run`](workflows/seo-run.md) | Interactive: dashboard, đề xuất bước tiếp, chờ duyệt |
| [`/seo-auto-run`](workflows/seo-auto-run.md) | Autonomous: chuỗi tất cả phases còn lại tự động |

### 42 Kỹ Năng (53 with shared)

Tổ chức thành 8 nhóm, 5 skills chia sẻ giữa agents. Xem [Kỹ Năng](ky-nang).

### 9 AI Agents (3-Layer)

| Layer | Agent | Skills | Chuyên môn | Workflow chính |
|:-----:|-------|:------:|-----------|---------------|
| 🎯 Meta | `seo-orchestrator` | meta | Lifecycle & coordination | `/seo-run`, `/seo-auto-run` |
| 🏗️ Foundation | `seo-technical-architect` | 9 | Infrastructure & diagnostics | `/seo-audit` |
| 🏗️ Foundation | `seo-content-authority` | 12 | Strategy & authority | `/seo-strategy`, `/seo-research` |
| 🏗️ Foundation | `seo-intelligence` | 5 | Analytics & monitoring | `/seo-monitor` |
| 🌐 Surface | `seo-ai-search` | 6 | AI/GEO visibility | `/seo-llm-visibility` |
| 🌐 Surface | `seo-multimedia` | 4 | Video, social, visual | `/seo-social-commerce` |
| 🌐 Surface | `seo-local-commerce` | 3 | Local & commerce | `/seo-local-suite` |
| 🔧 Enabler | `seo-creator` | 4 | Content execution | `/seo-write`, `/seo-page` |
| 🔧 Enabler | `seo-data-provider` | 3 | Data access layer | *(enabler)* |

Xem [Hệ thống Agent](kien-truc/he-thong-agent.md) để biết chi tiết.

### Mở Rộng (Extensions) - Sẽ ra mắt vào V2

| Extension | Chức Năng |
|-----------|----------|
| **[Solann API](mo-rong/solann-api.md)** | Mặc định — keyword volume, trends, CPC, competitor keywords |
| **[Search Console MCP](mo-rong/search-console-mcp.md)** | 30+ tools: GSC, Bing, GA4, SEO Intelligence |
| **[DataForSEO](mo-rong/dataforseo.md)** | 22 lệnh: SERP, từ khóa, backlinks, AI visibility |
| **[Ahrefs](mo-rong/ahrefs.md)** | DR/UR, backlink quality, content gap |
| **[Semrush](mo-rong/semrush.md)** | Keyword gap, toxic links, domain analytics |
| **[Banana Image Gen](mo-rong/banana-image-gen.md)** | OG image, hero, infographic qua Gemini AI |

## Phiên Bản

Phiên bản hiện tại: **1.0.7**. Xem [Ghi chú phát hành](ghi-chu-phat-hanh.md).

## Mua & Hỗ Trợ

- Mua license: [antigravityseokit.solann.io](https://antigravityseokit.solann.io/)
- Quản lý & gia hạn: [app.solann.io](https://app.solann.io/)
- Hỗ trợ: support@solann.io
