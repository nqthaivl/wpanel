<p align="center">
  <img src="https://img.shields.io/badge/WPanel-v2.0-blue?style=for-the-badge&logo=linux&logoColor=white" alt="WPanel">
  <img src="https://img.shields.io/badge/Python-3.12-green?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Ubuntu-22.04%20|%2024.04-orange?style=for-the-badge&logo=ubuntu&logoColor=white" alt="Ubuntu">
  <img src="https://img.shields.io/badge/Debian-13%20Trixie-A81D33?style=for-the-badge&logo=debian&logoColor=white" alt="Debian">
  <img src="https://img.shields.io/badge/CentOS%20Stream-9-262577?style=for-the-badge&logo=centos&logoColor=white" alt="CentOS">
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
| 🌐 **Quản lý Website** | Tạo, xoá, cấu hình Nginx/Apache/OpenLiteSpeed — **chọn web server riêng cho từng domain** |
| 🌐 **Multi-WebServer** | Nginx Reverse Proxy + Backend (Apache/OLS) — mô hình Production hiệu năng cao |
| 🔐 **SSL Manager** | Cài đặt SSL Let's Encrypt tự động (Certbot) |
| 🗄️ **Database** | Quản lý MySQL/MariaDB, phpMyAdmin tích hợp |
| 📁 **File Manager** | Trình quản lý tệp trực quan, upload/download/edit |
| 💻 **Web Terminal** | SSH trực tiếp trên trình duyệt (xterm.js) |
| 🐳 **Docker** | Quản lý Container, Images, Deploy Compose |
| ⏰ **Cron Job** | Lập lịch tự động + Thư viện Script có sẵn |
| 🔔 **Cảnh báo** | Thông báo Telegram/Discord khi CPU/RAM/Disk cao |
| ☁️ **Cloudflare** | Quản lý DNS records trực tiếp qua API |
| 📧 **Mail Server** | Cài đặt Postfix + Dovecot + Roundcube Webmail |
| 🛡️ **Bảo mật** | Fail2Ban, Firewall UFW, SSH Key, **Xác thực 2 bước (2FA TOTP)** |
| 💿 **Extend Disk** | Mở rộng ổ đĩa 1-click sau khi nâng cấp VPS |
| 🔄 **Swap** | Tạo/quản lý Swap Memory |
| 🔑 **SSH Key** | Quản lý SSH Key cho xác thực không mật khẩu |

---

## 💻 Yêu Cầu Hệ Thống

| Yêu cầu | Tối thiểu |
|---|---|
| **Hệ điều hành** | Ubuntu 22.04+|
| **CPU** | 1 vCPU |
| **RAM** | 512 MB |
| **Disk** | 5 GB trống |
| **Quyền** | Root |
| **Port** | 9002 (mặc định) |

### Hệ điều hành được hỗ trợ

| OS | Phiên bản | Ghi chú |
|---|---|---|
| **Ubuntu** | 22.04, 24.04 | ✅ Khuyên dùng |

---

## 🚀 Cài Đặt

### Cách 1: Cài 1 lệnh (khuyến nghị)

```bash
bash <(curl -sL domain.com)
```

Quá trình cài đặt gồm **5 bước** tự động:

```
[1/5] Đang tải mã nguồn WPanel...
[2/5] Đang giải nén mã nguồn...
[3/5] Kiểm tra phiên bản Python...     ← Tự cài Python 3.12 nếu cần
[4/5] Bắt đầu cài đặt WPanel...        ← Tạo venv, cài dependencies
[5/5] Cài đặt Web Stack...              ← LNMP/LAMP/LLMP/Multi-WS
```

### Cách 2: Cài thủ công

```bash
# Tải về
wget https://domain.com/wpanel.tar.gz

# Giải nén
tar xzf wpanel.tar.gz

# Cài đặt
cd wpanel && bash wpanel.sh
```

### Cách 3: Cài từ source (dev)

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
| `wpanel passwd` | Đổi mật khẩu tài khoản admin |
| `wpanel port` | Đổi port đăng nhập panel |
| `wpanel disable-2fa` | Tắt xác thực 2 bước (2FA) cho tài khoản |
| `wpanel update` | Cập nhật WPanel (cài lại dependencies) |
| `wpanel uninstall` | Gỡ cài đặt hoàn toàn |

### Ví dụ sử dụng

