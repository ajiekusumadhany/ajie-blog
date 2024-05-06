---
title: 'Belajar Html (Hypertext Markup Language)'
date: Mon, 13 Mar 2023 16:16:10 +0000
draft: false
tags: ['Html', 'Pemrograman']
---

HTML (Hypertext Markup Language) adalah bahasa markup yang digunakan untuk membuat dan merancang sebuah halaman web. HTML memungkinkan kita untuk menentukan struktur dan isi dari sebuah halaman web dengan menambahkan elemen markup, seperti teks, gambar, video, link, dan lain-lain.

Struktur Dasar Html
-------------------

```
<!DOCTYPE html> <!--untuk memberi informasi browser bahwa ini adalah dokumen html-->
<html> <!--tag pembuka dokumen html-->

<head> <!--untuk menyimpan berbagai informasi seperti: schema markup, memanggil css eksternal dsb.-->
    <title>Judul Halaman / Website</title> <!--judul website di bar browser-->
</head>

<body> <!--semua yang akan ditampilkan browser ditulis disini-->
    Isi Website
</body>

</html> <!--tag penutup halaman html-->


```

Heading Html
------------

Dalam html terdapat 6 tag heading, h1 adalah yang terbesar dan h6 adalah yang terkecil```
<h1>Judul dengan H1</h1>
<h2>Judul dengan H2</h2>
<h3>Judul dengan H3</h3>
<h4>Judul dengan H4</h4>
<h5>Judul dengan H5</h5>
<h6>Judul dengan H6</h6>
```

Paragraf Html
-------------

Paragraf dapat ditulis menggunakan tag <p>, apabila sebuah paragraf tidak diberi atribut align, maka defaultnya akan ditampilkan rata kiri```
<p>Html adalah bahasa markup, bukan bahasa pemrograman</p>
<p align="center">Ini adalah paragraf rata tengah</p>
<p align="right">Ini adalah paragraf rata kanan</p>
<p align="left">Ini adalah paragraf rata kiri</p>
```

### Style Teks

Berikut adalah beberapa tag yang dapat membuat suatu teks dicetak tebal, bergaris bawah, bergaris tengah, dicetak miring dsb. `<b>...</b>` Untuk membuat teks dicetak tebal `<i>...</i>` Untuk membuat teks dicetak miring `<u>...</u>` Untuk membuat teks bergaris bawah `<strike>...</b>` Untuk membuat teks bergaris tengah `<mark>...</mark>` Untuk membuat teks dengan background, sama seperti saat kita memberi stabilo pada tulisan di kertas `<strong>...</strong>` Membuat teks dicetak tebal sama seperti tag `<b>...</b>` bedanya kalau strong untuk menandai teks penting `<em>...</em>` Untuk menandai teks penting dan dicetak miring `<small>...</small>` Untuk membuat teks menjadi lebih kecil `<del>...</del>` Untuk membuat teks dicoret / bergaris tengah `<ins>...</ins>` Untuk membuat teks bergaris bawah

Komentar
--------

```
<!--ini adalah komentar, dan tidak akan ditampilkan di browser-->
```

Link
----

```
<a href="https://google.co.id">ke google</a>
```

List
----

Terdapat 2 jenis list yaitu: ordered list dan unordered list, ordered list memiliki beberapa type diantaranya sebagai berikut: type dapat diganti dengan: 1,a,A,atau i, sedangkan unordered list memiliki 3 type yaitu: round, disc atau square.

```
<ol type="A"> <!--type dapat diganti dengan: 1,a,A,atau i-->
    <li>Senin</li>
    <li>Selasa</li>
    <li>Rabu</li>
    <li>Kamis</li>
    <ul type="disc"> <!--type dapat diganti dengan: round, disc atau square-->
        <li>makan</li>
        <li>tidur</li>
    </ul>
    <li>Jumat</li>
    <li>Sabtu</li>
    <li>Minggu</li>
</ol>
```

Gambar
------

```
<img src="asset/gambar1.jpg" alt="gambar 1" title="ini adalah gambar 1" width="30%">
<img src="asset/gambar2.jpg" alt="gambar 2" title="ini adalah gambar 2" width="30%">
<img src="asset/gambar3.jpg" alt="gambar 3" title="ini adalah gambar 3" width="30%">
```src="lokasi file gambar / url gambar"

Audio
-----

```
<audio controls autoplay>
    <source src="asset/audio.mp3">
</audio>
```

contols: untuk menampilkan tombol control autoplay: agar audio langsung diputar saat dibuka di browser

Video
-----

```
<video autoplay controls>
    <source src="asset/anime.mp4">
</video>
```

contols: untuk menampilkan tombol control autoplay: agar video langsung diputar saat dibuka di browser

Table
-----

