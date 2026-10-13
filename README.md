# SIPOMAS

**Sistem Informasi Pendataan dan Informasi Organisasi Kemasyarakatan**  
Prototype digital untuk membantu menggambarkan pendataan, pembinaan, monitoring, dan pengawasan organisasi kemasyarakatan (ORMAS) di Kabupaten Bengkulu Selatan.

## Tentang aplikasi

SIPOMAS adalah prototype satu halaman yang dibuat dengan HTML, CSS, dan JavaScript. Tidak diperlukan proses build atau instalasi paket. Aplikasi dapat dibuka langsung dari `index.html` atau dipublikasikan sebagai situs statis, misalnya menggunakan GitHub Pages.

## Fitur

- **Dashboard** — jam dan tanggal WIB, ringkasan ORMAS dan anggota, informasi kegiatan, grafik status ORMAS, serta grafik jumlah anggota per ORMAS.
- **Profil SIPOMAS** — ruang lingkup, tujuan, alur informasi, dan manfaat yang diharapkan.
- **Data ORMAS** — pencarian serta tambah, edit, dan hapus data organisasi; tabel ringkas diselaraskan dengan data ORMAS terperinci.
- **Data anggota** — tambah, edit, dan hapus informasi anggota.
- **Jumlah anggota ORMAS** — melihat dan memperbarui jumlah anggota tiap organisasi.
- **Data ORMAS terperinci** — mengelola informasi kelembagaan, kepengurusan, alamat, bidang, kegiatan, dan jumlah anggota.
- **Monitoring & Pengawasan** — tambah, edit, dan hapus agenda, wilayah, tanggal, serta status tindak lanjut.
- **Pembinaan** — tambah, edit, dan hapus program, target, serta status pelaksanaan.
- **Dokumentasi** — mengelola dokumentasi kegiatan dan foto.
- **Laporan** — mengunduh workbook Excel, mencetak/menyimpan laporan sebagai PDF, atau mengunduh cadangan JSON lengkap dari data browser.

## Menjalankan dan memublikasikan

1. Simpan seluruh file proyek dalam susunan folder yang sama.
2. Buka `index.html` di browser, atau jalankan melalui ekstensi seperti **Live Server** di Visual Studio Code.
3. Untuk dipublikasikan di GitHub Pages, unggah file proyek ke repository GitHub, lalu aktifkan Pages pada pengaturan repository dan pilih branch serta folder publikasi yang sesuai.

Chart.js, SheetJS, Supabase JS, font, dan beberapa gambar/latar dimuat dari layanan eksternal. Koneksi internet diperlukan untuk memuat aset tersebut, grafik, ekspor Excel, dan sinkronisasi cloud. Logo kabupaten dan gambar pada folder proyek dimuat dari file lokal.

## File utama dan aset

| File | Keterangan |
| --- | --- |
| `index.html` | Halaman dan kode utama SIPOMAS. |
| `README.md` | Dokumentasi proyek. |
| `Kabupaten-Bengkulu-Selatan-Logo-removebg-preview.png` | Lambang Kabupaten Bengkulu Selatan di sidebar. |
| `bupati_bs-removebg-preview.png` | Foto Bupati dan Wakil Bupati pada banner dashboard. |

## Penyimpanan dan laporan

Aplikasi menyimpan data lokal di `localStorage` browser dan memiliki integrasi Supabase untuk sinkronisasi antarperangkat. Sinkronisasi bergantung pada koneksi, tabel `sipomas_app_data`, serta kebijakan akses Supabase yang benar. Statusnya terlihat pada indikator cloud di halaman. Data yang baru disunting sebaiknya dicadangkan terlebih dahulu sebelum mengganti konfigurasi atau memindahkan situs.

Laporan Excel dan cetak/PDF mengambil data dari penyimpanan aplikasi, termasuk data monitoring dan pembinaan. Cadangan JSON mencakup data SIPOMAS yang tersimpan di browser, termasuk foto dokumentasi. Sebelum mengandalkan salinan cloud, pastikan indikator menyatakan data telah tersinkron.

## Batasan dan keamanan

- Data awal adalah data contoh; periksa dan verifikasi sebelum digunakan.
- Prototype ini belum menyediakan login atau pembagian hak akses.
- Situs statis yang terhubung ke Supabase dengan kebijakan tulis publik dapat memungkinkan pengunjung mengubah data. Jangan masukkan informasi pribadi, rahasia, atau data operasional resmi.
- Integrasi cloud pada prototype bukan pengganti backend yang aman. Penggunaan operasional memerlukan autentikasi, otorisasi, validasi server, kebijakan database yang ketat, serta pengujian keamanan.
- Data lokal dapat hilang jika penyimpanan situs di browser dihapus. Buat cadangan berkala melalui menu **Laporan**.
