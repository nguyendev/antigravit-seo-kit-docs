# /seo-onboard — Phase 1: Khởi Tạo

Khởi tạo dự án SEO mới. Pre-scan domain, xác nhận thông tin với user, phân tích brand identity.

## Cách sử dụng

```
/seo-onboard yourdomain.com
```

## 3 Chế độ

| Chế độ | Trigger | Hành vi |
|--------|---------|---------|
| **Normal** | Domain reachable | Pre-scan → 5-7 câu hỏi thông minh → phân tích đầy đủ |
| **Greenfield** | Domain chưa publish | Full Q&A (7-10 câu hỏi) → chế độ lập kế hoạch |
| **Resume** | Project đã tồn tại | Hiển thị trạng thái → hỏi re-onboard hoặc `/seo-run` |

## Kỹ Năng Kích Hoạt (4)

| Kỹ năng | Vai trò |
|---------|---------|
| `seo-google` | Kiểm tra API credentials (GSC, GA4, CrUX) |
| `seo-source-context` | Brand identity, Semantic Anchor, E-E-A-T |
| `seo-audience` | Audience personas, journey mapping |
| `seo-plan` | Phát hiện ngành, đối thủ, chiến lược ban đầu |

## Quy trình

1. Kiểm tra project tồn tại
2. Pre-scan domain (ngôn ngữ, CMS, loại doanh nghiệp)
3. Hỏi câu hỏi xác nhận (AI gợi ý sẵn câu trả lời)
4. **Chờ user trả lời**
5. Tạo workspace `seo-projects/{domain-slug}/`
6. Phân tích Source Context
7. Xây dựng audience personas
8. Generate báo cáo onboarding

## Kết quả

- `project.json` với phase: `onboarded` (hoặc `greenfield`)
- Báo cáo: `reports/onboard-{date}.md`
- Gợi ý: `/seo-research` hoặc `/seo-audit`
