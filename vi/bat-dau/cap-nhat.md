# Cập Nhật & Phiên Bản

## Cập Nhật Nhanh

```bash
npx antigravity-seo-kit update
```

Lệnh này sẽ:
1. Xác thực license key hiện tại
2. Kiểm tra phiên bản mới nhất trên server
3. Tải và cập nhật toàn bộ skills, workflows, rules, và agents
4. Giữ nguyên license, thiết bị, và dữ liệu dự án (`seo-projects/`)

## Kiểm Tra Phiên Bản Hiện Tại

```bash
npx antigravity-seo-kit status
```

Output mẫu:

```
SEO Kit Installation Status

  Version:      1.0.7
  License Key:  SK-****-****-XXXX
  Device ID:    abc123...
  Device Name:  DESKTOP-ABC
  Installed:    2026-04-15T09:00:00Z
  Plan:         pro

  Files:        156/156 present
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
