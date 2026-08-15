# Portofolio QA Engineer - alsomefuad

Selamat datang di catatan perjalanan belajar saya menjadi QA Engineer.

## Tugas Module 1: Manual Testing - Fitur Login

Berikut adalah beberapa Test Case yang saya buat untuk fitur Login:

| TC ID | Title / Scenario | Steps to Reproduce | Expected Result | Actual Result | Status |
|-------|------------------|--------------------|-----------------|---------------|--------|
| TC-01 | Login dengan kredensial valid | 1. Buka halaman login<br>2. Isi email: user@email.com<br>3. Isi password: Password123<br>4. Klik tombol Login | Berhasil login dan redirect ke halaman dashboard/user homepage | Berhasil login dan redirect ke dashboard | Pass |
| TC-02 | Login dengan password salah | 1. Buka halaman login<br>2. Isi email: user@email.com<br>3. Isi password: salahpass<br>4. Klik tombol Login | Menampilkan pesan error "Password salah" atau "Kredensial tidak valid" dan tetap di halaman login | Muncul pesan error "Invalid credentials" dan tidak bisa masuk ke dashboard | Fail |
| TC-03 | Login tanpa mengisi email (field email kosong) | 1. Buka halaman login<br>2. Kosongkan field email<br>3. Isi password: Password123<br>4. Klik tombol Login | Menampilkan validasi error "Email wajib diisi" atau "Field email tidak boleh kosong" dan tidak memproses login | Muncul pesan validasi "Email is required" di bawah field email | Pass |

---

## Bug Report 1: Login dengan Password Salah

**Bug Title:** Sistem tidak menampilkan pesan error yang jelas saat login dengan password salah
**Description:** Ketika user memasukkan email yang valid tetapi password salah, sistem menampilkan pesan error generic "Invalid credentials" tanpa membedakan apakah email atau password yang salah. Hal ini membingungkan user dan tidak user-friendly.
**Steps to Reproduce:**
1. Buka halaman login
2. Isi email: user@email.com
3. Isi password: salahpass
4. Klik tombol Login

**Expected Result:** Menampilkan pesan error "Password salah" atau "Kredensial tidak valid" dan tetap di halaman login
**Actual Result:** Muncul pesan error "Invalid credentials" dan tidak bisa masuk ke dashboard
**Severity:** Medium