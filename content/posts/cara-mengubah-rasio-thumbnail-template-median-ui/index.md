---
title: "Mudah! Cara Mengubah Rasio Thumbnail Template Median UI"
date: 2023-05-13
categories: 
  - "blogging"
tags: 
  - "internet"
---

MedianUI adalah template Blogger yang sangat populer dengan tampilan menarik dan pemuatan yang cepat.

Namun, terkadang thumbnail postingan pada template ini terpotong, yang mungkin membuat beberapa pengguna merasa kurang nyaman.

Template ini menggunakan rasio thumbnail 18:9, sedangkan beberapa pengguna mungkin lebih terbiasa dengan rasio 16:9.

Untuk mengatasi masalah ini, Anda dapat mengubah ukuran rasio thumbnail dengan mengedit HTML template.

Berikut adalah langkah-langkah untuk mengubah rasio thumbnail postingan di template median-ui:

## Cara Mengubah Rasio Thumbnail Template Median UI

1. Masuk ke Blogger dan pilih menu "Tema".
2. Pilih "Edit HTML".
3. Cari kode berikut:
    
    ```
    .Blog article.post .post-thumbnail a{padding-top:34.61%}
    ```
    
4. Ganti dengan:
    
    ```
    .Blog article.post .post-thumbnail a{padding-top:56.25%}
    ```
    
5. Selanjutnya, cari kode berikut:
    
    ```
    <div class='post-content'>
      <div class='post-headline'>
        <!-- Gambar headline -->
        <b:if cond='data:view.isPost and data:post.featuredImage'>
          <div class='post-thumbnail'>
            <a expr:href='data:post.url' expr:title='data:post.title'>
              <img class='post-thumb lazy' expr:alt='data:post.title' expr:data-src='resizeImage(data:post.featuredImage, 900, &quot;18:9&quot;)' src='data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs='/>
            </a>
          </div>
        </b:if>
    ```
    
6. Ganti dengan kode berikut:
    
    ```
    <div class='post-content'>
      <div class='post-headline'>
        <!-- Gambar headline -->
        <b:if cond='data:view.isPost and data:post.featuredImage'>
          <div class='post-thumbnail'>
            <a expr:href='data:post.url' expr:title='data:post.title'>
              <img class='post-thumb lazy' expr:alt='data:post.title' expr:data-src='resizeImage(data:post.featuredImage, 900, &quot;16:9&quot;)' src='data:image/png;base64,R0lGODlhAQABAAD/ACwAAAAAAQABAAACADs='/>
            </a>
          </div>
        </b:if>
    ```
    
7. Klik "Simpan" untuk menyimpan perubahan.

**Baca Juga**: [Tutorial Tema Blogger Median Ui Lainnya](https://ajiekusumadhany.com/tag/median-ui/)

## Catatan:

- Pastikan untuk mencadangkan template median-ui terlebih dahulu sebelum melakukan proses mengubah rasio template median ui.
- Pada bagian kode `56.25%`, gantilah persentase tersebut dengan sesuai dengan ukuran rasio yang baru yang Anda inginkan.
- Pada bagian kode `18:9`, gantilah rasio tersebut dengan ukuran panjang x lebar yang Anda inginkan, normalnya biasanya itu memakai rasio `16:9`

Dengan mengikuti langkah-langkah di atas, Anda dapat mengubah rasio thumbnail postingan [tema median ui](https://median-ui.blogspot.com/) sesuai dengan keinginanAnda.

Hal ini akan membantu Anda dalam meningkatkan kualitas visual atau tampilan halaman blog Anda.
