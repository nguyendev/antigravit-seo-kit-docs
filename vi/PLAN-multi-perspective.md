# Project Plan: Bổ Sung Docs Đa Góc Nhìn (Multi-Perspective Docs)

## Overview
Dự án bổ sung các bài viết chuyên sâu nhằm phục vụ riêng biệt cho 3 nhóm đối tượng chính của Antigravity SEO Kit: Developer (Code Examples), Marketer (Content workflows), và DevOps (CI/CD Automation).

## Project Type
WEB (Documentation)

## Success Criteria
- Developer có file `react-chuan-seo.md` chứa snippet code Next.js mẫu.
- Marketer có bài hướng dẫn `viet-bai-information-gain.md`.
- DevOps có file hướng dẫn `tich-hop-cicd.md` kèm mẫu GitHub Actions.
- Menu điều hướng được cập nhật đầy đủ và hợp lệ.

## Task Breakdown

### 1. Dành Cho Developer: React Chuẩn SEO
- **Agent**: `documentation-writer` & `web-frontend-specialist`
- **INPUT**: Cần tạo mới `vi/ky-nang/xay-dung-web/react-chuan-seo.md`
- **OUTPUT**: Bài viết chi tiết về Server Components, cách tránh Waterfalls, kèm ví dụ code `layout.tsx` tối ưu LCP và Schema.
- **VERIFY**: Code blocks đúng chuẩn Next.js App Router.

### 2. Dành Cho Marketer: Viết Bài với Information Gain
- **Agent**: `documentation-writer` & `seo-creator`
- **INPUT**: Cần tạo mới `vi/huong-dan/viet-bai-information-gain.md`
- **OUTPUT**: Hướng dẫn dùng lệnh `/seo-write`, cách đọc điểm IG Score, và chiến lược chèn dữ liệu độc quyền (Trust Tier 0).
- **VERIFY**: Dễ hiểu, tập trung vào kết quả đầu ra thay vì kỹ thuật.

### 3. Dành Cho DevOps: Tích hợp CI/CD
- **Agent**: `documentation-writer` & `devops-engineer`
- **INPUT**: Cần tạo mới `vi/huong-dan/tich-hop-cicd.md`
- **OUTPUT**: Hướng dẫn đưa `verify_all.py` vào GitHub Actions để chặn các thay đổi làm rớt điểm Web Vitals hoặc hổng bảo mật.
- **VERIFY**: YAML script hợp lệ.

### 4. Cập Nhật docs-nav.json
- **Agent**: `web-backend-specialist`
- **INPUT**: `vi/docs-nav.json`
- **OUTPUT**: Thêm 3 links mới vào các mục thích hợp.
- **VERIFY**: JSON validation.

## Phase X: Verification
- [ ] Chạy JSON validation bằng Python.
- [ ] Review toàn bộ các link mới đảm bảo không bị 404.
