# Alphabet Adventure PWA — GitHub Pages

Paket ini berisi game HTML, manifest PWA, service worker offline, ikon, dan workflow GitHub Actions untuk deployment otomatis ke GitHub Pages.

## Publikasikan ke GitHub Pages

1. Buat repository baru di GitHub, misalnya `alphabet-adventure-pwa`.
2. Ekstrak ZIP ini, lalu unggah **seluruh isi folder** ke root repository (termasuk `.github/workflows/pages.yml` dan `.nojekyll`). Commit ke branch `main`.
3. Di repository GitHub, buka **Settings → Pages**.
4. Pada **Build and deployment → Source**, pilih **GitHub Actions**.
5. Buka tab **Actions**, pastikan workflow `Deploy Alphabet Adventure PWA to GitHub Pages` selesai dengan status hijau.
6. URL umumnya `https://USERNAME.github.io/REPOSITORY/`.

## Instalasi perangkat

- Android/Chrome: buka URL HTTPS, menu browser → Install app / Add to Home screen.
- iPhone/iPad: buka URL di Safari → Share → Add to Home Screen.
- Desktop Chrome/Edge: gunakan ikon Install atau menu browser bila tersedia.

## Offline

Buka aplikasi sekali saat online dan tunggu sampai halaman selesai dimuat agar service worker dapat menyimpan app shell. Kemudian uji dengan mematikan internet.

## Catatan

- GitHub Pages menggunakan HTTPS, yang dibutuhkan service worker.
- Tidak perlu npm build; situs statis ini dideploy langsung.
- Pada setiap push ke `main`, workflow akan menerbitkan perubahan secara otomatis.
- File `index.html` berisi aset game yang tertanam (gambar dan audio), sehingga ukuran HTML cukup besar.
