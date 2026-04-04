# Server API

SEO Kit License Server quản lý license keys, thiết bị, và tenant cho hệ thống licensing. Được xây dựng trên ABP Framework với DDD architecture.

## Endpoints

| Nhóm | Mô tả |
|------|-------|
| [API Công Khai](api-cong-khai.md) | Xác thực license, quản lý thiết bị |
| [API Quản Trị](api-quan-tri.md) | CRUD licenses, tenants, reports |

## Authentication

- Public API: License key trong header `X-License-Key`
- Admin API: Bearer token via OpenIddict OAuth2
