# Friend Chat - Mạng xã hội & Nhắn tin đa nền tảng

Friend Chat là dự án mạng xã hội kết hợp nhắn tin thời gian thực, lấy cảm hứng từ Messenger, Zalo và Facebook. Ứng dụng hỗ trợ chat cá nhân, chat nhóm, đăng bài, tương tác, quản lý bạn bè, thông báo real-time, shop, đa ngôn ngữ và nhiều tính năng mở rộng.

## 🚀 Tính năng nổi bật
- Nhắn tin cá nhân & nhóm (text, hình ảnh, video, file, emoji, sticker, voice...)
- Trạng thái tin nhắn: đã gửi, đã nhận, đã đọc
- Quản lý bạn bè, chặn, phân loại
- Đăng bài viết, bình luận, like, share, hashtag, gắn thẻ bạn bè
- Quản lý nhóm, trang (page), shop bán hàng
- Thông báo real-time, trạng thái online/offline
- Hỗ trợ đa ngôn ngữ, tối ưu hiệu suất với index
- Tích hợp lưu trữ media đa nền tảng (local, S3, Cloudinary...)
- Chuẩn bị sẵn cho mở rộng: mini game, gọi thoại/video, AI moderation...

## 🛠️ Công nghệ sử dụng
- **Next.js** (React 19) - Frontend & SSR
- **Prisma ORM** - Quản lý database MySQL
- **TailwindCSS** - Giao diện hiện đại
- **TypeScript** - An toàn & dễ bảo trì
- **Prisma Modules** - Chia schema thành module nhỏ dễ phát triển
- **WebSocket/Socket.io** - Real-time chat & notification
- **Cloud Storage** - AWS S3, Cloudinary, Azure Blob...

## 📁 Cấu trúc thư mục
```
friend-chat/
├── prisma/                # Quản lý schema, migration, seed
│   ├── schema.prisma      # Schema tổng hợp
│   └── modules/           # Các module: user, messaging, posts, shop...
├── src/
│   ├── app/               # Next.js app (pages, layout, css)
│   └── generated/prisma/  # Prisma client tự động sinh
├── public/                # Ảnh, icon, media tĩnh
├── .env                   # Biến môi trường (DB, API key...)
├── package.json           # Thông tin & script dự án
└── README.md              # Tài liệu dự án
```

## ⚡ Hướng dẫn cài đặt & phát triển
1. **Clone dự án & cài đặt phụ thuộc**
   ```bash
   git clone ...
   cd friend-chat
   npm install
   ```
2. **Cấu hình database**
   - Sửa file `.env` với thông tin MySQL:
     ```env
     DATABASE_URL="mysql://root:newpassword@localhost:3306/friendchat"
     ```
3. **Khởi tạo database & Prisma Client**
   ```bash
   npx prisma db push
   npx prisma generate
   ```
4. **Chạy server phát triển**
   ```bash
   npm run dev
   ```
   Truy cập [http://localhost:3000](http://localhost:3000)

## 🧩 Quản lý schema theo module
- Schema chia thành các module nhỏ trong `prisma/modules/`:
  - `user-management.prisma`: Người dùng, bảo mật, quyền riêng tư
  - `friendship.prisma`: Kết bạn, chặn, phân loại
  - `messaging.prisma`: Nhắn tin, media, trạng thái
  - `posts.prisma`: Đăng bài, bình luận, tương tác
  - `shop.prisma`: Sản phẩm, đơn hàng
- Có thể phát triển, test, migrate từng module độc lập

## 🌐 Đa ngôn ngữ & tối ưu hiệu suất
- Bảng `Translation` hỗ trợ lưu nội dung đa ngôn ngữ
- Thêm nhiều index cho các truy vấn phổ biến (authorId, conversationId...)
- Trường `storageProvider` giúp quản lý media linh hoạt

## 🔔 Real-time & mở rộng
- Hỗ trợ trạng thái online, typing, notification real-time
- Chuẩn bị sẵn cho tích hợp Redis, Pusher, WebSocket
- Có thể mở rộng mini game, gọi video, AI moderation...

## 📦 Triển khai & vận hành
- Có thể deploy trên Vercel, AWS, Azure, DigitalOcean...
- Hỗ trợ CI/CD, scaling, CDN cho media
- Theo dõi hiệu suất, cleanup dữ liệu cũ, tối ưu index

## 📚 Tài liệu & phát triển thêm
- Xem chi tiết từng module tại `prisma/modules/README.md`
- Tham khảo Next.js, Prisma, Tailwind, Socket.io docs
- Đóng góp, báo lỗi, ý tưởng: Pull Request hoặc Issues trên GitHub
- Hoặc liên hệ trực tiếp qua Zalo: 0393769711 hoặc Email: qh20812@gmail.com

---

> Dự án Friend Chat hướng tới xây dựng nền tảng mạng xã hội & nhắn tin hiện đại, bảo mật, dễ mở rộng, phục vụ hàng triệu người dùng Việt Nam & quốc tế.
