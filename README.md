# EduClass — Prototipe E-Learning Integral

EduClass adalah implementasi awal website e-learning matematika untuk SMA/SMK. Dibuat dengan HTML, CSS, dan JavaScript murni agar mudah diedit tanpa framework.

## Fitur yang sudah dapat dicoba
- Beranda dan indikator progres belajar.
- 8 topik integral: pengenalan, integral tak tentu, aturan pangkat, sifat integral, integral tentu, luas daerah, fungsi aljabar, dan aplikasi.
- Sematan GeoGebra untuk eksplorasi grafik/integral (membutuhkan internet).
- Kuis interaktif 5 soal, umpan balik untuk jawaban benar/salah, nilai dan riwayat percobaan.
- Daftar tugas dengan status demo.
- Catatan nilai, absensi, dan diskusi.
- Pengaturan nama sekolah/kelas dan warna identitas sekolah.
- Data prototipe disimpan pada `localStorage` browser yang digunakan.

## Cara menjalankan
1. Ekstrak ZIP.
2. Buka folder `EduClass`.
3. Buka `index.html` di Chrome, Edge, atau Firefox.
4. Internet diperlukan untuk Google Fonts dan GeoGebra; halaman utama tetap bisa dibuka secara lokal.
5. Buka menu **Pengaturan** untuk mengganti nama sekolah dan warna utama/aksen.

Jika browser membatasi iframe GeoGebra ketika dibuka langsung dari file, jalankan server lokal:
- Jika Python terpasang, buka terminal di folder `EduClass`, jalankan `python -m http.server 8000`.
- Buka `http://localhost:8000`.

## Struktur file
- `index.html` — struktur halaman dan komponen.
- `style.css` — desain, tata letak, warna, dan responsivitas.
- `app.js` — materi, kuis, umpan balik, tugas, nilai, absensi, diskusi, dan penyimpanan lokal.

## Cara menyesuaikan
- Warna dan nama sekolah: menu **Pengaturan** di website.
- Konten materi: edit array `lessons` di bagian atas `app.js`. Setiap materi memiliki `title`, `desc`, `icon`, `time`, dan `body` (HTML).
- Soal kuis: edit array `questions` di `app.js`. `correct` adalah indeks jawaban yang benar, dimulai dari 0. `why` berisi penjelasan yang tampil setelah jawaban diperiksa.
- Tugas: edit array `tasks` di `app.js`.
- Tata letak dan ukuran: edit `style.css`; warna awal berada di `:root`.
- Nama menu dan halaman: edit `index.html`.

## Batasan versi awal
Ini prototipe frontend, bukan LMS produksi. Data hanya tersimpan di browser/perangkat yang sama dan tidak dibagikan ke guru atau siswa lain. Belum ada login, database online, peran guru/siswa, unggah file tugas, penilaian guru, diskusi realtime, atau absensi terverifikasi. Untuk dipakai oleh satu sekolah, langkah berikutnya adalah membuat backend dan database (misalnya Node.js + Express + PostgreSQL/Supabase), autentikasi, kontrol akses, serta hosting HTTPS. Jangan memakai data siswa asli pada versi demo ini.
