# /seo-social-commerce — Social Commerce & Visual Search

## Mục Đích

Deep-dive workflow cho social commerce tại Việt Nam (2026). Tối ưu chuỗi Watch → Like → Buy trên Zalo, TikTok, YouTube Shorts, và visual search (Google Lens, Shopee).

> 📌 Đây là deep-dive workflow — KHÔNG thay đổi phase dự án.

## Cú Pháp

```
/seo-social-commerce <domain> [--focus zalo|video|visual|all]
```

## Agent Phụ Trách

`seo-growth-hacker` — 8 kỹ năng off-page & distribution

## Kỹ Năng Kích Hoạt (4)

| # | Kỹ năng | Vai trò | Điều kiện |
|---|---------|---------|-----------|
| 1 | `seo-audience` | Gen Z personas, hành vi mua sắm VN | Luôn chạy |
| 2 | `seo-social-zalo` | Audit Zalo OA, Mini App, conversion loop | Luôn chạy |
| 3 | `seo-video-transcript` | Tối ưu subtitle TikTok/YouTube Shorts | `--focus video` hoặc `all` |
| 4 | `seo-visual-search` | Google Lens, Shopee image search | `--focus visual` hoặc `all` |

## Các Bước

1. Load project, kiểm tra `target_market` chứa VN
2. Audience mapping cho Gen Z mua sắm
3. Audit hệ sinh thái Zalo (OA, Mini App, NAP)
4. SEO video ngắn (subtitle keywords, dead audio space)
5. Tối ưu visual search (alt text, product images)
6. Verification checkpoint
7. Lưu kết quả + đề xuất

## Kết Quả

```
seo-projects/{domain-slug}/
├── reports/social-commerce-{date}.md
└── data/social-commerce-{date}.json
```
