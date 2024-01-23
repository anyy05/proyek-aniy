---
layout: post
title:  "install jekyll"
date:   2024-01-23 14:14:24 +0800
categories: jekyll update
---
Berikut adalah langkah-langkah untuk menginstal Jekyll di Windows:

Instal Ruby:

Unduh installer Ruby untuk Windows dari rubyinstaller.org.
Pilih versi Ruby yang direkomendasikan dan unduh installer "Ruby+Devkit".
Jalankan installer dan pastikan untuk memilih opsi "Add Ruby executables to your PATH" saat proses instalasi.
Buka Command Prompt:

Buka Command Prompt sebagai administrator. Klik kanan pada ikon Command Prompt dan pilih "Run as administrator".
Verifikasi Instalasi Ruby:

Setelah instalasi Ruby selesai, verifikasi instalasinya dengan menjalankan perintah berikut di Command Prompt:
bash
Copy code
ruby --version
Instal Jekyll dan Bundler:

Setelah Ruby terinstal, jalankan perintah berikut untuk menginstal Jekyll dan Bundler:
bash
Copy code
gem install jekyll bundler
Verifikasi Instalasi Jekyll dan Bundler:

Pastikan instalasi Jekyll dan Bundler berhasil dengan menjalankan perintah-perintah berikut:
bash
Copy code
jekyll -v
bundler -v
Buat Proyek Jekyll Baru:

Pindah ke direktori di mana Anda ingin membuat proyek Jekyll.
Jalankan perintah berikut untuk membuat proyek baru:
bash
Copy code
jekyll new namaproyek
Pindah ke Direktori Proyek:

Pindah ke direktori proyek dengan perintah:
bash
Copy code
cd namaproyek
Jalankan Server Lokal:

Jalankan server lokal Jekyll dengan perintah:
bash
Copy code
bundle exec jekyll serve
Buka Browser:

Buka browser dan kunjungi http://localhost:4000 untuk melihat proyek Jekyll Anda secara lokal.
Setelah selesai, Anda dapat mulai menyesuaikan proyek Jekyll Anda dengan menambahkan konten, mengonfigurasi tema, dan membuat perubahan lain sesuai kebutuhan. Pastikan untuk menyimpan perubahan dan mengunggahnya ke repositori GitHub jika Anda ingin menggunakan GitHub Pages.





