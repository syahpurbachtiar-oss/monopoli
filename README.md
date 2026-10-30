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

Game memakai konfigurasi Firestore yang sudah tertanam di `index.html`, dengan proyek Firebase yang sama dengan game HAY Gaple. Pemain tidak perlu membuat proyek Firebase atau memasukkan konfigurasi.

1. Host memilih nama lalu klik **Buat Room**.
2. Bagikan kode room enam karakter.
3. Teman memasukkan kode tersebut dan klik **Gabung**.
4. Host memulai permainan setelah setidaknya dua pemain bergabung.

Data Monopoli disimpan dalam dokumen Firestore dengan prefix `MONO_` pada koleksi `rooms`, agar terpisah dari room Gaple.

## GitHub Pages

Repository ini harus dipublikasikan melalui GitHub Pages dengan:
- Branch: `main`
- Folder: `/(root)`

Di GitHub buka **Settings → Pages → Build and deployment → Deploy from a branch**, pilih `main` dan `/(root)`, lalu Save.

## Catatan

Permainan online memakai Firestore client-side dan aturan keamanan Firestore dari proyek Firebase yang sudah digunakan HAY Gaple. Cocok untuk permainan santai bersama teman; bukan untuk kompetisi berhadiah atau transaksi uang asli.
