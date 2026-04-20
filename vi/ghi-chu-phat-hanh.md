# Ghi Chú Phát Hành

## v1.0.4 (2026-04-20)

### Mới

- **8 AI Agents chuyên biệt** với routing tự động
- **13 workflows** (11 static + 2 dynamic meta-workflows)
- **46 skills** (49 with shared) — thêm `seo-writer`, `seo-content-intel`
- **5 rules** restructured — `seo-core.md` hợp nhất anti-hallucination + security + data provider
- `/seo-write` — **Content pipeline 7 bước**: radar → research → outline → draft → multimodal → validate → deploy
- `seo-content-intel` — Intelligence layer cho DNA Context, prompt simulation, brand entity, multimodal check
- Trust Tier hierarchy (Tier 0-6) cho content pipeline

### Thay Đổi

- Installer: assets download từ server thay vì embed trong npm package
- Agent skill counts cập nhật: auditor (10), content-writer (7), ai-specialist (7), growth-hacker (9)
- Shared skills concept: 3 skills chia sẻ giữa agents với mục đích khác nhau

---

## v1.5.0 (2026-03-19)

### Mới

- Frontmatter fields: `user-invokable`, `argument-hint`, `allowed-tools` cho tất cả SKILL.md
- Error handling sections cho tất cả SKILL.md
- Plugin manifest: `.claude-plugin/plugin.json`

### Sửa Lỗi

- Em dash elimination — giảm AI detection signals
- HTML comments trước frontmatter đã xóa

---

## v1.4.0 (2026-03-12)

### Bảo Mật

- Install script: thay `irm | iex` bằng `git clone + powershell -File`
- Version pinning cho install scripts

### Mới

- **GEO agent deployed**: 7 parallel agents (từ 6)
- `--googlebot` flag trong `fetch_page.py` cho SPA/CSR

### Sửa Lỗi

- URL normalization: chấp nhận bare domains
- FAQPage guidance cập nhật
- Python requirement: 3.8+ → 3.10+

---

## v1.3.0 (2026-03-06)

### Mới

- **Extension system**: `extensions/` directory
- **DataForSEO extension**: 22 commands, 9 API modules
- Plugin manifest cho plugin directory

---

## v1.2.1 (2026-02-28)

### Sửa Lỗi

- User-Agent: đổi từ bot-style sang Chrome-like string
- Custom `--user-agent` flag

---

## v1.2.0 (2026-02-19)

### Bảo Mật

- SSRF prevention, path traversal prevention
- venv-based pip install

### Sửa Lỗi

- YAML frontmatter parsing (8 files)
- Windows installer improvements

---

## v1.1.0 (2026-02-07)

### Bảo Mật

- urllib3 ≥2.6.3: CVE-2026-21441 (CVSS 8.9)
- lxml ≥6.0.2, Pillow ≥12.1.0, playwright ≥1.55.1, requests ≥2.32.4

### Mới

- **GEO major enhancement**: brand mention analysis, AI crawler detection, llms.txt, passage-level citability
- LCP Subparts analysis, Schema.org v29.4

---

## v1.0.0 (2026-02-07)

### Mới

- Initial release
- 9 skills, 6 subagents, industry templates
- Core Web Vitals (LCP, INP, CLS)
- E-E-A-T framework (September 2025 Quality Rater Guidelines)
