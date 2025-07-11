# 🛒 Aplikasi Toko Online - CodeIgniter 4

<div align="center">

![CodeIgniter](https://img.shields.io/badge/CodeIgniter-4.x-red?style=for-the-badge&logo=codeigniter)
![PHP](https://img.shields.io/badge/PHP-8.1+-blue?style=for-the-badge&logo=php)
![MySQL](https://img.shields.io/badge/MySQL-5.7+-orange?style=for-the-badge&logo=mysql)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-purple?style=for-the-badge&logo=bootstrap)

**Aplikasi e-commerce modern dengan manajemen produk, sistem diskon dinamis, keranjang belanja, dan integrasi API pengiriman real-time**

[🚀 Quick Start](#quick-start) • [✨ Fitur](#fitur-utama) • [🛠️ Instalasi](#instalasi-lengkap) 

</div>

---

## 📋 Daftar Isi

- [Tentang Proyek](#tentang-proyek)
- [Fitur Utama](#fitur-utama)
- [Tech Stack](#tech-stack)
- [Quick Start](#quick-start)
- [Instalasi Lengkap](#instalasi-lengkap)
- [Konfigurasi](#konfigurasi)
- [Struktur Proyek](#struktur-proyek)

---

## 🎯 Tentang Proyek

**Toko Online CI4** adalah aplikasi e-commerce yang dibangun menggunakan framework CodeIgniter 4 dengan arsitektur MVC. Aplikasi ini menggabungkan fitur-fitur modern seperti sistem diskon dinamis, integrasi API pengiriman real-time, dan dashboard analytics yang komprehensif.

### 🌟 Keunggulan

- ⚡ **Performance Optimized** - Dibangun dengan CodeIgniter 4 yang cepat dan ringan
- 🔒 **Security First** - Implementasi autentikasi, authorization, dan CSRF protection
- 📱 **Responsive Design** - UI yang optimal di semua perangkat
- 🔄 **Real-time Updates** - Data transaksi dan diskon yang selalu up-to-date
- 🚀 **API Ready** - RESTful API untuk integrasi dengan sistem lain
- 📊 **Analytics Dashboard** - Dashboard terpisah untuk monitoring bisnis

---

## ✨ Fitur Utama

### 👥 Manajemen User & Autentikasi

```
✅ Multi-role system (Admin/Customer)
✅ Secure authentication dengan session management
✅ Password encryption menggunakan PHP native hashing
✅ Auto-redirect filter untuk user yang sudah login
✅ Role-based access control (RBAC)
```

### 🛍️ Manajemen Produk

```
✅ CRUD produk dengan kategori
✅ Upload & validasi gambar produk
✅ Export data produk ke PDF
✅ Pencarian dan filtering produk
✅ Stock management (coming soon)
```

### 🎯 Sistem Diskon Dinamis

```
✅ Diskon berdasarkan tanggal (daily discount)
✅ Validasi tanggal unik - tidak ada duplikasi diskon
✅ Auto-apply diskon saat login berdasarkan tanggal
✅ Tampilan real-time diskon di header
✅ Form edit dengan tanggal readonly
✅ Tracking diskon per transaksi
```

### 🛒 Shopping Cart & Checkout

```
✅ Keranjang belanja dengan CodeIgniter Cart Library
✅ Auto-apply diskon saat add to cart
✅ Edit quantity, hapus item, clear cart
✅ Real-time price calculation dengan diskon
✅ Session-based cart storage
✅ Checkout process dengan validasi
```

### 🚚 Sistem Pengiriman

```
✅ Integrasi RajaOngkir API
✅ Pencarian lokasi dengan autocomplete
✅ Multiple courier options 
✅ Real-time shipping cost calculation
✅ Estimasi waktu pengiriman
```

### 💳 Transaksi & Payment

```
✅ Comprehensive checkout process
✅ Transaction detail dengan discount tracking
✅ Order history untuk customer
```

### 📊 Dashboard & Analytics

```
✅ Admin dashboard untuk management
✅ External dashboard dengan API consumption
✅ Real-time transaction monitoring
```

### 🔌 API & Integration

```
✅ JSON response format yang konsisten
✅ API key untuk pengiriman
✅ External dashboard integration
```

---

## 🛠️ Tech Stack

<table>
<tr>
<td>

**Backend**

- CodeIgniter 4+
- PHP 8.0+
- MySQL
- Composer
- Guzzle HTTP Client

</td>
<td>

**Frontend**

- Bootstrap 
- jQuery
- Select2 Plugin
- DataTables
- Bootstrap Icons

</td>
<td>

**Tools & Services**

- RajaOngkir API
- Xampp ( Apache, Mysql )

</td>
</tr>
</table>

---

## 🚀 Quick Start

### Prerequisites

```bash
✅ PHP >= 8.0
✅ MySQL >= 8.0
✅ Composer
✅ Apache/Nginx 
```

### Installation dalam 3 Langkah

```bash
# 1. Clone repository
git clone https://github.com/IqbalIka17/belajar-ci-tugas.git
cd belajar-ci

# 2. Install dependencies
composer install

# 3. Setup environment
cp env .env
# Edit .env file dengan konfigurasi database dan API keys

# 4. Setup database
php spark migrate
php spark db:seed UserSeeder
php spark db:seed ProductSeeder
php spark db:seed ProductDiskonSeeder

# 5. Start server
php spark serve
```

🎉 **Done!** Buka http://localhost:8080

### Login Credentials

```
👨‍💼 Admin:
Username: iqbaladmin
Password: 1234567

👤 Customer:
Username: iqbaluser
Password: 1234567
```

---

## 📦 Instalasi Lengkap

### 1. System Requirements

| Component  | Minimum                                 | Recommended      |
| ---------- | --------------------------------------- | ---------------- |
| PHP        | 8.0                                     | 8.0              |
| MySQL      | 8.0                                     | 8.0              |
| Memory     | 512MB                                   | 1GB+             |
| Extensions | intl, mbstring, json, mysqlnd, curl, gd | + opcache, redis |

### 2. Clone & Dependencies

```bash
# Clone project
git clone https://github.com/IqbalIka17/belajar-ci-tugas.git
cd belajar-ci

# Install Composer dependencies
composer install --optimize-autoloader

# Set permissions (Linux/Mac)
chmod -R 755 writable/
chmod -R 755 public/img/
```

### 3. Environment Configuration

```bash
# Copy environment template
cp env .env
```

### 4. Database Setup

```env
# Database Configuration
database.default.hostname = localhost
database.default.database = toko_online_db
database.default.username = your_username
database.default.password = your_password
database.default.DBDriver = MySQLi
database.default.port = 3306
```

```bash
# Create database
mysql -u root -p -e "CREATE DATABASE toko_online_db CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;"

# Run migrations
php spark migrate

# Seed initial data
php spark db:seed UserSeeder
php spark db:seed ProductSeeder
php spark db:seed ProductDiskonSeeder
```

### 5. API Configuration

```env
# Internal API Key
API_KEY = your-secret-api-key-2024

# RajaOngkir API (Register at rajaongkir.com)
COST_KEY = your-rajaongkir-api-key

# Application Settings
app.baseURL = 'http://localhost:8080/'
app.appTimezone = 'Asia/Jakarta'
app.sessionExpiration = 7200
```

## 🏗️ Struktur Proyek

```
belajar-ci/
├── 📁 app/                          # Core application
│   ├── 📁 Config/                   # Configuration files
│   │   ├── 📄 App.php              # App configuration
│   │   ├── 📄 Routes.php           # URL routing
│   │   ├── 📄 Filters.php          # Request filters
│   │   └── 📄 ...                  # Other configs
│   │
│   ├── 📁 Controllers/              # MVC Controllers
│   │   ├── 📄 AuthController.php   # Authentication logic
│   │   ├── 📄 Home.php            # Main page controller
│   │   ├── 📄 ProdukController.php # Product management
│   │   ├── 📄 DiskonController.php # Discount management
│   │   ├── 📄 TransaksiController.php # Cart & transactions
│   │   ├── 📄 ProdukKategoriController.php # Category management
│   │   └── 📄 ApiController.php    # RESTful API
│   │
│   ├── 📁 Models/                   # Data models
│   │   ├── 📄 UserModel.php        # User entity
│   │   ├── 📄 ProductModel.php     # Product entity
│   │   ├── 📄 ProductDiskonModel.php # Discount entity
│   │   ├── 📄 TransactionModel.php # Transaction entity
│   │   └── 📄 TransactionDetailModel.php # Transaction details
│   │
│   ├── 📁 Views/                    # Template files
│   │   ├── 📄 layout.php          # Main layout
│   │   ├── 📄 layout_clear.php    # Clean layout
│   │   ├── 📁 components/          # Reusable components
│   │   │   ├── 📄 header.php      # Header with discount notification
│   │   │   ├── 📄 footer.php      # Footer
│   │   │   └── 📄 sidebar.php     # Admin sidebar
│   │   ├── 📄 v_home.php          # Product catalog
│   │   ├── 📄 v_login.php         # Login page
│   │   ├── 📄 v_produk.php        # Product management
│   │   ├── 📄 v_diskon.php        # Discount management
│   │   ├── 📄 v_keranjang.php     # Shopping cart
│   │   ├── 📄 v_checkout.php      # Checkout process
│   │   ├── 📄 v_profile.php       # Order history
│   │   ├── 📄 v_contact.php       # Halaman Contact
│   │   ├── 📄 v_produkPDF.php     # Halaman PDF
│   │   └── 📄 v_faq.php           # FAQ page
│   │
│   ├── 📁 Database/                 # Database related
│   │   ├── 📁 Migrations/          # Database schema
│   │   │   ├── 📄 User.php        # Users table
│   │   │   ├── 📄 Product.php     # Products table
│   │   │   ├── 📄 Transaction.php # Transactions table
│   │   │   ├── 📄 TransactionDetail.php # Transaction details
│   │   │   └── 📄 ProductDiskon.php # Discounts table
│   │   └── 📁 Seeds/               # Initial data
│   │       ├── 📄 UserSeeder.php  # Default users
│   │       ├── 📄 ProductSeeder.php # Sample products
│   │       └── 📄 ProductDiskonSeeder.php # Sample discounts
│   │
│   └── 📁 Filters/                  # Request filters
│       ├── 📄 Auth.php            # Authentication filter
│       └── 📄 Redirect.php        # Redirect filter
│
├── 📁 public/                       # Web accessible files
│   ├── 📄 index.php               # Application entry point
│   ├── 📁 img/                    # Product images
│   ├── 📁 NiceAdmin/              # Admin template assets
│   │   ├── 📁 assets/             # CSS, JS, Images
│   │   └── 📁 forms/              # Form templates
│   └── 📁 dashboard-toko/         # External dashboard
│       └── 📄 index.php           # API consumer dashboard
│
├── 📁 writable/                     # Application writable files
│   ├── 📁 cache/                  # Cache files
│   ├── 📁 logs/                   # Application logs
│   └── 📁 session/                # Session storage
│
├── 📁 vendor/                       # Composer dependencies
├── 📄 .env                         # Environment configuration
├── 📄 composer.json               # PHP dependencies
├── 📄 spark                       # CLI tool
└── 📄 README.md                   # This file
```

---

## 🔌 API Documentation

### Base URL

```
https://yourdomain.com/api
```

### Authentication

Semua endpoint memerlukan API Key di header:

```bash
curl -H "Key: your-api-key-here" https://yourdomain.com/api
```

### Endpoints

#### 📊 GET /api - Get All Transactions

Mengambil semua data transaksi dengan detail lengkap

**Request:**

```bash
curl -X GET \
  -H "Key: your-api-key" \
  https://yourdomain.com/api
```

**Response:**

```json
{
  "status": {
    "code": 200,
    "description": "OK"
  },
  "results": [
    {
      "id": 1,
      "username": "iqbaluser",
      "total_harga": 1500000,
      "alamat": "Jl. Merdeka No. 123, Jakarta",
      "ongkir": 15000,
      "status": 1,
      "total_item": 3,
      "total_diskon": 150000,
      "created_at": "2025-07-03 10:30:00",
      "updated_at": "2025-07-03 10:30:00",
      "details": [
        {
          "id": 1,
          "transaction_id": 1,
          "product_id": 5,
          "jumlah": 2,
          "diskon": 50000,
          "subtotal_harga": 900000,
          "nama_produk": "Laptop Gaming",
          "foto_produk": "laptop.jpg",
          "harga_produk": 500000
        }
      ]
    }
  ]
}
```

#### 📋 GET /api/{id} - Get Transaction Detail

Mengambil detail transaksi berdasarkan ID

**Request:**

```bash
curl -X GET \
  -H "Key: your-api-key" \
  https://yourdomain.com/api/1
```

**Response:**

```json
{
  "status": {
    "code": 200,
    "description": "OK"
  },
  "results": {
    "id": 1,
    "username": "iqbaluser",
    "total_harga": 1500000,
    "total_item": 3,
    "total_diskon": 150000,
    "details": [...]
  }
}
```

## 📱 Penggunaan

### 1. Login sebagai Admin

1. Akses http://localhost:8080/login
2. Login dengan credentials admin
3. Kelola produk, kategori, dan diskon

### 2. Mengelola Diskon

1. Masuk ke menu "Diskon" (khusus admin)
2. Tambah diskon dengan tanggal yang unik
3. Sistem akan otomatis apply diskon untuk user yang login di tanggal tersebut

### 3. Shopping sebagai Customer

1. Login sebagai customer
2. Browse produk di halaman utama
3. Add to cart (diskon otomatis diterapkan jika ada)
4. Checkout dengan memilih alamat dan ongkir
5. Complete transaksi

### 4. Monitoring Dashboard

1. Akses external dashboard di http://localhost/dashboard-toko/
2. View real-time transaction data
3. Monitor jumlah item terjual per transaksi

---

### Debug Mode

Enable debug mode untuk development:

```env
# .env
CI_ENVIRONMENT = development
app.forceGlobalSecureRequests = false
```


## 🤝 Contributing

Kami sangat menghargai kontribusi dari community!

### Quick Contribute

1. **Fork** repository ini
2. **Clone** fork Anda:
   ```bash
   git clone https://github.com/yourusername/belajar-ci.git
   ```
3. **Create** branch baru:
   ```bash
   git checkout -b feature/amazing-feature
   ```
4. **Commit** perubahan:
   ```bash
   git commit -m "Add amazing feature"
   ```
5. **Push** ke branch:
   ```bash
   git push origin feature/amazing-feature
   ```
6. **Create** Pull Request


## 📞 Kontak & Support

<div align="center">

### 👥 Tim Developer

| Role          | Name    | Contact                                                                                             |
| ------------- | ------- | --------------------------------------------------------------------------------------------------- |
| **Developer** | [iqbal] | [![Email](https://img.shields.io/badge/-Email-red?style=flat&logo=gmail&logoColor=white)](mailto:#) |

</div>
