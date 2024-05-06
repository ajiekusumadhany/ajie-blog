---
title: 'Membuat Kalkulator dengan HTML CSS dan JavaScript'
date: Tue, 22 Aug 2023 05:14:03 +0000
draft: false
tags: ['Html', 'JavaScript', 'Pemrograman']
---

Selamat datang di blog saya! Pada kesempatan ini, saya akan membahas tentang bagaimana [cara membuat kalkulator](https://blog.ajiekusumadhany.com/membuat-kalkulator-html-css-javascript/) menggunakan HTML, memberikan tampilan menarik dengan CSS, dan menggunakan JavaScript. Untuk hasilnya bisa lihat disini: [https://calculator-html-css-js-ajie.netlify.app/](https://calculator-html-css-js-ajie.netlify.app/)

HTML
----

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <link rel="stylesheet" href="style.css">
    <script src="script.js"></script>
    <link rel="shortcut icon" href="asset/favicon.png" type="image/x-icon">
</head>

<body>
    <div class="container">
        <form>
            <input type="text" id="inputField" value="">
        </form>
        <div class="container-button">
            <div class="keypad">
                <button class="dark-light"><img src="asset/Group 58.svg" alt=""></button><button class="operator"
                    id="clear">AC</button>
                <button class="operator" id="backspace">CE</button><button class="operator" value="/">/</button>
                <button class="angka" value="7">7</button><button class="angka" value="8">8</button><button
                    class="angka" value="9">9</button> <button class="operator" value="\*">×</button>
                <button class="angka" value="4">4</button><button class="angka" value="5">5</button><button
                    class="angka" value="6">6</button>
                <button class="operator" value="-">–</button><button class="angka" value="1">1</button><button
                    class="angka" value="2">2</button><button class="angka" value="3">3</button>
                <button class="operator" value="+">+</button><button class="angka" value="0">0</button>
                <button class="angka" value=".">.</button><button class="result" id="result" value="=">=</button>
            </div>
        </div>
    </div>

    <script>

    </script>
</body>

</html>

```

CSS
---

```
body {
  width: 100%;
  height: 100%;
  background-color: #ffffff;
}
.container {
  width: 276px;
  height: 421px;
  background-color: #1e1e1e;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 10px;
  box-sizing: border-box;
}

form input {
  width: 100%;
  background-color: #1e1e1e;
  border: none;
  color: white;
  height: 20%;
  margin-top: 20px;
  font-weight: 500;
  font-size: 40px;
  text-align: right;
  box-sizing: border-box;
}
.container-button {
  background-color: #27292e;
  height: 80%;
  width: 100%;
  border-radius: 20px;
  position: absolute;
  bottom: 0px;
}
.keypad {
  width: 250px;
  height: 286px;
  background-color: #27292e;
  margin-left: auto;
  margin-right: auto;
  margin-top: 20px;
}
button {
  width: 44px;
  height: 44px;
  background-color: #27292e;
  border-radius: 32px;
  color: #ffffff;
  font-size: 18px;
  margin: 8.7px;
  box-sizing: border-box;
  cursor: pointer;
}
button:hover {
  width: 44px;
  height: 44px;
  border-radius: 32px;
  color: #ffffff;
  font-size: 18px;
  margin: 8.7px;
  box-sizing: border-box;
  cursor: pointer;
  border-color: #ed0e98;
}
.operator {
  width: 44px;
  height: 44px;
  background-color: #44474d;
  border: #44474d 2px solid;
  border-radius: 32px;
  color: #ffffff;
  font-size: 18px;
  margin: 8.7px;
}
.operator:hover {
  width: 44px;
  height: 44px;
  background-color: #44474d;
  border-radius: 32px;
  color: #ffffff;
  border: #ed0e98 2px solid;
  font-size: 18px;
  margin: 8.7px;
}
.result {
  width: 103px;
  height: 44px;
  background-image: linear-gradient(#ed0e98, #fe5a2d);
  border-radius: 32px;
  color: #ffffff;
  border: none;
  font-size: 20px;
}
.result:hover {
  width: 103px;
  height: 44px;
  background-image: linear-gradient(#ed0e98, #fe5a2d);
  border-radius: 32px;
  color: #ffffff;
  border: none;
  font-size: 20px;
  box-shadow: 0 0 15px 5px rgba(255, 255, 255, 0.315);
}
.dark-light {
  width: 44px;
  height: 44px;
  background-color: #1e1e1e;
  border: #44474d 2px solid;
  padding: 3px;
  color: #ffffff;
  font-size: 18px;
  margin: 8.7px;
}
.angka {
  width: 44px;
  height: 44px;
  color: #ffffff;
  border: transparent 1px solid;
  font-size: 18px;
  margin: 8.7px;
}
.angka:hover {
  width: 44px;
  height: 44px;
  color: #ffffff;
  border: #ed0e98 1px solid;
  background-color: #ed0e98;
  font-size: 18px;
  margin: 8.7px;
}

```

JavaScript
----------

```
document.addEventListener("DOMContentLoaded", function () {
  const inputField = document.getElementById("inputField");
  const keypadButtons = document.querySelectorAll(".angka, .operator");
  const clearButton = document.getElementById("clear");
  const backspaceButton = document.getElementById("backspace");
  const resultButton = document.getElementById("result");

  // Mengatur event listener untuk tombol angka dan operator
  keypadButtons.forEach((button) => {
    button.addEventListener("click", function () {
      const value = button.value;
      inputField.value += value;
    });
  });

  // Mengatur event listener untuk tombol AC (Clear)
  clearButton.addEventListener("click", function () {
    inputField.value = "";
  });

  // Mengatur event listener untuk tombol CE (Backspace)
  backspaceButton.addEventListener("click", function () {
    inputField.value = parseFloat(inputField.value);
    inputField.value = inputField.value.slice(0, -1);
  });

  // Mengatur event listener untuk tombol hasil (=)
  resultButton.addEventListener("click", function () {
    try {
      inputField.value = eval(inputField.value);
    } catch (error) {
      inputField.value = "Error";
    }
  });
});

```  Tadinya mau saya kasih fitur dark-light dan dark-mode tapi gak jadi, mungkin lain kali tak tambahin. Selamat mencoba! GitHub: [https://github.com/ajiekusumadhany/kalkulator-html-css-js](https://github.com/ajiekusumadhany/kalkulator-html-css-js)