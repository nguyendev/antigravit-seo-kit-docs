```json
//[doc-seo]
{
    "Description": "Tài liệu Antigravity SEO Kit — bộ công cụ phân tích SEO chuyên nghiệp với 35 kỹ năng chuyên biệt, vòng đời 5 giai đoạn, và hệ thống workflow tự động cho Google Antigravity."
}
```

Antigravity SEO Kit cung cấp **35 kỹ năng phân tích SEO chuyên biệt** được tổ chức thành **vòng đời 5 giai đoạn** với hệ thống workflow tự động. Được xây dựng cho nền tảng [Google Antigravity](https://deepmind.google/technologies/antigravity/), SEO Kit giúp bạn thực hiện kiểm tra kỹ thuật, đánh giá E-E-A-T, tối ưu Schema, Generative Engine Optimization (GEO), nghiên cứu từ khóa, phân tích đối thủ, và nhiều hơn nữa.

## Tại Sao Chọn Antigravity SEO Kit?

- **Agentic SEO**: AI agent tự động phân tích, đề xuất, và tạo bản sửa lỗi. Bạn chỉ cần duyệt và áp dụng.
- **Vòng đời toàn diện**: Từ onboarding đến monitoring, mỗi giai đoạn xây dựng trên kết quả giai đoạn trước.
- **Một lệnh duy nhất**: `/seo-run domain.com` tự động phát hiện giai đoạn hiện tại và đề xuất bước tiếp theo.

## Bắt Đầu Nhanh

```bash
npx ag-seo-kit install --key=SK-XXXX-XXXX-XXXX
```

Xem [Hướng dẫn cài đặt](bat-dau/cai-dat.md) để biết chi tiết. Sau khi cài đặt:

```
/seo-run yourdomain.com
```

## Vòng Đời SEO

```
📋 ONBOARD → 🔎 RESEARCH → 🔍 AUDIT → 🧠 STRATEGY → ⚡ EXECUTE → 📈 MONITOR → (lặp lại)
```

SEO Kit hướng dẫn bạn qua 5 giai đoạn. Đọc thêm tại [Workflows](workflows).

### Workflows — Hệ Thống Điều Phối

Workflows là **cốt lõi** của SEO Kit. Mỗi workflow là một quy trình nhiều bước, kích hoạt các kỹ năng chuyên biệt theo thứ tự tối ưu:

| Workflow | Giai Đoạn | Kỹ Năng | Mục Đích |
|----------|-----------|---------|----------|
| [`/seo-run`](workflows/seo-run.md) | Master | Ủy quyền | Tự phát hiện phase, đề xuất bước tiếp |
| [`/seo-onboard`](workflows/seo-onboard.md) | Phase 1 | 4 | Khởi tạo dự án, kiểm tra API, phân tích thương hiệu |
| [`/seo-research`](workflows/seo-research.md) | Nghiên cứu | 5 | Từ khóa, đối tượng, prompt AI |
| [`/seo-audit`](workflows/seo-audit.md) | Phase 2 | 9 | Kiểm tra toàn diện website |
| [`/seo-strategy`](workflows/seo-strategy.md) | Phase 3 | 10 | Chiến lược nội dung & thị trường |
| [`/seo-execute`](workflows/seo-execute.md) | Phase 4 | 6 | Tạo bản sửa lỗi & nội dung |
| [`/seo-monitor`](workflows/seo-monitor.md) | Phase 5 | 6 | Theo dõi & đo lường |
| [`/seo-local-suite`](workflows/seo-local-suite.md) | Đặc biệt | 2 | Local SEO chuyên sâu |
| [`/seo-page`](workflows/seo-page.md) | Tiện ích | 4 | Phân tích trang đơn |

### 35 Kỹ Năng Chuyên Biệt

Các kỹ năng được tổ chức thành 7 nhóm:

- **[Technical SEO](ky-nang/ky-thuat)**: Crawlability, indexability, Core Web Vitals, sitemap, hình ảnh, hreflang
- **[Content SEO](ky-nang/noi-dung)**: E-E-A-T, content gap, topical authority, entity SEO
- **[AI & GEO](ky-nang/ai-seo)**: Generative Engine Optimization, AI answer, agentic SEO, prompt research
- **[Nghiên Cứu](ky-nang/nghien-cuu)**: Từ khóa, đối tượng mục tiêu, source context, đối thủ
- **[Off-Page](ky-nang/off-page)**: Backlink, authority, local SEO
- **[Thực Thi](ky-nang/thuc-thi)**: Auto-fix, schema generation, migration, programmatic SEO, video
- **[Giám Sát](ky-nang/giam-sat)**: A/B test, server logs, Google APIs, Maps intelligence

### Mở Rộng (Extensions)

| Extension | Chức Năng |
|-----------|----------|
| **[DataForSEO](mo-rong/dataforseo.md)** | 22 lệnh: SERP trực tiếp, từ khóa, backlinks, phân tích on-page, AI visibility |
| **[Ahrefs](mo-rong/ahrefs.md)** | DR/UR, chất lượng backlink, content gap, referring domains |
| **[Semrush](mo-rong/semrush.md)** | Keyword gap, toxic links, backlink audit, domain analytics |
| **[Banana Image Gen](mo-rong/banana-image-gen.md)** | 6 lệnh: OG image, hero, product, infographic qua Gemini AI |

### Kiến Trúc

SEO Kit tuân theo tiêu chuẩn mở Agent Skills với kiến trúc 3 lớp (directive, orchestration, execution). Xem:

- [Hệ thống kỹ năng](kien-truc/he-thong-ky-nang.md) để hiểu cách skills hoạt động
- [Hệ thống workflow](kien-truc/he-thong-workflow.md) để hiểu cách workflows điều phối
- [Tích hợp MCP](kien-truc/tich-hop-mcp.md) để kết nối dữ liệu bên ngoài

## Phiên Bản

Phiên bản hiện tại: **0.9.0**. Xem [Ghi chú phát hành](ghi-chu-phat-hanh.md) để theo dõi các thay đổi.

## Mã Nguồn

SEO Kit được phát triển bởi **nguyendev**. Xem [hướng dẫn đóng góp](dong-gop.md) nếu bạn muốn tham gia dự án.
