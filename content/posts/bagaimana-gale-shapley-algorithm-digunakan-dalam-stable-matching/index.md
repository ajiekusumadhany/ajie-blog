---
title: "Bagaimana Gale-Shapley Algorithm Digunakan Dalam Stable Matching?"
date: 2025-09-27
categories: 
  - "pemrograman"
tags: 
  - "pemrograman"
---

Pernahkah kamu merasa seperti sedang bermain cinta segitiga yang rumit, tapi dalam skala yang lebih besar? Bayangkan mencoba mencocokkan ratusan mahasiswa kedokteran dengan rumah sakit residensi yang mereka impikan. Atau mungkin, menghubungkan ribuan siswa dengan sekolah yang paling sesuai dengan minat dan bakat mereka. Rumit, kan? Nah, di sinilah keajaiban **Bagaimana Gale-Shapley Algorithm Digunakan dalam Stable Matching** hadir untuk menyelamatkan kita dari kekacauan perjodohan massal!

Dalam artikel ini, kita akan menyelami dunia algoritma yang elegan ini, memahami cara kerjanya, dan melihat bagaimana ia diterapkan dalam berbagai skenario _stable matching_ yang krusial. Bersiaplah, karena kita akan mengungkap rahasia di balik perjodohan yang adil dan efisien!

## Memahami Dasar Stable Matching

Stable matching, atau perjodohan stabil, adalah masalah klasik dalam ilmu komputer dan ekonomi. Intinya, kita ingin mencocokkan dua kelompok yang memiliki preferensi satu sama lain, dengan tujuan menciptakan pasangan yang stabil.

Apa itu "stabil" dalam konteks ini? Sebuah perjodohan dianggap stabil jika tidak ada dua orang dari kelompok berbeda yang lebih suka satu sama lain daripada pasangan mereka saat ini. Jika ada, mereka akan membentuk "pasangan yang menghalangi" dan perjodohan tersebut tidak stabil.

Bayangkan kamu dan pacarmu. Jika ada orang lain yang kalian berdua lebih suka daripada satu sama lain, maka hubungan kalian rentan terhadap gangguan. Nah, stable matching berusaha menghindari situasi seperti ini.

## Gale-Shapley Algorithm: Sang Perjodoh Handal

Gale-Shapley Algorithm, yang juga dikenal sebagai _deferred acceptance algorithm_, adalah solusi elegan untuk masalah stable matching. Dikembangkan oleh David Gale dan Lloyd Shapley pada tahun 1962, algoritma ini menjamin akan menemukan perjodohan yang stabil.

Bagaimana cara kerjanya? Singkatnya, algoritma ini menggunakan proses lamaran yang berulang, di mana satu kelompok (biasanya disebut "proposers") melamar kepada anggota kelompok lain ("receivers"). Receivers kemudian mempertimbangkan lamaran tersebut dan memilih untuk menerima atau menolak.

Proses ini terus berlanjut hingga semua orang telah dipasangkan atau tidak ada lagi lamaran yang ditolak. Hasilnya adalah perjodohan yang stabil, di mana tidak ada pasangan yang menghalangi.

## Langkah-Langkah Gale-Shapley Algorithm

Mari kita bedah langkah-langkah Gale-Shapley Algorithm agar lebih mudah dipahami:

1. **Inisialisasi:** Semua proposers dan receivers belum dipasangkan.
2. **Proposing:** Setiap proposer yang belum dipasangkan melamar kepada receiver yang paling disukainya dalam daftar preferensinya.
3. **Acceptance/Rejection:** Setiap receiver mempertimbangkan semua lamaran yang diterimanya.
    - Jika receiver belum dipasangkan, ia menerima lamaran terbaik (berdasarkan daftar preferensinya).
    - Jika receiver sudah dipasangkan, ia membandingkan lamaran yang baru dengan pasangannya saat ini. Jika lamaran baru lebih disukai, ia menolak pasangannya saat ini dan menerima lamaran baru. Jika tidak, ia menolak lamaran baru.
4. **Iterasi:** Proposers yang lamarannya ditolak kembali ke langkah 2, melamar kepada receiver berikutnya dalam daftar preferensinya.
5. **Terminasi:** Algoritma berhenti ketika semua proposers telah dipasangkan atau tidak ada lagi lamaran yang ditolak.

## Contoh Sederhana Gale-Shapley Algorithm

Katakanlah kita memiliki 3 pria (A, B, C) dan 3 wanita (X, Y, Z) dengan preferensi sebagai berikut:

- **Pria:**
    - A: X > Y > Z
    - B: Y > Z > X
    - C: Z > X > Y
- **Wanita:**
    - X: B > C > A
    - Y: C > A > B
    - Z: A > B > C

Mari kita jalankan Gale-Shapley Algorithm:

1. **Iterasi 1:**
    - A melamar X
    - B melamar Y
    - C melamar Z
    - X, Y, dan Z menerima lamaran tersebut.
