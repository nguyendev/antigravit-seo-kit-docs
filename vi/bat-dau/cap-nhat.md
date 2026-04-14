# Cập Nhật & Phiên Bản

## Cập Nhật Nhanh

```bash
npx antigravity-seo-kit update
```

Lệnh này sẽ:
1. Xác thực license key hiện tại
2. Kiểm tra phiên bản mới nhất
3. Cập nhật toàn bộ skills, workflows, rules, và agents
4. Giữ nguyên license và dữ liệu dự án

## Kiểm Tra Phiên Bản Hiện Tại

```bash
npx antigravity-seo-kit status
```

Output mẫu:

```
SEO Kit Installation Status

  Version:      0.9.6
  License Key:  SK-****-****-XXXX
  Device ID:    abc123...
  Skills:       44/44 installed
  Workflows:    12/12 installed
  Agents:       8/8 installed
  Rules:        7/7 installed
```

## Gỡ Cài Đặt

```bash
npx antigravity-seo-kit uninstall --confirm
```

> ⚠️ Lệnh này xóa toàn bộ skills, workflows, agents, và rules. Dữ liệu dự án trong `seo-projects/` **KHÔNG bị xóa**.

## Cài Đặt Lại

Nếu cần cài lại hoàn toàn:

```bash
npx antigravity-seo-kit install --key=SK-XXXX-XXXX-XXXX
```

## Hỗ Trợ

- Lỗi cập nhật → Email: support@solann.io
- Quản lý license: [app.solann.io](https://app.solann.io/)
