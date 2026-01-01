# TradeTools Hub

> Kumpulan alat bantu sederhana untuk membantu Anda menganalisis pasar, menghitung risiko, dan mencatat performa trading.

[![Version](https://img.shields.io/badge/version-1.2-blue.svg)](https://github.com/yourusername/tradetools-hub)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)

## 📋 Daftar Isi

- [Tentang Project](#-tentang-project)
- [Fitur Utama](#-fitur-utama)
- [Teknologi](#-teknologi)
- [Instalasi](#-instalasi)
- [Penggunaan](#-penggunaan)
- [Struktur File](#-struktur-file)
- [Kontribusi](#-kontribusi)
- [Lisensi](#-lisensi)

## 🎯 Tentang Project

**TradeTools Hub** adalah koleksi web tools yang dirancang khusus untuk trader. Project ini menyediakan tiga alat utama yang membantu trader dalam menghitung profit/loss, mencatat performa trading, dan menghitung proyeksi compound interest. Semua tools dibangun dengan teknologi web modern, ringan, dan dapat diakses melalui browser tanpa perlu instalasi aplikasi tambahan.

## ✨ Fitur Utama

### 1. **Pip Calculator** (`calc.html`)

Kalkulator pip yang mendukung berbagai instrumen trading dengan kemampuan menghitung estimasi profit/loss secara real-time.

**Instrumen yang Didukung:**
- **Forex Major Pairs** - EUR/USD, GBP/USD, USD/JPY, AUD/USD
- **Commodities** - XAU/USD (Gold), XAG/USD (Silver), XTI/USD (Oil)
- **Cryptocurrency** - BTC/USD, ETH/USD
- **Indices** - US100 (Nasdaq), US30 (Dow Jones)

**Fitur Kalkulator:**
- Hitung estimasi profit/loss berdasarkan entry dan target price
- Kalkulasi otomatis nilai pip/point sesuai instrumen
- Support custom lot size (dari 0.01 lot)
- Responsive design untuk mobile dan desktop
- Real-time calculation dengan validasi input
- Format currency USD untuk hasil perhitungan

**Cara Kerja:**
- Standard calculation untuk forex major pairs dan commodities
- Inverse calculation untuk USD/JPY
- Raw calculation untuk crypto dan indices
- Automatic pip/point detection berdasarkan instrumen

### 2. **Trading Journal** (`journal.html`)

Aplikasi journaling lengkap untuk tracking dan analisis performa trading dengan penyimpanan data lokal.

**Dashboard Analytics:**
- **Win Rate** - Persentase trade yang profit
- **Total Trades** - Jumlah total trade yang dicatat
- **Net P&L** - Total profit/loss keseluruhan dalam USD

**Fitur Journaling:**
- **Entry Management** - Tambah, edit, dan hapus trade entries
- **Detail Recording** - Catat pair, posisi (Long/Short), entry/exit price, stop loss
- **Status Tracking** - Win, Loss, atau Break Even (BE)
- **P&L Recording** - Automatic color coding (hijau untuk profit, merah untuk loss)
- **TradingView Integration** - Simpan dan akses link chart langsung dari journal
- **Bulk Operations** - Select mode untuk hapus multiple entries sekaligus
- **Date Stamping** - Automatic timestamp untuk setiap trade

**Data Storage:**
- Menggunakan Local Storage browser
- Data tersimpan secara persisten
- Privacy-first approach (tidak ada cloud sync)
- Format JSON untuk easy export/import

**User Interface:**
- Card-based layout untuk easy reading
- Color-coded trade status (Win/Loss/BE)
- Tag system untuk Long/Short position
- Modal form untuk input/edit data
- Responsive mobile-first design

### 3. **Compound Calculator** (`compound.html`)

Kalkulator untuk proyeksi pertumbuhan modal dengan sistem bunga majemuk (compound interest).

**Fitur Kalkulasi:**
- Input nilai awal (modal awal)
- Set periode compound (berapa kali perhitungan)
- Custom rate (suku bunga dalam persen)
- Support multiple currency (USD, IDR)
- Counter control untuk adjust jumlah perhitungan

**Visualisasi:**
- Timeline growth display
- Numbered periode untuk setiap hasil compound
- Format currency dengan pemisah ribuan
- Real-time calculation tanpa page reload

**Interface:**
- Minimalist design dengan gradient effects
- Button controls untuk increment/decrement periode
- Dropdown currency selector
- Result display dengan auto-formatting

## 🛠 Teknologi

Project ini dibangun menggunakan teknologi web native tanpa framework atau library eksternal:

**Core Technologies:**
```
HTML5      - Struktur dan semantic markup
CSS3       - Styling dengan CSS Custom Properties (variables)
JavaScript - Vanilla JS untuk logic dan interactivity
```

**Design System:**
- Dark mode theme dengan custom color palette
- CSS Grid dan Flexbox untuk layout
- Glassmorphism effects dengan backdrop-filter
- Smooth animations dan transitions
- Responsive breakpoints untuk mobile/tablet/desktop

**Fonts:**
- Inter - Digunakan di Pip Calculator dan Trading Journal
- Poppins - Digunakan di Compound Calculator
- Loaded via Google Fonts CDN

**Browser Compatibility:**
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Membutuhkan support untuk ES6, CSS Grid, dan Local Storage

## 📦 Instalasi

### Metode 1: Clone Repository

```bash
# Clone repository
git clone https://github.com/yourusername/tradetools-hub.git

# Masuk ke directory
cd tradetools-hub

# Buka index.html di browser
# Atau gunakan live server
```

### Metode 2: Download ZIP

1. Download ZIP dari repository
2. Extract ke folder pilihan Anda
3. Buka `index.html` dengan browser favorit

### Metode 3: Local Development Server (Recommended)

**Menggunakan Python:**
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

**Menggunakan Node.js:**
```bash
# Install http-server globally
npm install -g http-server

# Run server
http-server -p 8000
```

**Menggunakan VS Code:**
- Install extension "Live Server"
- Right-click pada `index.html`
- Pilih "Open with Live Server"

Kemudian akses di browser: `http://localhost:8000`

## 🚀 Penggunaan

### Pip Calculator

**Langkah Penggunaan:**
1. Buka halaman Pip Calculator
2. Pilih instrumen/pair dari dropdown menu
3. Masukkan **Open Price** (harga entry Anda)
4. Masukkan **Target Price** (harga target/exit yang diinginkan)
5. Tentukan **Lot Size** (default: 0.01, bisa disesuaikan)
6. Klik tombol **"Hitung Profit"**
7. Hasil akan muncul menampilkan jarak pergerakan (pips/points) dan estimasi profit/loss

**Contoh Perhitungan:**
```
Instrumen: XAUUSD (Gold)
Open Price: 2640.00
Target Price: 2650.00
Lot Size: 0.01

Result:
- Jarak Pergerakan: 100.0 Points
- Estimasi Profit: +$1.00
```

**Tips:**
- Gunakan titik (.) sebagai pemisah desimal
- Perhatikan contoh harga yang muncul sesuai instrumen
- Lot size standar: 0.01 = micro lot, 0.1 = mini lot, 1.0 = standard lot
- Hasil negatif menunjukkan loss, positif menunjukkan profit

### Trading Journal

**Menambah Entry Baru:**
1. Klik tombol **"+ Jurnal Baru"**
2. Isi form dengan lengkap:
   - **Pair**: Instrumen yang ditrade (contoh: XAUUSD, EURUSD)
   - **Posisi**: Pilih Long (Buy) atau Short (Sell)
   - **Entry Price**: Harga masuk trade
   - **Exit Price**: Harga keluar trade
   - **Stop Loss**: Level SL yang dipasang
   - **Status**: Win, Loss, atau BE (Break Even)
   - **Profit/Loss**: Nominal dalam USD
   - **Link TradingView**: (Opsional) URL chart untuk referensi
3. Klik **"Simpan Data"**

**Mengedit Entry:**
1. Klik pada card trade yang ingin diedit
2. Modal akan terbuka dengan data yang sudah terisi
3. Ubah data yang diperlukan
4. Klik **"Simpan Data"**

**Menghapus Entry:**
1. Klik tombol **"Pilih"** untuk masuk selection mode
2. Tap/klik pada trade entries yang ingin dihapus
3. Entry yang terpilih akan mendapat checkmark
4. Klik **"Hapus Terpilih (X)"** dimana X adalah jumlah entry terpilih
5. Konfirmasi penghapusan
6. Klik **"Batal"** untuk keluar dari selection mode

**Membuka Chart TradingView:**
- Jika trade memiliki link TradingView (terlihat icon link di card)
- Klik card untuk membuka modal edit
- Klik link **"Buka Chart di Browser"**
- Chart akan terbuka di tab baru

### Compound Calculator

**Langkah Penggunaan:**
1. Gunakan tombol **+** / **-** untuk set jumlah output (periode tampilan)
2. Masukkan **Nilai Awal** dalam field pertama (modal awal)
3. Masukkan **Periode Compound** (berapa kali proses compounding)
4. Masukkan **Suku Bunga** dalam persen (contoh: 5 untuk 5%)
5. Pilih **Currency** dari dropdown (USD atau IDR)
6. Klik tombol **"Compound"**

**Contoh Perhitungan:**
```
Nilai Awal: $1000
Periode: 12
Suku Bunga: 5%
Currency: USD

Result:
Periode 1: $1,000.00
Periode 2: $1,050.00
Periode 3: $1,102.50
... (dan seterusnya)
```

**Formula yang Digunakan:**
```
Compound Value = Initial Value × (1 + Rate/100)^Period
```

## 📁 Struktur File

```
tradetools-hub/
│
├── index.html          # Landing page / dashboard utama
├── calc.html           # Pip Calculator
├── journal.html        # Trading Journal
├── compound.html       # Compound Calculator
├── README.md           # Dokumentasi project
└── LICENSE             # Lisensi MIT
```

### Detail File:

#### `index.html`
**Fungsi:** Landing page utama yang berfungsi sebagai hub untuk navigasi ke semua tools.

**Komponen:**
- Navigation bar dengan branding
- Hero section dengan judul dan deskripsi
- Card grid untuk 3 tools utama
- Footer dengan copyright info
- Glow effect untuk visual enhancement

**Styling:**
- Dark theme dengan custom CSS variables
- Grid responsive (1 kolom mobile, 2 kolom tablet, 3 kolom desktop)
- Hover effects pada cards
- Glassmorphism navbar dengan backdrop-filter

#### `calc.html`
**Fungsi:** Standalone pip calculator untuk berbagai instrumen trading.

**Komponen:**
- Navigation bar dengan link ke Journal
- Dropdown selector untuk instrumen
- Input fields untuk open price, target price, lot size
- Calculate button dengan onClick handler
- Result area dengan animation

**Logic:**
- Config object berisi setting untuk setiap instrumen:
  - `type`: std (standard), inv (inverse), raw
  - `k`: contract size multiplier
  - `pip`: pip/point size
  - `ex`: example price
- Function `calculate()` untuk komputasi profit/loss
- Function `updateUI()` untuk sync placeholder dengan instrumen

**Storage:** Tidak menggunakan storage (stateless calculator)

#### `journal.html`
**Fungsi:** Full-featured trading journal dengan CRUD operations.

**Komponen:**
- Stats dashboard (Win Rate, Total, Net P&L)
- Dual toolbar (default & selection mode)
- Trade cards list dengan dynamic rendering
- Modal form untuk input/edit
- Checkboxes untuk bulk selection

**Logic:**
- `data` array untuk store trade entries
- `render()` function untuk update DOM
- `stats()` function untuk calculate metrics
- `save()` function untuk CRUD operations
- Selection mode dengan `Set` untuk track selected IDs

**Storage:**
- Key: `TJ_DATA_FINAL_REV`
- Format: JSON array of objects
- Persistence: LocalStorage browser
- Structure: `{ id, date, pair, type, status, pnl, entry, exit, sl, tvlink }`

#### `compound.html`
**Fungsi:** Compound interest calculator dengan periode visualization.

**Komponen:**
- Counter controls (+/- buttons)
- Input fields untuk nilai awal, periode, rate
- Currency selector (USD/IDR)
- Result area dengan numbered list
- Compound button

**Logic:**
- `compoundTheValue()` function dengan loop untuk kalkulasi
- Dynamic result rendering dengan `createElement()`
- CSS counter untuk automatic periode numbering
- Currency formatting dengan `Intl.NumberFormat`

**Storage:** Tidak menggunakan persistent storage

## 🤝 Kontribusi

Kontribusi sangat diterima! Untuk berkontribusi pada project ini:

1. Fork repository
2. Buat feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request

**Guidelines:**
- Pastikan code rapi dan readable
- Test semua fitur sebelum submit PR
- Ikuti styling convention yang ada
- Update README jika menambah fitur baru
- Gunakan vanilla JavaScript (no frameworks)

## 📝 Changelog

### [1.2] - 2026-01-02
- Added Compound Calculator tool
- Improved mobile responsiveness across all pages
- Fixed pip calculation for JPY pairs
- Enhanced UI with glassmorphism effects
- Updated navigation links between tools

### [1.1] - 2025-12-15
- Added Trading Journal feature
- Implemented LocalStorage persistence
- Added TradingView link integration
- Created stats dashboard
- Added bulk delete functionality

### [1.0] - 2025-12-01
- Initial release
- Pip Calculator for Forex, Gold, Crypto, Indices
- Landing page design
- Responsive mobile-first layout

## 📄 Lisensi

Project ini dilisensikan di bawah MIT License. Lihat file `LICENSE` untuk informasi lengkap.

```
MIT License

Copyright (c) 2026 TradeTools Hub

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

<div align="center">

**⭐ Star repository ini jika bermanfaat! ⭐**

Made with ❤️ for Traders

</div>
