# Tutorial Setup GitHub dari Awal

## 1. Buat Akun GitHub

Jika belum punya akun GitHub, daftar di [GitHub](https://github.com/) dan login ke akun kamu.

## 2. Install Git di Komputer

- Unduh dan install Git sesuai OS kamu dari [git-scm.com](https://git-scm.com/).
- Setelah install, cek apakah Git sudah terpasang dengan menjalankan perintah berikut di terminal atau Command Prompt (CMD):

  ```sh
  git --version
  ```

## 3. Konfigurasi Git di Komputer

Atur nama pengguna dan email agar commit yang kamu buat dikenali oleh GitHub:

```sh
git config --global user.name "NamaKamu"
git config --global user.email "emailkamu@example.com"
```

## 4. Buat Repositori di GitHub

1. Masuk ke GitHub dan klik tombol **New** untuk membuat repositori baru.
2. Masukkan nama repositori dan deskripsi.
3. Pilih **Public** atau **Private** sesuai kebutuhan.
4. Klik **Create repository**.

## 5. Hubungkan Repositori GitHub ke Komputer

Buka terminal atau CMD dan navigasikan ke folder tempat proyek akan disimpan:

```sh
cd path/ke/folder/proyek
```

Inisialisasi Git di dalam folder proyek:

```sh
git init
```

Hubungkan ke repositori GitHub:

```sh
git remote add origin https://github.com/username/repository.git
```

## 6. Buat Commit dan Push ke GitHub

Tambahkan file atau ubah sesuatu dalam proyek, lalu lakukan commit dan push:

```sh
git add .
git commit -m "Commit pertama"
git branch -M main
git push -u origin main
```

## 7. Cek Kontribusi di GitHub

Jika langkah-langkah di atas berhasil, buka halaman profil GitHub kamu. Kamu akan melihat kontribusi pertama di grafik aktivitas GitHub.

## 8. (Opsional) Menjalankan SSH Authentication (Agar Tidak Perlu Login Setiap Push)

1. Jalankan perintah berikut untuk membuat SSH Key:

   ```sh
   ssh-keygen -t ed25519 -C "emailkamu@example.com"
   ```

2. Tambahkan kunci SSH ke GitHub:

   - Salin SSH Key dengan menjalankan:
     ```sh
     cat ~/.ssh/id_ed25519.pub
     ```
   - Buka GitHub → Settings → SSH and GPG keys → New SSH Key → Paste kunci tersebut → Save.

3. Ubah remote URL menjadi SSH:
   ```sh
   git remote set-url origin git@github.com:username/repository.git
   ```
