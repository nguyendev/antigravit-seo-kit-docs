# Cài Đặt Chi Tiết

Hướng dẫn từng bước cài đặt Antigravity SEO Kit, bao gồm cài Antigravity, tạo project, và kích hoạt SEO Kit.

## Bước 1: Cài Đặt Google Antigravity

Antigravity là nền tảng AI agent của Google DeepMind. SEO Kit chạy bên trong Antigravity.

1. Truy cập [antigravity.google/download](https://antigravity.google/download)
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

  Version:      1.0.7
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

---

## Cài Đặt Python

Antigravity SEO Kit sử dụng Python để chạy các script phân tích (audit, scoring, crawler). Bạn cần cài Python trước hoặc sau khi cài SEO Kit:

**Cách 1: Cài trực tiếp**

Tải và cài đặt Python tại [python.org/downloads](https://www.python.org/downloads/) (≥ 3.11).

> ✅ Khi cài, **nhớ tick ☑ "Add Python to PATH"** để terminal nhận diện được lệnh `python`.

**Cách 2: Cài extension Python trong Antigravity**

1. Mở Antigravity
2. Nhấn `Ctrl + Shift + X` để mở Extensions
3. Tìm và cài **Python** (by Microsoft)

Extension sẽ tự tải Python nếu chưa có.

---

## Extension Khuyên Dùng

Mở panel Extensions (`Ctrl + Shift + X`) trong Antigravity và cài các extension sau:

| Extension | Mục đích |
|-----------|----------|
| **Python** (Microsoft) | Chạy script phân tích SEO |
| **Markdown Preview Enhanced** | Xem preview báo cáo markdown |
| **AG Auto Click & Scroll** | Tự động retry khi lỗi + tự động duyệt |

---

## Xử Lý Lỗi Khi Cài Đặt

### Lỗi: "npx is not recognized"

```
npx : The term 'npx' is not recognized as the name of a cmdlet,
function, script file, or operable program.
```

**Nguyên nhân:** Chưa cài Node.js hoặc chưa thêm vào PATH.

**Cách giải quyết:**

1. Tải và cài đặt Node.js tại [nodejs.org](https://nodejs.org/) (chọn bản **LTS**)
2. Khi cài, **giữ nguyên** tùy chọn "Add to PATH"
3. **Đóng và mở lại** Antigravity (hoặc terminal) để nhận PATH mới
4. Chạy lại lệnh `npx antigravity-seo-kit install --key=...`

### Lỗi: "Running scripts is disabled on this system"

```
npx : File C:\Program Files\nodejs\npx.ps1 cannot be loaded because
running scripts is disabled on this system.
```

**Nguyên nhân:** Windows PowerShell mặc định chặn chạy script bên ngoài.

**Cách giải quyết (khuyên dùng):**

1. **Đóng** cửa sổ terminal/PowerShell hiện tại
2. Mở **Start Menu**, gõ `PowerShell`
3. **Click chuột phải** vào Windows PowerShell → chọn **Run as Administrator**
4. Dán lệnh sau và nhấn Enter:

```powershell
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```

5. Gõ `Y` (hoặc `A`) và nhấn Enter để xác nhận
6. Đóng cửa sổ Admin, quay lại Antigravity và chạy lại lệnh cài đặt

> 💡 Việc này chỉ cần làm **một lần duy nhất**. Sau khi cấp quyền, tất cả lệnh `npx`, `npm` sẽ hoạt động bình thường.
