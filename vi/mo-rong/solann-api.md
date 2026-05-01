# Solann API — Keyword Data Provider

Data provider mặc định của SEO Kit — cung cấp **premium Google Ads keyword data** tối ưu cho AI agent.

> 📌 Đây là **data provider ưu tiên #1** — được dùng trước DataForSEO, Ahrefs, Semrush. Nếu Solann API chưa cấu hình, hệ thống tự fall back sang nguồn khác.

## Tổng Quan

| Thuộc tính | Giá trị |
|-----------|---------|
| Skill | `seo-solann` |
| Scripts | 2 (keyword_volume.py, keyword_suggest.py) |
| Yêu cầu | API key (có sẵn khi mua license) |
| Dependencies | Không (Python stdlib only) |
| Agent | `seo-content-authority`, `seo-intelligence` |

## Tại Sao Solann Là Mặc Định?

- **Premium data**: Dữ liệu trực tiếp từ Google Ads API (volume, CPC, trends chính xác)
- **AI-optimized**: Hỗ trợ ngôn ngữ tự nhiên cho location/language (ví dụ: "vietnam", "tiếng việt")
- **Topic clusters**: Tự phân loại keywords theo semantic groups
- **Zero-dependency**: Không cần `pip install` — chỉ dùng Python stdlib
- **In-house**: Không phát sinh chi phí bên thứ ba

### Thứ Tự Ưu Tiên Provider

```
Solann API (#1) → Google Ads Keyword Planner → DataForSEO → HTML-only
```

## Cài Đặt

Tạo file `.agent/config/solann-api.json`:

```json
{
  "api_key": "sk-xxxx",
  "default_location": "VN",
  "default_language": "vi"
}
```

> 💡 API key được cung cấp khi mua license. Quản lý tại [app.solann.io](https://app.solann.io/).

Nếu chưa cấu hình, SEO Kit sẽ thông báo và tự fall back sang HTML-only mode.

## 2 Scripts

### 1. keyword_volume.py — Keyword Research

Lấy volume + trends + topics + competitor keyword extraction.

```bash
# Theo danh sách từ khóa
python .agent/skills/seo-solann/scripts/keyword_volume.py --keywords "mua sach, dien thoai"

# Theo URL đối thủ (tự trích xuất keywords)
python .agent/skills/seo-solann/scripts/keyword_volume.py --url "https://competitor.com"

# Kết hợp cả hai + tuỳ chỉnh location/language
python .agent/skills/seo-solann/scripts/keyword_volume.py \
  --keywords "seo tool" \
  --url "https://competitor.com" \
  --location vietnam \
  --language vi
```

### 2. keyword_suggest.py — Long-tail Expansion

1 seed keyword → hàng chục biến thể với đầy đủ metrics.

```bash
# Mở rộng cơ bản
python .agent/skills/seo-solann/scripts/keyword_suggest.py --seed "may loc nuoc" --max 30

# Chỉ Google Autocomplete (không Alphabet Soup)
python .agent/skills/seo-solann/scripts/keyword_suggest.py --seed "seo" --max 50 --no-alphabet-soup
```

**Phương pháp mở rộng:**
- Google Autocomplete suggestions
- Alphabet Soup technique (thêm a→j vào seed)
- Tất cả suggestions tự động enriched với volume + trend + topics

## Dữ Liệu Trả Về

Mỗi keyword bao gồm:

| Trường | Mô tả |
|--------|-------|
| `avgMonthlySearches` | Volume trung bình hàng tháng |
| `competition` | LOW / MEDIUM / HIGH |
| `competitionIndex` | Điểm cạnh tranh 0-100 |
| `lowTopOfPageBidMicros` | CPC thấp (÷ 1,000,000 = USD) |
| `highTopOfPageBidMicros` | CPC cao (÷ 1,000,000 = USD) |
| `monthlySearchVolumes[]` | Xu hướng 12 tháng (seasonality) |
| `topicClusters[]` | Nhóm chủ đề semantic |

## Tham Số Chung

| Flag | Mặc định | Mô tả |
|------|---------|-------|
| `--location` | Từ config (`VN`) | Vị trí: "vn", "vietnam", "us", "uk" |
| `--language` | Từ config (`vi`) | Ngôn ngữ: "vi", "tiếng việt", "en" |

## V1 — Tính Năng Hiện Tại

| Tính năng | Trạng thái |
|-----------|-----------|
| Keyword volume | ✅ Active |
| 12-month trends | ✅ Active |
| Topic clusters | ✅ Active |
| Competitor keywords | ✅ Active |
| Long-tail expansion | ✅ Active |
| CPC / bid data | ✅ Active |
| Ranking checker | 🔜 V2 |
| Index checker | 🔜 V2 |

## Xử Lý Sự Cố

| Lỗi | Nguyên nhân | Giải pháp |
|-----|-----------|-----------|
| `400 Bad Request` | Thiếu params hoặc location sai | Kiểm tra lại tham số |
| `401 Unauthorized` | API key không hợp lệ | Cập nhật `solann-api.json` |
| `502 Bad Gateway` | Google Ads API tạm lỗi | Chờ 30s, thử lại |
| `500 Internal Error` | Lỗi server | Thử lại sau, liên hệ support@solann.io |

## Workflow Liên Quan

| Workflow | Cách dùng |
|----------|----------|
| `/seo-research` | Enrichment step 6b: volume + trends cho top keywords |
| `/seo-strategy` | Competitor keyword extraction |
| `/seo-audit` | Keyword gap analysis |

## Kỹ Năng Liên Quan

| Kỹ năng | Vai trò |
|---------|---------|
| [seo-keyword](../ky-nang/nghien-cuu/seo-keyword.md) | Clustering & intent analysis (dùng Solann data) |
| [seo-content-gap](../ky-nang/noi-dung/seo-content-gap.md) | Gap prioritization (dùng Solann volume) |
| [seo-google](../ky-nang/giam-sat/seo-google.md) | GSC/PageSpeed (fallback nếu không có Solann) |
| [DataForSEO](dataforseo.md) | SERP data bổ sung (không thay thế Solann) |
