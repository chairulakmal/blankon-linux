# Petunjuk Penulisan Wiki

Halaman ini untuk siapa saja yang menulis atau menyunting halaman di wiki ini. Halaman ini menjelaskan cara menulis dan menempatkan halaman. Hal terpenting: setiap halaman ditulis untuk pembacanya, dan sebagian besar pembaca adalah pengguna BlankOn yang membaca Bahasa Inggris sebagai bahasa kedua. Halaman ini terdiri dari lima bagian: tempat halaman, bahasa yang dipakai, cara menulis halaman, templat panduan pengguna, dan cara mengelola terjemahan.

## Struktur Wiki

Penempatan dokumen mesti mengikuti struktur dan pola yang sudah ada. Jika Anda tidak yakin di mana sebuah dokumen mesti diletakkan, silakan konsultasikan dengan pengembang lain.

Direktori dan berkas harus menggunakan PascalCase (huruf pertama pakai kapital, tanpa spasi).

## Bahasa

Bahasa Inggris diutamakan.

Namun jika Anda tidak yakin dengan penulisan dalam Bahasa Inggris, silakan memulai dengan Bahasa Indonesia dan menamakan berkasnya dengan `*.id.md`. Namun demikian, nama direktori dan berkas tetap harus dalam Bahasa Inggris, disamakan dengan versi Bahasa Inggrisnya dengan suffix `*.id.md`.

## Menulis Halaman

Wiki ini punya dua kelompok pembaca. Sebagian besar adalah pengguna BlankOn. Sisanya adalah kontributor BlankOn. Tulislah halaman pengguna sehingga pengguna baru dapat mengikutinya tanpa bantuan.

1. **Mulai dengan siapa pembaca halaman ini.** Paragraf pertama menyebutkan siapa yang sebaiknya membaca halaman ini dan apa yang dapat mereka lakukan dengan bantuan halaman ini.
2. **Gunakan Bahasa Inggris yang sederhana.** Tulis kalimat pendek, satu gagasan per kalimat. Gunakan kata-kata yang umum. Hindari idiom dan bahasa gaul.
3. **Jelaskan istilah baru.** Saat pertama kali memakai istilah yang mungkin belum dikenal pembaca baru, jelaskan istilah itu atau tautkan ke halaman yang menjelaskannya. Nama-nama BlankOn seperti Sinambung dan Arsip dijelaskan di glosarium (`Glossary.md`).
4. **Tulis langkah yang persis.** Gunakan langkah bernomor, satu tindakan per langkah. Letakkan setiap perintah di dalam blok kode. Jangan menulis `$` di depan perintah, agar pembaca dapat menyalinnya.
5. **Tunjukkan cara memeriksa hasilnya.** Setelah langkah-langkah, beri tahu pembaca cara memastikan bahwa langkahnya berhasil.
6. **Tautkan, jangan mengulang.** Jika halaman lain sudah menjelaskan sesuatu, tautkan ke halaman itu. Gunakan URL GitHub lengkap, misalnya `https://github.com/BlankOn/blankon-linux/blob/main/Goals.md`, karena tautan relatif seperti `Goals.md` tidak berfungsi di situs web BlankOn.
7. **Jaga agar halaman saling sesuai.** Jika halaman Anda dan halaman lain tidak sesuai, perbaiki yang salah di pull request yang sama.

## Templat Panduan Pengguna

Salin templat ini untuk halaman baru di `UserGuides/`. Hapus bagian yang tidak diperlukan.

````markdown
# Page Title

This page is for <who>. It explains how to <do what>.

## Before You Start

- <What the reader needs first: hardware, packages, settings>

## Steps

1. <One action.>

   ```
   <command>
   ```

2. <Next action.>

## Check the Result

<How the reader can see that it worked.>

## If Something Goes Wrong

<Common problems and their fixes. For other problems, report an issue at https://github.com/BlankOn/blankon-linux/issues.>
````

## Terjemahan

Terjemahan diletakkan di sebelah halaman aslinya, dengan nama yang sama ditambah akhiran bahasa. Misalnya, versi Bahasa Indonesia dari `Docker.md` adalah `Docker.id.md`.

1. **Terjemahkan halaman setelah isinya stabil.** Halaman yang masih sering berubah membuat terjemahannya tertinggal.
2. **Jangan menerjemahkan nama, perintah, atau nama berkas.** Tulis persis seperti di halaman aslinya.
3. **Jaga agar kedua versi tetap sesuai.** Saat Anda mengubah halaman yang punya terjemahan, perbarui terjemahannya di pull request yang sama. Jika tidak bisa, buat issue yang meminta terjemahannya diperbarui.
