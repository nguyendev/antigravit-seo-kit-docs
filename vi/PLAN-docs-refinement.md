# Project Plan: Rà Soát & Hoàn Thiện Docs (Docs Refinement)

## Overview
Dự án bổ sung các thành phần còn thiếu để tài liệu Antigravity SEO Kit dễ hiểu hơn, tập trung vào việc hiển thị đầy đủ các lệnh lập trình web, luật hệ thống web, và quan trọng nhất là bài hướng dẫn kết hợp thực tế giữa Code và SEO.

## Project Type
WEB (Documentation)

## Success Criteria
- Danh sách lệnh `cli/lenh.md` bao phủ 100% lệnh SEO và Web.
- Quy tắc vận hành `quy-tac.md` bao gồm cả luật Web Development.
- Có bài hướng dẫn thực hành (tutorial) "Từ Code Đến Rank".

## Task Breakdown

### 1. Cập Nhật Danh Sách Lệnh CLI
- **Agent**: `documentation-writer`
- **Skills**: `documentation-templates`
- **INPUT**: `vi/cli/lenh.md`
- **OUTPUT**: Thêm 11 `/web-*` workflows và shared scripts.
- **VERIFY**: Các lệnh có mặt đầy đủ trong file.

### 2. Cập Nhật Quy Tắc Vận Hành
- **Agent**: `documentation-writer`
- **Skills**: `documentation-templates`
- **INPUT**: `vi/kien-truc/quy-tac.md`
- **OUTPUT**: Thêm `web-core.md` và `web-auto-routing.md`. Đổi tiêu đề thành 7 Rules.
- **VERIFY**: Nội dung bao quát kiến trúc mới.

### 3. Viết Hướng Dẫn Lập Trình Web Chuẩn SEO
- **Agent**: `web-frontend-specialist` (để đảm bảo hiểu quy trình code)
- **Skills**: `plan-writing`, `seo-agentic`
- **INPUT**: `vi/huong-dan/lap-trinh-web-chuan-seo.md`
- **OUTPUT**: Bài tutorial kết nối `/web-create`, `/web-ui-design` với `/seo-execute`.
- **VERIFY**: Đọc trôi chảy, đúng kỹ thuật.

### 4. Cập Nhật docs-nav.json
- **Agent**: `web-backend-specialist`
- **Skills**: `json-validation`
- **INPUT**: `vi/docs-nav.json`
- **OUTPUT**: Thêm link tới bài tutorial mới.
- **VERIFY**: JSON valid.

## Phase X: Verification
- [ ] Chạy JSON validation.
- [ ] Đọc thử lại luồng bài hướng dẫn xem có dễ hiểu với người mới hay không.
