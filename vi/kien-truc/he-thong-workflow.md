# Hệ Thống Workflow

Workflows là orchestrators kích hoạt nhiều skills theo thứ tự tối ưu.

## Vòng Đời

```
ONBOARD → RESEARCH → AUDIT → STRATEGY → EXECUTE → MONITOR → (lặp lại)
```

## Nguyên tắc

- **Suggest + Approve**: Không tự thực thi, luôn chờ duyệt
- **Phase tracking**: Mỗi workflow cập nhật `phase` trong `project.json`
- **Deep-dives**: `/seo-llm-visibility`, `/seo-social-commerce`, `/seo-local-suite` không đổi phase
- **Anti-hallucination**: Mọi output gắn tag nguồn dữ liệu
