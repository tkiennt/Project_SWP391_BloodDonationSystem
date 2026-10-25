# Blood Donation Support System (SWP391) 🩸🏥

<div align="center">

![Java](https://img.shields.io/badge/Java-Spring%20Boot-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![React](https://img.shields.io/badge/React-TypeScript-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![FPT University](https://img.shields.io/badge/FPT%20University-SWP391%20Project-F26522?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**Hệ sinh thái phần mềm quản lý, điều phối và kết nối hiến máu nhân đạo cho cơ sở y tế**

</div>

---

## 💉 1. Giới thiệu Dự án (Project Overview)

**Blood Donation Support System** là đồ án chuyên ngành phát triển phần mềm (**SWP391 - Trường Đại học FPT**). Dự án ra đời nhằm giải quyết tình trạng thiếu hụt nguồn máu cấp cứu, tối ưu hóa quy trình điều phối giữa người hiến máu tình nguyện và các cơ sở y tế, đồng thời số hóa toàn bộ khâu lưu trữ, quản lý kho máu và theo dõi sức khỏe người hiến.

Hệ thống cung cấp nền tảng Web tương tác hai chiều: giúp người dân dễ dàng đăng ký hiến máu, nhận cảnh báo khẩn cấp khi có ca cấp cứu cùng nhóm máu ở gần, đồng thời cung cấp cho đội ngũ y bác sĩ bảng điều khiển quản lý kho máu khoa học, tự động hóa tính toán tương thích nhóm máu.

---

## 🌟 2. Các Tính năng Trọng tâm (Key Features)

### 🏥 1. Cổng Thông tin Y tế & Đặt lịch Hiến máu (Donor Portal)
- Cung cấp tài liệu giáo dục về các nhóm máu (A, B, AB, O và hệ Rh+/-), cẩm nang sức khỏe trước và sau khi hiến máu.
- Đăng ký khung giờ và địa điểm hiến máu thuận tiện.
- **Nhắc nhở chu kỳ hồi phục (Donation Interval Reminder):** Tự động tính toán và gửi thông báo nhắc nhở khi người hiến đủ điều kiện sức khỏe cho lần hiến tiếp theo (sau 84 ngày).

### 🩸 2. Thuật toán Tương thích Nhóm máu (Blood Compatibility Engine)
- Tra cứu tính tương thích truyền máu toàn phần (Whole Blood).
- **Phân tách theo từng thành phần máu:** Hỗ trợ kiểm tra tương thích riêng biệt cho khối hồng cầu (Red Blood Cells), huyết tương (Plasma) và khối tiểu cầu (Platelets) theo tiêu chuẩn y khoa quốc tế.

### 📍 3. Định vị & Yêu cầu Máu Khẩn cấp (Proximity Search & Emergency Request)
- Tìm kiếm tình nguyện viên hiến máu tương thích dựa theo bán kính khoảng cách địa lý gần nhất.
- Đăng tải yêu cầu cần máu khẩn cấp cho các ca phẫu thuật/tai nạn, gửi thông báo đẩy (Notification) đến những người hiến phù hợp trong khu vực.

### 📦 4. Quản trị Kho máu Y tế (Blood Inventory Management)
- Theo dõi số lượng từng đơn vị máu theo thể tích (250ml, 350ml, 450ml), nhóm máu và hạn sử dụng.
- **Bộ lọc kho máu thông minh (Blood Storage Filter):** Cảnh báo các túi máu sắp hết hạn để ưu tiên điều phối sử dụng, tránh lãng phí nguồn máu quý giá.

### 📊 5. Bảng điều khiển Quản lý & Báo cáo (Manager Dashboard)
- Thống kê biểu đồ lưu lượng máu tiếp nhận, số ca hiến thành công, phân bố nhóm máu hiếm.
- Quản lý hồ sơ người dùng và lịch sử các lần hiến máu.

---

## 🛠 3. Kiến trúc & Công nghệ (Tech Stack)

| Hạng mục | Công nghệ sử dụng | Vai trò |
| :--- | :--- | :--- |
| **Backend** | **Java Spring Boot, Maven** | Xây dựng RESTful API, xử lý nghiệp vụ y tế & logic truyền máu |
| **Frontend** | **React, TypeScript, CSS3** | Giao diện Single Page Application mượt mà, phân loại Role rõ ràng |
| **Cơ sở dữ liệu** | **MySQL Database** | Lưu trữ thông tin người dùng, lịch hẹn, kho máu và nhật ký giao dịch |
| **Bảo mật** | **Spring Security, JWT Token**| Xác thực phân quyền Người hiến máu, Bác sĩ, Quản lý kho, Quản trị viên |
| **Thông báo** | **Custom Notification API** | Hệ thống thông báo lịch hẹn và cảnh báo khẩn cấp |

---

## 📂 4. Cấu trúc Mã nguồn (Project Structure)

```
Project_SWP391_BloodDonationSystem/
├── blooddonation/                     # Backend Source Code (Java Spring Boot)
│   ├── src/main/java/                 # Controllers, Services, Repositories, Entities
│   ├── src/main/resources/            # application.properties, Database Config
│   └── pom.xml                        # Maven Dependencies
├── blooddonationsystem_frontend/      # Frontend Source Code (React TypeScript)
│   ├── src/
│   │   ├── components/                # UI Components (Navbar, BloodCompatibility, Notification)
│   │   ├── pages/                     # User, Manager, Donor, Schedule, Request Pages
│   │   └── services/                  # API Services & Axios client
│   └── package.json                   # NPM Dependencies
└── README.md
```

---

## 💻 5. Hướng dẫn Cài đặt & Khởi chạy (Getting Started)

### 1. Khởi chạy Backend (Java Spring Boot)
```bash
cd blooddonation
# Cấu hình thông số kết nối MySQL trong src/main/resources/application.properties
mvn clean install
mvn spring-boot:run
# Server chạy tại: http://localhost:8080
```

### 2. Khởi chạy Frontend (React + TypeScript)
```bash
cd blooddonationsystem_frontend
npm install
npm start
# Ứng dụng mở tại: http://localhost:3000
```

---

## 👥 6. Tác giả & Đóng góp (Credits)

- **Dự án phát triển bởi:** Đội ngũ phát triển đồ án SWP391.
- **Thực hiện chính:** Trung Kiên ([@tkiennt](https://github.com/tkiennt)) — *Core Fullstack Developer*.

### 🏆 Đóng góp Nổi bật của Trung Kiên:
- Đóng góp kỷ lục **258 commits** và hơn **35 Pull Requests** được tích hợp vào nhánh chính.
- Trực tiếp thiết kế và lập trình:
  - Toàn bộ phân hệ **Manager Dashboard** và phân quyền quản lý cơ sở y tế.
  - Thuật toán kiểm tra tính tương thích nhóm máu toàn phần & từng thành phần máu (`BloodCompatibility`).
  - Phân hệ quản lý kho máu và bộ lọc kho lưu trữ thông minh (`Blood Storage Filter`).
  - Luồng gửi và xét duyệt yêu cầu cấp phát máu (`Blood Request`).
  - Hệ thống thông báo tự động (`Notification API`).
