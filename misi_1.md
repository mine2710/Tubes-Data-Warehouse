# LAPORAN MISI PERTAMA PERGUDANGAN DATA


## FASHION RETAIL SALES

**Perancangan dan Implementasi Gudang Data: Studi Kasus Penjualan Ritel Fashion**

## A. Profil Industri dan Masalah Bisnis

Industri Fashion, khususnya pada sektor retail, saat ini mengalami perkembangan yang cukup pesat. Namun, tetap menghadapi tantangan yang cukup kompleks, terutama dalam proses penjualan secara online. Meskipun produk yang ditawarkan memiliki kualitas yang baik dan harga yang kompetitif, banyak konsumen mengalami kesulitan dalam menemukan produk yang mereka inginkan di e-commerce. Hal ini disebabkan oleh tampilan website ataupun aplikasi yang digunakan kurang user-friendly, sehingga pelanggan cenderung memilih meinggalkan website tanpa melakukan pembelian. Kondisi ini dapat berdampak langsung pada penurunan kepuasan pelanggan dan angka penjualan harian. Oleh karena itu, pentingnya bagi pelaku bisnis untuk meningkatkan pengalaman pelanggan melalui integarsi teknologi. Salah satu solusi yang dapat diterapkan dengan cara melakukan pendekatan omnichannel, yaitu pendekatan dengan cara menggabungkan sistem penjualan offline dan online agar pengalaman pelanggan bisa lebih konsisten. Contohnya seperti menggunakan bantuan teknologi chatbot ataupun fitur pencarian produk berbasis AI, untuk membantu pelanggan dalam menemukan produk yang mereka cari dengan lebih mudah dan cepat. Dalam penerapan strategi ini, tidak hanya mampu dalam meningkatkan kepuasan konsumen dalam proses berbelanja, tetapi juga dapat berpotensi dalam peningkatan user experience, menekan biaya distribusi dan memperkenalkan produk baru dengan cara lebih efisien.

## B. Daftar Stakeholder & Tujuan Bisnis Daftar Stakeholder
**Daftar Stakeholder**

| Jabatan              | Peran                                                                                                                                |
| ------------------   | ------------------------------------------------------------------------------------------------------------------------------------ |
| Manager Logistik     | Untuk mengelola operasional rantai distribusi, pengiriman produk dan pengelolaan stok barang                                         |
| Tim Marketing        | Menyusun strategi pemasaran, promosi penjualan, melakukan kegiatan branding                                                          |
| Analisis Keuangan    | Mengawasi aspek keuangan bisnis, termasuk estimasi penjualan, manajemen biaya dan analisis keuntungan                                |
| Manajer Operasional  | Bertanggung jawab untuk operasi harian di toko dan mengelola kualitas layanan pelanggan                                              |
| Desain Produk        | Bertanggung jawab untuk menciptakan bentuk, tampilan dan fungsionalitas produk yang memenuhi kebutuhan dan keinginan konsumen        |
| Tim Penjualan        | Bertanggung jawab untuk menciptakan bentuk, tampilan dan fungsionalitas produk yang memenuhi kebutuhan dan keinginan konsumen        |

**Tujuan Bisnis**
| Tujuan Bisnis               | Deskripsi                                                                                                                         |
| ------------------   | ---------------------------------------------------------------------------------------------------------------------------------------- |
| Meningkatkan Retensi Pelanggan    | Berfokus pada strategi untuk mempertahankan pelanggan yang sudah ada                                                        |
| Mengurangi Biaya Distribusi       | Mengoptimalkan rantai distribusi dan pengiriman barang untuk menurunkan biaya logistik                                      |
| Memperkenalkan produk baru secara efektif | Menjamin setiap produk baru dikenal luas melalui promosi dan teknik pemasaran yang efektif dan tepat sasaran     |
| Meningkatkan penjualan online  | BMemanfaatkan platform digital untuk meningkatkan penjualan melalui e-commerce                                                 |
| Menjaga kualitas layanan pelanggan       | Meningkatkan pengalaman pelanggan agar pelanggan merasa puas dalam setiap interaksi baik secara online maupun offline|

**Interview simulasi**

