# Xử Lý Sự Cố

## Lỗi Cài Đặt

### "Cannot connect to license server"

- Kiểm tra kết nối internet
- Server tạm thời không khả dụng → thử lại sau vài phút
- Firewall/proxy chặn → cho phép `app.solann.io` và `antigravityseokit.solann.io`

### "Download failed" hoặc "Download too large"

- Kiểm tra kết nối internet ổn định
- Thử lại: `npx antigravity-seo-kit update`

### "License key is expired or invalid"

- Kiểm tra: `npx antigravity-seo-kit status`
- Key hết hạn → gia hạn tại [app.solann.io](https://app.solann.io/)

### "Maximum devices reached (3/3)"

- Xem danh sách: `npx antigravity-seo-kit devices`
- Xóa thiết bị cũ: `npx antigravity-seo-kit devices remove <deviceId>`

## Lỗi Sử Dụng

### "Skills not found"

- Cập nhật: `npx antigravity-seo-kit update`
- Kiểm tra: `npx antigravity-seo-kit status` (xem Files count)

### "Domain not reachable"

- Kiểm tra URL hợp lệ (cần `https://`)
- Domain chưa live: sử dụng chế độ Greenfield (`phase: greenfield`)

### Pre-scan thất bại

- Kiểm tra kết nối internet
- Domain có thể chặn bots → thử flag `--googlebot`

### Agent không đúng

- Gõ `@seo-auditor` để load agent cụ thể
- Xem [Routing tự động](kien-truc/he-thong-agent.md#routing-tự-động)

## Liên Hệ Hỗ Trợ

- Email: support@solann.io
- Quản lý license: [app.solann.io](https://app.solann.io/)
