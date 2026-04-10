# /seo-execute — Phase 4: Thực Thi

Tạo code fixes, schema JSON-LD, meta tags, llms.txt, CiteMET, visual search alt text.

## Cách sử dụng

```
/seo-execute yourdomain.com --categories meta,schema,robots,redirects
```

## Kỹ Năng Kích Hoạt (10)

| Kỹ năng | Vai trò |
|---------|---------|
| `seo-fix` | Auto-generate meta tags, schema, robots.txt, redirects |
| `seo-schema` | Generate JSON-LD cho pages thiếu structured data |
| `seo-content` | Content briefs, E-E-A-T guidance |
| `seo-migration` | Redirect mapping (nếu `--migration`) |
| `seo-video` | VideoObject schema, video sitemap |
| `seo-video-transcript` | LSI injection cho TikTok/YouTube Shorts |
| `seo-image-gen` | AI-generated SEO images (nếu extension) |
| `seo-llmstxt` | Generate `llms.txt` cho AI bot indexing |
| `seo-citemet` | AI share buttons (CiteMET) |
| `seo-visual-search` | Computer-vision Alt Text, WebP recommendations |

## CMS-Aware

Fix formats tự điều chỉnh theo CMS: WordPress → Yoast, Shopify → Liquid, Next.js → metadata API.

## Kết quả

- Thư mục `fixes/{date}/` với tất cả file sửa lỗi
- Execution report
- Phase: `executed`
