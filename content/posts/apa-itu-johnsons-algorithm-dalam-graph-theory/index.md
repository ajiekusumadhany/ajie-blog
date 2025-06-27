---
title: "Apa Itu Johnson’s Algorithm Dalam Graph Theory?"
date: 2025-09-13
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernah gak sih, lagi asyik main game strategi, terus bingung cara paling efisien buat kirim pasukan dari satu markas ke markas lain? Atau mungkin lagi bikin aplikasi peta, terus mikir gimana cara nyari rute tercepat antara dua lokasi? Nah, di situlah _Johnson’s Algorithm dalam Graph Theory_ berperan!

Algoritma ini bukan cuma buat game atau peta aja, lho. Banyak banget aplikasi dunia nyata yang terbantu dengan algoritma ini. Penasaran apa itu Johnson’s Algorithm dan kenapa algoritma ini penting? Yuk, kita bedah tuntas!

## Apa Itu Johnson’s Algorithm dalam Graph Theory?

Johnson’s Algorithm adalah sebuah algoritma dalam _Graph Theory_ yang digunakan untuk mencari jarak terpendek antara semua pasangan simpul (all-pairs shortest paths) dalam sebuah graf berbobot. Graf berbobot artinya setiap sisi (edge) dalam graf tersebut memiliki nilai atau "bobot" yang menunjukkan jarak atau biaya untuk melewati sisi tersebut.

Algoritma ini sangat berguna, terutama jika grafnya memiliki bobot negatif. Ingat ya, tidak semua algoritma jarak terpendek bisa menangani bobot negatif dengan baik. Di sinilah keunggulan Johnson’s Algorithm.

## Kenapa Johnson’s Algorithm Penting?

Pentingnya _Johnson’s Algorithm dalam Graph Theory_ terletak pada kemampuannya untuk mengatasi graf dengan bobot negatif, yang sering muncul dalam berbagai aplikasi praktis. Bayangkan:

- **Optimasi Rute Transportasi:** Menentukan rute terpendek untuk pengiriman barang atau perjalanan, di mana beberapa rute mungkin memiliki "diskon" (bobot negatif).
- **Analisis Jaringan Keuangan:** Mengidentifikasi peluang arbitrase (mendapatkan keuntungan dari perbedaan harga) dalam pasar keuangan, di mana transaksi dapat memiliki biaya (bobot positif) atau keuntungan (bobot negatif).
- **Perencanaan Proyek:** Menjadwalkan tugas-tugas dalam proyek, di mana beberapa tugas dapat mengurangi biaya atau waktu (bobot negatif).

Tanpa algoritma yang handal seperti Johnson’s, kita akan kesulitan mencari solusi optimal dalam situasi-situasi ini.

## Bagaimana Johnson’s Algorithm Bekerja?

Johnson’s Algorithm bekerja dengan menggabungkan dua algoritma lain yang sudah terkenal: Bellman-Ford Algorithm dan Dijkstra’s Algorithm. Secara garis besar, langkah-langkahnya adalah sebagai berikut:

### 1\. Modifikasi Graf Awal

- Tambahkan sebuah simpul (vertex) baru ke graf, sebut saja "s".
- Buat sisi (edge) dari simpul "s" ke semua simpul lain dalam graf, dengan bobot 0.
- Tujuannya adalah untuk memastikan tidak ada siklus negatif yang dapat diakses dari simpul "s".

### 2\. Gunakan Bellman-Ford Algorithm

- Jalankan Bellman-Ford Algorithm dari simpul "s" untuk mencari jarak terpendek dari "s" ke semua simpul lain.
- Jika Bellman-Ford Algorithm mendeteksi siklus negatif, maka algoritma berhenti karena graf tidak memiliki solusi jarak terpendek yang terdefinisi dengan baik.

### 3\. Re-weighting Sisi (Edges)

- Gunakan jarak yang dihitung oleh Bellman-Ford Algorithm untuk mengubah bobot setiap sisi dalam graf.
- Misalkan `h(v)` adalah jarak terpendek dari simpul "s" ke simpul `v` (dihitung oleh Bellman-Ford).
- Bobot baru untuk sisi dari `u` ke `v` (dengan bobot awal `w(u, v)`) adalah: `w'(u, v) = w(u, v) + h(u) - h(v)`.
- Tujuan dari re-weighting ini adalah untuk membuat semua bobot sisi menjadi non-negatif, sehingga kita bisa menggunakan Dijkstra’s Algorithm.

### 4\. Jalankan Dijkstra’s Algorithm

- Jalankan Dijkstra’s Algorithm dari setiap simpul dalam graf sebagai titik awal.
- Karena semua bobot sisi sekarang non-negatif, Dijkstra’s Algorithm akan memberikan jarak terpendek yang benar.

### 5\. Kembalikan Bobot Asli

