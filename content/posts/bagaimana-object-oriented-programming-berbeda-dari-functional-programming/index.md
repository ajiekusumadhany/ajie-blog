---
title: "Bagaimana Object-Oriented Programming Berbeda Dari Functional Programming?"
date: 2025-08-28
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernah bingung kenapa ada dua kubu programmer yang selalu debat soal gaya penulisan kode? Satu kubu cinta mati sama OOP, yang lain setia banget sama Functional Programming. Kira-kira, apa sih yang bikin mereka beda pendapat?

Nah, di artikel ini, kita bakal kupas tuntas **bagaimana Object-Oriented Programming berbeda dari Functional Programming**. Gak cuma teori, tapi juga contoh-contoh praktis biar kamu beneran paham perbedaannya. Jadi, siap jadi lebih jago ngoding? Yuk, lanjut!

## Landasan Filosofis: Dunia Objek vs. Dunia Fungsi

Perbedaan mendasar antara Object-Oriented Programming (OOP) dan Functional Programming (FP) terletak pada cara mereka memandang masalah dan menyusun kode. OOP fokus pada _objek_, sementara FP berpusat pada _fungsi_.

### Object-Oriented Programming (OOP): Segalanya Adalah Objek

Di dunia OOP, segala sesuatu direpresentasikan sebagai objek. Objek ini punya _state_ (data atau atribut) dan _behavior_ (metode atau fungsi yang bisa dilakukan objek). Konsep utama dalam OOP meliputi:

- **Encapsulation (Pengkapsulan):** Menggabungkan data dan metode yang beroperasi pada data tersebut dalam satu unit (objek). Ini melindungi data dari akses langsung dari luar.
- **Inheritance (Pewarisan):** Memungkinkan objek untuk mewarisi sifat dan perilaku dari objek lain (kelas induk). Ini mempromosikan penggunaan kembali kode.
- **Polymorphism (Polimorfisme):** Memungkinkan objek dari kelas yang berbeda untuk merespon panggilan metode yang sama dengan cara yang berbeda. Ini meningkatkan fleksibilitas kode.
- **Abstraction (Abstraksi):** Menyembunyikan detail implementasi yang kompleks dan hanya menampilkan informasi yang relevan. Ini menyederhanakan penggunaan objek.

Intinya, OOP mencoba memodelkan dunia nyata dengan objek-objek yang berinteraksi satu sama lain.

### Functional Programming (FP): Fungsi Murni dan Immutability

Functional Programming (FP), di sisi lain, menekankan penggunaan _fungsi murni_. Fungsi murni adalah fungsi yang:

- Selalu menghasilkan output yang sama untuk input yang sama.
- Tidak memiliki _side effects_ (tidak mengubah state di luar fungsi itu sendiri).

Konsep utama dalam FP meliputi:

- **Immutability (Tidak Berubah):** Data tidak dapat diubah setelah dibuat. Jika perlu mengubah data, kita membuat salinan baru.
- **First-Class Functions:** Fungsi dapat diperlakukan seperti variabel lain. Kita bisa mengirim fungsi sebagai argumen ke fungsi lain, mengembalikan fungsi dari fungsi lain, dan menyimpan fungsi dalam variabel.
- **Higher-Order Functions:** Fungsi yang menerima fungsi lain sebagai argumen atau mengembalikan fungsi sebagai hasilnya.
- **Recursion (Rekursi):** Fungsi memanggil dirinya sendiri untuk memecahkan masalah yang lebih kecil.

FP berfokus pada _what_ (apa yang ingin dicapai) daripada _how_ (bagaimana cara mencapainya). FP menghindari state yang dapat berubah dan side effects, sehingga kode lebih mudah dipahami, diuji, dan diparalelkan.

## Perbedaan Utama dalam Praktik

Selain filosofi dasarnya, OOP dan FP juga berbeda dalam implementasi dan penggunaan sehari-hari.

### State dan Mutability

Ini mungkin perbedaan paling mendasar. Dalam OOP, objek memiliki _state_ yang bisa berubah seiring waktu. Misalnya, objek `Mobil` bisa punya atribut `kecepatan` yang berubah saat mobil berjalan.

Dalam FP, _immutability_ adalah kunci. Data tidak boleh diubah. Jika kita ingin mengubah data, kita harus membuat salinan baru. Ini menghindari masalah _side effects_ dan membuat kode lebih mudah diprediksi.

### Side Effects

_Side effects_ adalah perubahan state di luar fungsi. Contoh _side effects_ termasuk mencetak ke konsol, menulis ke file, atau mengubah variabel global.

OOP seringkali bergantung pada _side effects_ untuk berinteraksi dengan dunia luar. Misalnya, metode `rem()` pada objek `BankAccount` akan mengubah saldo akun.

FP berusaha menghindari _side effects_ sebanyak mungkin. Fungsi murni hanya menghasilkan output berdasarkan inputnya dan tidak melakukan perubahan di luar dirinya sendiri.

