# /seo-monitor — Phase 5: Giám Sát

Theo dõi A/B tests, AI citability, brand sentiment, crawl logs, backlinks.

## Cách sử dụng

```
/seo-monitor yourdomain.com --focus experiments
```

## Kỹ Năng Kích Hoạt (8)

| Kỹ năng | Vai trò | Điều kiện |
|---------|---------|-----------|
| `seo-test` | A/B test tracking | Luôn |
| `seo-geo-monitor` | AI citability (SOV) | Luôn |
| `seo-brand-sentiment` | LLM bias, community sentiment | Luôn |
| `seo-reddit-scraper` | Unlinked discussions, semantic anchors | Luôn |
| `seo-logs` | Server logs, crawl budget, AI bots | Nếu file log |
| `seo-google` | GSC traffic, CWV, indexation | Nếu API |
| `seo-backlink` | Backlink growth/loss | v2+ |
| `seo-migration` | Post-migration health | Nếu migration |

## Vòng Lặp

- Score cải thiện → tiếp tục giám sát
- Score giảm → re-audit
- >30 ngày → audit mới

## Kết quả

- Monitor report + JSON data
- Phase: `monitoring`
