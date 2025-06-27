---
title: "Apa Itu Convex Hull Trick Dan Bagaimana Menggunakannya?"
date: 2025-09-16
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernah gak sih ngerasa mentok pas lagi ngoding optimasi, apalagi yang berhubungan sama geometri komputasional? Kayaknya udah coba berbagai cara, tapi tetep aja gak nemu solusi yang efisien. Nah, kalau iya, mungkin kamu belum kenalan sama teknik sakti satu ini: **Convex Hull Trick (CHT)**.

Tenang, namanya emang agak intimidating, tapi sebenarnya konsepnya cukup sederhana dan super powerful buat menyelesaikan berbagai masalah optimasi. Artikel ini akan membongkar tuntas **apa itu Convex Hull Trick dan bagaimana menggunakannya** secara praktis, lengkap dengan contoh dan tips biar kamu langsung jago! Jadi, siap buat naik level kemampuan ngoding kamu? Yuk, kita mulai!

## Apa Itu Convex Hull Trick Sebenarnya?

Sederhananya, Convex Hull Trick adalah teknik optimasi yang digunakan untuk mencari nilai minimum (atau maksimum) dari serangkaian fungsi linear. Bayangkan kamu punya banyak garis lurus, dan kamu pengen tahu, di titik x tertentu, garis mana yang paling rendah (atau paling tinggi). CHT membantu kita mencari garis itu dengan sangat cepat.

Intinya, CHT memanfaatkan fakta bahwa nilai optimal selalu terletak pada _convex hull_ dari garis-garis tersebut. Convex hull sendiri adalah bentuk poligon terkecil yang mencakup semua garis. Dengan hanya menyimpan garis-garis yang membentuk convex hull, kita bisa mengabaikan garis-garis lain yang pasti tidak optimal.

## Kapan Convex Hull Trick Bisa Digunakan?

CHT sangat berguna dalam menyelesaikan masalah pemrograman dinamis (dynamic programming) yang memiliki struktur khusus. Biasanya, ini terjadi ketika persamaan rekursi kita memiliki bentuk seperti ini:

`dp[i] = min/max(a[j] * i + b[j])`

Di mana `dp[i]` adalah nilai optimal untuk state `i`, `a[j]` dan `b[j]` adalah konstanta yang bergantung pada state `j`, dan kita ingin mencari nilai minimum atau maksimum dari ekspresi `a[j] * i + b[j]` untuk semua `j`.

Jika persamaan dinamis kamu memiliki struktur seperti ini, selamat! Convex Hull Trick bisa jadi senjata ampuh untuk mempercepat algoritma kamu.

## Bagaimana Cara Mengimplementasikan Convex Hull Trick?

Implementasi CHT biasanya melibatkan struktur data seperti _deque_ (double-ended queue) untuk menyimpan garis-garis yang membentuk convex hull. Berikut adalah langkah-langkah umum untuk mengimplementasikan CHT:

1. **Sort Garis Berdasarkan Slope:** Urutkan garis-garis berdasarkan slope (koefisien `a` dalam persamaan `a*x + b`). Ini penting agar kita bisa membangun convex hull secara efisien.
    
2. **Inisialisasi Deque:** Buat sebuah deque kosong untuk menyimpan garis-garis yang membentuk convex hull.
    
3. **Iterasi Melalui Garis:** Iterasi melalui garis-garis yang sudah diurutkan. Untuk setiap garis:
    
    - **Hapus Garis Belakang yang Tidak Optimal:** Selama deque memiliki minimal dua garis, dan garis baru ini membuat garis terakhir di deque menjadi tidak optimal (yaitu, tidak berada di convex hull), hapus garis terakhir dari deque.
    - **Hapus Garis Depan yang Tidak Optimal:** Selama deque memiliki minimal dua garis, dan garis baru ini membuat garis pertama di deque menjadi tidak optimal, hapus garis pertama dari deque.
    - **Tambahkan Garis Baru ke Deque:** Tambahkan garis baru ke bagian belakang deque.
4. **Query Nilai Optimal:** Untuk mencari nilai optimal pada titik `x` tertentu, lakukan binary search pada deque untuk menemukan garis yang memberikan nilai minimum (atau maksimum) pada titik tersebut.
    

## Contoh Kode Convex Hull Trick (C++)

Berikut adalah contoh kode C++ yang menunjukkan implementasi Convex Hull Trick:

