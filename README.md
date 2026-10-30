# Kota Kita — Bisnis Properti

Game board bisnis properti original, dibuat sebagai situs statis untuk HP dan PC.

## Live site

https://syahpurbachtiar-oss.github.io/monopoli/

## Fitur

- 2–4 pemain lokal dalam satu perangkat.
- Pemain manusia dan AI komputer.
- Online room untuk sampai 4 pemain menggunakan kode room enam karakter.
- Papan 40 petak, dadu, pembelian properti, sewa, lelang, rumah/hotel, gadai, kartu, penjara, dan kebangkrutan.
- Progres permainan lokal tersimpan di browser.
- Desain responsif untuk desktop dan smartphone.

## Online room

Konfigurasi Firestore sudah tertanam di `index.html`, menggunakan proyek Firebase yang sama dengan game HAY Gaple. Pemain tidak perlu membuat proyek Firebase, memasukkan API key, atau login.

1. Host klik **Buat Room** dan membagikan kode enam karakter.
2. Teman memasukkan kode dan klik **Gabung**.
3. Host klik **Mulai Permainan** setelah minimal dua pemain bergabung.

Room Monopoli memakai dokumen dengan prefix `MONO_` di koleksi Firestore `rooms`, sehingga terpisah dari room Gaple.

## Publikasi GitHub Pages

Workflow otomatis tersedia di `.github/workflows/pages.yml`. Untuk aktivasi pertama:
1. Buka **Settings → Pages** pada repository ini.
2. Pada **Build and deployment → Source**, pilih **GitHub Actions**.
3. Setelah disimpan, buka tab **Actions** dan lihat workflow **Deploy Kota Kita to GitHub Pages**.
4. Deployment berikutnya berjalan otomatis setiap ada push ke `main`.

## Catatan

Permainan online memakai Firestore client-side dan aturan keamanan Firestore dari proyek Firebase yang digunakan HAY Gaple. Cocok untuk permainan santai bersama teman, bukan untuk kompetisi berhadiah atau transaksi uang asli.