```
<table border="1" cellspacing="0" width="60%" align="center">
    <thead align="center">
        <tr>
            <th rowspan="2">Hari</th>
            <th colspan="2">Jam</th>
        </tr>
        <tr>
            <td>Pertama</td>
            <td>Kedua</td>
        </tr>
    </thead>
    <tbody align="center">
        <tr>
            <td>Senin</td>
            <td>Indonesia</td>
            <td>Matematika</td>
        </tr>
        <tr>
            <td>Selasa</td>
            <td>Indonesia</td>
            <td>Matematika</td>
        </tr>
    </tbody>
</table>
```

border = untuk mengatur tebal garis dipinggir. cellspacing = untuk mengatur jarak / margin rowspan = untuk menggabungkan kolom colspan = untuk menggabungkan baris

**Baca Juga: [Artikel Tentang Html Lainnya](/pemrograman/html)**

Form
----

Formulir digunakan untuk menginputkan data oleh user yang biasanya data tersebut nantinya akan disimpan dalam database Untuk membuat formulir kita dapat menggunakan tag form `<form>...</form>` tag form memiliki beberapa atribut didalamnya yaitu: Action, Method, Name

*   **Name**: atribut ini berfungsi untuk mengatur nama formulir
*   **Action**: untuk menentukan file atau URL tujuan di mana data inputan dari suatu form akan dikirimkan lalu proses.
*   **Method**: method adalah metode yang digunakan dalam mengirimkan data inputan, terdapat dua method yang bisa dipilih yaitu Get dan Post

```
<form action="proses.php" method="post"> <label for="nama">Nama</label> <input type="text" id="nama"><br> <label
        for="password">Password</label> <input type="password" id="password"><br> <label for="jk">Jenis Kelamin</label>
    <input type="radio" id="jk" value="L">Laki-laki <input type="radio" id="jk" value="P">Perempuan<br> <label
        for="status">Status</label> <input type="checkbox" value="Y" id="status">Mahasiswa<br> <label
        for="tanggal">Tanggal Lahir</label> <input type="date" id="tanggal"><br> <label for="jabatan">Jabatan</label>
    <select id="jabatan">
        <option value="Frontend">Frontend</option>
        <option value="Frontend">Backend</option>
        <option value="Frontend">Desainer Web</option>
    </select><br> <label for="warna"> Warna Favorit</label> <input type="color" id="warna"><br> <label for="hp">No.
        Hp</label> <input type="number" id="hp" minlength="12" maxlength="15"><br> <label for="berat"> Berat
        Badan</label> <input type="range" id="berat"><br> <label for="email">Email</label> <input type="email"
        id="email"><br> <label for="website">Website</label> <input type="url" id="website"><br> <label for="time">Jam
        Kerja</label> <input type="time" id="jam"><br> <label for="catatan"></label> <textarea id="catatan" cols="30"
        rows="5"></textarea><br> <input type="submit" value="Simpan"> <input type="reset" value="Reset"> </form>
```

### Tag Input Pada Form

Dalam formulir terdapat beberapa jenis / type input yang dapat kita gunakan, seperti:

*   **Teks**: jenis input untuk memasukkan teks biasa
*   **Number**: untuk menginputkan nomor
*   **Password**: untuk menginputkan password
*   **Email**: untuk memasukkan alamat email
*   **Url**: dapat digunakan untuk memasukkan alamat website
*   **Date**: untuk menginput tanggal
*   **Time**: untuk menginput waktu
*   **Color**: untuk menginputkan warna
*   **Button**: untuk membuat tombol
*   **Submit**: membuat tombol untuk mengirimkan inputan
*   **Reset**: membuat tombol untuk mengosongkan isi formulir
*   **Radio**: membuat opsi pilihan dan hanya bisa memilih satu pilihan
*   **Checkbock**: membuat opsi pilihan dan bisa memilih lebih dari satu pilihan

#### Atribut Tag Input

Berikut adalah beberapa atribut yang dapat kita gunakan pada tag input yaitu:

*   **Name**: memberi nama data yang dikirim
*   **Value**: memberi nilai default data yang dikirim
*   **Placeholder**: teks yang akan ditampilkan pada form input, pada saat belum ada data yang dimasukkan
*   **Size**: untuk mengatur lebar tag input
*   **Disabled**: supaya data input tidak dapat diubah
*   **Type**: menentukan type input yang akan digunakan
*   **Id**: untuk memberi identitas pada data inputan yang akan dikirim

### Tag Select

`<select>...</select>` Tag ini berfungsi untuk membuat option pilihan input yang dapat dipilih dalam bentuk dropdown contoh:```
<select id="jabatan">
    <option value="Frontend">Frontend</option>
    <option value="Frontend">Backend</option>
    <option value="Frontend">Desainer Web</option>
</select><br>
```

### Tag Text Area

`<textare>...</textarea>` untuk membuat inputan yang dapat diisi dengan banyak teks, biasanya dipakai untuk bagian alamat, komentar, pesan dan sebagainya. **Github**: [https://github.com/ajiekusumadhany/latihan\_coding/tree/main/html](https://github.com/ajiekusumadhany/latihan_coding/tree/main/html)