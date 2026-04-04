# Xử Lý Sự Cố

## Lỗi Thường Gặp

### "License key is expired or invalid"

- Kiểm tra key lại tại `npx ag-seo-kit status`
- Key hết hạn → gia hạn tại [app.solann.io](https://app.solann.io/)

### "Maximum devices reached (3/3)"

- Xóa thiết bị cũ: `npx ag-seo-kit devices remove <deviceId>`
- Xem danh sách: `npx ag-seo-kit devices`

### Agent không nhận diện skills

- Kiểm tra thư mục `.agent/skills/seo-*/SKILL.md` tồn tại
- Restart Antigravity session
- Chạy `npx ag-seo-kit status` để xác minh

### Python scripts lỗi

- Kiểm tra Python version: `python --version` (cần ≥ 3.11)
- Cài đặt dependencies: `pip install -r requirements.txt`
- Kiểm tra quyền truy cập file

### MCP extension không kết nối

- Kiểm tra API credentials trong MCP config
- Test kết nối: `npx ag-seo-kit test-mcp dataforseo`
- Xem logs trong Antigravity console

### Health Score luôn thấp

- Đảm bảo website accessible (không bị block bởi firewall/captcha)
- Kiểm tra robots.txt không chặn crawler
- Chạy `/seo-page <url>` để phân tích trang cụ thể

## Liên Hệ Hỗ Trợ

- Email: support@solann.io
- Quản lý license: [app.solann.io](https://app.solann.io/)
