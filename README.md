<p align="center">
  <img src="https://img.shields.io/badge/WPanel-v1.0-blue?style=for-the-badge&logo=linux&logoColor=white" alt="WPanel">
  <img src="https://img.shields.io/badge/Python-3.10+-green?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Ubuntu-22.04%20|%2024.04-orange?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu">
  <img src="https://img.shields.io/badge/License-Private-red?style=for-the-badge" alt="License">
</p>

<h1 align="center">🖥️ WPanel — Quản Trị VPS Đơn Giản</h1>

<p align="center">
  <b>Panel quản trị VPS giao diện web hiện đại, nhẹ, dễ sử dụng.</b><br>
  Thay thế hoàn toàn dòng lệnh — quản lý server chỉ qua trình duyệt.
</p>

---

## 📋 Mục Lục

- [Giới Thiệu](#-giới-thiệu)
- [Tính Năng](#-tính-năng)
- [Yêu Cầu Hệ Thống](#-yêu-cầu-hệ-thống)
- [Cài Đặt](#-cài-đặt)
- [Lệnh WPanel CLI](#-lệnh-wpanel-cli)
- [Chức Năng Chi Tiết](#-chức-năng-chi-tiết)
- [Ảnh Chụp Màn Hình](#-ảnh-chụp-màn-hình)
- [Liên Hệ](#-liên-hệ)

---

## 🎯 Giới Thiệu

**WPanel** là panel quản trị VPS/Server chạy trực tiếp trên máy chủ Linux, tương tự aaPanel/CyberPanel nhưng **nhẹ hơn, nhanh hơn** và hoàn toàn **bằng tiếng Việt**.

- 🚀 **Nhẹ** — Chỉ chiếm ~50MB RAM khi chạy
- 🔒 **Bảo mật** — Mã nguồn được biên dịch binary, database mã hoá SQLCipher
- 🇻🇳 **Tiếng Việt** — Toàn bộ giao diện tiếng Việt, dễ sử dụng
- ⚡ **Nhanh** — Cài đặt chỉ trong 2 phút

---

## ✨ Tính Năng

| Tính năng | Mô tả |
|---|---|
| 📊 **Dashboard** | Giám sát CPU, RAM, Disk, Network, Uptime realtime |
| 🌐 **Quản lý Website** | Tạo, xoá, cấu hình Nginx/Apache/OpenLiteSpeed |
| 🔐 **SSL Manager** | Cài đặt SSL Let's Encrypt tự động (Certbot) |
| 🗄️ **Database** | Quản lý MySQL/MariaDB, phpMyAdmin tích hợp |
| 📁 **File Manager** | Trình quản lý tệp trực quan, upload/download/edit |
| 💻 **Web Terminal** | SSH trực tiếp trên trình duyệt (xterm.js) |
| 🐳 **Docker** | Quản lý Container, Images, Deploy Compose |
| ⏰ **Cron Job** | Lập lịch tự động + Thư viện Script có sẵn |
| 🔔 **Cảnh báo** | Thông báo Telegram/Discord khi CPU/RAM/Disk cao |
| ☁️ **Cloudflare** | Quản lý DNS records trực tiếp qua API |
| 📧 **Mail Server** | Cài đặt Postfix + Dovecot + Roundcube Webmail |
| 🛡️ **Bảo mật** | Fail2Ban, Firewall UFW, SSH Key management |
| 💿 **Extend Disk** | Mở rộng ổ đĩa 1-click sau khi nâng cấp VPS |
| 🔄 **Swap** | Tạo/quản lý Swap Memory |
| 🔑 **SSH Key** | Quản lý SSH Key cho xác thực không mật khẩu |

---

## 💻 Yêu Cầu Hệ Thống

| Yêu cầu | Tối thiểu |
|---|---|
| **Hệ điều hành** | Ubuntu 22.04 / 24.04 LTS |
| **CPU** | 1 vCPU |
| **RAM** | 512 MB |
| **Disk** | 5 GB trống |
| **Quyền** | Root |
| **Port** | 9002 (mặc định) |

> **Lưu ý:** WPanel cũng hỗ trợ Debian 11+, CentOS Stream 9, AlmaLinux 9, Rocky Linux 9.

---

## 🚀 Cài Đặt

### Cách 1: Cài nhanh (khuyến nghị)

```bash
# Tải về
wget https://your-domain.com/wpanel-release.tar.gz

# Giải nén
tar xzf wpanel-release.tar.gz

# Cài đặt
cd wpanel && bash wpanel.sh
```

### Cách 2: Cài từ source

```bash
# Clone source code
git clone https://github.com/your-repo/wpanel.git

# Chạy install script
cd wpanel && bash wpanel.sh
```

### Sau khi cài xong

Trình cài đặt sẽ hiện thông tin đăng nhập:

```
╔══════════════════════════════════════════════════════╗
║       ✅ WPanel đã cài đặt thành công!               ║
╠══════════════════════════════════════════════════════╣
║                                                      ║
║  🌐 Panel URL: http://YOUR_IP:9002                   ║
║                                                      ║
║  👤 Username:  admin                                  ║
║  🔑 Password:  admin                                  ║
║                                                      ║
║  ⚠ Vui lòng đăng nhập và đổi mật khẩu ngay!        ║
╚══════════════════════════════════════════════════════╝
```

> ⚠️ **Quan trọng:** Đổi mật khẩu mặc định ngay sau khi đăng nhập lần đầu!

---

## 🛠️ Lệnh WPanel CLI

Sau khi cài đặt, bạn có thể quản lý WPanel bằng lệnh `wpanel` trên terminal:

```bash
wpanel              # Hiển thị menu trợ giúp + URL panel
```

### Danh sách lệnh

| Lệnh | Chức năng |
|---|---|
| `wpanel start` | Khởi động WPanel |
| `wpanel stop` | Dừng WPanel |
| `wpanel restart` | Khởi động lại WPanel |
| `wpanel status` | Xem trạng thái hoạt động |
| `wpanel log` | Xem log realtime (Ctrl+C để thoát) |
| `wpanel update` | Cập nhật WPanel (cài lại dependencies) |
| `wpanel uninstall` | Gỡ cài đặt hoàn toàn |

### Ví dụ sử dụng

```bash
# Khởi động lại khi gặp lỗi
wpanel restart

# Xem log để debug
wpanel log

# Kiểm tra trạng thái
wpanel status
```

---

## 📖 Chức Năng Chi Tiết

### 📊 Bảng Điều Khiển (Dashboard)

Trang tổng quan hiển thị toàn bộ thông tin hệ thống:
- **CPU** — Phần trăm sử dụng, load average, số nhân
- **RAM** — Đã dùng / Tổng, phần trăm
- **Ổ đĩa** — Dung lượng sử dụng, còn trống
- **Mạng** — Lưu lượng tải lên/tải xuống
- **Dịch vụ** — Danh sách service đang hoạt động
- **Kết nối** — Số kết nối TCP đang active
- **Uptime** — Thời gian hoạt động liên tục

---

### 🌐 Quản Lý Website

- Tạo website mới (Nginx / Apache / OpenLiteSpeed)
- Cấu hình Virtual Host
- Quản lý PHP version (7.4, 8.0, 8.1, 8.2, 8.3)
- Reverse Proxy cho ứng dụng Node.js, Python

---

### 🔐 SSL Manager

- Cài đặt SSL Let's Encrypt **tự động**
- Hỗ trợ Wildcard SSL qua Cloudflare DNS
- Gia hạn tự động qua cron
- Tích hợp Certbot

---

### 📁 Trình Quản Lý Tệp (File Manager)

- Duyệt thư mục trực quan
- Upload / Download file
- Chỉnh sửa file trực tiếp trên trình duyệt (Code Editor)
- Tạo, đổi tên, xoá, di chuyển file/thư mục
- Phân quyền (chmod) và đổi chủ sở hữu (chown)

---

### 💻 Web Terminal

- Terminal SSH ngay trên trình duyệt
- Hỗ trợ xterm-256color
- Copy/paste, resize tự động
- Kết nối trực tiếp qua WebSocket (không cần SSH client)

---

### 🐳 Docker Manager

- Xem danh sách Container, Images
- Start / Stop / Restart container
- Xem logs container
- **Deploy Docker Compose** trực tiếp từ giao diện
- Pull image mới

---

### ⏰ Cron Job

- **Tab Cron Job** — Xem và quản lý các tác vụ đang chạy
- **Tab Thư Viện Script** — Chọn từ danh sách script có sẵn:
  - Backup tự động
  - Dọn dẹp log
  - Cập nhật hệ thống
  - Kiểm tra SSL
  - Và nhiều script khác...

---

### 🛠️ Cài Đặt Dịch Vụ (Service Installer)

Cài đặt 1-click các dịch vụ phổ biến:

| Web Server | Database | Khác |
|---|---|---|
| Nginx | MySQL | Docker |
| Apache | MariaDB | Node.js |
| OpenLiteSpeed | PostgreSQL | Redis |
| PHP (đa version) | MongoDB | Memcached |

| Bảo mật | Mail | Công cụ |
|---|---|---|
| Fail2Ban | Postfix | Certbot |
| Firewall UFW | Dovecot | Rclone |
| SSH Key | Roundcube Webmail | phpMyAdmin |

---

### ⚙️ Cấu Hình Hệ Thống (Settings)

- **Máy chủ** — Hostname, Timezone, MOTD
- **Ổ đĩa** — Xem dung lượng, Extend Disk 1-click
- **Swap** — Tạo/xoá/cấu hình Swap Memory
- **Tài khoản** — Đổi username, mật khẩu Admin, mật khẩu Root
- **SSH Port** — Thay đổi port SSH mặc định
- **Thông báo** — Cấu hình cảnh báo Telegram / Discord
- **License** — Xem thông tin và đồng bộ license

---

### 🔔 Hệ Thống Cảnh Báo

Tự động gửi thông báo khi:
- CPU vượt ngưỡng (mặc định > 90%)
- RAM vượt ngưỡng (mặc định > 90%)
- Disk vượt ngưỡng (mặc định > 90%)

Hỗ trợ kênh thông báo:
- **Telegram Bot** — Nhận cảnh báo qua Telegram
- **Discord Webhook** — Nhận cảnh báo qua Discord

---

## 📸 Ảnh Chụp Màn Hình

> _Coming soon..._

---

## 🔒 Bảo Mật

- 🔐 Mật khẩu được hash bằng thuật toán an toàn
- 🗄️ Database người dùng mã hoá bằng **SQLCipher**
- 🛡️ Tích hợp Rate Limiter chống brute-force
- 🔑 Hỗ trợ SSH Key authentication
- 📦 Mã nguồn biên dịch binary (không thể đọc/chỉnh sửa)

---

## 📂 Cấu Trúc Thư Mục

```
/opt/wpanel/              # Thư mục cài đặt
├── *.so                  # Module biên dịch (binary)
├── run.py                # Entry point
├── requirements.txt      # Python dependencies
├── venv/                 # Python virtual environment
├── data/                 # Database & dữ liệu
├── web_templates/        # HTML templates
├── static/               # CSS, JS, images
│   ├── css/style.css
│   └── js/app.js
└── scripts/              # Shell scripts cài đặt dịch vụ
```

---

## 🆘 Xử Lý Sự Cố

### WPanel không truy cập được?

```bash
# Kiểm tra trạng thái
wpanel status

# Xem log lỗi
wpanel log

# Khởi động lại
wpanel restart
```

### Port 9002 bị chặn?

```bash
# Mở port trên UFW
ufw allow 9002/tcp

# Hoặc trên firewalld
firewall-cmd --permanent --add-port=9002/tcp && firewall-cmd --reload
```

### Quên mật khẩu admin?

Liên hệ hỗ trợ kỹ thuật để reset tài khoản.

---

## 📞 Liên Hệ

- 🌐 **Website:** [https://wpanel.vn](https://wpanel.vn)
- 📱 **Facebook:** [https://www.facebook.com/nqthaivl.1982](https://www.facebook.com/nqthaivl.1982)
- 📞 **Điện thoại:** 0917.833.184

---

<p align="center">
  <b>Made with ❤️ in Vietnam</b><br>
  © 2024-2026 WPanel.vn — All rights reserved.
</p>
