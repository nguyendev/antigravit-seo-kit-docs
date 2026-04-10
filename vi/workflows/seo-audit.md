# /seo-audit — Phase 2: Kiểm Tra

Kiểm tra toàn diện website với 9 kỹ năng song song. Health Score 0-100.

## Cách sử dụng

```
/seo-audit yourdomain.com --scope priority
```

## Scope Control

| Scope | Mô tả | Mặc định |
|-------|-------|----------|
| `homepage` | Chỉ trang chủ | Nếu không có priority pages |
| `priority` | Homepage + priority pages | ✅ Mặc định |
| `full` | Tất cả internal links (tối đa 50) | Audit sâu |

## Kỹ Năng Kích Hoạt (9)

| Kỹ năng | Luôn chạy? |
|---------|------------|
| `seo-technical` | ✅ |
| `seo-content` | ✅ |
| `seo-schema` | ✅ |
| `seo-sitemap` | ✅ |
| `seo-images` | ✅ |
| `seo-hreflang` | ✅ |
| `seo-geo` | ✅ |
| `seo-google` | Nếu có API credentials |
| `seo-local` | Nếu local business |

## Health Score Weights

| Danh mục | Trọng số |
|----------|----------|
| Technical SEO | 22% |
| Content Quality | 23% |
| On-Page SEO | 20% |
| Schema | 10% |
| Performance (CWV) | 10% |
| AI Search Readiness | 10% |
| Images | 5% |

> Trọng số tự điều chỉnh theo `primary_goal` và `industry`.

## Kết quả

- Health Score + Action Plan (Critical → Low)
- Delta tracking so với audit trước
- Phase: `audited`
