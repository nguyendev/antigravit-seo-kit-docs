# seo-information-gain — Phân Tích Thông Tin Hữu Ích

## Mô Tả

Kỹ năng cốt lõi giúp nội dung của bạn vượt qua các đối thủ trên SERP bằng cách phân tích **Information Gain (IG)**. Công cụ này so sánh nội dung của bạn với Top 10 đối thủ để tìm ra những điểm thông tin độc đáo, góc nhìn mới, hoặc dữ liệu mà đối thủ chưa đề cập. Nó giúp bạn đạt được điểm E-E-A-T cao hơn và tránh bị bộ lọc nội dung spam của Google nhắm tới.

## Agent Phụ Trách

- `seo-content-authority` (Pre-creation IG strategy)
- `seo-creator` (Post-creation IG validation)

## Chức Năng Chính

- **Content Gap Analysis**: Nhận diện những thực thể (entities), câu hỏi (FAQs) và subtopics mà đối thủ bỏ sót.
- **IG Brief Generation**: Tự động tạo Content Brief chứa chiến lược Information Gain (ví dụ: cần thêm bảng so sánh, số liệu độc quyền, case study).
- **Post-Creation IG Scoring**: Chấm điểm mức độ "độc bản" của bài viết so với SERP sau khi hoàn thành.
- **Data Extractor**: Tự động trích xuất các câu trích dẫn, góc nhìn, và dữ liệu có giá trị từ source context.

## Scopes & Script Tự Động

Kỹ năng này hoạt động chủ yếu thông qua script CLI:
- `information_gain_analyzer.py`:
  - `--mode pre`: Phân tích trước khi viết để lên cấu trúc (sinh IG Brief).
  - `--mode post`: Đánh giá bài viết sau khi hoàn thành và chấm điểm IG Score.

## Khi Nào Dùng

- "Làm sao để bài viết này hay hơn đối thủ?"
- "Phân tích IG của từ khóa này"
- "Tạo content brief với information gain"
- Bất cứ khi nào bạn chạy lệnh `/seo-write` (Kỹ năng này tự động được gọi trong Step 2 và Step 5).

## Workflow Liên Quan

- `/seo-strategy` — Xây dựng chiến lược nội dung cấp độ cao.
- `/seo-write` — Pipeline 5 bước tạo nội dung tự động chuẩn SEO.