```cpp
#include <iostream>
#include <vector>
#include <deque>
#include <algorithm>

using namespace std;

// Struktur untuk merepresentasikan garis
struct Line 
    double a, b; // y = a*x + b
;

// Fungsi untuk menghitung nilai y pada titik x
double eval(Line line, double x) 
    return line.a * x + line.b;

// Fungsi untuk menentukan apakah garis ketiga (c) membuat garis kedua (b) tidak optimal
bool bad(Line a, Line b, Line c) 
    return (b.b - a.b) * (c.a - b.a) < (c.b - b.b) * (b.a - a.a);

int main() 
    int n; // Jumlah garis
    double x; // Titik x untuk query

    cout << "Masukkan jumlah garis: ";
    cin >> n;

    vector<Line> lines(n);
    cout << "Masukkan koefisien a dan b untuk setiap garis (a b):" << endl;
    for (int i = 0; i < n; ++i) 
        cin >> lines[i].a >> lines[i].b;
    

    cout << "Masukkan titik x untuk query: ";
    cin >> x;

    // Urutkan garis berdasarkan slope (koefisien a)
    sort(lines.begin(), lines.end(), [](const Line& l1, const Line& l2) 
        return l1.a < l2.a;
    );

    deque<Line> hull;

    // Bangun convex hull
    for (auto& line : lines) 
        while (hull.size() >= 2 && bad(hull[hull.size() - 2], hull.back(), line)) 
            hull.pop_back();
        
        hull.push_back(line);
    

    // Cari garis optimal pada titik x
    int l = 0, r = hull.size() - 1;
    while (l < r) 
        int mid = (l + r) / 2;
        if (eval(hull[mid], x) < eval(hull[mid + 1], x)) 
            r = mid;
         else 
            l = mid + 1;
        
    

    // Output nilai optimal
    cout << "Nilai optimal pada x = " << x << " adalah: " << eval(hull[l], x) << endl;

    return 0;
```

Kode ini menunjukkan contoh sederhana bagaimana CHT dapat digunakan untuk mencari nilai minimum dari serangkaian garis pada titik `x` tertentu. Perhatikan bahwa kode ini mengasumsikan bahwa slope garis sudah terurut.

## Tips dan Trik Menggunakan Convex Hull Trick

- **Pahami Konsep Geometri:** Memahami konsep convex hull dan bagaimana garis-garis berinteraksi akan sangat membantu dalam memahami dan mengimplementasikan CHT.
- **Hati-hati dengan Kasus Edge:** Pastikan untuk menangani kasus edge dengan benar, seperti ketika deque kosong atau hanya memiliki satu garis.
- **Perhatikan Tipe Data:** Gunakan tipe data yang sesuai untuk menghindari overflow atau underflow, terutama saat menghitung perkalian dan pembagian.
- **Debugging dengan Visualisasi:** Jika kamu kesulitan memahami bagaimana CHT bekerja, coba visualisasikan garis-garis dan convex hull-nya. Ini bisa sangat membantu dalam menemukan bug.
- **Latihan Soal:** Cara terbaik untuk menguasai CHT adalah dengan berlatih menyelesaikan soal-soal yang melibatkan teknik ini. Banyak platform online seperti Codeforces, AtCoder, dan LeetCode menyediakan soal-soal CHT.

## Contoh Soal Convex Hull Trick

Salah satu contoh soal klasik yang bisa diselesaikan dengan CHT adalah masalah _Convex Hull Trick Dynamic Programming_. Intinya, soal ini meminta kita untuk menghitung nilai `dp[i]` berdasarkan nilai `dp[j]` sebelumnya, dengan persamaan rekursi yang memiliki struktur `dp[i] = min(dp[j] + a[j] * i + b[j])`. Dengan menggunakan CHT, kita bisa menghitung nilai `dp[i]` secara efisien tanpa harus mengiterasi semua nilai `j`.

## Kesimpulan

Convex Hull Trick adalah teknik optimasi yang powerful dan sangat berguna dalam menyelesaikan masalah pemrograman dinamis dengan struktur khusus. Meskipun konsepnya mungkin terlihat rumit pada awalnya, dengan pemahaman yang baik dan latihan yang cukup, kamu akan bisa menguasai teknik ini dan menggunakannya untuk menyelesaikan berbagai masalah optimasi yang menantang. Gimana, tertarik buat coba? Jangan ragu untuk eksperimen dan berbagi pengalaman kamu di kolom komentar!

## FAQ (Frequently Asked Questions)

**1\. Apakah Convex Hull Trick hanya bisa digunakan untuk mencari nilai minimum?**

Tidak, CHT juga bisa digunakan untuk mencari nilai maksimum. Perbedaannya hanya terletak pada bagaimana kita membandingkan garis-garis dan bagaimana kita membangun convex hull.

**2\. Apakah Convex Hull Trick selalu lebih cepat daripada solusi brute force?**

Tidak selalu. CHT hanya lebih cepat jika jumlah garis yang perlu dipertimbangkan cukup besar. Jika jumlah garisnya kecil, solusi brute force mungkin lebih cepat karena overhead implementasi CHT.

**3\. Apakah ada alternatif lain selain deque untuk mengimplementasikan Convex Hull Trick?**

Ya, ada beberapa alternatif lain, seperti menggunakan balanced binary search tree (misalnya, `std::set` di C++) untuk menyimpan garis-garis. Namun, deque biasanya lebih efisien dan lebih mudah diimplementasikan.
