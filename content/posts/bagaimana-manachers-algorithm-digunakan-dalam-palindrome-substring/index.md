---
title: "Bagaimana Manacher’s Algorithm Digunakan Dalam Palindrome Substring?"
date: 2025-11-06
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernahkah Anda bertanya-tanya bagaimana Google atau aplikasi perpesanan favorit Anda bisa menemukan kata-kata simetris tersembunyi dalam teks secepat kilat? Bayangkan mencari "madam" atau "racecar" di antara lautan huruf. Rumit, kan? Tapi ada satu trik cerdas yang memungkinkan hal itu: Manacher's Algorithm.

Artikel ini akan membuka rahasia **Bagaimana Manacher's Algorithm Digunakan dalam Palindrome Substring** untuk menemukan potongan-potongan kata yang unik ini. Siap menjadi ahli palindrome? Mari kita mulai!

## Apa Itu Palindrome Substring?

Sebelum kita menyelami lebih dalam tentang Manacher's Algorithm, mari kita pahami dulu apa itu Palindrome Substring. Sederhananya, ini adalah bagian dari sebuah string (urutan karakter) yang jika dibaca dari depan maupun belakang, hasilnya sama.

Contoh:

- String: "bananas"
- Palindrome Substring: "anana"

Palindrome bisa ganjil (seperti "madam") atau genap (seperti "rotor"). Mencari substring palindrome ini secara efisien adalah tantangan yang menarik.

## Mengapa Manacher's Algorithm Penting?

Mencari palindrome substring bisa dilakukan dengan cara yang sederhana, tapi cara itu seringkali lambat, terutama untuk string yang panjang. Bayangkan harus memeriksa setiap kemungkinan substring satu per satu!

Manacher's Algorithm hadir sebagai solusi yang elegan dan efisien. Algoritma ini memungkinkan kita menemukan semua palindrome substring dalam waktu linear, yaitu O(n), di mana n adalah panjang string. Jauh lebih cepat dibandingkan metode brute-force yang bisa memakan waktu O(n^2) atau bahkan lebih lama.

## Memahami Manacher's Algorithm: Langkah Demi Langkah

Manacher's Algorithm bekerja dengan cerdik dengan melakukan beberapa trik untuk menghindari perhitungan ulang yang tidak perlu. Berikut adalah langkah-langkah utamanya:

### 1\. Preprocessing String

Langkah pertama adalah memodifikasi string input dengan menyisipkan karakter khusus (biasanya '#') di antara setiap karakter dan di awal serta akhir string. Tujuannya adalah untuk menyederhanakan penanganan palindrome dengan panjang ganjil dan genap.

Contoh:

- String asli: "aba"
    
- String yang diproses: "#a#b#a#"
    
- String asli: "abba"
    
- String yang diproses: "#a#b#b#a#"
    

### 2\. Array Radius (P)

Algoritma ini menggunakan array `P` untuk menyimpan radius palindrome di setiap posisi dalam string yang telah diproses. Radius palindrome adalah jarak dari pusat palindrome ke ujungnya.

Contoh, pada string "#a#b#a#", `P[3]` (posisi 'b') akan menyimpan nilai 3, karena palindrome terpanjang yang berpusat di 'b' adalah "#a#b#a#", dengan radius 3.

### 3\. Pusat (C) dan Jangkauan Kanan (R)

Dua variabel penting lainnya adalah `C` (center) dan `R` (right boundary). `C` menyimpan indeks pusat palindrome terpanjang yang telah ditemukan sejauh ini, dan `R` menyimpan jangkauan kanan palindrome tersebut.

### 4\. Iterasi dan Perhitungan Radius

Algoritma ini melakukan iterasi melalui string yang telah diproses, dan untuk setiap posisi `i`, ia menghitung `P[i]` berdasarkan nilai `P` yang sudah dihitung sebelumnya. Inilah inti dari efisiensi Manacher's Algorithm.

Jika `i` berada di dalam jangkauan palindrome terpanjang yang telah ditemukan (`i < R`), maka kita dapat memanfaatkan simetri palindrome untuk memperkirakan `P[i]`. Jika `i` berada di luar jangkauan, maka kita harus memperluas palindrome secara manual.

### 5\. Memperbarui Pusat dan Jangkauan Kanan

Setelah menghitung `P[i]`, kita periksa apakah palindrome yang berpusat di `i` melampaui jangkauan kanan `R`. Jika ya, kita memperbarui `C` dan `R` dengan nilai yang baru.

### 6\. Menemukan Palindrome Terpanjang

