---
title: "Bagaimana Cara Kerja Depth-First Search Dan Breadth-First Search?"
date: 2025-08-16
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernahkah kamu merasa tersesat di labirin informasi dan bingung bagaimana menemukan jalan keluar? Nah, dalam dunia algoritma, ada dua cara populer untuk menjelajahi data: **Depth-First Search (DFS)** dan **Breadth-First Search (BFS)**. Keduanya bagaikan kompas yang membantumu menavigasi struktur data kompleks.

Artikel ini akan membongkar **bagaimana cara kerja Depth-First Search dan Breadth-First Search**, menjelaskan perbedaan utama, kelebihan, kekurangan, dan kapan sebaiknya menggunakan masing-masing. Siap menjelajah? Yuk, mulai!

## Depth-First Search (DFS): Menjelajahi Lebih Dalam

**Depth-First Search (DFS)** adalah algoritma pencarian graf atau pohon yang menjelajahi sepanjang setiap cabang sedalam mungkin sebelum melakukan backtracking. Bayangkan dirimu sedang menjelajahi hutan belantara. Kamu memilih satu jalur dan terus menyusurinya sampai mentok. Jika mentok, barulah kamu kembali dan mencoba jalur lain dari persimpangan terakhir. Itulah inti dari DFS.

### Bagaimana Cara Kerja Depth-First Search?

DFS bekerja dengan menggunakan stack (tumpukan) untuk melacak simpul-simpul yang belum dikunjungi. Berikut langkah-langkahnya:

1. Mulai dari simpul awal (root).
2. Tandai simpul tersebut sebagai "dikunjungi."
3. Dorong (push) simpul tersebut ke dalam stack.
4. Selama stack tidak kosong:
    - Ambil (pop) simpul teratas dari stack.
    - Periksa semua tetangga (neighbor) dari simpul tersebut.
    - Jika ada tetangga yang belum dikunjungi:
        - Tandai tetangga tersebut sebagai "dikunjungi."
        - Dorong tetangga tersebut ke dalam stack.
5. Jika stack kosong, berarti semua simpul yang dapat dijangkau dari simpul awal telah dikunjungi.

### Contoh Sederhana Depth-First Search

Misalnya, kita punya graf sederhana dengan simpul A, B, C, D, dan E. Kita mulai dari simpul A.

1. Mulai dari A, tandai A sebagai dikunjungi, push A ke stack.
2. Pop A dari stack. Tetangga A adalah B dan C. Kita pilih B (misalnya).
3. Tandai B sebagai dikunjungi, push B ke stack.
4. Pop B dari stack. Tetangga B adalah D.
5. Tandai D sebagai dikunjungi, push D ke stack.
6. Pop D dari stack. D tidak punya tetangga yang belum dikunjungi.
7. Kembali ke A (karena A masih memiliki tetangga yang belum dikunjungi).
8. Pilih C (tetangga A yang belum dikunjungi).
9. Tandai C sebagai dikunjungi, push C ke stack.
10. Pop C dari stack. Tetangga C adalah E.
11. Tandai E sebagai dikunjungi, push E ke stack.
12. Pop E dari stack. E tidak punya tetangga yang belum dikunjungi.
13. Stack kosong. Selesai.

Urutan kunjungan dalam contoh ini adalah: A, B, D, C, E.

### Kelebihan dan Kekurangan Depth-First Search

**Kelebihan:**

- Membutuhkan memori yang lebih sedikit dibandingkan BFS, terutama untuk graf yang sangat lebar.
- Dapat menemukan solusi lebih cepat jika solusi berada di kedalaman tertentu dari graf.
- Mudah diimplementasikan secara rekursif.

**Kekurangan:**

- Bisa terjebak dalam cabang tak terbatas jika graf memiliki siklus (loop).
- Tidak menjamin menemukan jalur terpendek.

## Breadth-First Search (BFS): Menjelajahi Secara Luas

**Breadth-First Search (BFS)** adalah algoritma pencarian graf atau pohon yang menjelajahi semua simpul di tingkat yang sama sebelum bergerak ke tingkat berikutnya. Bayangkan kamu melempar batu ke kolam. Gelombang menyebar ke segala arah secara merata. BFS bekerja dengan cara yang mirip.

### Bagaimana Cara Kerja Breadth-First Search?

BFS menggunakan queue (antrian) untuk melacak simpul-simpul yang belum dikunjungi. Berikut langkah-langkahnya:

1. Mulai dari simpul awal (root).
2. Tandai simpul tersebut sebagai "dikunjungi."
3. Masukkan (enqueue) simpul tersebut ke dalam queue.
4. Selama queue tidak kosong:
    - Ambil (dequeue) simpul terdepan dari queue.
    - Periksa semua tetangga (neighbor) dari simpul tersebut.
    - Jika ada tetangga yang belum dikunjungi:
        - Tandai tetangga tersebut sebagai "dikunjungi."
        - Masukkan tetangga tersebut ke dalam queue.
