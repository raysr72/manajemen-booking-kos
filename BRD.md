# Business Requirement Document (BRD)

## Sistem Manajemen & Reservasi Kos Titik Kumpul

---

## Business Background

Sistem Manajemen & Reservasi Kos Titik Kumpul dikembangkan untuk merespon kebutuhan digitalisasi di industri manajemen properti sewa (kamar kos). Latar belakang pengembangan ini didasarkan pada tingginya mobilitas calon penyewa dari luar daerah yang membutuhkan kemudahan akses informasi spesifikasi kamar dan visualisasi detail tanpa harus melakukan kunjungan fisik langsung ke lokasi kos, serta pentingnya sentralisasi data operasional dan finansial yang profesional.

## Problem Statement

- **Inefisiensi Waktu dan Lokasi:** Proses survei kunjungan kos secara konvensional memakan waktu dan biaya perjalanan yang tinggi bagi calon penyewa yang mayoritas berasal dari luar daerah.
- **Keterbatasan Metode Transaksi:** Sistem pembayaran biaya reservasi dan sewa yang masih terpusat secara tunai atau manual di lokasi kos menimbulkan gesekan operasional serta menyulitkan penyewa.
- **Celah Manajemen Pemeliharaan:** Perawatan fasilitas lingkungan kos yang bersifat rutin belum memiliki mekanisme penjadwalan dan pengingat otomatis, sehingga berisiko menurunkan standar kenyamanan penghuni.
- **Risiko Rekapitulasi Finansial:** Pembukuan pendapatan yang dilakukan secara manual menggunakan pencatatan buku fisik rentan terhadap human error, selisih kas, hingga ketidakakuratan margin bulanan.
- **Keterbatasan Kepatuhan Administratif:** Pendataan identitas penghuni untuk pelaporan berkala kepada pengurus RT/RW setempat masih dikelola secara terpisah.

## Project Objectives
- Mengembangkan platform aplikasi terpusat yang memudahkan calon penyewa dalam mengakses informasi detail aset dan melakukan pemesanan secara online secara efisien.
- Menghilangkan risiko selisih dan kesalahan pencatatan pembukuan melalui digitalisasi laporan keuangan dan transaksi.
- Meminimalisir risiko keterlambatan pemeliharaan lingkungan kos melalui sistem penjadwalan dan notifikasi terpadu.
- Menjamin kelangsungan pemeliharan lingkungan kos secara berkala melalui sistem kontrol operasional yang terstruktur serta basis data arsip identitas penyewa yang rapi.

## Project Scope

### In-Scope
- **Manajemen Pengguna:** Kontrol hak akses multi-lecel (Admin dan Customer/Penyewa).
- **Manajemen Master Aset:** Pengelolaan kategori kamar, spesifikasi detail ruangan, pembaruan status ketersediaan kamar(*ready/not ready*), dan arsip data identitas penyewa.
- **Siklus Transaksi & Keuangan:** Pengelolaan data pemesanan (*booking*), rekam bukti pembayaran, validasi administratif oleh admin, serta rekonsiliasi laporan keuangan.
- **Manajemen Operasional:** Penjadwalan pemeliharaan rutin fasilitas kos.
- **Automasi Notifikasi:** Integrasi WhatsApp Bot untuk pengiriman invoice dan status konfirmasi transaksi secara instan ke nomor telepon pengguna.

### Out-of-Scope

- integrasi langsung dengan payment gateway pihak ketiga (menggunakan verifikasi manual bukti transfer via admin).
- Sistem manajemen aset properti multi-lokasi di luar area kos titik kumpul.
- Pengelolaan inventasi aset bergerak di dalam kamar secara mendetail (seperti nomor seri elektronik perabot) dan penjadwalan renovasi berskala besar.
- Fitur multi-mata uang, kalkulasi pajak otomatis, dan integrasi akuntansi tingkat lanjut.

## Business Process Flow

- **Proses Saat Ini (As-Is):** Calon penyewa mendatangi lokasi fisik untuk melihat kamar dan melakukan transaksi pembayaran secara manual di tempat. Pemilik atau pengelola mengecek ketersediaan kamar secara manual lewat catatan buku, menjadwalkan tukang servis pemeliharaan secara insidental berdasarkan keluhan, serta mencatat seluruh transaksi keuangan harian ke dalam buku kas fisik secara konvensional.

- **Proses Usulan (To-Be):** Seluruh tahapan pencarian informasi, reservasi kamar, dan pengunggahan bukti bayar diproses secara terpusat melalui aplikasi tanpa mengharuskan kunjungan fisik ke lokasi. Status ketersediaan kamar dikelola secara digital (*CRUD* oleh Admin) dan terupdate otomatis setelah reservasi di validasi. Jadwal perawatan rutin terkelola dalam sistem terpadu, dan sistem secara otomatis memicu WhatsApp Bot untuk mengirimkan invoice digital ke nomor pengguna setelah pembayaran divalidasi oleh admin.