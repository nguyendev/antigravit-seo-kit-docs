# seo-agentic — SEO Cho AI Agent & WebMCP

## Mô Tả

Đưa SEO vượt ra khỏi ranh giới tìm kiếm thông thường và tiến vào **Agentic Web**. Kỹ năng này biến website của bạn thành một thực thể "có thể tương tác" (machine-readable và tool-ready) đối với các AI Agents (như ChatGPT, Claude, Gemini, Perplexity), sử dụng chuẩn **WebMCP (Web Model Context Protocol)** và Action Schema.

## Agent Phụ Trách

`seo-ai-search` (skill #3/7)

## Các Trụ Cột Chính (Core Components)

### 1. WebMCP Readiness (Chuẩn 2026)
Hỗ trợ tích hợp Model Context Protocol trực tiếp trên nền web:
- **Declarative WebMCP**: Cung cấp API schema tĩnh qua `.well-known/webmcp` (OpenAPI, Swagger) để Agent có thể gọi trực tiếp.
- **Imperative WebMCP**: Expose công cụ trực tiếp thông qua object `navigator.modelContext` cho các browser-native AI agents.
- **Tool Mapping**: Định nghĩa function call (`name`, `description`, `parameters`) từ HTML form thành dạng mà LLM có thể parse và gọi hàm.

### 2. Action Schema Coverage
Sử dụng Schema.org để gán nhãn hành động:
- `SearchAction` (cho thanh tìm kiếm)
- `BuyAction`, `OrderAction` (cho e-commerce)
- `ReserveAction` (cho dịch vụ đặt chỗ)

### 3. API & Endpoint Discoverability
Đảm bảo AI agent có thể tìm thấy dữ liệu máy đọc được:
- Liên kết JSON-LD rõ ràng (vd: URL API cho sản phẩm).
- Pagination và endpoint filtering dễ đoán.
- Sử dụng `<link rel="alternate" type="application/json">`.

### 4. Machine-Readable Commerce
Tối ưu hóa phễu thương mại điện tử cho AI:
- Gắn thẻ `readOnlyHint` cho nội dung thông tin.
- Gắn thẻ `untrustedContentHint` cho UGC (bình luận).
- Giỏ hàng (Cart) và thanh toán (Checkout) phải hoạt động dưới dạng stateful API đơn giản để Agent có thể thêm sản phẩm giúp người dùng.

## Scopes & Script Tự Động

Kỹ năng này đi kèm với 2 script tự động xử lý:
1. `webmcp_audit.py`: Quét toàn bộ website/form để tính điểm **WebMCP Readiness Score** (chiếm 20% tổng điểm Agentic SEO).
2. `webmcp_generator.py`: Tự động convert các Form HTML thông thường thành mã WebMCP tương thích cho AI.

## Khi Nào Dùng

- "agentic SEO", "AI agent optimization", "action schema", "webmcp", "model context protocol"
- "tối ưu web cho chatgpt tự mua hàng", "api discoverability"

## Workflow Liên Quan

- `/seo-llm-visibility` — Workflow chạy phân tích GEO, llms.txt, và Agentic Readiness.
- `/web-create` — Các API backend được tạo ra bởi Web Agent mặc định sẽ có discoverability hỗ trợ WebMCP.
