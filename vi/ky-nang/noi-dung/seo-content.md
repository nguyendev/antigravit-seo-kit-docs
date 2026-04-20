# seo-content — Chất Lượng Nội Dung & E-E-A-T

## Mô Tả

Đánh giá chất lượng nội dung: thin content detection, E-E-A-T scoring, readability, content optimization.

## Agent Phụ Trách

`seo-auditor` (scoring) + `seo-content-writer` (creating) — **shared skill**

## Chức Năng Chính

- **E-E-A-T scoring**: Experience, Expertise, Authoritativeness, Trustworthiness
- **Thin content detection**: Word count, unique value ratio
- **Readability**: Flesch-Kincaid, sentence length, paragraph structure
- **Content scoring**: Comprehensive quality score (0-100)
- **Keyword optimization**: Density, prominence, LSI terms
- **Freshness signals**: Update dates, temporal relevance

## Scripts

| Script | Chức năng |
|--------|----------|
| `content_scorer.py` | Quality scoring toàn diện |

## Khi Nào Dùng

- "content quality", "đánh giá nội dung", "thin content"
- "E-E-A-T", "readability", "content score"

## Workflow Liên Quan

- `/seo-audit` — Content quality trong audit
- `/seo-write` — Content scoring trong pipeline (Step 3, 5)
