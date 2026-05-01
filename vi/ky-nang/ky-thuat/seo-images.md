# seo-images — Tối Ưu Hình Ảnh

## Mô Tả

Tối ưu hóa hình ảnh cho SEO: alt text, formats, lazy loading, CLS prevention, responsive images, file size.

## Agent Phụ Trách

`seo-technical-architect` (skill #6/10)

## Chức Năng Chính

- **Alt text**: Kiểm tra missing/generic alt, đề xuất alt text mô tả
- **Format**: WebP/AVIF recommendations
- **Performance**: Lazy loading, srcset, sizes attribute
- **CLS prevention**: Width/height attributes, aspect-ratio
- **File size**: Phát hiện ảnh quá nặng (>200KB)
- **Responsive**: srcset, picture element analysis

## Scripts

| Script | Chức năng |
|--------|----------|
| `image_auditor.py` | Audit hình ảnh toàn diện |

## Khi Nào Dùng

- "image optimization", "hình ảnh", "alt text"
- "lazy loading", "image compression", "CLS"

## Workflow Liên Quan

- `/seo-audit` — Kiểm tra hình ảnh trong audit toàn diện
