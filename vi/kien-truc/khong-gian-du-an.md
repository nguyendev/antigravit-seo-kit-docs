# Không Gian Dự Án (Domain Workspaces)

## Cấu Trúc

Mỗi domain tạo một workspace riêng biệt:

```
seo-projects/
├── example-com/               ← Domain workspace
│   ├── project.json           ← State, config, history
│   ├── competitors.json       ← Cached competitors
│   ├── reports/               ← Markdown reports
│   │   ├── onboard-{date}.md
│   │   ├── audit-{date}.md
│   │   ├── strategy-{date}.md
│   │   └── monitor-{date}.md
│   ├── data/                  ← Machine-readable data
│   │   ├── audit-{date}.json
│   │   ├── keywords-{date}.json
│   │   ├── clusters-{date}.json
│   │   └── backlink-{date}.json
│   └── fixes/                 ← Generated fix files
│       └── {date}/
│           ├── meta-tags.html
│           ├── schema-jsonld/
│           └── robots.txt
└── another-site-org/          ← Another domain
    └── ...
```

## project.json

```json
{
  "domain": "example.com",
  "slug": "example-com",
  "phase": "audited",
  "health_score": 72,
  "industry": "SaaS",
  "settings": {
    "google_api_tier": 2
  },
  "competitors": ["comp1.com", "comp2.com"],
  "phase_history": [],
  "runs": []
}
```

## Quy Tắc

- Mỗi domain = 1 workspace
- Slug tự tạo từ domain (`.` → `-`, strip `www`)
- Data files dùng date suffix cho versioning
- Reports giữ lại lịch sử (không overwrite)
