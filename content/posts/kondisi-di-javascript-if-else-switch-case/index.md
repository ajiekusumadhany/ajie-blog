---
title: "Kondisi di JavaScript: If-Else, Switch-Case, dan Nested If-Else"
date: 2023-03-26
categories: 
  - "javascript"
---

Dalam pemrograman, kondisi adalah salah satu fitur yang sangat penting. Kondisi memungkinkan kita untuk mengeksekusi blok kode tertentu jika kondisi tertentu terpenuhi.

## Kondisi di JavaScript

Pada bahasa pemrograman JavaScript, terdapat dua jenis kondisi utama yaitu if-else dan switch-case.

## 1\. If-else

If-else adalah jenis kondisi yang paling dasar pada JavaScript. Kondisi ini digunakan untuk mengeksekusi blok kode tertentu jika kondisi yang diberikan bernilai benar (true).

Berikut ini adalah contoh penggunaan if-else pada JavaScript:

```
let x = 10;

if (x > 5) {
  console.log("x lebih besar dari 5");
} else {
  console.log("x kurang dari atau sama dengan 5");
}

```

Pada contoh di atas, kita menggunakan if-else untuk mengecek apakah nilai variabel x lebih besar dari 5. Jika iya, maka kita akan mencetak pesan "x lebih besar dari 5".

Namun, jika kondisi tersebut tidak terpenuhi, maka blok kode yang akan dijalankan adalah yang berada pada else.

## 2\. Nested If\_Else

Selain menggunakan if-else secara sederhana seperti di atas, kita juga bisa menggunakan nested if-else.

Nested if-else adalah kondisi yang terdiri dari beberapa if-else yang bersarang di dalam satu sama lain.

Berikut ini adalah contoh penggunaan nested if-else pada JavaScript:

```
let x = 10;
let y = 20;

if (x > 5) {
  if (y > 10) {
    console.log("x lebih besar dari 5 dan y lebih besar dari 10");
  } else {
    console.log("x lebih besar dari 5 dan y kurang dari atau sama dengan 10");
  }
} else {
  console.log("x kurang dari atau sama dengan 5");
}

```

Pada contoh di atas, kita menggunakan nested if-else untuk mengecek apakah nilai variabel x lebih besar dari 5 dan nilai variabel y lebih besar dari 10.  Jika iya, maka kita akan mencetak pesan "x lebih besar dari 5 dan y lebih besar dari 10".

Namun, jika kondisi tersebut tidak terpenuhi, maka kita akan memeriksa kondisi lain hingga kita menemukan blok kode yang tepat untuk dijalankan.

### 3\. Switch-case

Switch-case adalah jenis kondisi lain yang bisa kita gunakan pada JavaScript. Kondisi ini digunakan untuk mengeksekusi blok kode tertentu berdasarkan nilai variabel tertentu.

Berikut ini adalah contoh penggunaan switch-case pada JavaScript:

```
let day = "Senin";

switch (day) {
  case "Senin":
    console.log("Hari ini adalah hari Senin");
    break;
  case "Selasa":
    console.log("Hari ini adalah hari Selasa");
    break;
  case "Rabu":
    console.log("Hari ini adalah hari Rabu");
    break;
  default:
    console.log("Hari tidak dikenal");
}

```

Pada contoh di atas, kita menggunakan switch-case untuk mengecek nilai variabel day. Jika nilai variabel day adalah "Senin", maka blok kode yang dijalankan adalah yang berada pada case "Senin".

Jika nilai variabel day adalah "Selasa", maka blok kode yang dijalankan adalah yang berada pada case "Selasa", dan seterusnya.

Jika nilai variabel day tidak sama dengan semua case yang diberikan, maka blok kode yang dijalankan adalah yang berada pada default.

Selain itu, pada switch-case kita juga bisa menggunakan kata kunci "break" untuk keluar dari kondisi switch-case.

Kata kunci "break" akan menghentikan eksekusi blok kode pada switch-case dan melanjutkan eksekusi kode di bawahnya.

Berikut ini adalah contoh penggunaan kata kunci "break" pada switch-case:

```
let day = "Senin";

switch (day) {
  case "Senin":
    console.log("Hari ini adalah hari Senin");
    break;
  case "Selasa":
    console.log("Hari ini adalah hari Selasa");
    break;
  case "Rabu":
    console.log("Hari ini adalah hari Rabu");
    break;
  default:
    console.log("Hari tidak dikenal");
}

console.log("Ini adalah kode di luar switch-case");

```

Pada contoh di atas, setelah eksekusi switch-case selesai, kode di bawahnya akan dieksekusi karena kita sudah menggunakan kata kunci "break" pada setiap case.

## Kesimpulan

Dalam artikel ini, kita telah membahas tentang dua jenis kondisi pada JavaScript yaitu if-else dan switch-case.

If-else digunakan untuk mengeksekusi blok kode tertentu jika kondisi yang diberikan bernilai benar atau salah,

sedangkan switch-case digunakan untuk mengeksekusi blok kode tertentu berdasarkan nilai variabel tertentu.

Selain itu, kita juga bisa menggunakan nested if-else dan kata kunci "break" pada switch-case untuk mengatur eksekusi kode pada kondisi tertentu.

Kondisi pada JavaScript sangat penting dalam pembuatan program. Dengan memahami kondisi pada JavaScript, kita dapat mengembangkan program dengan lebih efektif dan efisien.

Semoga artikel ini bermanfaat bagi Anda dalam memahami kondisi pada JavaScript.

**Baca Juga**: [Menguasai Konsep dan Teknik Looping pada Javascript](https://ajiekusumadhany.com/konsep-dan-teknik-looping-pada-javascript/)
