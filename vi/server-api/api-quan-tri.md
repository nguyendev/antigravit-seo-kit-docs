# API Quản Trị

Endpoints cho admin: quản lý licenses, tenants, reports. Yêu cầu Bearer token qua OpenIddict OAuth2 (client_credentials).

## Licenses

### GET /api/seo-kit/admin/licenses

Danh sách tất cả licenses (phân trang).

### POST /api/seo-kit/admin/licenses

Tạo license mới.

### PUT /api/seo-kit/admin/licenses/{id}

Cập nhật license.

### DELETE /api/seo-kit/admin/licenses/{id}

Vô hiệu hóa license.

## Tenants

### GET /api/seo-kit/admin/tenants

Danh sách tenants.

### POST /api/seo-kit/admin/tenants

Tạo tenant mới (khi user mua license).

## Reports

### GET /api/seo-kit/admin/reports/usage

Báo cáo sử dụng license theo thời gian.

### GET /api/seo-kit/admin/reports/revenue

Báo cáo doanh thu.
