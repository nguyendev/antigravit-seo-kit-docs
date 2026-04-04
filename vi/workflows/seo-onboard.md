# /seo-onboard — Phase 1: Khởi Tạo Dự Án

## Tổng Quan

Khởi tạo dự án SEO mới. Thiết lập baseline identity, kết nối nguồn dữ liệu, và xác định đối thủ. Đây luôn là bước ĐẦU TIÊN cho bất kỳ domain mới nào.

## Cách Sử Dụng

```
/seo-onboard example.com
```

## Kỹ Năng Kích Hoạt (4)

| # | Kỹ năng | Vai trò |
|---|---------|---------|
| 1 | `seo-google` | Kiểm tra API credentials (GSC, GA4, PageSpeed, CrUX) |
| 2 | `seo-source-context` | Brand identity, credibility score, Semantic Anchor |
| 3 | `seo-audience` | Audience personas, journey mapping, community language |
| 4 | `seo-plan` | Phát hiện ngành, đối thủ, chiến lược ban đầu |

## Các Bước Thực Hiện

1. **Khởi tạo domain project**:
   - Tạo `seo-projects/{domain-slug}/` với subdirs
   - Tạo `project.json` với `phase: "onboarded"`

2. **Kiểm tra Google API credentials**:
   - Ghi nhận tier khả dụng (0-3) vào project.json
   - Không có credentials → ghi nhận hạn chế, tiếp tục

3. **Phân tích Source Context**:
   - Trích xuất brand identity, credibility score, semantic anchor
   - Xác định topical focus areas

4. **Phát hiện ngành & đối thủ**:
   - Fetch homepage, phát hiện loại doanh nghiệp (SaaS, local, ecommerce, publisher, agency)
   - Tự phát hiện đối thủ (nếu MCP khả dụng) hoặc hỏi người dùng
   - Cache vào `competitors.json` và `project.json`

5. **Xây dựng audience personas**:
   - Tạo 2-4 user personas với pain points, goals, search behavior
   - Map customer journey stages (Awareness → Decision)

6. **Tạo báo cáo onboarding**:
   - Lưu tại `seo-projects/{domain-slug}/reports/onboard-{date}.md`
   - Bao gồm: brand profile, API readiness, industry type, competitors, personas

7. **Cập nhật project.json**: Set `phase: "onboarded"`

8. **Gợi ý tiếp**: "Onboarding hoàn tất. Chạy `/seo-research` để nghiên cứu từ khóa, `/seo-audit` để kiểm tra sức khỏe website."

## Output

```
seo-projects/{domain-slug}/
├── project.json
└── reports/
    └── onboard-{date}.md
```
