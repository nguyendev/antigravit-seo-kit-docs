# /seo-local-suite — Local SEO Chuyên Sâu

## Tổng Quan

Phân tích Local SEO toàn diện kết hợp GBP optimization và Maps intelligence. Sử dụng khi doanh nghiệp có địa điểm vật lý hoặc phục vụ khu vực địa lý cụ thể.

## Cách Sử Dụng

```
/seo-local-suite example.com
```

## Kỹ Năng Kích Hoạt (2)

| # | Kỹ năng | Vai trò |
|---|---------|---------|
| 1 | `seo-local` | GBP optimization, NAP consistency, citations, reviews, local schema |
| 2 | `seo-maps` | Geo-grid rank tracking, GBP audit, review intelligence, competitor radius |

## Các Bước Thực Hiện

1. **Load domain project**
2. **Phát hiện loại doanh nghiệp**:
   - brick-and-mortar, SAB (service-area business), hybrid
   - Ngành: restaurant, healthcare, legal, home services, real estate, automotive
3. **Verification checkpoint** (anti-hallucination):
   - "Phát hiện [loại] + [ngành]. Đúng không?"
   - Tag `[INFERRED]` — phải xác nhận trước khi tiếp tục
4. **Phân tích Local SEO**:
   - NAP consistency
   - GBP signals, review health, citation presence
   - LocalBusiness schema validation
   - Location page quality (multi-location)
5. **Chạy Maps intelligence**:
   - Geo-grid rank tracking (nếu DataForSEO MCP)
   - GBP profile audit
   - Review intelligence analysis
   - Competitive radius map

## Quality Gates

| Ngưỡng | Hành động |
|--------|----------|
| 30+ location pages | ⚠️ WARNING: Yêu cầu 60%+ nội dung duy nhất |
| 50+ location pages | 🛑 HARD STOP: Yêu cầu giải trình từ người dùng |

## Output

```
seo-projects/{domain-slug}/reports/local-suite-{date}.md
```
