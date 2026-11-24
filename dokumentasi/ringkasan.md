# Ringkasan Tugas 10 – Selaras Coffee

Website Selaras Coffee dibangun satu halaman dengan Bootstrap 5.3.3 yang dimuat lewat CDN. Komponen yang dipakai adalah navbar responsif, hero, tiga card menu, satu alert promo, tiga modal detail menu, form kontak, dan footer. Branding dibuat melalui stylesheet custom (css/style.css) dengan palet ungu, font Rajdhani untuk judul, Nunito Sans untuk teks, serta sudut terpotong (clip-path) pada tombol, card, dan hero sebagai ciri khas visual.

Perubahan utama dari tampilan bawaan Bootstrap ada pada variabel warna dan font di :root, gaya tombol, card, alert, modal, dan form. Animasi uap kopi pada hero dibuat dengan CSS dan dimatikan bagi pengguna yang memilih reduced motion.

Masalah pertama, navbar fixed-top menutupi judul bagian saat menu diklik. Solusinya memberi padding atas pada hero dan scroll-margin-top pada setiap section, ditambah scrollspy Bootstrap agar menu aktif berganti otomatis. Masalah kedua, tinggi card tidak seragam karena panjang deskripsi berbeda. Solusinya memakai h-100 dan flex column, dengan harga bermargin mt-auto agar tombol sejajar. Masalah ketiga, tombol "Pesan sekarang" pada modal tidak menutup modal, karena data-bs-dismiss pada tautan href="#kontak" membuat Bootstrap mencari elemen #kontak, bukan modalnya. Solusinya menambahkan data-bs-target yang menunjuk ke modal masing-masing.

Tampilan diuji pada lebar desktop 1366 px dan mobile 390 px tanpa scroll horizontal.
