# **Aplikasi Chat Realtime dengan Laravel**

Aplikasi chat berbasis web menggunakan **Laravel, Chatify, dan Pusher** untuk komunikasi realtime.


## **Screenshoot**
User 1:
<img src="https://drive.google.com/file/d/1rgJLkwo7YbyiFdSL7VlL01Nb5TUVjte7/view?usp=drive_link">

User 2:
<img src="https://drive.google.com/file/d/1TXm2vTibMj9f4oMlPE1RYkEqtHtplfei/view?usp=sharing">

## **Fitur**
✅ Chat privat antara pengguna
✅ Dukungan WebSocket dengan Pusher
✅ Tampilan modern dengan Chatify
✅ Autentikasi pengguna menggunakan Laravel Breeze

---

## **1. Instalasi**

### **1.1 Clone Repository**
Jalankan perintah berikut untuk meng-clone repository ke komputer Anda:

```bash
git clone https://github.com/username/repository.git
```

*(Gantilah `username/repository` dengan repo GitHub yang sesuai.)*

Masuk ke direktori proyek:

```bash
cd repository
```

### **1.2 Instal Dependensi Laravel**
```bash
composer install
```

### **1.3 Buat dan Konfigurasi File `.env`**
Salin file `.env.example` menjadi `.env`:

```bash
cp .env.example .env
```

Generate key aplikasi Laravel:

```bash
php artisan key:generate
```

Edit file `.env` dan sesuaikan pengaturan database:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nama_database
DB_USERNAME=root
DB_PASSWORD=yourpassword
```

---

## **2. Konfigurasi Chatify dan Pusher**

### **2.1 Instalasi Chatify**
```bash
composer require munafio/chatify
php artisan chatify:install
```

### **2.2 Konfigurasi Pusher**
Daftar akun di [Pusher](https://pusher.com/), buat aplikasi baru, dan salin kredensialnya ke file `.env`:

```env
PUSHER_APP_ID=your_app_id
PUSHER_APP_KEY=your_app_key
PUSHER_APP_SECRET=your_app_secret
PUSHER_APP_CLUSTER=mt1
```

---

## **3. Migrasi Database dan Seed Data**

Jalankan perintah berikut untuk melakukan migrasi database:

```bash
php artisan migrate --seed
```

Jika ingin menghapus dan mengulang migrasi dari awal:

```bash
php artisan migrate:fresh --seed
```

---

## **4. Menjalankan Aplikasi**

### **4.1 Jalankan Server Laravel**
```bash
php artisan serve
```

Akses aplikasi di `http://127.0.0.1:8000`.

### **4.2 Menjalankan Vite untuk Frontend**
Jika menggunakan Laravel Breeze:

```bash
npm install && npm run dev
```

---

## **5. Pengujian Chat**

1. **Daftarkan dua pengguna baru.**
2. **Login dengan kedua akun di dua browser berbeda.**
3. **Kirim pesan dan pastikan pesan muncul secara realtime tanpa refresh.**

Jika terjadi error pada WebSocket, pastikan kredensial Pusher sudah benar dan jalankan ulang server.

---

## **6. Troubleshooting**

| Masalah                          | Solusi |
|----------------------------------|--------|
| Chat tidak realtime | Periksa konfigurasi Pusher di `.env` |
| Error saat migrasi database | Pastikan koneksi database sudah benar di `.env` |
| CSS/JS tidak muncul | Jalankan `npm install && npm run dev` |

---

## **7. Teknologi yang Digunakan**
- Laravel
- Chatify
- Pusher
- Laravel Breeze
- MySQL

---

## **Lisensi**
Proyek ini menggunakan lisensi **MIT**. Silakan gunakan dan modifikasi sesuai kebutuhan.
