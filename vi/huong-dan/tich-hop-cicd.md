# Tích Hợp Tự Động Hóa CI/CD (Cho DevOps)

Antigravity SEO Kit không chỉ hoạt động trên local terminal của bạn. Kỹ năng `devops-engineer` cho phép mang toàn bộ sức mạnh Master Script của SEO Kit lên pipeline tự động hóa như GitHub Actions hoặc GitLab CI.

## 1. Mục Đích

Tự động chặn các Pull Request / Merge Request nếu:
- Mã nguồn dính lỗi bảo mật (OWASP).
- Điểm Core Web Vitals giả lập bị rớt thảm hại.
- Mất các thẻ SEO quan trọng hoặc gãy Schema.

## 2. GitHub Actions (Ví Dụ Mẫu)

Dưới đây là đoạn cấu hình `.github/workflows/seo-kit-verify.yml`. Pipeline này sẽ chạy lệnh `verify_all.py` mỗi khi có người push code lên nhánh `main`.

```yaml
name: Antigravity Verification Pipeline

on:
  push:
    branches: [ "main", "dev" ]
  pull_request:
    branches: [ "main" ]

jobs:
  verify:
    runs-on: ubuntu-latest
    
    steps:
    - name: Checkout Code
      uses: actions/checkout@v3

    - name: Setup Python
      uses: actions/setup-python@v4
      with:
        python-version: '3.12'

    - name: Cài Đặt Antigravity SEO Kit Scripts
      run: |
        npm install -g antigravity-seo-kit@latest
        pip install -r .agent/scripts/requirements.txt
        
    - name: Chạy Master Audit Script (Lighthouse + Security + Schema)
      run: |
        python .agent/scripts/verify_all.py --strict-mode
        
    # Bước này chỉ chạy nếu script trên pass
    - name: Build & Deploy
      if: success()
      run: npm run build
```

## 3. Cách Hoạt Động (Strict Mode)
Lưu ý thẻ `--strict-mode` khi chạy `verify_all.py`. Ở chế độ này, Script sẽ trả về Exit Code `1` (báo lỗi làm hỏng Pipeline) nếu:
- `security_scan.py` tìm thấy >0 lỗi Critical.
- `lighthouse_audit.py` chấm điểm Perfomance < 85.
- `webmcp_audit.py` phát hiện mất Action Schema.

> [!WARNING]
> Việc cấu hình `--strict-mode` đòi hỏi đội Dev phải viết code rất chuẩn. Nếu bạn mới tích hợp, có thể chạy thử nghiệm ở Warning Mode (bỏ thẻ `--strict-mode`) để pipeline chỉ cảnh báo chứ không chặn Deploy.
