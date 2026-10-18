# 🚀 Hướng dẫn Deploy BCK Profile lên Render

## Bước 1: Chuẩn bị files (ĐÃ XONG)
Folder `C:\Users\kiet8\Downloads\profile\` có:
- ✅ `profile.html` - Trang chính
- ✅ `logo.svg` - Logo BCK
- ✅ `music.mp3` - Nhạc nền
- ✅ `README.md` - Mô tả

## Bước 2: Push lên GitHub

### Nếu bạn đã có repo `bck-profile` rồi:

Mở **Git Bash** hoặc **PowerShell** tại folder `profile`:

```bash
cd C:\Users\kiet8\Downloads\profile

git init
git add .
git commit -m "BCK System V.I.P Profile"
git branch -M main
git remote add origin https://github.com/USERNAME/bck-profile.git
git push -u origin main
```

### Nếu CHƯA có repo:

1. Vào https://github.com → **New repository**
2. Đặt tên: `bck-profile`
3. Chọn **Public**
4. **KHÔNG** tích "Add README" (vì đã có)
5. Click **Create repository**
6. Chạy lệnh trên với URL repo của bạn

## Bước 3: Deploy lên Render

1. Vào https://render.com → **Sign up** (dùng GitHub)
2. Click **New +** → **Static Site**
3. Click **Connect GitHub** → Chọn repo `bck-profile`
4. Cấu hình:
   - **Name**: `bck-profile`
   - **Branch**: `main`
   - **Publish Directory**: `.` (dấu chấm)
5. Click **Create Static Site**
6. Đợi 1-2 phút → Xong!

## Bước 4: Lấy link

Sau khi deploy xong, bạn sẽ có link dạng:
```
https://bck-profile.onrender.com
```

Đây là link public, ai cũng vào được! 🎉

## 🎯 Tùy chọn nhanh hơn

### Netlify Drop (30 giây):
1. Vào https://app.netlify.com/drop
2. Kéo thả folder `profile` vào trang
3. Có link ngay! `https://random-name-123.netlify.app`

### Vercel (1 phút):
1. Vào https://vercel.com → Sign up bằng GitHub
2. **Add New Project** → Import repo `bck-profile`
3. Click **Deploy** → Xong!

## ⚠️ Lưu ý

- File `music.mp3` phải nhỏ hơn **100MB** (file hiện tại ~1.5MB ✅ OK)
- Nếu file quá lớn, upload lên Google Drive / Dropbox rồi sửa link trong HTML
- Nhạc có thể không tự phát do chính sách trình duyệt → Click chuột 1 lần là phát

## 🎨 Tùy chỉnh

- **Đổi LED text**: Sửa trong `profile.html` tìm `led-text`
- **Đổi video**: Thay link trong `<video>` tag
- **Đổi nhạc**: Thay file `music.mp3`
- **Đổi màu**: Tìm `#a855f7` (tím) và `#06b6d4` (cyan) trong file

---
© 2026 BCK SYSTEM - Bùi Chí Kiệt
