# Tentang Dataset
Dataset berisi 1.000 baris data billing bulanan pelanggan dairy, mencakup informasi pelanggan, kurir pengantar, jumlah pengiriman susu, tagihan, dan status pembayaran. Dataset ini mengandung missing value, data duplikat, serta inkonsistensi 
kapitalisasi pada beberapa kolom kategori.

# Tools
- SQLite (via Python `sqlite3`)
- Google Colab
- Pandas (untuk menampilkan hasil query)

# Isi Analisis
| No | Query | Fokus Analisis |
|----|-------|-----------------|
| 1 | WHERE + IS NULL | Mendeteksi baris dengan data kosong/hilang |
| 2 | GROUP BY + HAVING COUNT | Mendeteksi baris data duplikat |
| 3 | UPPER + TRIM + DISTINCT | Merapikan kategori pembayaran yang tidak konsisten |
| 4 | GROUP BY + SUM (data bersih) | Ringkasan total pembayaran per metode setelah dibersihkan |

# Masalah Data yang Ditemukan
- Missing value di beberapa kolom (status pelanggan, tanggal tagihan, metode pembayaran, dll)
- 20 baris data duplikat
- Kategori pembayaran tidak konsisten (contoh: "UPI", "upi", "Upi" dianggap berbeda)
