# Quản Lý License

## Thông Tin License

Mỗi license key hỗ trợ tối đa **3 thiết bị** cùng lúc.

- Mua license tại: [https://antigravityseokit.solann.io/](https://antigravityseokit.solann.io/)
- Quản lý & gia hạn tại: [https://app.solann.io/](https://app.solann.io/)

## Kiểm Tra Trạng Thái

```bash
npx ag-seo-kit status
```

## Quản Lý Thiết Bị

### Xem danh sách thiết bị đã kích hoạt

```bash
npx ag-seo-kit devices
```

### Xóa thiết bị để giải phóng slot

```bash
npx ag-seo-kit devices remove <deviceId>
```

## Quy Tắc License

| Quyền | Cho phép |
|-------|----------|
| ✅ Sử dụng trên tối đa 3 thiết bị | Có |
| ✅ Chỉnh sửa cho mục đích cá nhân/doanh nghiệp | Có |
| ❌ Phân phối lại | Không |
| ❌ Cấp phép phụ (sublicensing) | Không |

## API Endpoints

License được xác thực qua API:

| Method | Endpoint | Mô tả |
|--------|----------|-------|
| `POST` | `/api/seo-kit/licenses/verify` | Xác thực key + kích hoạt thiết bị |
| `GET` | `/api/seo-kit/licenses/status` | Trạng thái license |
| `GET` | `/api/seo-kit/licenses/devices` | Danh sách thiết bị |
| `DELETE` | `/api/seo-kit/licenses/devices/{id}` | Xóa thiết bị |
