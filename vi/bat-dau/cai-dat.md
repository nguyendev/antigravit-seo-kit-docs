# Cài Đặt Chi Tiết

Hướng dẫn từng bước cài đặt Antigravity SEO Kit, bao gồm cài Antigravity, tạo project, và kích hoạt SEO Kit.

## Bước 1: Cài Đặt Google Antigravity

Antigravity là nền tảng AI agent của Google DeepMind. SEO Kit chạy bên trong Antigravity.

1. Truy cập [deepmind.google/technologies/antigravity](https://deepmind.google/technologies/antigravity/)
2. Tải và cài đặt Antigravity cho hệ điều hành của bạn (Windows, macOS, Linux)
3. Đăng nhập bằng tài khoản Google

## Bước 2: Tạo Project Mới Trong Antigravity

Sau khi cài đặt Antigravity, bạn cần tạo một **project** (dự án) để chứa SEO Kit:

1. Mở Antigravity
2. Nhấn **"Open Folder"** (Nên tạo thư mục trống và mở thư mục đó)

> 📁 **Ghi nhớ**: Đây là thư mục gốc mà SEO Kit sẽ tạo file `seo-projects/` bên trong.

## Bước 3: Mở Terminal Trong Antigravity

Antigravity có **terminal tích hợp** để chạy lệnh:

1. Trong giao diện Antigravity, tìm phần **Terminal** (thường ở phía dưới)
2. Hoặc sử dụng phím tắt (thường là `` Ctrl+` `` hoặc `Cmd+J` trên macOS)
3. Terminal sẽ mở ra với đường dẫn đến thư mục project của bạn

## Bước 4: Cài Đặt SEO Kit

Trong terminal Antigravity, chạy lệnh:

```bash
npx antigravity-seo-kit install --key=SK-XXXX-XXXX-XXXX
```

Thay `SK-XXXX-XXXX-XXXX` bằng license key bạn đã mua tại [antigravityseokit.solann.io](https://antigravityseokit.solann.io/).

### Quá trình tự động:

SEO Kit sẽ:
1. ✅ Xác thực license key với server
2. ✅ Tải assets từ server (skills, workflows, agents, rules)
3. ✅ Giải nén và cài đặt vào thư mục `.agent/`
4. ✅ Lưu manifest vào `.seo-kit-license` (danh sách files đã cài)
5. ✅ Kích hoạt thiết bị (mỗi license cho phép tối đa 3 thiết bị)

### Xác nhận cài đặt:

```bash
npx antigravity-seo-kit status
```

Kết quả mẫu:

```
SEO Kit Installation Status

  Version:      1.0.0
  License Key:  SK-****-****-XXXX
  Device ID:    abc123...
  Device Name:  DESKTOP-ABC
  Installed:    2026-04-15T09:00:00Z
  Plan:         pro

  Files:        156/156 present
```

## Bước 5: Bắt Đầu Sử Dụng

Sau khi cài đặt thành công, bạn sử dụng SEO Kit bằng cách **chat** với AI agent trong Antigravity. Không cần mở terminal nữa — chỉ cần gõ lệnh vào khung chat:

```
/seo-run yourdomain.com
```

SEO Kit sẽ tự phát hiện đây là dự án mới và hướng dẫn bạn từng bước.

> 💡 **Xem tiếp**: [Dự án đầu tiên](du-an-dau-tien.md) để được hướng dẫn chi tiết cách setup dự án SEO đầu tiên.

## Cập Nhật

```bash
npx antigravity-seo-kit update
```

Xem chi tiết tại [Cập nhật & Phiên bản](cap-nhat.md).

## Gỡ Cài Đặt

```bash
npx antigravity-seo-kit uninstall --confirm
```

> ⚠️ Lệnh này xóa toàn bộ SEO Kit files. Dữ liệu dự án trong `seo-projects/` **KHÔNG bị xóa**.
