# SIPOMAS

**Sistem Informasi Pendataan dan Informasi Organisasi Kemasyarakatan**  
Prototype digital untuk mendukung pendataan, pembinaan, monitoring, dan pengawasan organisasi kemasyarakatan (ORMAS) di Kabupaten Bengkulu Selatan.

## Tentang aplikasi

SIPOMAS dibuat sebagai prototype satu halaman berbasis HTML, CSS, dan JavaScript. Aplikasi dapat dibuka langsung di browser tanpa memasang dependensi atau menjalankan server.

## Fitur

- **Dashboard** — ringkasan angka ORMAS dan anggota, sebaran per kecamatan, serta informasi terkini. Angka dashboard dapat diedit.
- **Profil SIPOMAS** — menjelaskan tujuan dan perubahan yang diharapkan dari sistem.
- **Data ORMAS** — mencari, menambah, mengubah, dan menghapus data organisasi.
- **Data anggota** — mengelola informasi anggota ORMAS.
- **Jumlah anggota ORMAS** — melihat serta memperbarui jumlah anggota tiap organisasi.
- **Data ORMAS terperinci** — mengelola informasi kelembagaan, kepengurusan, alamat, bidang, dan kegiatan organisasi.
- **Monitoring dan pembinaan** — menampilkan contoh kegiatan dan status pelaksanaannya.
- **Laporan** — menampilkan rekapitulasi; fitur cetak masih berupa pemberitahuan prototype.
- **Dokumentasi** — menambah, mengubah, dan menghapus dokumentasi kegiatan, termasuk foto.

## Menjalankan aplikasi

1. Pastikan seluruh file dalam folder proyek tetap berada pada susunan yang sama.
2. Buka `index.html` menggunakan browser, atau gunakan ekstensi seperti **Live Server** di Visual Studio Code.
3. Untuk penyimpanan yang lebih konsisten, jalankan melalui Live Server dan gunakan browser yang sama setiap kali membuka aplikasi.

Tidak diperlukan proses build maupun instalasi paket.

## File utama dan aset

| File | Keterangan |
| --- | --- |
| `index.html` | Halaman utama aplikasi SIPOMAS. |
| `Kabupaten-Bengkulu-Selatan-Logo-removebg-preview.png` | Lambang Kabupaten Bengkulu Selatan di sidebar. |
| `bupati_bs-removebg-preview.png` | Foto Bupati dan Wakil Bupati di banner dashboard. |

Foto gedung yang digunakan sebagai latar halaman dan banner dashboard dimuat dari URL eksternal. Karena itu, latar tersebut memerlukan koneksi internet; logo dan foto pada folder proyek tetap dimuat dari file lokal.

## Penyimpanan data

Perubahan data disimpan menggunakan `localStorage` pada browser. Artinya, data tersimpan hanya di browser dan profil pengguna yang sedang digunakan, bukan di server atau basis data bersama. Data tidak otomatis tersinkronisasi dengan pengguna/perangkat lain dan dapat hilang jika data situs di browser dihapus.

Aplikasi belum menyediakan fitur ekspor atau pemulihan cadangan. Hindari menghapus data situs di browser jika perubahan ingin dipertahankan. Foto dokumentasi yang diunggah juga disimpan di penyimpanan lokal browser.

## Batasan prototype

- Data awal yang tersedia adalah data contoh dan perlu diverifikasi sebelum digunakan untuk keperluan resmi.
- Belum tersedia login, pembagian hak akses, server, maupun basis data terpusat.
- Data monitoring dan pembinaan masih berupa contoh statis.
- Tombol cetak laporan belum menghasilkan berkas PDF atau Excel.
- Validasi, pencadangan, dan keamanan data belum dirancang untuk penggunaan produksi.

Untuk penggunaan operasional, aplikasi perlu diintegrasikan dengan backend dan basis data, dilengkapi autentikasi serta hak akses, dan menjalani pengujian serta peninjauan keamanan.