2. **Iterasi 2:** Tidak ada perubahan, semua orang sudah dipasangkan.

Hasilnya: A-X, B-Y, C-Z. Ini adalah perjodohan yang stabil.

## Bagaimana Gale-Shapley Algorithm Digunakan dalam Stable Matching? Aplikasi Nyata

Sekarang, mari kita lihat bagaimana **Bagaimana Gale-Shapley Algorithm Digunakan dalam Stable Matching** dalam berbagai aplikasi nyata:

### National Resident Matching Program (NRMP)

Ini adalah salah satu aplikasi paling terkenal dari Gale-Shapley Algorithm. NRMP mencocokkan lulusan sekolah kedokteran dengan program residensi di rumah sakit di seluruh Amerika Serikat. Algoritma ini memastikan bahwa setiap lulusan mendapatkan penempatan yang adil dan stabil, berdasarkan preferensi mereka dan preferensi rumah sakit.

### School Choice Programs

Banyak kota dan negara menggunakan Gale-Shapley Algorithm untuk mencocokkan siswa dengan sekolah pilihan mereka. Ini membantu memastikan bahwa setiap siswa mendapatkan kesempatan untuk bersekolah di sekolah yang paling sesuai dengan minat dan bakat mereka, sambil mempertimbangkan kuota dan preferensi sekolah.

### Matching Organ Donors and Recipients

Dalam bidang transplantasi organ, Gale-Shapley Algorithm dapat digunakan untuk mencocokkan donor organ dengan penerima yang paling cocok. Algoritma ini mempertimbangkan berbagai faktor, seperti golongan darah, ukuran tubuh, dan jarak geografis, untuk memastikan bahwa organ tersebut diberikan kepada penerima yang paling membutuhkannya.

### Online Dating Platforms

Beberapa platform kencan online menggunakan variasi Gale-Shapley Algorithm untuk mencocokkan pengguna berdasarkan preferensi dan minat mereka. Algoritma ini dapat membantu meningkatkan kemungkinan menemukan pasangan yang cocok dan membangun hubungan yang langgeng.

## Keuntungan dan Kekurangan Gale-Shapley Algorithm

Seperti algoritma lainnya, Gale-Shapley Algorithm memiliki kelebihan dan kekurangan:

**Keuntungan:**

- **Menjamin Stable Matching:** Algoritma ini selalu menemukan perjodohan yang stabil.
- **Relative Simplicity:** Implementasinya relatif mudah dipahami dan diimplementasikan.
- **Strategy-Proof for Proposers:** Proposers tidak dapat meningkatkan hasil mereka dengan berbohong tentang preferensi mereka. Ini mendorong kejujuran dan transparansi.

**Kekurangan:**

- **Proposer-Optimality:** Algoritma ini cenderung menguntungkan proposers. Receivers mungkin tidak mendapatkan hasil yang optimal.
- **Data Requirements:** Membutuhkan daftar preferensi yang lengkap dan akurat dari semua pihak.
- **Scalability:** Mungkin menjadi kurang efisien dengan jumlah data yang sangat besar.

## Kesimpulan

**Bagaimana Gale-Shapley Algorithm Digunakan dalam Stable Matching** adalah pertanyaan yang memiliki jawaban yang sangat luas dan berdampak. Algoritma ini bukan hanya konsep teoritis, tetapi alat praktis yang digunakan untuk menyelesaikan masalah perjodohan yang kompleks di berbagai bidang. Dari mencocokkan dokter residen hingga menghubungkan siswa dengan sekolah impian mereka, Gale-Shapley Algorithm membuktikan dirinya sebagai solusi yang adil, efisien, dan stabil.

Apakah kamu punya pengalaman dengan sistem perjodohan yang menggunakan algoritma serupa? Bagikan pengalamanmu di kolom komentar!

## FAQ

**1\. Apakah Gale-Shapley Algorithm selalu memberikan hasil yang adil untuk semua pihak?**

Meskipun Gale-Shapley Algorithm menjamin stable matching, algoritma ini cenderung lebih menguntungkan proposers. Receivers mungkin tidak mendapatkan hasil yang optimal. Namun, secara keseluruhan, algoritma ini dianggap lebih adil daripada sistem perjodohan manual atau acak.

**2\. Apa yang terjadi jika ada preferensi yang sama (tie) dalam daftar preferensi?**

Dalam kasus preferensi yang sama, algoritma dapat dimodifikasi untuk menangani situasi ini. Salah satu caranya adalah dengan menggunakan tie-breaking rule yang telah ditentukan sebelumnya.

**3\. Apakah Gale-Shapley Algorithm dapat digunakan untuk mencocokkan lebih dari dua kelompok?**

Gale-Shapley Algorithm dirancang khusus untuk mencocokkan dua kelompok. Untuk mencocokkan lebih dari dua kelompok, diperlukan algoritma yang lebih kompleks.
