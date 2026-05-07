# Business Requirement Document (BRD)

**Proyek:** Sistem Informasi Manajemen Akademik Sekolah (TK–SMA)
**Domain:** Ilmu Komputer / Teknologi Pendidikan
**Pemilik Bisnis:** Dinas Pendidikan / Yayasan Sekolah
**Versi:** 1.0
**Tanggal:** 2025

---

## 1. Latar Belakang Bisnis

Sekolah dari jenjang TK hingga SMA masih banyak mengelola data akademik secara manual atau terpisah-pisah (Excel, kertas, WhatsApp). Hal ini menyulitkan **guru, siswa, akademik, dan orang tua** dalam memantau proses belajar dan administrasi secara efektif.

---

## 2. Tujuan Bisnis (Business Objectives)

- Memudahkan pengelolaan akademik sekolah secara terpusat dan terintegrasi
- Meningkatkan efisiensi waktu guru dan staf tata usaha hingga **40%**
- Meningkatkan transparansi nilai dan kehadiran bagi orang tua

---

## 3. Ruang Lingkup Bisnis

| Aspek | Detail |
|-------|--------|
| **Jenjang** | TK, SD, SMP, SMA |
| **Modul** | Kelola siswa, jadwal, nilai, kehadiran, ujian, rapor, komunikasi orang tua–guru |
| **Platform** | Web (responsive, mobile-friendly) |

---

## 4. Stakeholders

| Stakeholder | Kebutuhan Utama |
|-------------|----------------|
| Guru | Input nilai, absensi, cetak laporan kelas |
| Siswa | Lihat jadwal, nilai, tugas |
| Akademik (Staff TU) | Kelola data master (kelas, mapel, guru) |
| Orang Tua | Pantau progres anak, izin, komunikasi wali kelas |

---

## 5. Key Performance Indicators (KPI)

| KPI | Target |
|-----|--------|
| Adopsi pengguna aktif (guru) | > 80% dalam 3 bulan pertama |
| Waktu input nilai per kelas | < 10 menit |
| Orang tua login minimal 1x/minggu | ≥ 60% |

---

## 6. Asumsi & Batasan

- Sistem digunakan dalam lingkungan sekolah dengan koneksi internet minimal
- Integrasi Dapodik bersifat opsional (tidak termasuk MVP)
- Data siswa wajib dienkripsi sesuai regulasi perlindungan data pribadi

---

## 7. Risiko Bisnis

| Risiko | Mitigasi |
|--------|----------|
| Resistensi adopsi dari guru senior | Pelatihan onboarding + antarmuka sederhana |
| Ketidaksesuaian format rapor antar daerah | Tersedia template yang dapat dikustomisasi |
| Gangguan koneksi internet di sekolah | Mode offline terbatas untuk input kehadiran |