```bash
# Khởi động lại khi gặp lỗi
wpanel restart

# Đổi mật khẩu admin
wpanel passwd

# Đổi port đăng nhập (mặc định 9002)
wpanel port
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

- Tạo website mới với **chọn Web Server riêng cho từng domain**:
  - Nginx (trực tiếp)
  - Apache (trực tiếp)
  - OpenLiteSpeed (trực tiếp)
  - **Multi-WebServer** (Nginx Proxy → Apache/OLS backend)
- Cấu hình Virtual Host tự động
- Quản lý PHP version (7.4, 8.1, 8.2, 8.3)
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

### 🌐 Cấu Hình Web Stack (1-Click)

Cài đặt trọn bộ Web Stack chỉ với 1 click:

| Stack | Thành phần | Ghi chú |
|---|---|---|
| **LNMP** | Nginx + MariaDB + PHP + phpMyAdmin + Certbot | Hiệu năng cao, chịu tải lớn |
| **LAMP** | Apache + MariaDB + PHP + phpMyAdmin + Certbot | Tương thích .htaccess |
| **LLMP** | OpenLiteSpeed + MariaDB + LsPHP + phpMyAdmin + Certbot | HTTP/3 QUIC, cache tích hợp |
| **Multi-WebServer** | Nginx (Proxy :80/:443) + Apache (Backend :8080) + MariaDB + PHP | **Mô hình Production khuyên dùng** |

#### Multi-WebServer Hosting

```
Client → Nginx (Reverse Proxy :80/:443) → Apache (Backend :8080/:8443) → PHP → MariaDB
             │                                    │
             ├─ SSL termination (Certbot)         ├─ Xử lý PHP
             ├─ Static files (cache)              ├─ .htaccess
             └─ Load balancing                    └─ Dynamic content
```

| Thành phần | Port | Vai trò |
|---|---|---|
| **Nginx** | 80, 443 | Reverse Proxy, SSL, static files |
| **Apache** | 8080, 8443 | Backend xử lý PHP, .htaccess |
| **Certbot** | — | SSL Let's Encrypt qua Nginx plugin |

- **Nginx đứng trước** xử lý SSL termination, static files (ảnh, CSS, JS), caching và load balancing
- **Backend (Apache)** xử lý PHP, .htaccess và dynamic content
- Hiệu năng cao nhất, phù hợp cho môi trường **Production**
- Mỗi domain có thể chọn web server riêng biệt

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
- 🔒 **Xác thực 2 bước (2FA)** — TOTP compatible (Google Authenticator, Authy)
- 🔗 **URL bảo mật** — Đường dẫn truy cập panel được mã hoá ngẫu nhiên

---

## 📂 Cấu Trúc Thư Mục

```
/opt/wpanel/              # Thư mục cài đặt
├── *.so                  # Module biên dịch (binary)
├── .python_version       # Python version yêu cầu (VD: 3.12)
├── run.py                # Entry point
├── requirements.txt      # Python dependencies
├── venv/                 # Python virtual environment (python3.12)
├── data/                 # Database & dữ liệu
├── web_templates/        # HTML templates
├── templates/            # Nginx/Apache/LiteSpeed config templates
│   ├── nginx_template.conf
│   ├── nginx_proxy_template.conf   # Multi-WebServer template
│   ├── apache_template.conf
│   └── litespeed_template.conf
├── static/               # CSS, JS, images
│   ├── css/style.css
│   └── js/app.js         # Giao diện Lucide Icons
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
# Ubuntu/Debian — Mở port trên UFW
ufw allow 9002/tcp

# CentOS/RHEL — Mở port trên firewalld
firewall-cmd --permanent --add-port=9002/tcp && firewall-cmd --reload
```

### Lỗi `undefined symbol: _PyThreadState_UncheckedGet`?

Lỗi này xảy ra khi Python version trên VPS khác với bản dùng để build binary.

```bash
# Kiểm tra Python version cần thiết
cat /opt/wpanel/.python_version

# Cài đúng Python version (VD: 3.12)
# Ubuntu:
add-apt-repository ppa:deadsnakes/ppa && apt install python3.12 python3.12-venv

# Debian:
curl -fsSL https://packages.sury.org/python/apt.gpg | gpg --dearmor -o /usr/share/keyrings/sury-python.gpg

# CentOS:
dnf install python3.12

# Sau đó cài lại WPanel
bash <(curl -sL https://domain.com/install.sh)
```

### Quên mật khẩu admin?

```bash
wpanel passwd
```

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
