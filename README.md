# 📈 TradeTools Hub

**TradeTools Hub** adalah kumpulan alat bantu (toolkit) berbasis web yang dirancang khusus untuk trader. Aplikasi ini ringan, responsif, dan berjalan sepenuhnya di sisi klien (browser) tanpa memerlukan backend server.

Dibangun dengan antarmuka modern bernuansa **Dark Mode** (terinspirasi oleh gaya *shadcn/ui*), aplikasi ini mencakup tiga fitur utama: Kalkulator Pip, Jurnal Trading, dan Kalkulator Compounding.

![Project Status](https://img.shields.io/badge/Status-Active-success?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)

## ✨ Fitur Utama

### 1. 🏠 Dashboard (Hub)
- Halaman pendaratan (Landing Page) yang modern dengan efek *glow* dan navigasi responsif.
- Desain *mobile-first* yang menyesuaikan tampilan grid berdasarkan ukuran layar.

### 2. 🧮 Pip & Profit Calculator
- **Multi-Aset:** Mendukung Forex (Major), Commodities (Gold/XAU, Silver, Oil), Crypto (BTC, ETH), dan Indices (US30, Nas100).
- **Logika Cerdas:** Menghitung pip/poin secara otomatis berdasarkan tipe instrumen (Standard, Inverted, atau Raw).
- **Estimasi Profit:** Menghitung potensi keuntungan/kerugian berdasarkan Lot Size, Entry, dan Target Price.

### 3. 📓 Trading Journal
- **Penyimpanan Lokal:** Menggunakan `localStorage` browser, sehingga data tersimpan aman di perangkat Anda tanpa perlu database.
- **Statistik Otomatis:** Menghitung **Win Rate**, **Total Trade**, dan **Net PnL** secara real-time.
- **Manajemen Jurnal:** Fitur *Create, Edit, Delete* (CRUD) yang mudah.
- **Mode Seleksi:** Fitur *bulk delete* untuk menghapus banyak jurnal sekaligus.
- **TradingView Link:** Menyimpan link chart analisis Anda.

### 4. 🚀 Compound Calculator
- Simulasi pertumbuhan akun dengan bunga majemuk (compounding).
- Rincian pertumbuhan per periode.
- Format mata uang otomatis (IDR/USD).

---

## 🛠️ Teknologi yang Digunakan

Proyek ini dibangun menggunakan **Vanilla Web Technologies** murni untuk performa maksimal dan kemudahan deployment:

- **HTML5:** Struktur semantik.
- **CSS3:** Styling modern menggunakan *CSS Variables*, *Flexbox*, *Grid*, dan *Backdrop Filter*. Tidak ada framework CSS eksternal (style ditulis manual meniru estetika modern).
- **JavaScript (ES6+):** Logika kalkulasi, manipulasi DOM, dan manajemen `localStorage`.

---

## 📂 Struktur Folder

```bash
.
├── index.html      # Halaman utama (Menu/Hub)
├── calc.html       # Halaman Pip Calculator
├── journal.html    # Halaman Trading Journal
├── compound.html   # Halaman Compound Calculator
└── README.md       # Dokumentasi proyek
