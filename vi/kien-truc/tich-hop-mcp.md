# Tích Hợp MCP

SEO Kit sử dụng Model Context Protocol (MCP) để kết nối dữ liệu bên ngoài.

## MCP là gì?

MCP (Model Context Protocol) là tiêu chuẩn mở cho phép AI agents truy cập dữ liệu và công cụ bên ngoài thông qua server-client protocol.

## Provider Priority

Khi nhiều extensions khả dụng, SEO Kit ưu tiên theo thứ tự:

```
DataForSEO > Ahrefs > Semrush > Không có (HTML-only)
```

## Cấu Hình

MCP servers cấu hình trong Antigravity settings:

```json
{
  "mcpServers": {
    "dataforseo": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-dataforseo"],
      "env": {
        "DATAFORSEO_LOGIN": "xxx",
        "DATAFORSEO_PASSWORD": "xxx"
      }
    },
    "ahrefs": {
      "command": "npx",
      "args": ["-y", "@anthropic/mcp-ahrefs"],
      "env": {
        "AHREFS_API_KEY": "xxx"
      }
    }
  }
}
```

## Tự Phát Hiện

Workflows tự động kiểm tra MCP availability trước khi chạy:
1. Đọc danh sách MCP servers đã đăng ký
2. Kiểm tra kết nối
3. Nếu không có → fallback sang phân tích HTML thuần
4. Ghi nhận trong output: `[FETCHED]` vs `[INFERRED]`
