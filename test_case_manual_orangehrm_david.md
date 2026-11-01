# Test Case — OrangeHRM Modules (10 Skema)

| Field | Keterangan |
| --- | --- |
| **Nama Proyek** | OrangeHRM Open Source Demo |
| **URL** | https://opensource-demo.orangehrmlive.com/ |
| **Modul** | Login, Search, Dashboard, My Info, Recruitment, Performance, Directory, Maintenance, Claim, Buzz |
| **Jumlah Test Case** | 10 (TC-001 s/d TC-010) |
| **Tanggal Dibuat** | 1 November 2026 |
| **Tester** | [Nama Anda] |
| **Environment** | Web Browser (Chrome/Firefox/Edge) |
| **Referensi** | template-test-case-automationexercise.md |

**Keterangan kolom `Jenis`**

- **Positive** → skenario dengan input/flow valid, sistem diharapkan sukses.
- **Negative** → skenario dengan input tidak valid, sistem diharapkan menolak dan menampilkan pesan error.

---

## Tabel Test Case

| ID | Skenario | Step | Jenis | Expected |
| --- | --- | --- | --- | --- |
| **TC-001** | **Skema Login:** Login dengan kredensial valid | 1. Buka halaman URL login OrangeHRM<br>2. Input username `Admin`<br>3. Input password `admin123`<br>4. Klik tombol 'Login' | Positive | Pengguna berhasil masuk, diarahkan ke halaman Dashboard, dan melihat menu pada sidebar kiri. |
| **TC-002** | **Skema Search:** Mencari modul melalui kolom pencarian sidebar | 1. Login ke aplikasi<br>2. Ketik kata `Admin` pada kolom *Search* di sidebar kiri<br>3. Pilih hasil pencarian yang muncul di bawah kolom tersebut | Positive | Sidebar hanya menampilkan menu yang mengandung kata "Admin". Setelah diklik, sistem beralih ke halaman Admin. |
| **TC-003** | **Skema Dashboard:** Menampilkan widget ringkasan pada Dashboard | 1. Login ke aplikasi<br>2. Klik menu `Dashboard` di sidebar<br>3. Periksa ketersediaan widget (Time at Work, My Actions, dll) | Positive | Halaman Dashboard termuat dengan sempurna dan seluruh widget standar (seperti Quick Launch, Employees on Leave Today) tampil tanpa error. |
| **TC-004** | **Skema My Info:** Melihat profil detail akun mandiri | 1. Login ke aplikasi<br>2. Klik menu `My Info` di sidebar<br>3. Periksa form yang terdapat pada tab *Personal Details* | Positive | Halaman terbuka menampilkan detail data pribadi, foto profil, serta sub-menu profil yang relevan dengan pengguna login (misal: Paul Collin). |
| **TC-005** | **Skema Recruitment:** Menampilkan daftar kandidat pelamar | 1. Login ke aplikasi<br>2. Klik menu `Recruitment` di sidebar<br>3. Pastikan berada di tab *Candidates*<br>4. Klik tombol 'Search' | Positive | Tabel menampilkan daftar nama kandidat pelamar pekerjaan, posisi (Job Title), status kandidat, beserta action button (mata/download). |
| **TC-006** | **Skema Performance:** Memeriksa daftar Key Performance Indicators (KPIs) | 1. Login ke aplikasi<br>2. Klik menu `Performance`<br>3. Pada navbar atas, klik dropdown `Configure` lalu pilih `KPIs` | Positive | Halaman daftar KPI berhasil dimuat yang menampilkan berbagai indikator performa untuk tiap Job Title (jabatan). |
| **TC-007** | **Skema Directory:** Melakukan pencarian spesifik data karyawan | 1. Login ke aplikasi<br>2. Klik menu `Directory` di sidebar<br>3. Ketik nama `Peter` di field *Employee Name*<br>4. Klik tombol 'Search' | Positive | Sistem memfilter direktori dan hanya menampilkan kartu profil karyawan yang namanya mengandung kata "Peter" beserta jabatan dan lokasinya. |
| **TC-008** | **Skema Maintenance:** Gagal masuk mode Maintenance karena password salah | 1. Login ke aplikasi sebagai Admin<br>2. Klik menu `Maintenance` di sidebar<br>3. Muncul prompt otorisasi. Input password `salah123`<br>4. Klik tombol 'Confirm' | Negative | Sistem menampilkan pesan error `Invalid Credentials` warna merah muda, dan pengguna tetap berada di prompt akses (tidak bisa mengakses module Maintenance). |
| **TC-009** | **Skema Claim:** Melihat riwayat pengajuan klaim (Employee Claims) | 1. Login ke aplikasi<br>2. Klik menu `Claim` di sidebar<br>3. Masukkan rentang tanggal atau biarkan kosong, klik 'Search' | Positive | Tabel *Claim Requests* menampilkan daftar riwayat klaim biaya atau asuransi beserta *Reference ID*, *Event Name*, dan *Status*. |
| **TC-010** | **Skema Buzz:** Membuat postingan (Status Update) pada feed | 1. Login ke aplikasi<br>2. Klik menu `Buzz` di sidebar<br>3. Ketik "Halo tim, selamat pagi!" pada kolom *Update Status*<br>4. Klik tombol 'Post' | Positive | Postingan berhasil dikirim, muncul notifikasi "Successfully Saved", dan status langsung tayang di paling atas beranda (newsfeed) Buzz. |

---

## Ringkasan

| Jenis | Jumlah | ID |
| --- | --- | --- |
| Positive | 9 | TC-001 s/d TC-007, TC-009 s/d TC-010 |
| Negative | 1 | TC-008 |
| **Total** | **10** | TC-001 s/d TC-010 |

---