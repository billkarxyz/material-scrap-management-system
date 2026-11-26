# E-SCRAP — Material Scrap Management System

Sistem manajemen scrap material berbasis web statis (tanpa backend, tanpa build step, tanpa dependensi eksternal). Dibuat untuk mencatat dan memantau scrap dari proses produksi per kategori: Assembly, Machining, Casting, dan Others.

## Cara Membuka

**Paling mudah:** buka file `index.html` langsung di browser (klik dua kali).

**GitHub Pages (opsional):**
1. Buka Settings repo → Pages.
2. Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. Simpan — situs akan tersedia di `https://billkarxyz.github.io/material-scrap-management-system/`.

## Fitur

- **Dashboard** — 4 kartu kategori (Assembly, Machining, Casting, Others) dengan Qty dan Amount (Rp), ringkasan Total / Terjual / Pending, grafik batang Qty per bulan (Jan–Mei, ditumpuk per kategori) dan grafik donat Cost per kategori. Grafik digambar dengan SVG murni, tanpa library eksternal.
- **Data Scrap** — tabel semua catatan scrap dengan pencarian (material / kode / pembeli) dan filter kategori, status, dan bulan.
- **Input / Edit / Hapus Scrap** — form tanggal, material, kode, kategori, qty, satuan, harga, pembeli, dan status; total (qty × harga) dihitung otomatis dan ditampilkan saat mengisi form. Kode duplikat ditolak.
- **Export CSV** — unduh seluruh data scrap sebagai CSV (kompatibel dengan Excel).
- **Penyimpanan lokal** — semua data tersimpan di `localStorage` browser, jadi tetap ada setelah halaman ditutup dan dibuka lagi.
- **Muat Data Contoh** — memuat 20 catatan contoh (Jan–Mei 2026) supaya dashboard langsung terisi.
- **Hapus Semua Data** — mengosongkan seluruh catatan.

## Data Contoh

20 catatan (Jan–Mei 2026) dengan total per kategori:

| Kategori | Qty | Amount |
|---|---|---|
| Assembly | 1.028 pcs | Rp34.016.120 |
| Machining | 12.420 pcs | Rp772.687.167 |
| Casting | 9.245 pcs | Rp1.382.326.837 |
| Others | 7.744 pcs | Rp99.002.097 |
| **Total** | **30.437 pcs** | **Rp2.288.032.221** |

Catatan: angka total dihitung dari penjumlahan keempat kategori di atas. (Pada gambar referensi E-SCRAP, angka total yang tertera adalah Rp2.177.796.221 — angka tersebut tidak sama dengan jumlah keempat kategori, jadi dashboard di aplikasi ini menampilkan jumlah sebenarnya yang dihitung dari data.)

## Teknologi

HTML + CSS + JavaScript murni dalam satu file `index.html`. Tidak ada framework, tidak ada CDN, tidak ada server — cukup dibuka di browser modern apa pun.
