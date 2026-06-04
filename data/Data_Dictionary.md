# Data Dictionary (Kamus Data)

Dokumen ini berisi informasi mengenai struktur, tipe data, dan deskripsi fungsional dari setiap kolom yang terdapat dalam dataset analisis *time series* / pergerakan harga aset keuangan ini.

## Ringkasan Dataset (Dataset Summary)

* **Total Baris (Rows):** 2.483 baris
* **Total Kolom (Columns):** 14 kolom
* **Kondisi Data:** 100% Bersih (Tidak ditemukan *missing values* atau data kosong pada semua kolom).

---

## Tabel Kamus Data (Data Dictionary Table)

| # | Nama Kolom (Column Name) | Jumlah Non-Null | Tipe Data (Dtype) | Deskripsi / Penjelasan Fungsi |
|---|-------------------------|-----------------|-------------------|--------------------------------|
| 0 | `Close`                 | 2483            | `float64`         | Harga penutupan (*closing price*) dari aset pada tanggal terkait. |
| 1 | `Low`                   | 2483            | `float64`         | Harga terendah (*lowest price*) yang dicapai aset selama sesi perdagangan harian. |
| 2 | `High`                  | 2483            | `float64`         | Harga tertinggi (*highest price*) yang dicapai aset selama sesi perdagangan harian. |
| 3 | `Open`                  | 2483            | `float64`         | Harga pembukaan (*opening price*) aset saat sesi perdagangan dimulai. |
| 4 | `Lag_1`                 | 2483            | `float64`         | Nilai harga (umumnya dari kolom `Close`) pada 1 hari/periode sebelumnya ($t-1$). |
| 5 | `EMA_7`                 | 2483            | `float64`         | *Exponential Moving Average* periode 7 hari; digunakan sebagai indikator tren jangka pendek. |
| 6 | `EMA_30`                | 2483            | `float64`         | *Exponential Moving Average* periode 30 hari; digunakan sebagai indikator tren jangka menengah. |
| 7 | `Lag_7`                 | 2483            | `float64`         | Nilai harga (umumnya dari kolom `Close`) pada 7 hari/periode sebelumnya ($t-7$). |
| 8 | `Lag_30`                | 2483            | `float64`         | Nilai harga (umumnya dari kolom `Close`) pada 30 hari/periode sebelumnya ($t-30$). |
| 9 | `Volatility_30`         | 2483            | `float64`         | Tingkat fluktuasi atau standar deviasi pergerakan harga dalam rentang waktu 30 hari terakhir. |
| 10| `Date`                  | 2483            | `datetime64[ns]`  | Tanggal pencatatan data transaksi (format indeks waktu). |
| 11| `Volatility_7`          | 2483            | `float64`         | Tingkat fluktuasi atau standar deviasi pergerakan harga dalam rentang waktu 7 hari terakhir. |
| 12| `HL_Spread`             | 2483            | `float64`         | Selisih rentang harga harian yang dihitung dari rumus: `High` - `Low`. |
| 13| `Momentum_30`           | 2483            | `float64`         | Indikator kecepatan atau kekuatan perubahan tren harga dalam rentang waktu 30 hari terakhir. |
