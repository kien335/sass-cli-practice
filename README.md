# Thực hành SASS bằng npm và SASS CLI

Mục tiêu: cài SASS, biên dịch 1 file, bật watch, và biên dịch nhiều file SCSS.

## Kiểm tra cài đặt trên máy Windows

```powershell
node -v
npm.cmd -v
npm.cmd install -g sass
sass.cmd --version
```

Nếu chưa có Node.js, cài từ https://nodejs.org/en/download rồi mở lại Terminal.

## Biên dịch một file

```powershell
sass.cmd styles.scss styles.css
```

## Chế độ watch

```powershell
sass.cmd styles.scss styles.css --watch
```

Sửa biến `$primary` trong `styles.scss`, lưu file và quan sát `styles.css` được cập nhật. Nhấn `Ctrl+C` để dừng.

## Biên dịch nhiều file (thư mục)

```powershell
sass.cmd scss/:css/ --watch
```

Thử sửa `scss/features.scss` hoặc `scss/tags.scss`, lưu file và kiểm tra CSS tương ứng trong `css/`. Nhấn `Ctrl+C` để dừng.

**Chú ý:** Mỗi lệnh `--watch` chiếm một Terminal. Muốn chạy đồng thời hai watcher, mở hai Terminal.

## Kiểm tra kết quả

Mở `index.html` bằng trình duyệt hoặc VS Code Live Server. Có thể chụp ảnh giao diện và Terminal sau khi thực hành để minh chứng.

### Sửa lỗi PowerShell

Nếu lệnh `npm` hoặc `sass` báo lỗi `running scripts is disabled`, sử dụng `npm.cmd` / `sass.cmd` như ở trên. Không cần đặt `Set-ExecutionPolicy Unrestricted` cho toàn máy.
