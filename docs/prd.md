# Product Requirement Document (PRD)

**Nama Produk:** Edulink School
**Platform:** Web (Responsive)
**Target Pengguna:** Guru, Siswa, Staff Akademik, Orang Tua
**Jenjang:** TK, SD, SMP, SMA
**Versi:** 1.0
**Tanggal:** 2025

---

## 1. Ringkasan Produk

Edulink School adalah sistem berbasis web untuk mengelola seluruh kegiatan akademik sekolah dari jenjang TK hingga SMA. Antarmuka disesuaikan per jenjang — TK menggunakan capaian perkembangan deskriptif, sementara SMP/SMA menggunakan sistem nilai angka dengan bobot.

---

## 2. Pengguna & Kebutuhan Fungsional

| Peran | Fitur Utama |
|-------|-------------|
| **Admin Akademik** | CRUD data siswa, guru, kelas, mata pelajaran; generate tahun ajaran; atur hak akses per role |
| **Guru** | Input nilai (angka & deskripsi); rekap absensi; cetak daftar nilai & rapor sementara; kirim pengumuman ke kelas/orang tua |
| **Siswa** | Lihat jadwal harian; lihat nilai per mata pelajaran; unduh tugas dari guru |
| **Orang Tua** | Monitoring nilai & absensi anak; riwayat pelanggaran/prestasi; kirim pesan ke wali kelas |

---

## 3. Penyesuaian per Jenjang

| Jenjang | Penyesuaian |
|---------|-------------|
| **TK** | Tidak menggunakan nilai angka; menggunakan capaian perkembangan (bintang/deskripsi) |
| **SD** | Mata pelajaran tematik, rapor deskriptif |
| **SMP/SMA** | Nilai angka + bobot, rapor numerik, ujian online sederhana |

---

## 4. Fitur MVP (Minimum Viable Product)

### Epik 1 – Manajemen Master Data
- Import/export data siswa (Excel)
- Kelola kelas & wali kelas
- Kelola periode akademik (semester gasal/genap)

### Epik 2 – Pengelolaan Nilai & Kehadiran
- Form input kehadiran per pertemuan
- Input nilai tugas, UTS, UAS
- Perhitungan rata-rata otomatis sesuai bobot

### Epik 3 – Portal Orang Tua & Siswa
- Dashboard ringkasan nilai & izin
- Notifikasi jika nilai di bawah KKM (email/WA gateway — opsional)

### Epik 4 – Laporan
- Cetak rapor per siswa (format TK/SD/SMP/SMA berbeda)
- Ekspor data kelas (CSV/PDF)

---

## 5. Kebutuhan Non-Fungsional

| Aspek | Spesifikasi |
|-------|-------------|
| **Kinerja** | Waktu muat dashboard < 2 detik untuk 500 user simultan |
| **Keamanan** | Autentikasi role-based, log aktivitas, enkripsi data pribadi siswa |
| **Aksesibilitas** | Mode baca untuk orang tua dengan disabilitas ringan |
| **Dukungan Perangkat** | Web responsif (desktop, tablet) |
| **Integrasi** | Sinkronisasi Dapodik (opsional, post-MVP) |

---

## 6. Alur Pengguna (User Flow)

### Guru → Input Nilai
```
Login
  └─> Pilih Kelas
        └─> Pilih Mata Pelajaran
              └─> Pilih Siswa
                    └─> Isi Nilai (Tugas / UH / UTS / UAS)
                          └─> Simpan
                                └─> Sistem hitung rata-rata otomatis
                                      └─> Tampil di dashboard siswa & orang tua
```

### Orang Tua → Lihat Nilai Anak
```
Login
  └─> Pilih Anak (jika > 1)
        └─> Lihat Semester Berjalan
              └─> Klik Mata Pelajaran
                    └─> Tampil detail nilai & grafik perkembangan
```

---

## 7. Matriks Kesesuaian RUMPUN ILMU

| Elemen | Isi | Status |
|--------|-----|--------|
| **P** – Platform | Web | ✅ Web responsive |
| **I** – Pengguna | Guru, siswa, akademik, orang tua | ✅ Role spesifik tersedia |
| **C** – Sistem untuk | TK, SD, SMP, SMA | ✅ Penyesuaian per jenjang |
| **O** – Tujuan | Pendidikan | ✅ Fokus akademik & monitoring |
| **S** – Manfaat | Memudahkan pengelolaan akademik | ✅ Inti value proposition |

---

## 8. Kriteria Penerimaan (Acceptance Criteria)

- Guru dapat menginput nilai untuk seluruh siswa dalam satu kelas dalam < 10 menit
- Orang tua dapat melihat nilai dan absensi anak secara real-time setelah guru menyimpan
- Sistem menghasilkan rapor yang dapat dicetak sesuai format jenjang masing-masing
- Admin dapat menambahkan/menghapus data siswa dengan fitur import Excel
- Seluruh data pribadi siswa tersimpan terenkripsi di database