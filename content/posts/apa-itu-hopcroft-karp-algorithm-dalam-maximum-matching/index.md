---
title: "Apa Itu Hopcroft-Karp Algorithm Dalam Maximum Matching?"
date: 2025-09-29
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernahkah Anda membayangkan bagaimana Google mencocokkan miliaran pencarian dengan halaman web yang paling relevan dalam hitungan detik? Atau bagaimana aplikasi kencan mencocokkan Anda dengan orang yang paling mungkin menjadi pasangan ideal? Di balik layar, seringkali ada algoritma cerdas yang bekerja keras, salah satunya adalah **Hopcroft-Karp Algorithm** yang sangat efisien dalam menyelesaikan masalah **maximum matching**.

Penasaran apa itu **Hopcroft-Karp Algorithm** dan bagaimana ia berperan penting dalam menemukan **maximum matching**? Mari kita bedah algoritma ini secara mendalam!

## Apa Itu Maximum Matching?

Sebelum membahas **Hopcroft-Karp Algorithm**, kita perlu memahami dulu apa itu **maximum matching**. Bayangkan Anda memiliki dua kelompok orang: laki-laki dan perempuan. Tujuan Anda adalah memasangkan sebanyak mungkin laki-laki dan perempuan sehingga setiap orang hanya dipasangkan dengan satu orang. Ini adalah contoh sederhana dari masalah **maximum matching** dalam graf bipartite.

Secara formal, **maximum matching** dalam graf bipartite adalah himpunan tepi (pasangan) terbesar yang tidak berbagi simpul (orang). Dengan kata lain, kita ingin menemukan sebanyak mungkin pasangan yang mungkin tanpa ada orang yang berpacaran dengan lebih dari satu orang.

## Apa Itu Hopcroft-Karp Algorithm dalam Maximum Matching?

**Hopcroft-Karp Algorithm** adalah algoritma yang efisien untuk menemukan **maximum matching** dalam graf bipartite. Algoritma ini dikembangkan oleh John Hopcroft dan Richard Karp pada tahun 1973. Keunggulan utama algoritma ini adalah kompleksitas waktunya yang relatif rendah, yaitu O(E√V), di mana E adalah jumlah tepi dan V adalah jumlah simpul dalam graf.

Algoritma ini bekerja dengan mencari jalur augmentasi (augmenting path) secara berulang. Jalur augmentasi adalah jalur dalam graf bipartite yang dimulai dari simpul yang belum dipasangkan, berakhir di simpul yang belum dipasangkan, dan bergantian antara tepi yang tidak termasuk dalam matching dan tepi yang termasuk dalam matching.

## Bagaimana Cara Kerja Hopcroft-Karp Algorithm?

Secara garis besar, **Hopcroft-Karp Algorithm** bekerja dalam beberapa langkah:

1. **Inisialisasi:** Mulai dengan matching kosong. Artinya, belum ada simpul yang dipasangkan.
2. **Pencarian BFS:** Gunakan Breadth-First Search (BFS) untuk mencari jalur augmentasi terpendek. BFS dimulai dari semua simpul yang belum dipasangkan di satu sisi graf bipartite (misalnya, laki-laki).
3. **Pencarian DFS:** Jika BFS menemukan jalur augmentasi, gunakan Depth-First Search (DFS) untuk menelusuri jalur tersebut dan memperbarui matching.
4. **Iterasi:** Ulangi langkah 2 dan 3 sampai tidak ada lagi jalur augmentasi yang ditemukan.

Mari kita bedah setiap langkah lebih detail:

### 1\. Inisialisasi

Pada tahap ini, kita memulai dengan matching yang kosong. Ini berarti tidak ada tepi yang termasuk dalam matching kita. Semua simpul dianggap belum dipasangkan.

### 2\. Pencarian BFS (Breadth-First Search)

BFS digunakan untuk menemukan set jalur augmentasi terpendek secara bersamaan. BFS dimulai dari semua simpul yang belum dipasangkan di satu sisi graf bipartite (misalnya, laki-laki).

- **Level:** Setiap simpul dalam BFS diberi level. Simpul yang belum dipasangkan di sisi laki-laki memiliki level 0.
- **Alternasi Tepi:** BFS menelusuri graf secara bergantian antara tepi yang tidak termasuk dalam matching (tepi bebas) dan tepi yang termasuk dalam matching (tepi yang dipasangkan).
- **Jalur Augmentasi:** BFS berhenti ketika menemukan simpul yang belum dipasangkan di sisi perempuan. Jalur dari simpul awal (laki-laki yang belum dipasangkan) ke simpul akhir (perempuan yang belum dipasangkan) melalui BFS adalah jalur augmentasi.
- **Blocking Set:** BFS tidak hanya menemukan satu jalur augmentasi, tetapi juga menemukan set jalur augmentasi terpendek yang saling disjoint (tidak berbagi simpul). Set ini disebut "blocking set".

### 3\. Pencarian DFS (Depth-First Search)

Setelah BFS menemukan blocking set jalur augmentasi, kita menggunakan DFS untuk menelusuri setiap jalur dalam blocking set dan memperbarui matching.