### Data dan Behavior

Dalam OOP, data dan behavior (metode) digabungkan dalam objek. Objek bertanggung jawab untuk mengelola datanya sendiri.

Dalam FP, data dan behavior dipisahkan. Data seringkali direpresentasikan sebagai struktur data sederhana (seperti list atau tuple), dan behavior diimplementasikan sebagai fungsi yang beroperasi pada data tersebut.

### Control Flow

OOP seringkali menggunakan _imperative programming_, di mana kita secara eksplisit menentukan langkah-langkah yang harus dilakukan program.

FP lebih cenderung menggunakan _declarative programming_, di mana kita mendeskripsikan _what_ yang ingin kita capai, dan compiler atau interpreter yang menentukan _how_ cara mencapainya. Ini seringkali melibatkan penggunaan fungsi _higher-order_ seperti `map`, `filter`, dan `reduce`.

## Contoh Sederhana: Menghitung Luas Lingkaran

Mari kita lihat contoh sederhana untuk mengilustrasikan perbedaan antara OOP dan FP. Kita akan menghitung luas lingkaran.

### OOP (Python)

```python
class Lingkaran:
    def __init__(self, radius):
        self.radius = radius

    def hitung_luas(self):
        return 3.14 * self.radius * self.radius

lingkaran = Lingkaran(5)
luas = lingkaran.hitung_luas()
print(f"Luas lingkaran: luas")
```

Dalam contoh OOP ini, kita membuat kelas `Lingkaran` yang memiliki atribut `radius` dan metode `hitung_luas`.

### FP (Python)

```python
def hitung_luas_lingkaran(radius):
    return 3.14 * radius * radius

radius = 5
luas = hitung_luas_lingkaran(radius)
print(f"Luas lingkaran: luas")
```

Dalam contoh FP ini, kita membuat fungsi `hitung_luas_lingkaran` yang menerima `radius` sebagai argumen dan mengembalikan luas lingkaran. Tidak ada objek yang terlibat.

## Kapan Menggunakan OOP dan Kapan Menggunakan FP?

Tidak ada jawaban tunggal untuk pertanyaan ini. Pilihan antara OOP dan FP tergantung pada jenis masalah yang ingin dipecahkan, preferensi pribadi, dan budaya tim.

**OOP cocok untuk:**

- Aplikasi dengan banyak objek yang berinteraksi satu sama lain.
- Proyek yang membutuhkan penggunaan kembali kode yang ekstensif (melalui pewarisan).
- Aplikasi yang memodelkan dunia nyata.

**FP cocok untuk:**

- Aplikasi yang berfokus pada transformasi data.
- Proyek yang membutuhkan kode yang mudah diuji dan diparalelkan.
- Aplikasi yang memerlukan kejelasan dan prediktabilitas.
- Kasus dimana _side effects_ harus diminimalkan.

Seringkali, pendekatan terbaik adalah menggunakan kombinasi OOP dan FP. Misalnya, kita bisa menggunakan OOP untuk struktur aplikasi secara keseluruhan, dan FP untuk implementasi logika bisnis yang kompleks.

## Kesimpulan

Jadi, **bagaimana Object-Oriented Programming berbeda dari Functional Programming?** Perbedaan utamanya terletak pada filosofi, cara menangani state, dan organisasi kode. OOP berfokus pada objek dengan state yang bisa berubah, sementara FP berfokus pada fungsi murni dan immutability.

Meskipun ada perbedaan yang signifikan, baik OOP maupun FP memiliki kelebihan dan kekurangan masing-masing. Pilihan terbaik tergantung pada konteks proyek dan preferensi pengembang. Bagaimana pengalamanmu dengan OOP dan FP? Mari berbagi di kolom komentar!

## FAQ

**1\. Apakah OOP lebih baik dari FP, atau sebaliknya?**

Tidak ada yang lebih baik secara absolut. Keduanya memiliki kelebihan dan kekurangan masing-masing. Pilihan terbaik tergantung pada jenis masalah yang ingin dipecahkan dan preferensi pribadi.

**2\. Bisakah saya menggunakan OOP dan FP secara bersamaan?**

Tentu saja! Banyak bahasa pemrograman modern (seperti Python, Java, dan JavaScript) mendukung paradigma OOP dan FP. Kita bisa menggunakan kombinasi keduanya untuk mendapatkan yang terbaik dari kedua dunia.

**3\. Apakah sulit mempelajari Functional Programming jika saya sudah terbiasa dengan Object-Oriented Programming?**

Awalnya mungkin terasa sedikit aneh, karena FP memiliki cara berpikir yang berbeda. Namun, dengan latihan dan pemahaman konsep dasar, kamu pasti bisa menguasainya. Ada banyak sumber daya online yang tersedia untuk membantu kamu belajar FP.
