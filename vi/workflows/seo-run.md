# /seo-run — Master Orchestrator

## Tổng Quan

Đây là **lệnh duy nhất bạn cần nhớ**. `/seo-run` đọc `project.json` của domain, xác định giai đoạn hiện tại trong vòng đời SEO, hiển thị dashboard trạng thái, và đề xuất hành động tiếp theo.

**Không bao giờ tự động thực thi** — luôn chờ duyệt từ người dùng.

## Cách Sử Dụng

```
/seo-run example.com
```

## State Machine

```
project.json NOT found     → Gợi ý: /seo-onboard
phase = "onboarded"        → Gợi ý: /seo-research (hoặc /seo-audit)
phase = "researched"       → Gợi ý: /seo-audit
phase = "audited"          → Gợi ý: /seo-strategy
phase = "strategized"      → Gợi ý: /seo-execute
phase = "executed"         → Gợi ý: /seo-monitor
phase = "monitoring"       → Dashboard, gợi ý re-audit
```

## Các Bước Thực Hiện

1. **Phân tích domain** từ input (loại bỏ protocol, www, trailing path)
2. **Kiểm tra dự án**: Tìm `seo-projects/{domain-slug}/project.json`
   - Không tìm thấy → "Phát hiện dự án mới" → gợi ý `/seo-onboard`
3. **Đọc project.json** và lấy trường `phase`
4. **Hiển thị Status Dashboard**:
   ```markdown
   ## 📊 SEO Project: {domain}

   | Trường | Giá trị |
   |--------|---------|
   | **Phase** | {phase} ({emoji}) |
   | **Health Score** | {score}/100 |
   | **Lần chạy cuối** | {date} |
   | **Ngành** | {industry} |
   | **Tổng số lần chạy** | {count} |
   ```
5. **Đề xuất bước tiếp** (KHÔNG tự thực thi):
   ```markdown
   ### 🎯 Bước Tiếp Theo Khuyến Nghị
   **→ /seo-{next-phase}** — {mô tả}
   Kích hoạt {N} kỹ năng: {danh sách}
   **Tiếp tục?** (có / không / nhảy đến phase cụ thể)
   ```
6. **Chờ duyệt**:
   - "có" / "proceed" / "tiếp" → ủy quyền cho workflow tương ứng
   - "skip to {phase}" → nhảy đến phase đó
   - "không" → dừng

## Phase Emojis

| Phase | Emoji | Mô tả |
|-------|-------|-------|
| (mới) | 🆕 | Dự án chưa tạo |
| onboarded | 📋 | Setup xong, sẵn sàng nghiên cứu/audit |
| researched | 🔎 | Nghiên cứu xong, sẵn sàng audit |
| audited | 🔍 | Audit xong, sẵn sàng chiến lược |
| strategized | 🧠 | Chiến lược xong, sẵn sàng thực thi |
| executed | ⚡ | Sửa lỗi xong, sẵn sàng giám sát |
| monitoring | 📈 | Đang theo dõi hiệu quả |

## Quy Tắc

- KHÔNG BAO GIỜ tự thực thi phase mà không có duyệt từ người dùng
- Luôn hiển thị dashboard trước khi đề xuất
- Nếu project không có trường `phase` (legacy) → coi như "onboarded"
