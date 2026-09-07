# 🏯 Hệ thống Cơ sở dữ liệu Du lịch Huế

> **Phân tích và thiết kế hệ thống Cơ sở dữ liệu Du lịch Huế**

## 📌 Giới thiệu

**Hệ thống Cơ sở dữ liệu Du lịch Huế** là hệ thống được xây dựng nhằm quản lý, chuẩn hóa, lưu trữ và khai thác tập trung các thông tin liên quan đến hoạt động du lịch trên địa bàn thành phố Huế.

Hệ thống hướng tới việc hình thành một **kho dữ liệu du lịch tập trung, đồng bộ, chính xác, nhất quán và có khả năng mở rộng**, hỗ trợ cơ quan quản lý nhà nước, doanh nghiệp du lịch và du khách trong việc quản lý, cập nhật, tra cứu và khai thác thông tin du lịch.

Hệ thống cũng được định hướng để có khả năng tích hợp với các nền tảng số của thành phố như **Hue-S, GIS** và các hệ thống bên ngoài thông qua API.

---

## 🎯 Mục tiêu

- Xây dựng cơ sở dữ liệu du lịch tập trung và chuẩn hóa.
- Đảm bảo tính **chính xác, nhất quán và toàn vẹn** của dữ liệu.
- Hỗ trợ cơ quan quản lý trong việc quản lý, giám sát, thống kê và báo cáo.
- Hỗ trợ doanh nghiệp cập nhật và quản lý thông tin dịch vụ du lịch.
- Hỗ trợ du khách tìm kiếm và tra cứu thông tin du lịch.
- Tích hợp dữ liệu với các hệ thống bên ngoài.
- Tạo nền tảng dữ liệu phục vụ các ứng dụng **AI, Big Data và phân tích dữ liệu** trong tương lai.

---

## 👥 Đối tượng sử dụng

Hệ thống bao gồm 5 nhóm tác nhân chính:

| Đối tượng | Vai trò |
|---|---|
| 👤 Du khách | Tìm kiếm, xem thông tin du lịch và gửi đánh giá |
| 🏢 Doanh nghiệp | Quản lý và cập nhật thông tin dịch vụ |
| 👨‍💼 Quản trị viên | Quản lý, kiểm duyệt và phê duyệt dữ liệu |
| ⚙️ Quản trị hệ thống | Quản lý tài khoản, phân quyền và cấu hình hệ thống |
| 🔗 Hệ thống bên ngoài | Trao đổi và đồng bộ dữ liệu thông qua API |

Các tác nhân và phạm vi quyền hạn được mô tả trong tài liệu phân tích thiết kế của hệ thống.

---

## ✨ Chức năng chính

### 🔐 1. Xác thực hệ thống

- Đăng nhập.
- Đăng xuất.
- Đăng ký tài khoản.
- Đăng nhập thông qua:
  - VNeID
  - Hue-S
  - SSO
- Xác thực và phân quyền người dùng.

Hệ thống định hướng sử dụng JWT và có khả năng tích hợp với các nền tảng xác thực tập trung.

### 👥 2. Quản lý người dùng

- Xem danh sách người dùng.
- Thêm người dùng.
- Chỉnh sửa thông tin.
- Xóa người dùng.
- Khóa tài khoản.
- Quản lý tài khoản du khách.
- Phân quyền người dùng.

### ⚙️ 3. Quản lý danh mục hệ thống

Quản lý các danh mục dùng chung:

- Địa bàn.
- Loại hình doanh nghiệp.
- Loại hình lưu trú.
- Loại hình dịch vụ.
- Loại điểm đến.
- Tiện ích.
- Các danh mục liên quan khác.

Các danh mục được quản lý theo quy trình CRUD tiêu chuẩn.

### 🏢 4. Quản lý doanh nghiệp

- Khai báo thông tin doanh nghiệp.
- Cập nhật thông tin.
- Xóa thông tin.
- Xem hồ sơ doanh nghiệp.
- Gửi hồ sơ để kiểm duyệt.
- Quản trị viên phê duyệt hoặc từ chối hồ sơ.

### 🏨 5. Quản lý cơ sở lưu trú

- Quản lý danh sách cơ sở lưu trú.
- Thêm mới.
- Chỉnh sửa.
- Xóa.
- Kiểm duyệt hồ sơ.
- Phê duyệt hoặc từ chối hồ sơ.

### 🚌 6. Quản lý lữ hành & hướng dẫn viên

- Quản lý doanh nghiệp lữ hành.
- Quản lý tour.
- Quản lý danh sách hướng dẫn viên.
- Quản lý hồ sơ/chứng chỉ hướng dẫn viên.
- Kiểm duyệt thông tin trước khi công khai.

### 🍜 7. Quản lý dịch vụ ăn uống & mua sắm