- **Perbarui Matching:** Untuk setiap jalur augmentasi, kita membalik status tepi di sepanjang jalur tersebut. Tepi yang sebelumnya tidak termasuk dalam matching sekarang termasuk dalam matching, dan sebaliknya. Ini secara efektif meningkatkan ukuran matching dengan satu.
- **Blocking Set Processing:** DFS memproses semua jalur augmentasi dalam blocking set yang ditemukan oleh BFS.

### 4\. Iterasi

Kita ulangi langkah 2 dan 3 sampai BFS tidak lagi menemukan jalur augmentasi. Ketika tidak ada lagi jalur augmentasi yang ditemukan, matching saat ini adalah **maximum matching**.

## Contoh Sederhana Hopcroft-Karp Algorithm

Mari kita ilustrasikan **Hopcroft-Karp Algorithm** dengan contoh sederhana. Misalkan kita memiliki graf bipartite dengan 4 laki-laki (L1, L2, L3, L4) dan 4 perempuan (P1, P2, P3, P4). Tepinya adalah sebagai berikut:

- L1 terhubung ke P1 dan P2
- L2 terhubung ke P2 dan P3
- L3 terhubung ke P3 dan P4
- L4 terhubung ke P4

1. **Inisialisasi:** Matching kosong.
2. **BFS:** BFS dimulai dari L1, L2, L3, dan L4 (semua belum dipasangkan). BFS menemukan jalur augmentasi:
    - L1 -> P1 (belum dipasangkan)
    - L2 -> P2 (belum dipasangkan)
    - L3 -> P3 (belum dipasangkan)
    - L4 -> P4 (belum dipasangkan)
3. **DFS:** DFS menelusuri setiap jalur dan memperbarui matching:
    - L1 dipasangkan dengan P1
    - L2 dipasangkan dengan P2
    - L3 dipasangkan dengan P3
    - L4 dipasangkan dengan P4
4. **Iterasi:** BFS tidak lagi menemukan jalur augmentasi karena semua simpul sudah dipasangkan.

Hasilnya adalah **maximum matching** di mana setiap laki-laki dipasangkan dengan satu perempuan.

## Kelebihan dan Kekurangan Hopcroft-Karp Algorithm

**Kelebihan:**

- **Efisiensi:** Kompleksitas waktu O(E√V) membuatnya efisien untuk graf bipartite yang besar.
- **Implementasi:** Algoritma ini relatif mudah diimplementasikan.

**Kekurangan:**

- **Hanya untuk Graf Bipartite:** Algoritma ini hanya berfungsi untuk graf bipartite.
- **Kompleksitas:** Meskipun efisien, kompleksitasnya masih bisa menjadi masalah untuk graf yang sangat besar.

## Penerapan Hopcroft-Karp Algorithm dalam Dunia Nyata

**Hopcroft-Karp Algorithm** memiliki banyak penerapan dalam dunia nyata, di antaranya:

- **Pencocokan Pekerjaan:** Mencocokkan pelamar kerja dengan lowongan pekerjaan yang sesuai.
- **Penugasan Sumber Daya:** Menugaskan sumber daya (misalnya, server) ke tugas yang membutuhkan sumber daya tersebut.
- **Rekomendasi:** Mencocokkan pengguna dengan item yang mungkin mereka sukai (misalnya, film, musik, produk).
- **Jaringan Komputer:** Alokasi bandwidth dalam jaringan komputer.
- **Bioinformatika:** Mencocokkan sekuens DNA.

## Perbandingan dengan Algoritma Lain

Ada beberapa algoritma lain yang dapat digunakan untuk menemukan **maximum matching** dalam graf bipartite, seperti Ford-Fulkerson algorithm. Namun, **Hopcroft-Karp Algorithm** seringkali lebih efisien daripada algoritma lain, terutama untuk graf yang besar dan padat.

## Kesimpulan

**Hopcroft-Karp Algorithm** adalah alat yang ampuh untuk menyelesaikan masalah **maximum matching** dalam graf bipartite. Dengan kompleksitas waktu yang efisien dan implementasi yang relatif mudah, algoritma ini banyak digunakan dalam berbagai aplikasi di dunia nyata. Apakah Anda pernah menggunakan aplikasi yang memanfaatkan algoritma ini tanpa Anda sadari? Bagikan pengalaman Anda di kolom komentar!

## FAQ (Frequently Asked Questions)

**1\. Apa perbedaan antara matching dan maximum matching?**

Matching adalah himpunan tepi di mana tidak ada dua tepi yang berbagi simpul. Maximum matching adalah matching dengan ukuran terbesar yang mungkin.

**2\. Bisakah Hopcroft-Karp Algorithm digunakan untuk graf non-bipartite?**

Tidak, **Hopcroft-Karp Algorithm** dirancang khusus untuk graf bipartite. Untuk graf non-bipartite, Anda perlu menggunakan algoritma yang berbeda, seperti Blossom Algorithm.

**3\. Bagaimana cara mengimplementasikan Hopcroft-Karp Algorithm?**

Anda dapat menemukan implementasi **Hopcroft-Karp Algorithm** dalam berbagai bahasa pemrograman seperti Python, Java, dan C++ di internet. Pastikan untuk memahami kode tersebut sebelum menggunakannya.
