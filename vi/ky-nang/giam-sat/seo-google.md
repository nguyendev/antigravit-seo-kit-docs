# seo-google — Google APIs

Tích hợp Google APIs: Search Console, PageSpeed Insights, CrUX, GA4.

## API Tiers

| Tier | APIs | Yêu cầu |
|------|------|---------|
| 0 | Không | Phân tích HTML thuần |
| 1 | PageSpeed Insights | API key |
| 2 | + Search Console | Credentials JSON |
| 3 | + GA4 | Full OAuth |

## Chức năng
- GSC traffic trends, top queries, page performance
- PageSpeed Insights lab metrics
- CrUX field data (LCP, INP, CLS, TTFB)
- Indexation status
- GA4 traffic data (tier 3)
