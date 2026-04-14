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
1. ✅ Xác thực license key
2. ✅ Tải và cài đặt skills vào thư mục `.agent/skills/`
3. ✅ Cài đặt workflows vào `.agent/workflows/`
4. ✅ Cấu hình rules vào `.agent/rules/`
5. ✅ Kích hoạt thiết bị (mỗi license sẽ cho phép dùng tối đa số thiết bị tương ứng)

### Xác nhận cài đặt:

```bash
npx antigravity-seo-kit status
```

Kết quả mẫu:

```
✅ Antigravity SEO Kit v0.9.6
License: SK-****-****-XXXX (valid until 2027-04-01)
Devices: 1/3 active
Skills: 44 loaded
Workflows: 12 loaded
Agents: 8 loaded
Rules: 7 loaded
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

## Gỡ Cài Đặt

```bash
npx antigravity-seo-kit uninstall --confirm
```