5. Jika queue kosong, berarti semua simpul yang dapat dijangkau dari simpul awal telah dikunjungi.

### Contoh Sederhana Breadth-First Search

Menggunakan graf yang sama dengan contoh DFS (simpul A, B, C, D, dan E, mulai dari A):

1. Mulai dari A, tandai A sebagai dikunjungi, enqueue A ke queue.
2. Dequeue A. Tetangga A adalah B dan C.
3. Tandai B dan C sebagai dikunjungi, enqueue B dan C ke queue.
4. Dequeue B. Tetangga B adalah D.
5. Tandai D sebagai dikunjungi, enqueue D ke queue.
6. Dequeue C. Tetangga C adalah E.
7. Tandai E sebagai dikunjungi, enqueue E ke queue.
8. Dequeue D. D tidak punya tetangga yang belum dikunjungi.
9. Dequeue E. E tidak punya tetangga yang belum dikunjungi.
10. Queue kosong. Selesai.

Urutan kunjungan dalam contoh ini adalah: A, B, C, D, E.

### Kelebihan dan Kekurangan Breadth-First Search

**Kelebihan:**

- Menjamin menemukan jalur terpendek antara dua simpul.
- Cocok untuk mencari solusi yang dekat dengan simpul awal.
- Tidak rentan terjebak dalam cabang tak terbatas.

**Kekurangan:**

- Membutuhkan memori yang lebih besar dibandingkan DFS, terutama untuk graf yang sangat lebar.
- Bisa lebih lambat dibandingkan DFS jika solusi berada di kedalaman tertentu dari graf.

## Kapan Menggunakan DFS dan BFS?

Pemilihan antara DFS dan BFS tergantung pada masalah yang ingin dipecahkan dan karakteristik graf.

- **Gunakan DFS jika:**
    - Kamu ingin mencari solusi yang berada di kedalaman tertentu dari graf.
    - Memori adalah batasan utama.
    - Kamu tidak perlu menemukan jalur terpendek.
    - Contoh: Mencari siklus dalam graf, topological sorting.
- **Gunakan BFS jika:**
    - Kamu ingin menemukan jalur terpendek antara dua simpul.
    - Solusi diharapkan berada dekat dengan simpul awal.
    - Memori bukan masalah utama.
    - Contoh: Mencari jalur terpendek dalam peta, crawling web.

## Perbedaan Utama Antara DFS dan BFS

| Fitur | Depth-First Search (DFS) | Breadth-First Search (BFS) |
| --- | --- | --- |
| Struktur Data | Stack | Queue |
| Pencarian | Vertikal | Horizontal |
| Jalur Terpendek | Tidak dijamin | Dijamin |
| Memori | Lebih sedikit | Lebih banyak |
| Implementasi | Rekursif atau Iteratif | Iteratif |

## Contoh Kasus Penggunaan Nyata

- **DFS:**
    - **Penyelesaian Labirin:** DFS sangat cocok untuk mencari jalan keluar dari labirin.
    - **Pencarian File:** Sistem operasi dapat menggunakan DFS untuk mencari file dalam direktori.
- **BFS:**
    - **Social Networking:** Menemukan teman terdekat di jaringan sosial.
    - **GPS Navigation:** Mencari rute terpendek antara dua lokasi.

## Kesimpulan

Memahami **bagaimana cara kerja Depth-First Search dan Breadth-First Search** adalah fundamental dalam ilmu komputer. Keduanya menawarkan pendekatan unik untuk menjelajahi struktur data dan memecahkan masalah. Dengan memahami kelebihan dan kekurangan masing-masing, kamu dapat memilih algoritma yang paling tepat untuk tugas yang ada. Apakah kamu lebih suka menjelajahi kedalaman atau lebar? Bagikan pengalamanmu dengan DFS dan BFS di kolom komentar!

## FAQ

**1\. Apakah DFS selalu lebih cepat daripada BFS?**

Tidak selalu. DFS bisa lebih cepat jika solusi berada di kedalaman tertentu dari graf, tetapi BFS lebih cepat jika solusi dekat dengan simpul awal.

**2\. Apakah BFS selalu menemukan jalur terpendek?**

Ya, BFS menjamin menemukan jalur terpendek jika semua edge memiliki bobot yang sama.

**3\. Kapan saya harus menggunakan algoritma pencarian lain selain DFS dan BFS?**

Jika graf memiliki bobot yang berbeda pada setiap edge, kamu bisa menggunakan algoritma seperti Dijkstra atau A\* untuk mencari jalur terpendek. Algoritma lain seperti bidirectional search juga bisa lebih efisien dalam beberapa kasus.
