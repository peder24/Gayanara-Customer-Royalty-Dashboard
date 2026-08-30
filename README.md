# GAYANARA - Customer Loyalty & Retention Dashboard
### Business Intelligence README | Data Coverage: 2022-2024

![Customer Loyalty & Retention Dashboard](https://res.cloudinary.com/dk2tex4to/image/upload/v1788071053/Screenshot_2026-08-30_132353_cysoix.png)

> **Audience:** C-level, Sales Director, CRM Manager, Marketing Manager
> **Tujuan dokumen ini:** Memberikan konteks analitik lengkap atas data yang ditampilkan di dashboard Customer Loyalty & Retention, sehingga stakeholder dapat memahami perilaku pembelian berulang pelanggan dan mengambil keputusan berbasis data untuk meningkatkan loyalitas pelanggan.
> **Catatan penting:** Seluruh KPI dan analisis **tidak termasuk** order berstatus *cancelled* dan *returned*.

## Daftar Isi

1. [Overview](#1-overview)
2. [Business Objective](#2-business-objective)
3. [Definisi Metrik](#3-definisi-metrik)
4. [Ringkasan Eksekutif](#4-ringkasan-eksekutif)
5. [Repeat Purchase Rate per Tahun](#5-repeat-purchase-rate-per-tahun)
6. [Cohort Retention Analysis](#6-cohort-retention-analysis)
7. [Top Kota / Provinsi dengan Repeat Buyer Tertinggi](#7-top-kota--provinsi-dengan-repeat-buyer-tertinggi)
8. [Kategori Produk yang Paling Sering Dibeli Ulang](#8-kategori-produk-yang-paling-sering-dibeli-ulang)
9. [Temuan Kritis & Rekomendasi Strategis](#9-temuan-kritis--rekomendasi-strategis)
10. [Pertanyaan Bisnis Lanjutan](#10-pertanyaan-bisnis-lanjutan)
11. [Catatan Metodologi](#11-catatan-metodologi)

## 1. Overview

Customer Loyalty & Retention Dashboard adalah dashboard tambahan dari Executive Sales Dashboard GAYANARA yang berfokus pada analisis perilaku pembelian berulang pelanggan. Dashboard ini menjawab pertanyaan yang tidak dapat dijawab oleh Executive Dashboard — seberapa loyal pelanggan GAYANARA dan bagaimana pola retention mereka dari waktu ke waktu.

Dashboard menyediakan filter: **Year** (2022, 2023, 2024, All).

## 2. Business Objective

Dashboard ini dibuat untuk menjawab:

- Berapa persen pelanggan yang melakukan pembelian lebih dari sekali dalam satu tahun?
- Bagaimana tren repeat purchase rate berubah dari 2022 ke 2024?
- Rata-rata berapa kali repeat buyer melakukan order dalam satu tahun?
- Seberapa cepat pelanggan melakukan pembelian kedua setelah pembelian pertama?
- Cohort pelanggan mana yang memiliki retention rate terbaik?
- Wilayah mana yang memiliki repeat buyer rate tertinggi?
- Produk apa yang paling sering memicu pembelian berulang?

## 3. Definisi Metrik

### Repeat Purchase Rate

Persentase customer yang melakukan order lebih dari 1 kali dalam tahun yang dipilih (intra-year repeat). Customer yang order 2 kali atau lebih dalam tahun yang sama dihitung sebagai repeat buyer.

```
Repeat Purchase Rate = Repeat Buyers / Total Customers
```

### Repeat Buyers

Jumlah customer unik yang melakukan order lebih dari 1 kali dalam tahun yang dipilih, exclude cancelled dan returned.

### One-time Buyers

Jumlah customer unik yang hanya melakukan 1 kali order dalam tahun yang dipilih.

### Avg Orders per Repeat Customer

Rata-rata jumlah order yang dilakukan oleh repeat buyer dalam tahun yang dipilih.

```
Avg Orders per Repeat Customer = Total Orders by Repeat Buyers / Repeat Buyers
```

### Avg Gap Days

Rata-rata jarak hari antara dua pembelian berturut-turut dari customer yang sama. Dihitung dari selisih tanggal order saat ini dengan tanggal order sebelumnya per customer, kemudian dirata-rata. Order pertama setiap customer tidak dihitung karena tidak memiliki pembelian sebelumnya.

### Cohort Retention Rate

Persentase customer dari cohort quarter tertentu yang masih aktif melakukan order pada bulan ke-N setelah pembelian pertama mereka.

```
Retention Rate (Bulan N) = Customer Cohort yang Order di Bulan N / Total Customer Cohort
```

Cohort dikelompokkan berdasarkan quarter pertama kali customer melakukan pembelian (Q1, Q2, Q3, Q4 per tahun).

### Catatan Definisi "All Years"

Saat slicer dipilih "All", repeat buyer didefinisikan sebagai customer yang total ordernya lebih dari 1 di seluruh periode 2022-2024 — bukan dalam satu tahun. Karena itu angka All Years tidak dapat dibandingkan langsung dengan angka per tahun.

## 4. Ringkasan Eksekutif

| Metrik | 2022 | 2023 | 2024 | All Years |
|---|---|---|---|---|
| **Repeat Purchase Rate** | 22.1% | 47.4% | 48.9% | 82.6% |
| **Repeat Buyers** | 68 | 250 | 283 | 625 |
| **One-time Buyers** | 307 | 526 | 578 | 756 |
| **Avg Orders per Repeat Customer** | 2 | 2 | 3 | 3 |
| **Avg Gap Days** | 121.35 | 178.94 | 225.21 | 203.14 |

### Headline Insight

- Repeat Purchase Rate naik drastis dari **22.1% di 2022 ke 47.4% di 2023**, lalu sedikit meningkat ke **48.9% di 2024**. Kualitas loyalitas pelanggan membaik signifikan di 2023 dan bertahan di 2024.
- **Avg Orders per Repeat Customer naik dari 2 ke 3** antara 2023 dan 2024 — repeat buyer di 2024 lebih aktif bertransaksi dibanding tahun sebelumnya.
- **Avg Gap Days terus meningkat** dari 121 hari (2022) ke 178 hari (2023) ke 225 hari (2024). Pelanggan membutuhkan waktu semakin lama untuk kembali membeli — ini sinyal yang perlu diwaspadai.
- Di 2024, **repeat buyer (283) hampir menyamai one-time buyer (296)** — kondisi yang sangat positif untuk bisnis fashion.

## 5. Repeat Purchase Rate per Tahun

### Data

| Tahun | Total Customers | Repeat Buyers | One-time Buyers | Repeat Rate |
|---|---|---|---|---|
| 2022 | 308 | 68 | 307 | 22.1% |
| 2023 | 527 | 250 | 526 | 47.4% |
| 2024 | 579 | 283 | 578 | 48.9% |

### Kondisi Bisnis

Repeat Purchase Rate meningkat sangat tajam dari 2022 ke 2023 (+25.3 poin persentase), kemudian stabil di kisaran 48-49% di 2023 dan 2024. Di 2022, mayoritas customer hanya membeli sekali (307 dari 375 customer). Di 2024, hampir separuh customer sudah menjadi repeat buyer.

### Implikasi

Lonjakan repeat rate di 2023 bersamaan dengan lonjakan revenue +115% menunjukkan bahwa ekspansi 2023 tidak hanya mendatangkan customer baru tetapi juga berhasil mempertahankan sebagian besar dari mereka untuk kembali membeli di tahun yang sama.

Plateau di 48-49% antara 2023 dan 2024 menunjukkan bisnis sudah menemukan natural rate loyalitasnya. Untuk naik ke level berikutnya di atas 55%, diperlukan intervensi aktif berupa program loyalty, personalized campaign, atau subscription model.

### Rekomendasi

- Investigasi apa yang berubah di 2023 yang mendorong repeat rate naik drastis — apakah ada program promosi, perubahan produk, atau perubahan channel yang menjadi faktor utama.
- Rancang program loyalty formal (poin reward, tier membership) untuk mendorong repeat rate melampaui 50% di 2025.
- Fokus pada one-time buyers 2024 (578 customer) sebagai target konversi ke repeat buyer di 2025.

## 6. Cohort Retention Analysis

### Cara Membaca Cohort Table

- **Baris** = cohort pelanggan berdasarkan quarter pertama kali mereka membeli
- **Kolom** = bulan ke-N setelah pembelian pertama
- **Nilai** = persentase customer dari cohort tersebut yang masih aktif di bulan ke-N
- Kolom 0 selalu 100% karena semua customer pasti aktif di bulan pertama
- Tanda kosong berarti cohort belum cukup umur untuk mencapai bulan tersebut

### Data Cohort Lengkap (All Years)

| Cohort | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Q1 2022 | 100% | 3.37% | 3.37% | 3.37% | 2.25% | 4.49% | 8.99% | 5.62% | 2.25% | 5.62% | 2.25% | 14.61% | 12.36% |
| Q2 2022 | 100% | 3.80% | 3.80% | 1.27% | 2.53% | 1.27% | 2.53% | 6.33% | 2.53% | 6.33% | 11.39% | 11.39% | 10.13% |
| Q3 2022 | 100% | 2.94% | 4.41% | 4.41% | 5.88% | 1.47% | 8.82% | 13.24% | 7.35% | 13.24% | 4.41% | 8.82% | 13.24% |
| Q4 2022 | 100% | 1.39% | 8.33% | 5.56% | 6.94% | 2.78% | 8.33% | 6.94% | 4.17% | 9.72% | 4.17% | 12.50% | 9.72% |
| Q1 2023 | 100% | 10.19% | 6.48% | 12.96% | 10.19% | 11.11% | 12.04% | 7.41% | 8.33% | 7.41% | 5.56% | 13.89% | 12.04% |
| Q2 2023 | 100% | 6.86% | 7.84% | 10.78% | 5.88% | 12.75% | 10.78% | 6.86% | 10.78% | 10.78% | 9.80% | 13.73% | 6.86% |
| Q3 2023 | 100% | 6.25% | 9.38% | 7.81% | 6.25% | 12.50% | 9.38% | 7.81% | 3.13% | 4.69% | 10.94% | 9.38% | 7.81% |
| Q4 2023 | 100% | 12.24% | 8.16% | 12.24% | 6.12% | 8.16% | 6.12% | 10.20% | 8.16% | 8.16% | 8.16% | 10.20% | 10.20% |
| Q1 2024 | 100% | 22.92% | 6.25% | 18.75% | 10.42% | 10.42% | 14.58% | 12.50% | 10.42% | 14.58% | 2.08% | | |
| Q2 2024 | 100% | 12.50% | 10.00% | 5.00% | 10.00% | 7.50% | 12.50% | 10.00% | 2.50% | | | | |
| Q3 2024 | 100% | 12.50% | 12.50% | 12.50% | 12.50% | 6.25% | | | | | | | |
| Q4 2024 | 100% | 4.55% | 4.55% | | | | | | | | | | |

### Kondisi Bisnis

Retention rate 2022 sangat rendah di bulan-bulan awal (1-4%) — wajar untuk tahun pertama bisnis di mana basis pelanggan masih kecil dan belum ada sistem loyalty.

Cohort 2023 menunjukkan retention yang jauh lebih baik (6-13% per bulan) — konsisten dengan lonjakan repeat rate di 2023.

Cohort Q1 2024 memiliki bulan 1 tertinggi (22.92%) — indikasi bahwa pelanggan yang pertama kali beli di awal 2024 langsung aktif kembali di bulan berikutnya. Ini adalah cohort terkuat sepanjang periode.

### Implikasi

Angka retention bulanan yang relatif kecil (3-13%) normal untuk bisnis fashion — pelanggan tidak membeli pakaian setiap bulan. Yang lebih penting adalah konsistensi angka dari bulan ke bulan.

Pola retention 2022 tidak konsisten (naik turun tidak beraturan) berbeda dengan 2023 yang lebih stabil — ini menandakan bisnis semakin mature dalam mempertahankan pelanggan.

### Rekomendasi

- Gunakan cohort Q1 2024 sebagai benchmark untuk memahami karakteristik pelanggan paling loyal — dari mana mereka datang, produk apa yang dibeli pertama kali, channel apa yang digunakan.
- Rancang triggered email atau notifikasi untuk re-engage pelanggan yang tidak aktif setelah bulan ke-2 atau ke-3.
- Analisis lebih lanjut apakah cohort dengan retention tinggi berasal dari channel, produk, atau promosi yang spesifik.

## 7. Top Kota / Provinsi dengan Repeat Buyer Tertinggi

### Data per Tahun

**2022**

| Provinsi | Repeat Buyer Rate |
|---|---|
| Jawa Timur | 26.32% |
| Jawa Tengah | 23.81% |
| Kalimantan Selatan | 21.43% |
| Sulawesi Selatan | 20.00% |
| Kalimantan Barat | 18.75% |
| Banten | 18.18% |
| Jawa Barat | 17.24% |
| Riau | 15.38% |
| Kalimantan Timur | 13.64% |
| DI Yogyakarta | 11.76% |
| Sumatera Utara | 11.76% |

**2023**

| Provinsi | Repeat Buyer Rate |
|---|---|
| Sumatera Barat | 40.00% |
| Jawa Timur | 38.89% |
| DKI Jakarta | 37.14% |
| Sulawesi Selatan | 35.29% |
| Kalimantan Selatan | 33.33% |
| Banten | 32.26% |
| Sumatera Utara | 31.82% |
| Sumatera Selatan | 29.17% |
| Riau | 29.03% |
| Jawa Barat | 28.89% |
| Sulawesi Utara | 28.57% |

**2024**

| Provinsi | Repeat Buyer Rate |
|---|---|
| DKI Jakarta | 42.31% |
| Jawa Tengah | 40.54% |
| Sulawesi Selatan | 38.24% |
| Sumatera Selatan | 37.84% |
| Jawa Timur | 37.31% |
| Kalimantan Barat | 33.33% |
| Sumatera Barat | 33.33% |
| Jawa Barat | 32.61% |
| Sumatera Utara | 32.56% |
| Riau | 32.14% |
| Banten | 27.50% |

**All Years**

| Provinsi | Repeat Buyer Rate |
|---|---|
| Banten | 54.10% |
| DI Yogyakarta | 52.94% |
| Sumatera Barat | 50.00% |
| Jawa Barat | 49.55% |
| Sulawesi Selatan | 47.37% |
| DKI Jakarta | 47.17% |
| Kalimantan Timur | 46.03% |
| Kalimantan Selatan | 44.00% |
| Sumatera Selatan | 43.40% |
| Sulawesi Utara | 42.65% |
| Bali | 40.74% |

### Kondisi Bisnis

**DKI Jakarta menjadi provinsi dengan repeat buyer rate tertinggi di 2024 (42.31%)** — menarik karena di Executive Dashboard, Jakarta masuk Bottom 5 provinsi berdasarkan revenue. Artinya customer Jakarta yang membeli memang lebih loyal, tetapi jumlah customer Jakarta masih sangat sedikit.

**Jawa Timur konsisten masuk Top 3** di 2022 dan 2023, dan Top 5 di 2024 — kombinasi revenue besar dan repeat rate tinggi menjadikan Jawa Timur salah satu market terkuat GAYANARA.

**Repeat rate meningkat di hampir semua provinsi** dari 2022 ke 2024 — konsisten dengan kenaikan overall repeat rate.

### Implikasi

Jakarta adalah anomali yang menarik — pelanggan yang sudah mengenal GAYANARA di Jakarta ternyata sangat loyal, tetapi penetrasi awalnya masih sangat rendah. Masalah Jakarta bukan di kualitas produk atau kepuasan pelanggan, tetapi di awareness dan akuisisi.

### Rekomendasi

- Prioritaskan kampanye akuisisi di Jakarta dengan argumen data: begitu customer Jakarta mengenal GAYANARA, mereka cenderung loyal.
- Pertahankan dan perkuat engagement di Jawa Timur — kombinasi revenue tinggi dan repeat rate tinggi adalah market paling valuable.
- Monitor Riau yang repeat rate-nya terus naik dari 15% ke 32% dalam 3 tahun — potensi emerging market yang perlu diperhatikan.

## 8. Kategori Produk yang Paling Sering Dibeli Ulang

### Top Produk 2022

| Produk | Rate |
|---|---|
| T-Shirt Graphic SandangIndo | 3.90% |
| Dress Mini Casual Riang Apparel | 3.57% |
| Topi Baseball Cendana Co | 3.57% |
| Jacket Denim Ratu Mode | 3.25% |
| Jaket Hoodie Cendana Co | 3.25% |
| Jaket Hoodie Kanvas Lokal | 3.25% |
| Dress Wrap Senja Wear | 2.92% |
| Jacket Denim Tropika Style | 2.92% |
| Shirt Slim Fit Tropika Style | 2.92% |
| Topi Baseball SandangIndo | 2.92% |

### Top Produk 2023

| Produk | Rate |
|---|---|
| Jacket Denim Ratu Mode | 4.93% |
| Jaket Hoodie Kanvas Lokal | 4.55% |
| Kaos Striped Kanvas Lokal | 4.17% |
| T-Shirt Graphic BajuKita | 4.17% |
| Jacket Coach NusaBrand | 3.98% |
| T-Shirt Graphic SandangIndo | 3.61% |
| Celana Kulot Tropika Style | 3.42% |
| Dress Bodycon Senja Wear | 3.42% |
| Topi Baseball Cendana Co | 3.42% |
| Topi Baseball SandangIndo | 3.42% |

### Top Produk 2024

| Produk | Rate |
|---|---|
| Jacket Denim Ratu Mode | 5.35% |
| Kaos Oversize BajuKita | 4.66% |
| Topi Baseball Cendana Co | 4.49% |
| Jaket Hoodie Kanvas Lokal | 4.15% |
| Topi Baseball SandangIndo | 3.97% |
| Celana Jeans Slim SandangIndo | 3.63% |
| Kemeja Flanel Tropika Style | 3.63% |
| Celana Jeans Slim Senja Wear | 3.45% |
| Dress Mini Casual Riang Apparel | 3.45% |
| Kaos Oversize Tropika Style | 3.45% |

### Top Produk All Years

| Produk | Rate |
|---|---|
| Jacket Denim Ratu Mode | 8.59% |
| Jaket Hoodie Kanvas Lokal | 7.53% |
| Topi Baseball Cendana Co | 7.27% |
| Kaos Oversize BajuKita | 6.74% |
| Topi Baseball SandangIndo | 6.34% |
| T-Shirt Graphic SandangIndo | 6.21% |
| Dress Mini Casual Riang Apparel | 5.94% |
| Jacket Coach NusaBrand | 5.68% |
| Kemeja Flanel Tropika Style | 5.42% |
| Dompet Kulit Pesona Indo | 5.28% |

### Kondisi Bisnis

**Jacket Denim Ratu Mode adalah produk yang paling konsisten memicu pembelian berulang** — masuk Top 1 di 2023 dan 2024, Top 4 di 2022, dan Top 1 secara keseluruhan (8.59%). Ini menunjukkan produk ini memiliki loyalitas pelanggan yang sangat kuat.

**Kategori Jacket dan Topi (Accessories)** mendominasi daftar produk yang sering dibeli ulang di semua tahun — konsisten dengan temuan di Executive Dashboard bahwa Accessories dan Jacket adalah core category.

**Kaos Oversize BajuKita** muncul sebagai produk baru dengan repeat rate tinggi di 2024 (4.66%) — kandidat top performer yang perlu diperhatikan.

**T-Shirt Graphic SandangIndo** adalah satu-satunya produk yang masuk Top 10 di 2022 dan All Years tetapi tidak masuk Top 10 di 2023 dan 2024 — indikasi produk ini mulai kehilangan daya tariknya.

### Implikasi

Produk-produk di daftar ini bukan hanya top revenue product, tetapi top loyalty product. Sebuah produk bisa memiliki revenue tinggi karena harganya mahal, tapi belum tentu memicu pelanggan untuk kembali membeli. Dua metrik ini perlu dibaca bersama.

### Rekomendasi

- Jadikan Jacket Denim Ratu Mode sebagai produk anchor dalam kampanye retention — misalnya sebagai rekomendasi produk di email follow-up pasca pembelian.
- Cross-sell antara Jacket dengan Topi — keduanya sering dibeli berulang dan kemungkinan besar oleh segmen customer yang sama.
- Monitor T-Shirt Graphic SandangIndo yang mulai turun dari daftar top repeat product — evaluasi apakah perlu revitalisasi produk ini.
- Eksplorasi mengapa Jacket Denim Ratu Mode memiliki repeat rate tertinggi — kualitas, harga, atau variasi desain? Pemahaman ini bisa diterapkan ke produk lain.

## 9. Temuan Kritis & Rekomendasi Strategis

### Temuan #1: Avg Gap Days Terus Meningkat

**Fakta:** Avg Gap Days naik dari 121 hari (2022) ke 178 hari (2023) ke 225 hari (2024).

**Implikasi:** Pelanggan membutuhkan waktu semakin lama untuk kembali membeli. Meski repeat rate stabil di 48-49%, frekuensi pembelian per customer melambat. Ini bisa berarti customer puas tetapi tidak ada trigger yang mendorong mereka kembali lebih cepat.

**Rekomendasi:**
- Implementasi email atau notifikasi yang dipersonalisasi 60-90 hari setelah pembelian terakhir untuk mendorong pembelian berikutnya lebih cepat.
- Buat event atau peluncuran produk baru secara berkala sebagai trigger pembelian.
- Analisis apakah ada hubungan antara jenis produk yang dibeli dengan Avg Gap Days — pelanggan yang beli accessories mungkin kembali lebih cepat dari pelanggan yang beli jacket.

### Temuan #2: Jakarta Anomali — Loyal tapi Sedikit

**Fakta:** DKI Jakarta repeat rate tertinggi di 2024 (42.31%) tapi masuk Bottom 5 provinsi di revenue pada Executive Dashboard.

**Implikasi:** Masalah Jakarta bukan di kualitas layanan atau kepuasan pelanggan, tetapi di awareness dan akuisisi. Customer yang sudah mengenal GAYANARA di Jakarta ternyata sangat loyal.

**Rekomendasi:**
- Gunakan data ini sebagai argumen untuk investasi marketing di Jakarta — ROI dari akuisisi customer Jakarta berpotensi tinggi karena retention rate-nya sudah terbukti baik.
- Pertimbangkan Jakarta sebagai priority market untuk campaign berbayar di 2025.

### Temuan #3: One-time Buyers Masih Mendominasi

**Fakta:** 2022: 307 one-time buyers vs 68 repeat buyers. 2023: 526 vs 250. 2024: 578 vs 283.

**Implikasi:** Ada pool besar customer yang berpotensi dikonversi menjadi repeat buyer tetapi belum pernah kembali membeli. One-time buyers dari 2022 dan 2023 yang tidak aktif adalah target win-back yang paling realistis.

**Rekomendasi:**
- Identifikasi one-time buyers 2022 dan 2023 yang belum pernah order lagi — rancang win-back campaign dengan insentif seperti diskon, free ongkir, atau hadiah untuk mendorong pembelian kedua.
- Analisis karakteristik one-time buyers vs repeat buyers untuk menemukan pola yang membedakan keduanya sejak pembelian pertama.

### Peluang #1: Q1 2024 Cohort Paling Promising

**Fakta:** Q1 2024 memiliki bulan 1 retention tertinggi (22.92%) dibanding cohort manapun sepanjang 2022-2024.

**Rekomendasi:** Analisis karakteristik customer Q1 2024 — dari mana mereka datang, produk apa yang dibeli pertama kali, dan channel apa yang digunakan. Replikasi kondisi ini untuk cohort berikutnya.

### Peluang #2: Jacket Denim Ratu Mode sebagai Produk Anchor Loyalty

**Fakta:** Produk ini konsisten menjadi top repeat product selama 3 tahun berturut-turut dengan rate tertinggi 8.59% secara keseluruhan.

**Rekomendasi:** Jadikan produk ini sebagai centerpiece kampanye loyalty — rekomendasi produk, bundle deals, atau first-purchase incentive untuk mendorong customer mencoba produk ini di pembelian pertama.

## 10. Pertanyaan Bisnis Lanjutan

| # | Pertanyaan | Prioritas |
|---|---|---|
| 1 | Dari channel mana one-time buyers 2022 dan 2023 berasal? | Kritis |
| 2 | Apakah ada korelasi antara produk pertama yang dibeli dengan kemungkinan repeat purchase? | Kritis |
| 3 | Mengapa Q1 2024 memiliki bulan 1 retention jauh lebih tinggi dari cohort lain? | Kritis |
| 4 | Apakah pelanggan yang membeli via promo (RAMADAN, HARBOLNAS) memiliki repeat rate berbeda? | Penting |
| 5 | Berapa customer lifetime value rata-rata per repeat buyer? | Penting |
| 6 | Apakah ada perbedaan repeat rate berdasarkan gender atau age group? | Penting |
| 7 | Produk apa yang paling sering menjadi pembelian kedua setelah pembelian pertama? | Penting |
| 8 | Apakah Avg Gap Days berbeda signifikan antar provinsi? | Strategis |
| 9 | Apakah kurir yang digunakan berpengaruh terhadap kemungkinan repeat purchase? | Strategis |
| 10 | Berapa batas minimum repeat purchase untuk seorang customer dianggap highly loyal? | Strategis |

## 11. Catatan Metodologi

- Data yang digunakan adalah valid orders, tidak termasuk cancelled dan returned.
- **Repeat buyer** didefinisikan sebagai customer yang melakukan order lebih dari 1 kali dalam tahun kalender yang dipilih (intra-year repeat).
- **Cohort** dikelompokkan berdasarkan quarter pertama kali customer melakukan pembelian valid.
- **Avg Gap Days** dihitung dari selisih tanggal order saat ini dengan tanggal order valid sebelumnya dari customer yang sama. Order pertama setiap customer tidak dihitung karena tidak memiliki pembelian sebelumnya.
- **Repeat Buyer Rate by Province** dihitung dari: repeat buyers di provinsi tersebut dibagi total customers di provinsi tersebut pada tahun yang dipilih.
- **Repeat Buyer Rate by Product** dihitung dari: repeat buyers yang pernah membeli produk tersebut dibagi total customers keseluruhan pada tahun yang dipilih.
- Data 2025 dikecualikan dari seluruh analisis.
- Angka "All Years" menggunakan definisi cross-period (pernah order lebih dari sekali di seluruh periode 2022-2024) dan tidak dapat dibandingkan langsung dengan angka per tahun.
- Cohort bulan yang kosong menandakan cohort belum cukup umur untuk mencapai bulan tersebut, bukan berarti tidak ada aktivitas.

*Dokumen ini dibuat berdasarkan data yang ditampilkan pada Customer Loyalty & Retention Dashboard GAYANARA, periode 2022-2024.*
*Untuk pertanyaan analitik lebih lanjut atau permintaan drill-down data, hubungi tim Data & Analytics.*

**Dibuat oleh:** Data & Analytics Team
**Last Updated:** 2024
