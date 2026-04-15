# Ghi Chú Phát Hành

## v1.0.0 (2026-04-15)

### Mới

- **Hệ thống cài đặt mới**: Installer giờ tải assets từ server (download-based), thay vì copy file local. Manifest lưu danh sách files trong `.seo-kit-license`
- **8 AI Agents chuyên biệt**: seo-auditor (10 skills), seo-strategist (6), seo-content-writer (6), seo-ai-specialist (7), seo-local-expert (3), seo-growth-hacker (9), seo-data-analyst (4), seo-migration-expert (2)
- **12 workflows**: 10 static + 2 dynamic meta-workflows (`/seo-run`, `/seo-auto-run`)
- **Agent routing tự động**: AI tự chọn agent phù hợp dựa trên lệnh, ý định, hoặc domain
- **Cross-agent workflow**: `/seo-execute` kích hoạt skills từ 5 agents khác nhau
- **Shared skills**: 3 skills chia sẻ giữa agents (seo-content, seo-source-context, seo-geo) với mục đích khác nhau

### Thay Đổi

- Installer: copy local → download `.tar.gz` từ server
- Status command: hiển thị Device Name, Plan, manifest file count
- License file: `.seo-kit-license` giờ chứa `installedFiles` manifest

### Bảo Mật

- Path traversal prevention trong tar extraction
- Download size limit 50MB
- HTTPS enforcement cho license verification

---

## v0.9.0 (2026-04-01)

### Mới

- 44 kỹ năng chuyên biệt (tăng từ 35)
- 11 workflows (thêm `/seo-llm-visibility`, `/seo-social-commerce`)
- Nhóm **Vietnam Market**: Zalo OA, Cốc Cốc AI, Video Transcript
- Nhóm **AI & GEO**: fan-out generator, llms.txt, CiteMET, brand sentiment
- Anti-hallucination system toàn diện
- Smart routing (AI Search → GEO workflow, Social → Social Commerce workflow)

### Thay Đổi

- Strategy workflow: 12 kỹ năng (từ 10)
- Execute workflow: 10 kỹ năng (từ 6)
- Monitor workflow: 8 kỹ năng (từ 6)
- Research workflow: 6 kỹ năng (từ 5)
