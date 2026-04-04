# Cài Đặt

## Cài Đặt Nhanh (Khuyến Nghị)

```bash
npx ag-seo-kit install --key=SK-XXXX-XXXX-XXXX
```

Lệnh này tự động:
- Tải SEO Kit vào workspace hiện tại
- Xác thực license key
- Kích hoạt thiết bị (tối đa 3 thiết bị/license)
- Cài đặt các file skill vào `.agent/skills/`

## Cài Đặt Thủ Công

### Bước 1: Cài đặt package

```bash
npx ag-seo-kit install --key=SK-XXXX-XXXX-XXXX
```

### Bước 2: Cài đặt Python dependencies

```bash
pip install -r requirements.txt
```

### Bước 3: (Tùy chọn) Cài đặt Google API dependencies

```bash
pip install -r requirements-google.txt
```

### Bước 4: (Tùy chọn) Cài đặt Playwright

```bash
pip install playwright && playwright install chromium
```

### Bước 5: Mở workspace trong Google Antigravity

Agent sẽ tự động phát hiện:
- Skills trong `.agent/skills/`
- Workflows trong `.agent/workflows/`
- Agent instructions trong `.agent/agent.md`

## Cấu Trúc Sau Cài Đặt

| Thành phần | Đường dẫn |
|------------|-----------|
| Agent config | `.agent/agent.md` |
| Main skill | `.agent/skills/seo/SKILL.md` |
| Sub-skills | `.agent/skills/seo-*/SKILL.md` |
| Workflows | `.agent/workflows/seo-*.md` |
| References | `.agent/skills/seo/references/` |
| Scripts | `.agent/skills/seo/scripts/` |
| Schema templates | `.agent/skills/seo/schema/` |

## Xác Minh Cài Đặt

1. Mở workspace trong Antigravity
2. Agent liệt kê 35 SEO skills khả dụng
3. Chạy lệnh master:
   ```
   /seo-run yourdomain.com
   ```

## Cập Nhật

```bash
npx ag-seo-kit update
```

## Gỡ Cài Đặt

```bash
npx ag-seo-kit uninstall --confirm
```
