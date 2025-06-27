---
title: "Membuat E-Library Landing Page dengan HTML CSS dan JS"
date: 2023-09-18
categories: 
  - "javascript"
tags: 
  - "e-library"
  - "html-2"
  - "landing-page"
  - "web-perpustakaan"
---

Di era digital ini, perpustakaan telah menjalani transformasi besar-besaran. Perpustakaan fisik tradisional kini dipadukan dengan teknologi untuk membentuk perpustakaan elektronik atau yang sering disebut sebagai "e-perpus."

E-perpus memungkinkan kita untuk mengakses ribuan buku, jurnal, dan sumber daya lainnya dalam hitungan detik, tanpa harus meninggalkan kenyamanan rumah atau kantor kita.

Salah satu aspek penting dari e-perpus adalah landing page-nya. Halaman ini berfungsi sebagai pintu gerbang utama yang mengundang pengguna untuk menjelajahi koleksi yang tersedia.

Membuat landing page e-perpus yang menarik dan fungsional merupakan tantangan yang menarik, jadi Saya akan mencoba membuatan landing page e-perpus menggunakan HTML, CSS, dan JavaScript.

**File Lengkap**: [github e-perpus](https://github.com/ajiekusumadhany/e-perpus-landing-page)

## Html

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/style.css">

    <!-- Meta Seo -->
    <title>E-Perpus Indonesia | Yuk Membaca!</title>
    <meta name="description" content="Perpustakaan elektronik indonesia, tempat membaca dan upgrade ilmu pengetahuan">
    <!-- akhir meta -->

    <!-- favicon -->
    <link rel="shortcut icon" href="assets/img/logo-eperpus.svg" type="image/x-icon">
</head>

<body>
    <header>
        <div class="logo-header">
            <img src="assets/img/logo-eperpus.svg" alt="logo e-perpus" title="E-Perpus Indonesia">
            <h1>E-Perpus</h1>
        </div>
        <nav class="nav-header">
            <ul>
                <li><a href="#">Beranda</a></li>
                <li><a href="#">Kategori</a></li>
                <li><a href="#">Blog</a></li>
                <li><a href="#tentang">Tentang</a></li>
            </ul>
        </nav>
        <div class="login-header">Masuk</div>
        <div class="menu-mobile">
            <input type="checkbox" />
            <p>Menu</p>
        </div>

    </header>

    <main>
        <div class="container-landing">
            <div class="landing-kiri">
                <p>Mari baca buku dan tingkatkan ilmu</p>
                <h2>Selamat Datang <br>Di E-Perpus <br>Indonesia</h2>
                <p>Yuk, belajar dan membaca!</p>

                <div class="button-landing">
                    <button class="mulai-button"><a href="#buku">Mulai Baca!</a></button>
                    <button class="jelajahi-button"><a href="#buku">Jelajahi</a></button>
                </div>
            </div>
            <div class="landing-kanan">
                <img src="assets/img/buku-landing.svg" alt="buku landing">
            </div>
        </div>
        <div class="content-sidebar" id="buku">
            <div class="content">
                <article>
                    <div class="card-book">
                        <img src="assets/img/book-1.jpg" alt="The First 20 Hours">
                        <div class="deskripsi-book">
                            <h3>The First 20 Hours: How to Learn Anything</h3>
                            <p>Josh Kaufman</p>
                            <button>Baca</button>
                        </div>
                    </div>
                </article>
                <article>
                    <div class="card-book">
                        <img src="assets/img/book-2.jpg" alt="How To Accept Yourself In A World">
                        <div class="deskripsi-book">
                            <h3>How To Accept Yourself In A World</h3>
                            <p>Haemin Sumin</p>
                            <button>Baca</button>
                        </div>
                    </div>
                </article>
                <article>
                    <div class="card-book">
                        <img src="assets/img/book-3.jpg" alt="Today Ends Tomorrow Comes">
                        <div class="deskripsi-book">
                            <h3>Today Ends Tomorrow Comes</h3>
                            <p>Denanda Putri</p>
                            <button>Baca</button>
                        </div>
                    </div>
                </article>
                <article>
                    <div class="card-book">
                        <img src="assets/img/book-4.jpg" alt="Seni Mengelola Waktu">
                        <div class="deskripsi-book">
                            <h3>Self Defelopment: Seni Mengelola Waktu</h3>
                            <p>Fellexandro Ruby</p>
                            <button>Baca</button>
                        </div>
                    </div>
                </article>
                <article>
                    <div class="card-book">
                        <img src="assets/img/book-5.jpg" alt="7 Materi Pemrograman Web Modern">
                        <div class="deskripsi-book">
                            <h3>7 Materi Pemrograman Web Modern</h3>
                            <p>Rohi Abdulloh</p>
                            <button>Baca</button>
                        </div>
                    </div>
                </article>
                <article>
                    <div class="card-book">
                        <img src="assets/img/book-6.jpg" alt="Buku Pemrograman Python">
                        <div class="deskripsi-book">
                            <h3>Pemrograman Python untuk Guru dan Murid</h3>
                            </h3>
                            <p>Jubilee Enterprise</p>
                            <button>Baca</button>
                        </div>
                    </div>
                </article>
                <article>
                    <div class="card-book">
                        <img src="assets/img/book-7.jpg" alt="Robotik Dengan Pemrograman C++">
                        <div class="deskripsi-book">
                            <h3>Robotik Dengan Pemrograman C++</h3>
                            <p>Oscar Rachman</p>
                            <button>Baca</button>
                        </div>
                    </div>
                </article>
                <article>
                    <div class="card-book">
                        <img src="assets/img/book-8.jpg" alt="Buku Filsafat Untuk Pemalas">
                        <div class="deskripsi-book">
                            <h3>Buku Filsafat Untuk Pemalas</h3>
                            <p>Ach. Dhofir Zuhryn</p>
                            <button>Baca</button>
                        </div>
                    </div>
                </article>
                <article>
                    <div class="card-book">
                        <img src="assets/img/book-9.jpg" alt="Mental Tempe: Mencari Sang Makanan Harapan">
                        <div class="deskripsi-book">
                            <h3>Mental Tempe: Mencari Sang Makanan Harapan</h3>
                            <p>A. Driando Ahnan-Winarno</p>
                            <button>Baca</button>
                        </div>
                    </div>
                </article>
            </div>
            <aside id="tentang">
                <div class="avatar">
                    <img src="assets/img/fotoku.png" alt="Avatarku">
                </div>
                <H3>Author E-Perpus</H3>
                <p>Nama: Ajie Kusumadhany</p>
                <p>Usia: 18 Tahun</p>
                <p>Asal: Indonesia</p>
                <button><a href="mailto:ajiekusumadhany@gmail.com">Email Me</a></button>

            </aside>
        </div>
    </main>

    <footer>
        <div class="footer-satu">
            <div class="logo-footer">
                <img src="assets/img/logo-eperpus.svg" alt="logo e-perpus">
                <p>Sebuah perpusatakaan online, tempat membaca dan tingkatkan pengetahuan!</p>
            </div>
            <div class="kategori-footer">
                <h2>Kategori</h2>
                <ul>
                    <li><a href="#">Pemrograman</a></li>
                    <li><a href="#">Keuangan</a></li>
                    <li><a href="#">Self Improvement</a></li>
                    <li><a href="#">Cerita Fiksi</a></li>
                </ul>
            </div>
            <div class="sosial-media">
                <h2>Sosial Media</h2>
                <ul>
                    <li><a href="#">Facebook</a></li>
                    <li><a href="#">Twitter</a></li>
                    <li><a href="#">Instagram</a></li>
                    <li><a href="#">Youtube</a></li>
                </ul>
            </div>
            <div class="learn-more">
                <h2>Learn More</h2>
                <ul>
                    <li><a href="#">Tentang Kami</a></li>
                    <li><a href="#">Faq</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </div>
        </div>
        <div class="footer-dua">
            <p>Copyright &copy ajiekusumadhany</p>
        </div>
    </footer>
    <script src="js/script.js"></script>
</body>

</html>
```

## Css

```
/* font */
@import url("https://fonts.googleapis.com/css2?family=Quicksand:wght@500;700&family=Roboto:wght@400;500&display=swap");
/* tutup font */
html {
  scroll-behavior: smooth;
}
body {
  margin: 0;
  padding: 0;
  font-family: "Quicksand", sans-serif;
  font-family: "Roboto", sans-serif;
}
/* Awal style css header */
header {
  display: flex;
  background-color: #fff;
  height: 70px;
  justify-content: space-between;
  align-items: center;
  color: #000000;
  font-weight: 400;
  padding-top: 10px;
  position: fixed;
  left: 0;
  right: 0;
  box-sizing: border-box;
  padding-left: 40px;
  padding-right: 40px;
  z-index: 999999;
  border-bottom: 1px solid #ded3d3;
}

header .login-header {
  height: 33px;
  width: 100px;
  background-color: #0d9488;
  color: #fff;
  border-radius: 30px;
  justify-content: center;
  display: flex;
  align-items: center;
}
header .login-header:hover {
  cursor: pointer;
  background-color: #16877d;
}
header nav.nav-header ul {
  padding-left: 0;
  display: flex;
  justify-content: center;
  gap: 55px;
}

header nav.nav-header ul li {
  list-style-type: none;
}
header nav.nav-header ul li:hover {
  cursor: pointer;
  transform: scale(1.1);
}
header nav.nav-header ul li a {
  text-decoration: none;
  color: #000;
}

header .logo-header {
  display: flex;
  font-size: 12px;
  gap: 10px;
}
header .logo-header:hover {
  cursor: pointer;
}
header .logo-header img {
  width: 45px;
}

.menu-mobile {
  display: none;
}

/* Akhir style css header */

/* landing */
main .container-landing {
  display: flex;
  background-color: #fff;
  height: 100vh;
  justify-content: space-around;
}

/* landing kiri */
main .container-landing .landing-kiri {
  width: 50%;
  padding-left: 140px;
  padding-top: 12%;
  letter-spacing: 1px;
  box-sizing: border-box;
}
main .container-landing .landing-kiri h2 {
  font-size: 2.5rem;
}
button.mulai-button {
  height: 33px;
  width: 100px;
  background-color: #0d9488;
  border-radius: 30px;
  border: none;
  color: #fff;
  margin-top: 30px;
  margin-right: 20px;
}
button.mulai-button a {
  text-decoration: none;
  color: #ffffff;
}
button.mulai-button:hover {
  cursor: pointer;
  background-color: #16877d;
  transform: translate(-0.05em, -0.05em);
}

button.jelajahi-button {
  height: 33px;
  width: 100px;
  border: 2px solid #0d9488;
  border-radius: 30px;
  color: #000;
  margin-top: 30px;
}
button.jelajahi-button a {
  text-decoration: none;
  color: #000000;
}
button.jelajahi-button:hover {
  cursor: pointer;
  border: 2px solid #16877d;
  transform: translate(-0.05em, -0.05em);
}
/* akhir landing kiri */

/* awal landing kanan */
main .container-landing .landing-kanan {
  width: 50%;
  padding-right: 140px;
  box-sizing: border-box;
  display: flex;
  justify-content: center;
  align-items: center;
  -webkit-animation-name: fadeInUp;
  animation-name: fadeInUp;
  -webkit-animation-duration: 1s;
  animation-duration: 1s;
  -webkit-animation-fill-mode: both;
  animation-fill-mode: both;
}
@-webkit-keyframes fadeInUp {
  0% {
    opacity: 0;
    -webkit-transform: translate3d(0, 100%, 0);
    transform: translate3d(0, 100%, 0);
  }
  100% {
    opacity: 1;
    -webkit-transform: none;
    transform: none;
  }
}
main .container-landing .landing-kanan img {
  width: 480px;
  margin-top: 75px;
}
/* akhir landing kanan */
/* Akhir landing */

/* awal  content dan sidebar*/
.content-sidebar {
  display: flex;
  justify-content: space-between;
  box-sizing: border-box;
  padding-left: 50px;
  padding-right: 50px;
  gap: 5rem;
  margin-top: 70px;
  scroll-margin-top: 80px;
}
/* awal sidebar */

aside {
  background-color: #0d9488;
  display: flex;
  flex-grow: 1;
  border-radius: 10px;
  flex-flow: column;
  height: 470px;
  scroll-margin-top: 80px;
}
.avatar {
  display: flex;
  justify-content: center;
  width: 100%;
}
aside img {
  width: 100px;
  border-radius: 50%;
  background-color: #fff;
  margin-top: 30px;
}
aside h3 {
  text-align: center;
  color: #fff;
}
aside p {
  background-color: #fff;
  margin: 15px;
  padding: 5px;
  border-radius: 5px;
}
aside button {
  background-color: #fff;
  margin: 15px;
  padding: 5px;
  border-radius: 5px;
  text-align: center;
  border: none;
}
aside button a {
  text-decoration: none;
  font-size: 17px;
  color: #000;
}
aside button a:hover {
  color: #0d9488;
}
/* akhir sidebar */

/* awal content */
.content {
  border: 1px solid #0d9488;
  flex-grow: 4;
  border-radius: 10px;
  display: flex;
  justify-content: space-around;
  flex-wrap: wrap;
  width: 700px;
  padding: 20px;
  gap: 30px 20px;
}
.content .card-book {
  width: 250px;
  height: 120px;
  background-color: #fff;
  display: flex;
}
.content .card-book img {
  height: 120px;
}
.content .card-book .deskripsi-book {
  margin-left: 20px;
  margin-right: 5px;
  display: flex;
  flex-direction: column;
  box-sizing: border-box;
}
.content .card-book .deskripsi-book h3 {
  font-size: 13px;
}
.content .card-book .deskripsi-book p {
  font-size: 11px;
}
.content .card-book .deskripsi-book button {
  border: 1px solid #0d9488;
  border-radius: 30px;
  height: 25px;
  width: 80px;
  background-color: #fff;
}
.content .card-book .deskripsi-book button:hover {
  background-color: #0d9488;
  color: #fff;
  cursor: pointer;
}

/* akhir content */
/* akhir  content dan sidebar*/

/* Awal footer */
footer {
  margin-top: 100px;
  width: 100%;
}
.footer-satu {
  width: 100%;
  height: 250px;
  background-color: #1f283bff;
  display: flex;
  justify-content: space-between;
  color: #fff;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  padding-left: 40px;
  padding-right: 40px;
  box-sizing: border-box;
  border-bottom: 1px solid #2a384aff;
}

footer .logo-footer {
  width: 300px;
}
footer .logo-footer img {
  width: 150px;
}

footer .kategori-footer ul,
.sosial-media ul,
.learn-more ul {
  list-style-type: none;
  padding-left: 0;
  color: #cad0d5ff;
}
footer .kategori-footer ul li,
.sosial-media ul li,
.learn-more ul li {
  margin-bottom: 10px;
}
footer .kategori-footer ul li a,
.sosial-media ul li a,
.learn-more ul li a {
  text-decoration: none;
  color: #fff;
}

footer .footer-dua {
  width: 100%;
  background-color: #1f283bff;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #fff;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  box-sizing: border-box;
}
/* Akhir footer */
/* responsive */
@media only screen and (max-width: 600px) {
  header .login-header {
    display: none;
  }
  header .menu-mobile {
    background-color: #0d9488;
    width: 60px;
    height: 30px;
    border-radius: 30px;
    display: flex;
    z-index: 8999;
  }
  header .menu-mobile input {
    width: 150%;
    opacity: 0;
    z-index: 99;
  }
  header .menu-mobile p {
    position: absolute;
    top: 15px;
    right: 30px;
    color: #fff;
    z-index: 80;
  }

  nav ul {
    position: absolute;
    right: 0;
    top: -20px;
    width: 60%;
    height: 100vh;
    flex-direction: column;
    align-items: center;
    background-color: #ffffff;
    transform: translateX(100%);
    transition: all 1s;
    opacity: 0;
    color: #ffffff;
    z-index: -1;
  }

  nav ul.nyala {
    transform: translateX(0);
    opacity: 1;
    z-index: 899;
  }
  main .container-landing {
    flex-direction: column;
  }
  main .container-landing .landing-kiri {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-top: 600px;
    padding-left: 20px;
    padding-top: 0;
    letter-spacing: 1px;
    box-sizing: border-box;
  }
  main .container-landing .landing-kanan {
    visibility: hidden;
  }

  .content-sidebar {
    display: flex;
    flex-direction: column;
    box-sizing: border-box;
    padding-left: 10px;
    padding-right: 10px;
    margin-top: 20px;
    box-sizing: border-box;
    scroll-margin-top: 90px;
  }
  .content {
    border: 1px solid #0d9488;
    flex-grow: 1;
    justify-content: start;
    width: 100%;
    padding: 3px;
    gap: 30px 20px;
    border: none;
  }
  .content .card-book {
    width: 300px;
    height: 120px;
    background-color: #fff;
    display: flex;
  }
  .footer-satu {
    height: 900px;
    flex-direction: column;
  }

  header {
    padding-left: 20px;
    padding-right: 20px;
  }
}
/* akhir responsive */
```

## JavaScript

```
const menuMobile = document.querySelector(".menu-mobile input");
const nav = document.querySelector("nav ul");

menuMobile.addEventListener("click", function () {
  nav.classList.toggle("nyala");
});
```
