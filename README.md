<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=4F46E5&height=200&section=header&text=Nexkola&fontSize=80&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Platform+Manajemen+Sekolah+Digital&descAlignY=60&descColor=c7d2fe" />

<p align="center">
  <img src="https://img.shields.io/badge/Status-In%20Development-yellow?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Laravel-11-FF2D20?style=for-the-badge&logo=laravel&logoColor=white" />
  <img src="https://img.shields.io/badge/SSO-Laravel%20Passport-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" />
</p>

<p align="center">
  <b>Nexkola</b> adalah platform manajemen sekolah digital yang mengintegrasikan seluruh kebutuhan akademik dalam satu ekosistem — satu akun untuk semua fitur.
</p>

</div>

---

## 🌐 Tentang Nexkola

**Nexkola** hadir sebagai solusi pengelolaan sekolah modern yang menggabungkan presensi, pembelajaran, pelaporan, dan manajemen akademik dalam satu platform terpadu. Dibangun dengan **Laravel** dan menggunakan arsitektur **Single Sign-On (SSO)** berbasis **Laravel Passport**, Nexkola memastikan pengalaman yang mulus untuk semua pengguna — Admin, Guru, Siswa, maupun Orang Tua.

> 🚧 **Project ini sedang dalam tahap pengembangan aktif.** Fitur-fitur di bawah merupakan rencana yang akan dirilis secara bertahap.

---

## ✨ Fitur Utama

### 🔐 Auth & SSO
- Login/Logout terpusat via **Laravel Passport**
- 1 akun untuk semua modul
- Manajemen role: `Admin` `Guru` `Siswa` `Orang Tua`
- Reset password & manajemen token OAuth2

### 🏫 Manajemen Sekolah
- Manajemen kelas, jurusan, & mata pelajaran
- Manajemen tahun ajaran & semester
- Jadwal pelajaran
- CRUD data guru & siswa
- Import data siswa via Excel

### ✅ Presensi
- Absen harian siswa & guru
- QR Code untuk absen *(opsional)*
- Rekap kehadiran harian, bulanan, per semester
- Notifikasi ke orang tua jika siswa tidak hadir
- Export rekap ke PDF/Excel

### 📚 Modul Belajar
- Upload materi per mapel & kelas (PDF, video, link)
- Manajemen tugas & pengumpulan
- Batas waktu & penilaian tugas
- Diskusi/komentar per materi

### 📢 Pengaduan
- Form pengaduan untuk siswa & orang tua
- Kategori & tracking status *(Pending → Diproses → Selesai)*
- Balasan dari admin/guru
- Riwayat pengaduan

### ⚠️ Pelanggaran
- Input pelanggaran by guru
- Kategori & bobot poin pelanggaran
- Rekap poin per siswa
- Notifikasi otomatis ke orang tua
- Auto-flag siswa dengan poin melebihi batas

### 📊 Nilai & Rapor
- Input nilai harian, UTS, UAS
- Kalkulasi nilai akhir otomatis
- Rapor digital per semester
- Export rapor ke PDF

### 📣 Pengumuman
- Pengumuman sekolah by admin/guru
- Target per kelas atau seluruh sekolah
- Notifikasi real-time

### 💬 Notifikasi
- Notifikasi in-app
- Email notifikasi
- WhatsApp via Fonnte *(opsional)*

### 📈 Dashboard & Laporan
- Dashboard berbeda tiap role
- Laporan presensi, pelanggaran, & akademik

---

## 🗺️ Roadmap

```
✅ = Planned   🔄 = In Progress   ✔️ = Done
```

| Fase | Fitur | Status |
|------|-------|--------|
| **v0.1** | Auth & SSO (Laravel Passport) | ✅ |
| **v0.1** | Manajemen Role & User | ✅ |
| **v0.2** | Manajemen Sekolah (kelas, mapel, jadwal) | ✅ |
| **v0.2** | Presensi Siswa & Guru | ✅ |
| **v0.3** | Modul Belajar & Tugas | ✅ |
| **v0.3** | Form Pengaduan | ✅ |
| **v0.4** | Form Pelanggaran & Poin | ✅ |
| **v0.4** | Nilai & Rapor Digital | ✅ |
| **v0.5** | Notifikasi (in-app, email, WA) | ✅ |
| **v0.5** | Dashboard & Laporan | ✅ |
| **v1.0** | QR Code Presensi | ✅ |
| **v1.0** | Export PDF & Excel | ✅ |
| **Future** | Pembayaran SPP (Midtrans) | ✅ |
| **Future** | Chat Internal | ✅ |
| **Future** | Forum Diskusi Per Kelas | ✅ |
| **Future** | Perpustakaan Digital | ✅ |

---

## 🛠️ Tech Stack

| Layer | Teknologi |
|-------|-----------|
| Backend | Laravel 11 |
| Auth / SSO | Laravel Passport (OAuth2) |
| Permission | Spatie Laravel Permission |
| Frontend | Blade + Tailwind CSS |
| Database | MySQL |
| File Storage | Laravel Storage |
| Notifikasi WA | Fonnte API *(opsional)* |
| Export | DomPDF + Laravel Excel |

---

## 🏗️ Arsitektur SSO

```
┌─────────────────────────────────────────────┐
│              Nexkola Auth Server             │
│           (Laravel Passport / OAuth2)        │
└──────────────────┬──────────────────────────┘
                   │ Token
       ┌───────────┼───────────┐
       ▼           ▼           ▼
  [Presensi]  [Akademik]  [Pengaduan]
   Module      Module       Module
```

> Satu token, akses ke semua modul.

---

## 📁 Repositories

| Repo | Deskripsi |
|------|-----------|
| `nexkola/auth-server` | Core SSO — Laravel Passport |
| `nexkola/app` | Main Application |
| `nexkola/docs` | Dokumentasi & API Spec |

---

## 🤝 Kontribusi

Nexkola masih dalam tahap awal pengembangan. Kontribusi sangat terbuka!

1. Fork repository
2. Buat branch baru (`feature/nama-fitur`)
3. Commit perubahan kamu
4. Buat Pull Request

---

## 📄 Lisensi

Didistribusikan di bawah lisensi **MIT**. Lihat `LICENSE` untuk informasi lebih lanjut.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=4F46E5&height=100&section=footer" />

<p>Made with ❤️ for better school management</p>

</div>
