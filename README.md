# Cohort & Retention Analysis – Online Retail UK

## Business Understanding
Dalam proyek ini, saya melakukan analisis kohort dan retensi pelanggan berbasis waktu menggunakan Python untuk memahami perilaku pelanggan dari waktu ke waktu.
Dataset yang digunakan berasal dari Kaggle dan merupakan data transaksi aktual dari sebuah perusahaan ritel online berbasis di Inggris yang menjual hadiah unik untuk berbagai kesempatan, dengan sebagian besar pelanggannya berasal dari segmen grosir.

Karena sebagian besar dataset e-commerce bersifat privat dan sulit diakses, dataset ini menjadi sumber yang sangat berharga untuk eksplorasi analisis perilaku pelanggan.

Melalui analisis kohort, pelanggan dikelompokkan berdasarkan bulan pertama mereka melakukan pembelian (cohort month). Selanjutnya, dihitung cohort index sebagai jumlah bulan sejak akuisisi untuk mengukur retensi pelanggan dari waktu ke waktu.

Tujuan analisis:

- Menilai efektivitas strategi akuisisi dan retensi pelanggan.

- Mengidentifikasi cohort dengan tingkat loyalitas tinggi.

- Memberikan insight bagi pengambilan keputusan berbasis data.

- Hasil visualisasi disajikan dalam bentuk heatmap yang intuitif, memudahkan identifikasi pola retensi dan churn pelanggan.

## Data Understanding
Dataset berisi data transaksi dari perusahaan ritel online di Inggris antara 1 Desember 2010 – 9 Desember 2011.
Berikut adalah deskripsi variabel utama:

- Invoice :	Nomor faktur unik untuk setiap transaksi.
- StockCode :	Kode unik produk yang dijual.
- Description :	Deskripsi produk.
- Quantity :	Jumlah unit produk yang dibeli.
- InvoiceDate	: Tanggal & waktu transaksi.
- UnitPrice :	Harga per unit dalam Pound Sterling (£).
- CustomerID :	ID unik pelanggan.
- Country	: Negara asal pelanggan.

## Data Preparation
Langkah-langkah pembersihan data sebelum analisis:

1. Menghapus nilai duplikat untuk menghindari perhitungan ganda.

2. Menghapus nilai kosong (missing values) pada kolom penting seperti CustomerID dan Description.

3. Menghapus pesanan yang dibatalkan (canceled orders) dengan memfilter InvoiceNo yang diawali huruf "C".

4. Reformat timestamp pada kolom InvoiceDate menjadi format datetime agar dapat digunakan untuk ekstraksi bulan & tahun.

## Cohort Analysis – Hasil & Insight
<img width="827" height="684" alt="image" src="https://github.com/user-attachments/assets/0dab3cd5-68e1-4c6e-ac4e-de5e45a9e9bd" />


Berdasarkan hasil Cohort & Retention Analysis, terlihat bahwa pada bulan pertama setelah akuisisi semua cohort memiliki retensi 100%, namun mengalami penurunan signifikan pada bulan-bulan berikutnya. Sebagian besar cohort hanya mempertahankan 20–40% pengguna di bulan kedua dan stabil di kisaran 20–30% setelah bulan ketiga, menunjukkan adanya basis pengguna loyal namun relatif kecil. Cohort Desember 2010 memiliki kinerja retensi terbaik, bahkan mencapai 50% di bulan ke-11, sedangkan cohort pertengahan hingga akhir 2011 menunjukkan retensi yang lebih rendah, beberapa hanya 10–20% setelah 3–4 bulan. Pola ini menunjukkan perlunya strategi engagement yang lebih efektif di bulan-bulan awal, serta analisis lebih lanjut terhadap cohort dengan retensi tinggi untuk mengidentifikasi faktor keberhasilannya.

