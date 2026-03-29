# Notes Application

Notes Application adalah proyek monorepo yang memisahkan aplikasi web (client) dan layanan API (server) untuk pengelolaan catatan. Proyek ini dirancang sebagai fondasi pembelajaran full-stack JavaScript dengan struktur yang jelas, mudah dikembangkan, dan mudah dipisah saat akan di-deploy.

## Gambaran Umum

Aplikasi memungkinkan pengguna membuat, membaca, memperbarui, dan menghapus catatan (CRUD). Frontend dibangun dengan Next.js untuk pengalaman antarmuka yang responsif, sementara backend dibangun dengan Express.js untuk menyediakan endpoint API yang ringan.

## Struktur Monorepo

1. `apps-web`
Frontend berbasis Next.js yang menangani tampilan, interaksi pengguna, dan konsumsi API.

2. `services-api`
Backend berbasis Express.js yang menyediakan endpoint `notes` dan logika pengelolaan data catatan in-memory.

## Arsitektur Komunikasi

Frontend berkomunikasi ke backend melalui HTTP API. Secara default, frontend mengarah ke `http://localhost:5000/` sebagai base URL API dan dapat diubah dari antarmuka aplikasi melalui fitur `Change URL`.

Pemisahan ini memberi beberapa keuntungan:

1. Frontend dan backend bisa dikembangkan secara independen.
2. Integrasi API dapat diuji tanpa bergantung pada penyatuan codebase.
3. Struktur siap ditingkatkan untuk skenario production (misalnya auth service, persistence database, dan deployment terpisah).

## Status Fitur Saat Ini

Yang sudah tersedia dan terhubung dengan baik:

1. Manajemen catatan dasar (CRUD) melalui endpoint `notes`.
2. Integrasi frontend-backend untuk alur catatan utama.

Yang masih bersifat pengembangan lanjutan:

1. Otorisasi/autentikasi penuh di backend.
2. Dukungan upload, kolaborasi, dan ekspor catatan pada sisi API.
3. Persistensi data permanen (saat ini masih in-memory).

## Tujuan Pengembangan

Repositori ini cocok digunakan sebagai:

1. Template awal aplikasi catatan full-stack.
2. Media belajar integrasi Next.js + Express.js.
3. Dasar refaktor ke arsitektur yang lebih modular (service-per-domain).