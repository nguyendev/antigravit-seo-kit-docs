# Hướng Dẫn: Lập Trình Web Chuẩn SEO (Từ Code Đến Rank)

Bài hướng dẫn này sẽ demo cách sử dụng The Grand Unification (sự kết hợp giữa Web Development Domain và SEO Domain) của Antigravity SEO Kit để dựng một website tối ưu Core Web Vitals, Schema, và WebMCP từ những dòng code đầu tiên.

## Bối Cảnh Thực Tế

Thay vì viết code xong mới lo đi "tối ưu SEO" (cách làm truyền thống tốn nhiều thời gian sửa lỗi), chúng ta sẽ sử dụng kiến trúc **"Code để Rank"**. Mọi components được sinh ra bởi các Web Agents sẽ lập tức được SEO Agents kiểm duyệt.

---

## Bước 1: Khởi Tạo Dự Án (Web Creation)

Sử dụng lệnh tạo project để gọi `web-orchestrator`:

```bash
/web-create blog cá nhân với Next.js
```

Lúc này, hệ thống tự động:
1. Xác định Stack: React + Next.js App Router.
2. Gọi `project-planner` để chia nhỏ task.
3. Gọi `web-frontend-specialist` và yêu cầu **KHÔNG** sử dụng client-side rendering (`"use client"`) ở những nơi không cần thiết để tối ưu LCP (Largest Contentful Paint).

---

## Bước 2: Thiết Kế Giao Diện & Tối Ưu Vitals (Web Design)

Tiếp theo, bạn cần làm UI đẹp và chuẩn Accessibility:

```bash
/web-ui-design thiết kế trang chủ màu dark mode, dùng Tailwind CSS
```

Agent `web-frontend-specialist` sẽ can thiệp. Quy tắc hệ thống buộc Agent này:
- Tránh dùng thẻ `<div>` bừa bãi. Sử dụng Semantic HTML (`<main>`, `<article>`, `<aside>`).
- Cấu hình file `globals.css` để định nghĩa biến CSS, tránh viết inline utility nhồi nhét.
- Dùng `next/image` thay cho `<img>` để auto lazy load và optimize định dạng WebP.

---

## Bước 3: Tích Hợp Agentic SEO & WebMCP

Đây là sự kết hợp với SEO Domain. Bạn muốn site này tương tác được với các AI Agent như ChatGPT hay Perplexity.

```bash
/seo-execute tạo WebMCP schema cho API lấy bài viết
```

`seo-ai-search` sẽ vào việc:
- Chạy script `webmcp_generator.py` vào source code.
- Tạo ra file `.well-known/webmcp` định nghĩa Action Schema.
- Thêm tag `<link rel="alternate" type="application/json">` vào `<head>` của Next.js.

---

## Bước 4: Kiểm Tra Toàn Diện (Verification)

Trước khi tung ra thị trường, bạn không thể thiếu khâu kiểm duyệt:

```bash
python .agent/scripts/verify_all.py
```

Master Script này sẽ đi qua 5 lớp phòng thủ:
1. **Security**: OWASP check.
2. **Lint**: ESLint & Type Check.
3. **UX & Accessibility**: Báo lỗi nếu thiếu `aria-label` hoặc màu chữ không đủ độ tương phản.
4. **Lighthouse**: Test tự động điểm Core Web Vitals, đảm bảo đạt xanh > 90.
5. **SEO Schema**: Kiểm tra JSON-LD.

---

## Bước 5: Triển Khai (Deployment)

Cuối cùng, dùng lệnh deploy để gọi `devops-engineer`:

```bash
/web-deploy
```

Dự án của bạn sẽ được đóng gói (build) và triển khai thông qua pipeline 5-phase an toàn tuyệt đối.

> [!TIP]
> **Kết Luận**: Với quy trình này, sản phẩm đầu ra đã giải quyết xong 80% công việc Technical SEO ngay khi vừa code xong. Đội ngũ Marketing có thể ngay lập tức bắt tay vào tạo Content mà không lo lỗi kỹ thuật!
