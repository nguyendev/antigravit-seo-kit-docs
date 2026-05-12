# Viết Bài Với Information Gain (Cho Marketer)

Đây là bí mật giúp các bài viết được tạo bởi hệ thống Antigravity SEO Kit không bao giờ bị Google đánh dấu là "AI Spam". Bí quyết nằm ở quy trình kết hợp kỹ năng `seo-information-gain`.

## 1. Vấn Đề Của LLM Content

AI thông thường (ChatGPT/Claude) khi được yêu cầu "viết một bài SEO" sẽ chỉ tổng hợp lại những gì đã có trên Internet. Nó **không tạo ra giá trị mới**, khiến bài viết dễ dính án phạt của Google Spam Update (Hữu Ích Content Update).

## 2. Giải Pháp: Information Gain (IG)

**Information Gain** là độ bao phủ những dữ liệu độc nhất vô nhị mà bài viết của bạn có, còn đối thủ top 10 thì không có.

Để thao tác với Antigravity SEO Kit, bạn làm theo các bước sau:

### Bước 1: Khởi động quá trình viết với IG Analyzer
Gõ lệnh để agent bắt đầu chạy:

```bash
/seo-write "Cách nuôi mèo Anh lông ngắn"
```

Hệ thống sẽ chạy Script `information_gain_analyzer.py --mode pre` và xuất cho bạn một báo cáo:
- **Câu hỏi đối thủ chưa trả lời**: "Chi phí thú y hàng tháng là bao nhiêu?"
- **Dữ liệu đối thủ chưa có**: Chưa ai có bảng so sánh lượng calo tiêu thụ theo độ tuổi.

### Bước 2: Bơm dữ liệu độc quyền (Trust Tier 0)
Hệ thống sẽ dừng lại và hỏi bạn (Socratic Gate):
> *"Tôi thấy đối thủ chưa có dữ liệu chi phí thú y thực tế. Bạn có hóa đơn hay số liệu thực tế nào từ phòng khám của bạn không?"*

Lúc này, bạn hãy paste dữ liệu **chỉ bạn mới có** vào terminal. Hành động này được Antigravity đánh giá là **Tier 0 Data (Mức độ tin cậy cao nhất)**. Hệ thống sẽ ưu tiên dùng data này hơn bất kỳ thứ gì AI tự biết.

### Bước 3: Hoàn thiện và chấm điểm IG
Hệ thống sẽ viết bài. Sau khi hoàn tất, nó tự chạy `information_gain_analyzer.py --mode post`.

Bạn sẽ nhận được report:
```
- Độ dài: 1500 từ
- SEO Score: 95/100
- Information Gain Score: 8.5/10 (Tốt)
- Dữ liệu độc quyền đã chèn: Bảng chi phí thực tế, Hình ảnh hóa đơn.
```

## Tổng Kết

Chỉ bằng cách trò chuyện với Agent và **cung cấp dữ liệu độc quyền (case study, báo cáo, kinh nghiệm cá nhân)** khi được hỏi, bài viết do AI viết ra đã mang đậm màu sắc cá nhân (E-E-A-T) và đạt chuẩn IG cao nhất!