- Setelah Dijkstra’s Algorithm selesai, kita perlu mengembalikan bobot asli untuk mendapatkan jarak terpendek yang sebenarnya.
- Jarak terpendek antara simpul `u` dan `v` (setelah re-weighting) adalah `d'(u, v)`.
- Jarak terpendek yang sebenarnya adalah: `d(u, v) = d'(u, v) - h(u) + h(v)`.

## Contoh Sederhana Johnson’s Algorithm

Misalkan kita punya graf dengan simpul A, B, dan C. Sisi-sisinya adalah:

- A ke B: Bobot 2
- A ke C: Bobot 5
- B ke C: Bobot -3
- C ke A: Bobot 1

1. **Tambahkan simpul S:** Kita tambahkan simpul S dengan sisi ke A, B, dan C masing-masing dengan bobot 0.
2. **Bellman-Ford dari S:** Bellman-Ford akan menghitung jarak terpendek dari S ke A, B, dan C. Misalkan hasilnya adalah: h(A) = 0, h(B) = 2, h(C) = -1.
3. **Re-weighting:** Kita hitung bobot baru untuk setiap sisi. Contoh: Bobot baru dari B ke C adalah -3 + 2 - (-1) = 0.
4. **Dijkstra:** Kita jalankan Dijkstra dari setiap simpul (A, B, dan C) dengan bobot yang sudah diubah.
5. **Kembalikan Bobot:** Setelah Dijkstra selesai, kita kembalikan bobot asli untuk mendapatkan jarak terpendek yang sebenarnya.

## Kelebihan dan Kekurangan Johnson’s Algorithm

Seperti algoritma lainnya, Johnson’s Algorithm punya kelebihan dan kekurangan:

**Kelebihan:**

- **Menangani Bobot Negatif:** Mampu menangani graf dengan bobot negatif tanpa mendeteksi siklus negatif.
- **Efisien untuk Graf Sparse:** Lebih efisien dibandingkan algoritma lain (seperti Floyd-Warshall) untuk graf yang _sparse_ (sedikit sisi).

**Kekurangan:**

- **Kompleksitas Implementasi:** Implementasinya lebih kompleks dibandingkan algoritma lain yang lebih sederhana.
- **Tidak Cocok untuk Graf Dense:** Kurang efisien dibandingkan Floyd-Warshall untuk graf yang _dense_ (banyak sisi).

## Kapan Sebaiknya Menggunakan Johnson’s Algorithm?

Gunakan Johnson’s Algorithm ketika:

- Anda perlu mencari jarak terpendek antara semua pasangan simpul.
- Graf Anda mungkin memiliki bobot negatif.
- Graf Anda relatif _sparse_.

Jika graf Anda _dense_ dan tidak memiliki bobot negatif, Floyd-Warshall mungkin menjadi pilihan yang lebih baik. Jika Anda hanya perlu mencari jarak terpendek dari satu simpul ke semua simpul lain, Dijkstra’s Algorithm (dengan modifikasi untuk menangani bobot non-negatif) mungkin lebih efisien.

## Implementasi Johnson’s Algorithm

Implementasi Johnson’s Algorithm bisa dilakukan dalam berbagai bahasa pemrograman seperti Python, Java, atau C++. Implementasinya melibatkan implementasi Bellman-Ford dan Dijkstra’s Algorithm. Banyak library dan framework yang sudah menyediakan implementasi siap pakai untuk kedua algoritma ini.

## Kesimpulan

_Johnson’s Algorithm dalam Graph Theory_ adalah alat yang ampuh untuk mencari jarak terpendek dalam graf berbobot, terutama ketika graf tersebut memiliki bobot negatif. Meskipun implementasinya sedikit kompleks, pemahaman yang baik tentang algoritma ini dapat membantu Anda memecahkan berbagai masalah optimasi rute dan jaringan dalam dunia nyata.

Punya pengalaman menggunakan Johnson’s Algorithm? Atau mungkin ada pertanyaan lain seputar algoritma ini? Jangan ragu untuk berbagi di kolom komentar!

## FAQ

**1\. Apa perbedaan utama antara Johnson’s Algorithm dan Dijkstra’s Algorithm?**

Dijkstra’s Algorithm tidak dapat menangani graf dengan bobot negatif, sedangkan Johnson’s Algorithm bisa. Johnson’s Algorithm menggunakan Dijkstra’s Algorithm sebagai bagian dari prosesnya setelah melakukan re-weighting untuk menghilangkan bobot negatif.

**2\. Kapan Floyd-Warshall Algorithm lebih baik daripada Johnson’s Algorithm?**

Floyd-Warshall Algorithm lebih baik untuk graf yang _dense_, sedangkan Johnson’s Algorithm lebih baik untuk graf yang _sparse_. Floyd-Warshall juga lebih mudah diimplementasikan.

**3\. Apakah Johnson’s Algorithm bisa mendeteksi siklus negatif?**

Ya, Johnson’s Algorithm menggunakan Bellman-Ford Algorithm yang dapat mendeteksi siklus negatif. Jika siklus negatif terdeteksi, algoritma akan berhenti karena graf tidak memiliki solusi jarak terpendek yang terdefinisi dengan baik.
