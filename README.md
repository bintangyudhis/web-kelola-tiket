# Web Kelola Tiket

Web Kelola Tiket adalah backend API untuk aplikasi pengelolaan tiket bantuan. Pengguna terdaftar dapat membuat tiket dan menulis balasan pada tiket. Sisi server menyediakan endpoint autentikasi, data statistik dashboard, dan pengelolaan tiket dalam format JSON. Repositori ini berisi kode backend saja. Frontend terpisah tidak disertakan.

## Fitur

- Registrasi dan login pengguna dengan token Laravel Sanctum
- Endpoint profil pengguna yang sedang login dan logout
- Daftar tiket dengan pencarian dan filter
- Detail tiket berdasarkan kode tiket
- Buat tiket baru dengan validasi form request
- Balasan tiket oleh pengguna
- Statistik jumlah tiket untuk dashboard
- Response API terstruktur memakai API Resource

## Teknologi

- PHP 8.2
- Laravel 12
- Laravel Sanctum
- MySQL
- Vite dan Tailwind CSS untuk aset bawaan

## Cara Instalasi

Prasyarat:

- PHP 8.2 atau lebih baru
- Composer
- MySQL

Langkah instalasi:

1. Clone repositori ini.
2. Masuk ke folder proyek lalu jalankan `composer install`.
3. Salin file `.env.example` menjadi `.env`, lalu sesuaikan isinya. Bagian penting adalah `APP_KEY` dan koneksi database `DB_CONNECTION`, `DB_HOST`, `DB_PORT`, `DB_DATABASE`, `DB_USERNAME`, `DB_PASSWORD`. Nama database bawaan pada `.env.example` adalah `api_tick_track`.
4. Jalankan `php artisan key:generate`.
5. Jalankan `php artisan migrate`.

## Cara Menjalankan

```bash
php artisan serve
```

API berjalan di `http://127.0.0.1:8000`. Endpoint utama berada pada grup autentikasi, tiket, dan balasan tiket.

## Catatan Kelengkapan Repositori

Repositori ini belum menyertakan beberapa berkas kerangka Laravel, yaitu file `artisan`, folder `bootstrap`, folder `routes`, dan folder `database`. Karena itu proyek belum dapat dijalankan langsung dari hasil clone. Kode yang tersedia adalah controller, model, form request, API resource, konfigurasi, dan view bawaan. Berkas kerangka yang hilang perlu dilengkapi lebih dulu, misalnya dari proyek Laravel 12 baru, sebelum mengikuti langkah instalasi di atas.

## Lisensi

Proyek ini memakai lisensi MIT. Lihat berkas [LICENSE](LICENSE).
