# API Công Khai

Endpoints cho người dùng cuối: xác thực license, quản lý thiết bị.

## POST /api/seo-kit/licenses/verify

Xác thực license key và kích hoạt thiết bị.

**Request:**
```json
{
  "licenseKey": "SK-XXXX-XXXX-XXXX",
  "deviceFingerprint": "abc123",
  "deviceName": "My Laptop"
}
```

**Response (200):**
```json
{
  "isValid": true,
  "expiresAt": "2026-12-31T23:59:59Z",
  "deviceId": "d001",
  "remainingDeviceSlots": 2
}
```

## GET /api/seo-kit/licenses/status

Trạng thái license hiện tại.

**Headers:** `X-License-Key: SK-XXXX-XXXX-XXXX`

**Response (200):**
```json
{
  "licenseKey": "SK-****-****-XXXX",
  "plan": "professional",
  "maxDevices": 3,
  "activeDevices": 1,
  "expiresAt": "2026-12-31T23:59:59Z"
}
```

## GET /api/seo-kit/licenses/devices

Danh sách thiết bị đã kích hoạt.

## DELETE /api/seo-kit/licenses/devices/{id}

Xóa thiết bị để giải phóng slot.