- Quản lý nhà hàng.
- Quản lý cửa hàng.
- Quản lý thông tin dịch vụ.
- Quản lý thực đơn/sản phẩm.
- Quản lý vị trí kinh doanh.

### 📍 8. Quản lý điểm đến

- Quản lý các điểm đến du lịch.
- Phân loại điểm đến.
- Quản lý thông tin mô tả.
- Quản lý hình ảnh.
- Quản lý tọa độ địa lý.
- Tích hợp bản đồ GIS.

Dữ liệu điểm đến có thể được gắn tọa độ và hiển thị trên bản đồ số GIS.

### 🎉 9. Quản lý lễ hội & sự kiện

- Thêm sự kiện.
- Chỉnh sửa sự kiện.
- Xóa sự kiện.
- Quản lý thời gian tổ chức.
- Quản lý địa điểm.
- Quản lý hình ảnh.
- Đồng bộ thông tin với hệ thống liên quan.

### ⭐ 10. Quản lý phản hồi & đánh giá

Du khách có thể:

- Gửi đánh giá.
- Chấm điểm từ **1–5 sao**.
- Viết nhận xét.
- Gửi hình ảnh thực tế.

Quản trị viên có thể kiểm duyệt và xử lý các phản hồi không hợp lệ.

### 🔎 11. Tìm kiếm thông tin du lịch

Hỗ trợ tìm kiếm và lọc thông tin theo nhiều tiêu chí:

- Khu vực.
- Mức giá.
- Loại hình.
- Tiện ích.
- Loại điểm đến.
- Các tiêu chí liên quan.

### 🔌 12. Quản lý API

- Quản lý API Key.
- Cấp API Key cho đối tác.
- Thiết lập phạm vi dữ liệu.
- Thiết lập Rate Limit.
- Tạm dừng API Key.
- Thu hồi API Key.
- Theo dõi số lượng request.

Hệ thống có cơ chế tự động phát hiện trường hợp vượt hạn mức request và tạm khóa API Key khi cần thiết.

### 📊 13. Báo cáo & thống kê

Dashboard hỗ trợ tổng hợp:

- Số lượng doanh nghiệp.
- Dữ liệu du lịch.
- Lượt phản hồi.
- Mật độ truy cập.
- Các số liệu phục vụ quản lý và dự báo.

Hệ thống định hướng hỗ trợ xuất báo cáo dưới dạng **Excel/PDF**.

---

## 🏗️ Kiến trúc hệ thống

Hệ thống được định hướng theo kiến trúc **Service-Oriented Architecture (SOA)**, kết hợp **MVC** và Microservices nhằm tăng khả năng mở rộng và tích hợp.

Kiến trúc dữ liệu du lịch được chia thành 4 lớp:

```text
┌──────────────────────────────────────────────┐
│       1. INTERACTION & MEASUREMENT           │
│       Hue-S / VNeID / SSO / Web / KPI        │
└──────────────────────┬───────────────────────┘
                       │
┌──────────────────────▼───────────────────────┐
│          2. APPLICATION / BUSINESS            │
│ User / Business / Tourism / Report / API     │
└──────────────────────┬───────────────────────┘
                       │
┌──────────────────────▼───────────────────────┐
│             3. DATA & CORE PLATFORM           │
│ PostgreSQL / PostGIS / GIS / Cloud Storage   │
└──────────────────────┬───────────────────────┘
                       │
┌──────────────────────▼───────────────────────┐
│       4. DIGITAL INFRASTRUCTURE & SECURITY    │
│ Docker / Server / Network / SOC / Backup     │
└──────────────────────────────────────────────┘
```

Hệ thống sử dụng cơ sở dữ liệu tập trung để quản lý các thực thể như điểm đến, cơ sở lưu trú, doanh nghiệp và lễ hội; đồng thời có định hướng sử dụng PostGIS cho dữ liệu không gian GIS.

---

## 🛠️ Công nghệ đề xuất

| Thành phần | Công nghệ |
|---|---|
| Backend | C# .NET / Java Spring Boot |
| Frontend | ReactJS / Angular / .NET |
| Database | PostgreSQL / PostGIS |
| API | REST API / OpenAPI 3.0 |
| Architecture | SOA / Microservices / MVC |
| Web Server | Nginx / Apache / IIS |
| Deployment | Docker |
| Operating System | Ubuntu Server 22.04 LTS |
| GIS | PostGIS / GIS Huế |
| Authentication | JWT / SSO / VNeID / Hue-S |
| Data Format | JSON / CSV / Excel |
| Storage | Cloud Storage |

> **Lưu ý:** Tài liệu thiết kế có đề cập nhiều phương án công nghệ, vì vậy các công nghệ trên được xem là **công nghệ đề xuất/định hướng**, không phải tất cả đều đã được triển khai thực tế trong phiên bản hiện tại.

---

## 🔒 Bảo mật

Hệ thống định hướng áp dụng:

