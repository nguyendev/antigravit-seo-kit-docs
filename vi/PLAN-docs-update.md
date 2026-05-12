# Project Plan: Cập Nhật Tài Liệu Antigravity SEO Kit v1.1.0

## Overview
Dự án cập nhật hệ thống tài liệu công khai (`antigravity-seo-kit-docs`) để phản ánh những thay đổi khổng lồ từ `seo-kit` version 1.0.4 lên 1.1.0. Điểm nhấn là "The Grand Unification" (sáp nhập web-kit vào seo-kit) và sự bổ sung của kỹ năng WebMCP/Information Gain.

## Project Type
WEB (Documentation)

## Success Criteria
- Toàn bộ 24 agents và 77 skills được ánh xạ trên docs.
- Khái niệm "The Grand Unification" và Web Development Domain được giới thiệu rõ ràng.
- `docs-nav.json` phản ánh đầy đủ cấu trúc mới.

## Task Breakdown

### 1. Cập Nhật Core SEO & Kiến Trúc
- **Agent**: `documentation-writer`
- **Skills**: `documentation-templates`
- **INPUT**: `vi/index.md`, `vi/kien-truc/he-thong-agent.md`, `vi/ghi-chu-phat-hanh.md`
- **OUTPUT**: Các file được update version 1.1.0 và kiến trúc đa miền (SEO, Web, Shared).
- **VERIFY**: Version hiển thị là 1.1.0, tổng số 24 agents.

### 2. Cập Nhật SEO Skills Mới
- **Agent**: `documentation-writer`
- **Skills**: `seo-information-gain`, `seo-agentic`
- **INPUT**: Nội dung từ `.agent/skills/`
- **OUTPUT**: Mở rộng `seo-agentic.md` (WebMCP) và tạo mới `seo-information-gain.md`.
- **VERIFY**: Đọc file thành công.

### 3. Tạo Docs cho Web Development Domain
- **Agent**: `documentation-writer`
- **Skills**: `documentation-templates`
- **INPUT**: Cấu trúc mới
- **OUTPUT**: Thư mục `vi/web/` và các trang mô tả Web Workflows/Agents.
- **VERIFY**: Nội dung bao quát được `/web-create`, `/web-enhance`, frontend, backend agents.

### 4. Cập Nhật Navigation Navigation
- **Agent**: `web-frontend-specialist`
- **Skills**: `json-validation`
- **INPUT**: `vi/docs-nav.json`
- **OUTPUT**: Cây thư mục sidebar hỗ trợ SEO, Web, và Shared.
- **VERIFY**: `Get-Content vi/docs-nav.json | ConvertFrom-Json` thành công.

## Phase X: Verification
- [ ] Chạy JSON validation.
- [ ] Kiểm tra lỗi chính tả và đường dẫn hỏng.
- [ ] Xác nhận toàn bộ version references (1.0.4 -> 1.1.0).
