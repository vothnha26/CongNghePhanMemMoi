# Node.js CRUD với Express, Sequelize & MySQL

Dự án này là một ứng dụng web cơ bản thực hiện các chức năng CRUD (Create, Read, Update, Delete) người dùng, sử dụng Express.js làm backend framework, Sequelize làm ORM và MySQL làm cơ sở dữ liệu.

## 🛠 Công nghệ sử dụng

- **Backend:** Node.js, Express.js
- **ORM:** Sequelize
- **Database:** MySQL
- **View Engine:** EJS
- **Compiler:** Babel (hỗ trợ cú pháp ES6+)
- **Tool:** Nodemon (tự động restart server khi có thay đổi)

## 📋 Yêu cầu hệ thống

- Node.js (phiên bản >18)
- MySQL Server

## 🚀 Hướng dẫn cài đặt

1. **Clone project hoặc tải mã nguồn về máy.**
2. **Cài đặt các phụ thuộc:**
   ```bash
   npm install
   ```
3. **Cấu hình biến môi trường:**
   Tạo file `.env` tại thư mục gốc (nếu chưa có) và cấu hình:
   ```env
   PORT=8088
   NODE_ENV=development
   ```
4. **Cấu hình Database:**
   Mở file `src/config/config.json` và cập nhật thông tin kết nối MySQL của bạn (username, password, host).

5. **Khởi tạo Database và Bảng:**
   ```bash
   npx sequelize-cli db:create
   npx sequelize-cli db:migrate
   ```

## 💻 Cách chạy ứng dụng

Sử dụng lệnh sau để khởi động server:
```bash
npm start
```
Server sẽ chạy tại địa chỉ: `http://localhost:8088`

## 🔗 Các Routes chức năng

| Chức năng | URL | Phương thức |
|---|---|---|
| Trang chủ | `/home` | GET |
| Form tạo người dùng | `/crud` | GET |
| Lưu người dùng mới | `/post-crud` | POST |
| Danh sách người dùng | `/get-crud` | GET |
| Form chỉnh sửa người dùng | `/edit-crud?id={id}` | GET |
| Cập nhật người dùng | `/put-crud` | POST |
| Xóa người dùng | `/delete-crud?id={id}` | GET |

## 📁 Cấu trúc thư mục chính

```
src/
├── config/      # Cấu hình DB, View Engine
├── controller/  # Xử lý logic điều hướng
├── migrations/  # Các file script tạo bảng database
├── models/      # Định nghĩa các Schema/Model Sequelize
├── route/       # Định nghĩa các tuyến đường (routes)
├── services/    # Xử lý logic nghiệp vụ (Business Logic)
├── views/       # Giao diện người dùng (EJS)
└── server.js    # Điểm khởi đầu của ứng dụng
```

---
*Chúc bạn học tập và làm việc hiệu quả!*