- HTTPS/TLS 1.2 trở lên.
- JWT.
- Refresh Token.
- Phân quyền theo nguyên tắc **Least Privilege**.
- Bảo vệ trước SQL Injection.
- XSS.
- CSRF.
- Audit Log.
- Mã hóa mật khẩu bằng **bcrypt**.
- Sao lưu dữ liệu tự động.
- Giám sát và cảnh báo lỗi.

Các yêu cầu bảo mật, hiệu năng và vận hành được quy định trong phần yêu cầu phi chức năng của tài liệu.

---

## ⚡ Yêu cầu hiệu năng

Một số yêu cầu chính:

- Thời gian phản hồi trung bình cho tìm kiếm/tra cứu: **< 2 giây**.
- Thời gian tải trang lần đầu: **< 3 giây** với kết nối 10 Mbps.
- Hỗ trợ tối thiểu **500 người dùng đồng thời**.
- Hỗ trợ mở rộng theo chiều ngang.
- SLA tối thiểu **99.5% uptime/năm**.
- Cơ chế failover và phục hồi khi xảy ra sự cố.

---

## 📐 Quy định giao diện

Giao diện được định hướng theo phong cách:

- **Modern / Clean**.
- Màu chủ đạo xanh đậm và vàng theo nhận diện du lịch Huế.
- Responsive Design.
- Hỗ trợ Desktop / Tablet / Mobile.
- Hỗ trợ tiếng Việt và tiếng Anh.
- Hỗ trợ Dark Mode.
- Sử dụng Font Awesome / Material Icons.



---

## 🗂️ Cấu trúc tài liệu dự án

Tài liệu phân tích và thiết kế được chia thành các nội dung chính:

```text
Tài liệu
│
├── 1. Mục tiêu, nhiệm vụ
│
├── 2. Yêu cầu trong nội dung thiết kế
│   ├── Tiêu chuẩn kỹ thuật
│   ├── Tác nhân
│   ├── Use Case
│   ├── Quy định thiết kế
│   ├── Yêu cầu phi chức năng
│   └── Kiến trúc hệ thống
│
├── 3. Thiết kế chi tiết chức năng
│   ├── Đăng nhập
│   ├── Quản lý người dùng
│   ├── Quản lý danh mục
│   ├── Quản lý lưu trú
│   ├── Quản lý lữ hành & HDV
│   ├── Ăn uống & mua sắm
│   ├── Điểm đến
│   ├── Lễ hội & sự kiện
│   ├── Phản hồi
│   ├── Tìm kiếm
│   ├── API
│   └── Báo cáo thống kê
│
├── 4. Thiết kế cơ sở dữ liệu
│   ├── Mô tả thực thể
│   ├── Lược đồ quan hệ
│   └── Đặc tả bảng dữ liệu
│
└── 5. Kết quả đạt được
```

Nội dung này tương ứng với cấu trúc của tài liệu phân tích và thiết kế dự án.

---

## 👨‍💻 Thành viên thực hiện

**Dự án:** Phân tích và thiết kế hệ thống Cơ sở dữ liệu Du lịch Huế

**Cơ quan chủ trì:** Trung tâm Công nghệ thông tin thành phố Huế

**Thành viên:**

- Đặng Văn Long
- Trần Đình Long
- Nguyễn Viết Phú

**Địa điểm:** Huế  
**Năm:** 2026

---

## 📌 Trạng thái dự án

```text
🟢 Phân tích yêu cầu        — Hoàn thành
🟢 Xây dựng Use Case        — Hoàn thành
🟢 Thiết kế nghiệp vụ       — Hoàn thành
🟢 Thiết kế giao diện       — Hoàn thành
🟢 Thiết kế cơ sở dữ liệu   — Hoàn thành
🟡 Phát triển hệ thống      — Đang phát triển
⚪ Kiểm thử                  — Chưa hoàn tất
⚪ Triển khai                — Chưa triển khai
```

---

## 📄 Tài liệu tham khảo trong dự án

- Tài liệu Phân tích và Thiết kế Hệ thống Cơ sở dữ liệu Du lịch Huế.
- Kiến trúc Chính phủ số Việt Nam.
- Khung Kiến trúc số thành phố Huế.
- ISO/IEC 27001:2022.
- OWASP Top 10.
- REST API / OpenAPI 3.0.
- WCAG 2.1.
- Các quy định liên quan đến cơ sở dữ liệu du lịch.

---

## 📜 License

Dự án được thực hiện phục vụ mục đích **học tập, nghiên cứu và phân tích thiết kế hệ thống**.

---

<p align="center">
  <b>🏯 Hệ thống Cơ sở dữ liệu Du lịch Huế</b>
  <br>
  <i>Chuẩn hóa dữ liệu — Kết nối hệ thống — Phát triển du lịch thông minh</i>
</p>
