---
title: "Membuat Kalkulator dengan HTML CSS dan JavaScript"
date: 2023-08-22
categories: 
  - "javascript"
tags: 
  - "html-2"
---

Selamat datang di blog saya! Pada kesempatan ini, saya akan membahas tentang bagaimana [cara membuat kalkulator](https://ajiekusumadhany.com/membuat-kalkulator-html-css-javascript/) menggunakan HTML, memberikan tampilan menarik dengan CSS, dan menggunakan JavaScript.

Untuk hasilnya bisa lihat disini: [https://calculator-html-css-js-ajie.netlify.app/](https://calculator-html-css-js-ajie.netlify.app/)

## HTML

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

            <button class="dark-light"><img src="asset/Group 58.svg" alt=""></button><button class="operator"
                id="clear">AC</button>
            <button class="operator" id="backspace">CE</button><button class="operator" value="/">/</button>
            <button class="angka" value="7">7</button><button class="angka" value="8">8</button><button class="angka"
                value="9">9</button> <button class="operator" value="*">×</button>
            <button class="angka" value="4">4</button><button class="angka" value="5">5</button><button class="angka"
                value="6">6</button>
            <button class="operator" value="-">–</button><button class="angka" value="1">1</button><button class="angka"
                value="2">2</button><button class="angka" value="3">3</button>
            <button class="operator" value="+">+</button><button class="angka" value="0">0</button>
            <button class="angka" value=".">.</button>
            <button class="result" id="result" value="=">=</button>
        </div>
    </div>

    <script>

    </script>
</body>

</html>
```

## CSS

```
body {
  width: 100vw;
  height: 100vh;
  background-color: #248bc653;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
}
.container {
  width: 276px;
  background-color: #1e1e1e;
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
  margin-top: 20px;
  border-radius: 20px;
  display: flex;
  flex-wrap: wrap;
  padding: 10px;
  justify-content: space-between;
}

button {
  width: 44px;
  height: 44px;
  background-color: #27292e;
  border-radius: 32px;
  color: #ffffff;
  font-size: 18px;
  cursor: pointer;
  margin: 8.7px;
}
button:hover {
  border-color: #ed0e98;
}
.operator {
  background-color: #44474d;
  border: #44474d 2px solid;
  color: #ffffff;
}
.operator:hover {
  border: #ed0e98 2px solid;
}
button.result {
  width: 103px;
  height: 44px;
  background-image: linear-gradient(#ed0e98, #fe5a2d);
  border-radius: 32px;
  color: #ffffff;
  border: none;
}
button.result:hover {
  box-shadow: 0 0 15px 5px rgba(255, 255, 255, 0.315);
}
.dark-light {
  border: #44474d 2px solid;
}
.angka {
  border: transparent 1px solid;
  font-size: 18px;
  margin: 8.7px;
}
.angka:hover {
  background-color: #ed0e98;
}
```

## JavaScript

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
```

Tadinya mau saya kasih fitur dark-light dan dark-mode tapi gak jadi, mungkin lain kali tak tambahin.

Selamat mencoba!

GitHub: [https://github.com/ajiekusumadhany/kalkulator-html-css-js](https://github.com/ajiekusumadhany/kalkulator-html-css-js)
