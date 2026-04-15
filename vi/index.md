```json
//[doc-seo]
{
    "Description": "Tài liệu Antigravity SEO Kit — bộ công cụ AI SEO chuyên nghiệp với 8 agents, 44 kỹ năng, 12 workflows, và vòng đời 5 giai đoạn cho Google Antigravity."
}
```

Antigravity SEO Kit cung cấp **8 AI agents chuyên biệt**, **44 kỹ năng phân tích SEO**, và **12 workflows tự động**, tổ chức thành **vòng đời 5 giai đoạn**. Được xây dựng cho nền tảng [Google Antigravity](https://deepmind.google/technologies/antigravity/).

## Tại Sao Chọn Antigravity SEO Kit?

- **Agentic SEO**: AI agent tự phân tích, đề xuất, và tạo bản sửa lỗi. Bạn chỉ cần duyệt và áp dụng.
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

### 12 Workflows (10 Static + 2 Dynamic)

| Workflow | Agent | Skills | Mục Đích |
|----------|-------|--------|----------|
| [`/seo-run`](workflows/seo-run.md) | *theo phase* | — | Tự phát hiện phase, đề xuất bước tiếp |
| [`/seo-auto-run`](workflows/seo-auto-run.md) | *theo phase* | All | Pipeline tự động hoàn toàn |
| [`/seo-onboard`](workflows/seo-onboard.md) | `seo-strategist` | 4 | Khởi tạo dự án, brand identity, personas |
| [`/seo-research`](workflows/seo-research.md) | `seo-strategist` | 6 | Từ khóa, audience, prompt AI, content gap |
| [`/seo-audit`](workflows/seo-audit.md) | `seo-auditor` | 9 | Kiểm tra toàn diện website |
| [`/seo-strategy`](workflows/seo-strategy.md) | `seo-strategist` | 12 | Chiến lược nội dung & thị trường |
| [`/seo-execute`](workflows/seo-execute.md) | `seo-migration-expert` | 10 | Tạo bản sửa lỗi & nội dung |
| [`/seo-monitor`](workflows/seo-monitor.md) | `seo-data-analyst` | 8 | Theo dõi & đo lường |
| [`/seo-llm-visibility`](workflows/seo-llm-visibility.md) | `seo-ai-specialist` | 5 | GEO: AI SOV, fan-out, brand sentiment |
| [`/seo-social-commerce`](workflows/seo-social-commerce.md) | `seo-growth-hacker` | 4 | Zalo, TikTok, Visual Search |
| [`/seo-local-suite`](workflows/seo-local-suite.md) | `seo-local-expert` | 2 | Local SEO chuyên sâu |
| [`/seo-page`](workflows/seo-page.md) | `seo-content-writer` | 4 | Phân tích trang đơn |

### 44 Kỹ Năng (47 with shared)

Tổ chức thành 8 nhóm, 3 skills chia sẻ giữa agents. Xem [Kỹ Năng](ky-nang).

### 8 AI Agents

| Agent | Skills | Chuyên môn | Workflow chính |
|-------|:------:|-----------|---------------|
| `seo-auditor` | 10 | Chẩn đoán toàn diện | `/seo-audit` |
| `seo-strategist` | 6 | Lập kế hoạch & từ khóa | `/seo-strategy` |
| `seo-content-writer` | 6 | Tạo nội dung | `/seo-page` |
| `seo-ai-specialist` | 7 | GEO / AI visibility | `/seo-llm-visibility` |
| `seo-local-expert` | 3 | Local SEO | `/seo-local-suite` |
| `seo-growth-hacker` | 9 | Off-page & phân phối | `/seo-social-commerce` |
| `seo-data-analyst` | 4 | Analytics & giám sát | `/seo-monitor` |
| `seo-migration-expert` | 2 | Di chuyển & sửa lỗi | `/seo-execute` |

Xem [Hệ thống Agent](kien-truc/he-thong-agent.md) để biết chi tiết.

### Mở Rộng (Extensions)

| Extension | Chức Năng |
|-----------|----------|
| **[DataForSEO](mo-rong/dataforseo.md)** | 22 lệnh: SERP, từ khóa, backlinks, AI visibility |
| **[Ahrefs](mo-rong/ahrefs.md)** | DR/UR, backlink quality, content gap |
| **[Semrush](mo-rong/semrush.md)** | Keyword gap, toxic links, domain analytics |
| **[Banana Image Gen](mo-rong/banana-image-gen.md)** | OG image, hero, infographic qua Gemini AI |

## Phiên Bản

Phiên bản hiện tại: **1.0.0**. Xem [Ghi chú phát hành](ghi-chu-phat-hanh.md).

## Mua & Hỗ Trợ

- Mua license: [antigravityseokit.solann.io](https://antigravityseokit.solann.io/)
- Quản lý & gia hạn: [app.solann.io](https://app.solann.io/)
- Hỗ trợ: support@solann.io
