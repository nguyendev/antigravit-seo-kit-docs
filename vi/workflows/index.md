```json
//[doc-seo]
{
    "Description": "Tổng quan hệ thống Workflows của Antigravity SEO Kit — vòng đời 5 giai đoạn với 9 workflow, state machine tự động, và 35 kỹ năng chuyên biệt."
}
```

# Workflows — Hệ Thống Điều Phối SEO

Workflows là **cốt lõi** của SEO Kit. Mỗi workflow là một quy trình nhiều bước, được định nghĩa trong `.agent/workflows/`, kích hoạt các kỹ năng chuyên biệt theo thứ tự tối ưu.

## Vòng Đời SEO (5 Giai Đoạn)

```
┌─────────────┐    ┌─────────────┐    ┌───────────┐    ┌──────────────┐    ┌─────────────┐    ┌─────────────┐
│ 📋 Phase 1  │───▶│ 🔎 RESEARCH │───▶│ 🔍 Phase 2│───▶│ 🧠 Phase 3   │───▶│ ⚡ Phase 4  │───▶│ 📈 Phase 5  │
│  ONBOARD    │    │ (5 skills)  │    │   AUDIT   │    │  STRATEGY    │    │  EXECUTE   │    │  MONITOR    │
│  (4 skills) │    │  tùy chọn   │    │ (9 skills)│    │ (10 skills)  │    │ (6 skills) │    │ (6 skills)  │
└─────────────┘    └─────────────┘    └───────────┘    └──────────────┘    └─────────────┘    └──────┬──────┘
                                                                                                     │
                                                                                                     ▼
                                                                                             Chu kỳ re-audit
```

## State Machine

Mỗi dự án SEO theo dõi giai đoạn hiện tại trong `project.json`:

| Giai đoạn | Thiết lập bởi | Gợi ý tiếp theo |
|-----------|---------------|-----------------|
| *(mới)* | — | `/seo-onboard` |
| `onboarded` | `/seo-onboard` | `/seo-research` hoặc `/seo-audit` |
| `researched` | `/seo-research` | `/seo-audit` |
| `audited` | `/seo-audit` | `/seo-strategy` |
| `strategized` | `/seo-strategy` | `/seo-execute` |
| `executed` | `/seo-execute` | `/seo-monitor` |
| `monitoring` | `/seo-monitor` | `/seo-audit` (chu kỳ mới) |

## Lệnh Duy Nhất Cần Nhớ

```
/seo-run domain.com
```

[`/seo-run`](seo-run.md) đọc `project.json`, xác định giai đoạn hiện tại, hiển thị dashboard, và đề xuất bước tiếp theo. Không bao giờ tự động thực thi — luôn chờ duyệt từ người dùng.

## Danh Sách Workflows

| Workflow | Giai Đoạn | Kỹ Năng | Mục Đích |
|----------|-----------|---------|----------|
| [`/seo-run`](seo-run.md) | Master | Ủy quyền | Tự phát hiện phase, đề xuất bước tiếp |
| [`/seo-onboard`](seo-onboard.md) | Phase 1 | 4 | Khởi tạo dự án, API, thương hiệu, personas |
| [`/seo-research`](seo-research.md) | Nghiên cứu | 5 | Từ khóa, đối tượng, prompt AI, content gap |
| [`/seo-audit`](seo-audit.md) | Phase 2 | 9 | Kiểm tra toàn diện, Health Score |
| [`/seo-strategy`](seo-strategy.md) | Phase 3 | 10 | Chiến lược, roadmap 30/60/90 ngày |
| [`/seo-execute`](seo-execute.md) | Phase 4 | 6 | Tạo bản sửa lỗi, schema, redirects |
| [`/seo-monitor`](seo-monitor.md) | Phase 5 | 6 | Theo dõi, đo lường, so sánh baseline |
| [`/seo-local-suite`](seo-local-suite.md) | Đặc biệt | 2 | GBP, NAP, geo-grid, Maps |
| [`/seo-page`](seo-page.md) | Tiện ích | 4 | Phân tích trang đơn (không đổi phase) |

## Truy Cập Kỹ Năng Trực Tiếp

Bạn luôn có thể gọi bất kỳ kỹ năng nào trực tiếp bằng tên, bỏ qua vòng đời:

```
"Run seo-entity analysis for example.com"
"Check seo-backlink for competitor.com"
```

Gọi trực tiếp **KHÔNG** thay đổi trạng thái phase của dự án.

## Nguyên Tắc Hoạt Động

1. **Suggest + Approve**: AI không bao giờ tự thực thi. Luôn hiển thị trạng thái và chờ duyệt.
2. **Progressive Disclosure**: SKILL.md ngắn gọn, reference files tải khi cần.
3. **Skill Composition**: Mỗi workflow kích hoạt nhiều kỹ năng song song khi có thể.
4. **Quality Gates**: Ngưỡng tích hợp ngăn đề xuất sai (ví dụ: giới hạn location pages).
