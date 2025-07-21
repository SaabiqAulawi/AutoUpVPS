# Panduan Penggunaan Git di GitHub

---

## 0. Instalasi Git, Git Bash, dan Inisialisasi Akun

### 1. Instalasi Git & Git Bash
1. Download Git dari [https://git-scm.com/downloads](https://git-scm.com/downloads)
2. Jalankan installer, pilih opsi default, dan pastikan **Git Bash** ikut terinstall.
3. Setelah selesai, buka **Git Bash** dari Start Menu.

### 2. Konfigurasi Akun Git
Setelah instalasi, lakukan konfigurasi identitas akun:
```bash
git config --global user.name "Nama Anda"
git config --global user.email "email@domain.com"
```
Ganti dengan nama dan email GitHub Anda.

### 3. (Opsional) Mengatur Default Editor
```bash
git config --global core.editor "code --wait"
```
Perintah di atas mengatur Visual Studio Code sebagai editor default.

### 4. (Opsional) Cek Konfigurasi
```bash
git config --list
```
Pastikan nama dan email sudah sesuai.

---

# Panduan Penggunaan Git di GitHub

Dokumen ini berisi langkah-langkah dasar penggunaan Git dalam konteks pengelolaan repository di GitHub, mulai dari clone, pull, add, commit, push, hingga sinkronisasi dengan repository remote.

---

## 1. Clone Repository
Untuk mengunduh repository dari GitHub ke komputer lokal:
```bash
git clone https://github.com/username/nama-repo.git
```
Ganti `username/nama-repo` dengan akun dan nama repository yang sesuai.

---

## 2. Membuat Perubahan (Edit/Add File)
Lakukan perubahan pada file yang diinginkan atau tambahkan file baru ke dalam folder project.

---

## 3. Melihat Status Perubahan
Untuk melihat file apa saja yang telah diubah:
```bash
git status
```

---

## 4. Menambahkan Perubahan ke Staging Area
Untuk menambahkan semua perubahan:
```bash
git add .
```
Atau tambahkan file tertentu:
```bash
git add nama_file.ext
```

---

## 5. Commit Perubahan
Commit digunakan untuk menyimpan snapshot perubahan ke repository lokal.
```bash
git commit -m "Judul Commit"
```
### Standarisasi Judul Commit
- [In Progres]
- Contoh: `-`

---

## 6. Push ke Repository GitHub
Untuk mengirim commit dari lokal ke repository GitHub:
```bash
git push origin main
```
Ganti `main` jika menggunakan branch lain.

---

## 7. Pull Update dari Repository GitHub
Untuk mengambil update terbaru dari repository GitHub:
```bash
git pull origin main
```
---

## 8. Membuat Branch Baru (Opsional)
Jika ingin mengerjakan fitur/bug secara terpisah:
```bash
git checkout -b nama-branch
```

---

## 9. Merge Branch (Opsional)
Setelah selesai di branch, gabungkan ke branch utama:
```bash
git checkout main
git merge nama-branch
```

---

## 10. Melihat Log Commit
Untuk melihat riwayat commit:
```bash
git log --oneline
```

---

## 11. Menghapus File dari Git
Untuk menghapus file dan mengupdate repository:
```bash
git rm nama_file.ext
git commit -m "hapus: menghapus file yang tidak diperlukan"
```

---

## 12. Sinkronisasi Fork (Jika menggunakan fork)
Untuk sinkronisasi fork dengan repository utama:
```bash
git remote add upstream https://github.com/original-owner/nama-repo.git
git fetch upstream
git merge upstream/main
```

---

**Catatan:**
- Selalu lakukan `git pull` sebelum melakukan perubahan untuk menghindari konflik.
- Gunakan pesan commit yang jelas dan sesuai standar tim.

---