Setelah iterasi selesai, nilai maksimum dalam array `P` menunjukkan radius palindrome terpanjang. Kita dapat menggunakan informasi ini untuk menemukan palindrome substring terpanjang dalam string asli.

## Contoh Implementasi Manacher's Algorithm (Python)

Berikut adalah contoh sederhana implementasi Manacher's Algorithm dalam Python:

```python
def manachers_algorithm(s):
    s_processed = '#' + '#'.join(s) + '#'
    n = len(s_processed)
    P = [0] * n
    C = 0
    R = 0
    max_len = 0
    center_index = 0

    for i in range(n):
        mirror = 2 * C - i

        if i < R:
            P[i] = min(R - i, P[mirror])

        # Attempt to expand palindrome centered at i
        a = i + (1 + P[i])
        b = i - (1 + P[i])

        while a < n and b >= 0 and s_processed[a] == s_processed[b]:
            P[i] += 1
            a += 1
            b -= 1

        # If palindrome centered at i expand past R,
        # adjust center based on new palindrome.
        if i + P[i] > R:
            C = i
            R = i + P[i]

        if P[i] > max_len:
            max_len = P[i]
            center_index = i

    start = (center_index - max_len) // 2
    return s[start: start + max_len]

# Contoh penggunaan
string = "bananas"
longest_palindrome = manachers_algorithm(string)
print(f"Palindrome terpanjang dalam 'string' adalah: 'longest_palindrome'")
```

## Keunggulan Manacher's Algorithm

- **Efisiensi Waktu:** Kompleksitas waktu O(n) menjadikannya sangat cepat untuk string yang panjang.
- **Sederhana dan Elegan:** Algoritma ini relatif mudah dipahami dan diimplementasikan.
- **Menangani Palindrome Ganjil dan Genap:** Preprocessing string menyederhanakan penanganan kedua jenis palindrome.

## Penerapan Manacher's Algorithm

**Bagaimana Manacher's Algorithm Digunakan dalam Palindrome Substring**? Algoritma ini memiliki banyak penerapan praktis, termasuk:

- **Pencarian Teks:** Menemukan pola palindrome dalam dokumen atau teks.
- **Bioinformatika:** Menganalisis urutan DNA untuk menemukan struktur palindrome.
- **Kompresi Data:** Mengidentifikasi pola berulang dalam data untuk kompresi yang lebih efisien.
- **Pemrosesan Gambar:** Mendeteksi simetri dalam gambar.

## Kesimpulan

Manacher's Algorithm adalah alat yang ampuh untuk menemukan palindrome substring dalam waktu linear. Pemahaman tentang **Bagaimana Manacher's Algorithm Digunakan dalam Palindrome Substring** dapat membuka pintu ke berbagai aplikasi di berbagai bidang. Apakah Anda seorang pengembang perangkat lunak, ilmuwan data, atau hanya ingin tahu tentang algoritma cerdas, Manacher's Algorithm adalah konsep yang berharga untuk dipelajari.

Punya pengalaman menggunakan Manacher's Algorithm? Atau mungkin ada pertanyaan yang belum terjawab? Bagikan di kolom komentar!

## FAQ (Frequently Asked Questions)

**1\. Mengapa kita perlu melakukan preprocessing string sebelum menjalankan Manacher's Algorithm?**

Preprocessing string dengan menyisipkan karakter khusus '#' memungkinkan kita untuk menangani palindrome dengan panjang ganjil dan genap secara seragam. Tanpa preprocessing, kita perlu menangani kedua kasus ini secara terpisah, yang akan membuat algoritma menjadi lebih rumit.

**2\. Apa kompleksitas waktu dari Manacher's Algorithm?**

Kompleksitas waktu dari Manacher's Algorithm adalah O(n), di mana n adalah panjang string input. Ini berarti bahwa waktu yang dibutuhkan untuk menjalankan algoritma tumbuh secara linear dengan panjang string.

**3\. Bisakah Manacher's Algorithm digunakan untuk mencari semua palindrome substring, bukan hanya yang terpanjang?**

Ya, Manacher's Algorithm dapat dimodifikasi untuk mencari semua palindrome substring. Kita dapat menyimpan semua nilai `P[i]` yang dihitung selama iterasi, dan setiap nilai `P[i]` yang lebih besar dari 0 menunjukkan adanya palindrome substring dengan panjang `P[i]` yang berpusat di posisi `i`. Kita kemudian dapat menggunakan informasi ini untuk mengekstrak semua palindrome substring.