| Stakeholder              | Pertanyaan interview simulasi                                                                                                      |
| ------------------   | ------------------------------------------------------------------------------------------------------------------------------------ |
| Manager Logistik     | Apa tantangan terbesar yang anda hadapi dalam menjaga stok barang tetap tersedia?                                         |
| Tim Marketing        | Apa pendekatan yang anda gunakan untuk meningkatkan penjualan terhadap barang yang semakin kompetitif di pasar?                                                          |
| Analisis Keuangan    | Apa langkah yang Anda lakukan ketika terjadi ketidaksesuaian antara laporan keuangan dan stok aktual di toko?                                |
| Manajer Operasional  | Indikator apa yang anda gunakan untuk mengukur keberhasilan operasional ?                                              |
| Desain Produk        | Apa yang menjadi tantangan utama dalam menjaga keseimbangan antara estetika desain dan efisiensi biaya produksi?        |
| Tim Penjualan        | Apa feedback yang sering anda terima dari pelanggan terkait produk atau pengalaman belanja?      |

**Studi Kasus(Analisis Masalah Nyata di Industri Fashion Retail Sales)**
Masalah :Sebuah toko retail fashion yang sedang mengalami penurunan penjualan online, Meskipun barang yang dijual terdiri dari berbagai produk dengan kualitas yang baik serta harga yang bersaing. Hal ini terjadi karena pelanggan yang sering mengalami kesulitan untuk menemukan produk yang mereka inginkan dan pengalaman kerja yang tidak memadai.
Solusi yang diusulkan:

1. Memanfaatkan Aplikasi E-commerce agar memudahkan dalam melakukan pencarian produk .
2. Peningkatan Pengalaman Pelanggan : Menerapkan fitur chatbots untuk membantu pelanggan dalam melakukan pencarian produk.




## C. Fakta & Dimensi
![Diagram Gudang Data](https://github.com/username/Tubes-Data-Warehouse/raw/main/fix.drawio.png)

### Tabel Dimensi

| Tabel Dimensi | Atribut               | Deskripsi                            |
| ------------- | --------------------- | ------------------------------------ |
| Pelanggan     | Customer Reference ID | ID unik pelanggan                    |
|               | Customer Name         | Nama pelanggan                       |
|               | Customer Address      | Alamat pelanggan                     |
|               | Customer Email        | Email pelanggan                      |
| Pembayaran    | Payment Method ID     | ID metode pembayaran                 |
|               | Payment Method        | Jenis pembayaran (Cash, Credit Card) |
| Item          | Item ID               | ID produk                            |
|               | Item Purchased        | Nama produk yang dibeli              |
| Tanggal       | Date Key              | ID tanggal pembelian                 |
|               | Date Purchase         | Tanggal pembelian                    |

### Tabel Fakta

| Tabel Fakta         | Atribut                    | Deskripsi                            |
| ------------------- | -------------------------- | ------------------------------------ |
| Transaksi Penjualan | Transaction ID             | ID unik transaksi                    |
|                     | Payment Method ID (FK)     | Relasi ke Dimensi Pembayaran         |
|                     | Customer Reference ID (FK) | Relasi ke Dimensi Pelanggan          |
|                     | Item ID (FK)               | Relasi ke Dimensi Item               |
|                     | Date Key (FK)              | Relasi ke Dimensi Tanggal            |
|                     | Purchase Amount (USD)      | Jumlah uang pembelian dalam USD      |
|                     | Review Rating              | Rating pelanggan terhadap produk     |
|                     | Total Discount             | Diskon yang diberikan pada transaksi |

## D. Sumber Data & Metadata

###  1. Identifikasi Sumber Data

Nama Dataset : Fashion Retail Sales
Jenis File : CSV ( Comma-Separated Values)
Sumber Data : File CSV dari Kaggle/GitHub (open-source)
Tipe Sumber Data : Transaksi penjualan ritel fashion (berbasis file, bukan database langsung)
Link Dataset : Kaggle_Fashion_Retail_Sales

###  2. Frekuensi Update
Sumber data : File CSV (Transaksi)
Frekuensi Update : Tidak real-time (batch, bisa harian/mingguan tergantung dengan proses ETL

###  3. Dokumentasi Metadata
| Nama Kolom         | Tipe Data                    | Deskripsi                           |
| ------------------- | -------------------------- | ------------------------------------ |
| Customer Reference ID | Integer              | ID unik pelanggan. Tidak menyimpan informasi pribadi, hanya nomor acak.                    |
| Item Purchased                     | String      | Nama item fashion yang dibeli (contoh: "Handbag", "Leggings").        |
| Date Purchase                    | Float  | Tanggal transaksi dilakukan dalam format YYYY-MM-DD          |
| Review Rating                    | Date              | Penilaian pelanggan terhadap produk (skala 1–5).              |
| Payment Method                    | String               | Metode pembayaran: contoh "Credit Card", "Cash".            |
| Purchase Amount (USD)                     | Float     | Nilai pembelian dalam dolar AS, sudah termasuk pajak     |
