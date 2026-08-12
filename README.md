# Perancangan Data Warehouse — Fashion Retail Sales

Proyek perancangan **Data Warehouse** untuk studi kasus **penjualan ritel fashion
(Fashion Retail Sales)**. Mencakup analisis kebutuhan bisnis, identifikasi stakeholder,
pemodelan dimensional (star schema), dan perancangan proses ETL.

**Konteks bisnis:** industri fashion retail menghadapi penurunan penjualan online akibat
pengalaman belanja yang kurang optimal. Data warehouse dirancang untuk mendukung analisis
perilaku pelanggan, produk terlaris, metode pembayaran, dan tren pendapatan berdasarkan waktu.

## Ruang Lingkup
- **Misi 1:** Analisis kebutuhan bisnis dan identifikasi sumber data.
- **Misi 2:** Perancangan skema dimensional (fact & dimension table) dan desain ETL.
- Diagram skema tersedia pada `fix.drawio.png`.

## Isi Repo
```
├── misi_1.md                     # Dokumentasi analisis kebutuhan
├── misi2.md                      # Dokumentasi perancangan skema
├── misi 1.pdf                    # Laporan Misi 1
├── Tugas Misi 2 _Kelompok 24.pdf # Laporan Misi 2
└── fix.drawio.png                # Diagram skema data warehouse
```

## Desain Skema (Star Schema)
- **Fact table — Transaksi Penjualan:** Purchase Amount (USD), Review Rating, Total
  Discount, dengan foreign key ke seluruh dimensi.
- **Dimensi:**
  - **Pelanggan** — Customer Reference ID, nama, alamat, email
  - **Item** — Item ID, nama produk
  - **Tanggal** — Date Key, tanggal pembelian
  - **Pembayaran** — Payment Method ID, jenis pembayaran (Cash, Credit Card)

## Sumber Data
- Dataset **Fashion Retail Sales** (format CSV, sumber Kaggle/open-source).
- Update bersifat batch (harian/mingguan) melalui proses ETL, bukan real-time.

## Konsep yang Diterapkan
- Pemodelan dimensional (**star schema**)
- Fact table & dimension table + denormalisasi untuk performa query
- Proses **ETL** (Extract dari CSV → Transform/mapping → Load ke dimensi & fakta)
- Perancangan diagram skema menggunakan **draw.io** (`fix.drawio.png`)

## Tim
Proyek Kelompok 24 — Mata kuliah Data Warehouse, ITERA.

## Author
**Sofyan Fauzi Dzaki Arif** — [github.com/mine2710](https://github.com/mine2710)
