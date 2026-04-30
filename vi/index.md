```json
//[doc-seo]
{
    "Description": "Tài liệu Antigravity SEO Kit — bộ công cụ AI SEO chuyên nghiệp với 8 agents, 46 kỹ năng, 13 workflows, và vòng đời 5 giai đoạn cho Google Antigravity."
}
```

Antigravity SEO Kit cung cấp **8 AI agents chuyên biệt**, **46 kỹ năng phân tích SEO**, và **13 workflows tự động** (11 static + 2 dynamic), tổ chức thành **vòng đời 5 giai đoạn**. Được xây dựng cho nền tảng [Google Antigravity](https://antigravity.google/download).

## Tại Sao Chọn Antigravity SEO Kit?

- **Agentic SEO**: AI agent tự phân tích, đề xuất, và tạo bản sửa lỗi. Bạn chỉ cần duyệt và áp dụng.
- **Agentic Content Pipeline**: `/seo-write` — viết bài 7 bước tự động từ radar đến deploy.
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
| [`/seo-onboard`](workflows/seo-onboard.md) | `seo-strategist` | Khởi tạo dự án, brand identity, personas |
| [`/seo-research`](workflows/seo-research.md) | `seo-strategist` | Từ khóa, audience, prompt AI, content gap |
| [`/seo-audit`](workflows/seo-audit.md) | `seo-auditor` | Kiểm tra toàn diện website |
| [`/seo-strategy`](workflows/seo-strategy.md) | `seo-strategist` | Chiến lược nội dung & thị trường |
| [`/seo-execute`](workflows/seo-execute.md) | `seo-migration-expert` | Tạo bản sửa lỗi & nội dung |
| [`/seo-monitor`](workflows/seo-monitor.md) | `seo-data-analyst` | Theo dõi & đo lường |
| [`/seo-write`](workflows/seo-write.md) | `seo-content-writer` | **Content pipeline 7 bước** |
| [`/seo-page`](workflows/seo-page.md) | `seo-content-writer` | Phân tích trang đơn |
| [`/seo-llm-visibility`](workflows/seo-llm-visibility.md) | `seo-ai-specialist` | GEO: AI SOV, fan-out, brand sentiment |
| [`/seo-social-commerce`](workflows/seo-social-commerce.md) | `seo-growth-hacker` | Zalo, TikTok, Visual Search |
| [`/seo-local-suite`](workflows/seo-local-suite.md) | `seo-local-expert` | Local SEO chuyên sâu |

**Dynamic Meta-Workflows (2):**

| Workflow | Mô tả |
|----------|--------|
| [`/seo-run`](workflows/seo-run.md) | Interactive: dashboard, đề xuất bước tiếp, chờ duyệt |
| [`/seo-auto-run`](workflows/seo-auto-run.md) | Autonomous: chuỗi tất cả phases còn lại tự động |

### 46 Kỹ Năng (49 with shared)

Tổ chức thành 8 nhóm, 3 skills chia sẻ giữa agents. Xem [Kỹ Năng](ky-nang).

### 8 AI Agents

| Agent | Skills | Chuyên môn | Workflow chính |
|-------|:------:|-----------|---------------|
| `seo-auditor` | 10 | Chẩn đoán toàn diện | `/seo-audit` |
| `seo-strategist` | 6 | Lập kế hoạch & từ khóa | `/seo-strategy` |
| `seo-content-writer` | 7 | Tạo nội dung & pipeline | `/seo-write`, `/seo-page` |
| `seo-ai-specialist` | 7 | GEO / AI visibility | `/seo-llm-visibility` |
| `seo-local-expert` | 3 | Local SEO | `/seo-local-suite` |
| `seo-growth-hacker` | 9 | Off-page & phân phối | `/seo-social-commerce` |
| `seo-data-analyst` | 4 | Analytics & giám sát | `/seo-monitor` |
| `seo-migration-expert` | 2 | Di chuyển & sửa lỗi | `/seo-execute` |

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

Phiên bản hiện tại: **1.0.6**. Xem [Ghi chú phát hành](ghi-chu-phat-hanh.md).

## Mua & Hỗ Trợ

- Mua license: [antigravityseokit.solann.io](https://antigravityseokit.solann.io/)
- Quản lý & gia hạn: [app.solann.io](https://app.solann.io/)
- Hỗ trợ: support@solann.io
