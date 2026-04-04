# Mở Rộng (Extensions)

SEO Kit sử dụng Model Context Protocol (MCP) để kết nối dữ liệu bên ngoài. Các extension cung cấp dữ liệu trực tiếp (live data) cho phân tích chính xác hơn.

## Extensions Hiện Có

| Extension | Lệnh | Chức năng chính |
|-----------|-------|----------------|
| [DataForSEO](dataforseo.md) | 22 | SERP trực tiếp, từ khóa, backlinks, on-page, AI visibility |
| [Ahrefs](ahrefs.md) | — | DR/UR, backlink quality, content gap, referring domains |
| [Semrush](semrush.md) | — | Keyword gap, toxic links, backlink audit, domain analytics |
| [Banana Image Gen](banana-image-gen.md) | 6 | OG images, hero images, product photos, infographics |

## Cách Extensions Hoạt Động

1. Extensions đăng ký qua MCP server configuration
2. SEO Kit tự động phát hiện extensions khả dụng
3. Workflows ưu tiên dữ liệu từ extensions (provider priority: DataForSEO > Ahrefs > Semrush)
4. Không có extension → SEO Kit vẫn hoạt động bằng phân tích HTML thuần

## Cấu Hình

Extensions cấu hình trong MCP server settings. Xem [Tích hợp MCP](../kien-truc/tich-hop-mcp.md) để biết chi tiết.
