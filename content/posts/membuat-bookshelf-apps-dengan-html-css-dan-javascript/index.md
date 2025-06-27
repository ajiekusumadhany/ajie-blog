---
title: "Membuat Bookshelf Apps dengan Html, Css dan Javascript"
date: 2023-10-17
categories: 
  - "javascript"
tags: 
  - "bookshelf-apps"
  - "html-2"
---

## Source Code

GitHub: [https://github.com/ajiekusumadhany/bookshelf-apps](https://github.com/ajiekusumadhany/bookshelf-apps)

Demo: [https://bookshelf-apps-ajie.netlify.app/](https://bookshelf-apps-ajie.netlify.app/)

### Html

```
<!doctype html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport"
    content="width=device-width, user-scalable=no, initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Bookshelf Apps</title>
  <meta name="description" content="Bockshelf Apps by Ajie Ikrus Kusumadhany">
  <link rel="preconnect" href="https://fonts.gstatic.com">
  <link href="https://fonts.googleapis.com/css2?family=Open+Sans:wght@300;400;600;700;800&display=swap"
    rel="stylesheet">
  <link rel="stylesheet" href="style.css">
</head>

<body>
  <header class="head_bar">
    <h1 class="head_bar__title">Bookshelf Apps</h1>
    <section class="search_section">
      <form id="searchBook">
        <label for="searchBookTitle"></label>
        <input id="searchBookTitle" type="text">
        <button id="searchSubmit" type="submit">Cari</button>
      </form>
    </section>
  </header>
  <main>
    <section class="input_section">
      <div class="input-container">
        <h2>Masukkan Buku Baru</h2>
        <form id="inputBook">
          <div class="input">
            <label for="inputBookTitle">Judul</label>
            <input id="inputBookTitle" type="text" required>
          </div>
          <div class="input">
            <label for="inputBookAuthor">Penulis</label>
            <input id="inputBookAuthor" type="text" required>
          </div>
          <div class="input">
            <label for="inputBookYear">Tahun</label>
            <input id="inputBookYear" type="number" required>
          </div>
          <div class="input_inline">
            <label for="inputBookIsComplete">Selesai dibaca</label>
            <input id="inputBookIsComplete" type="checkbox">
          </div>
          <button id="bookSubmit" type="submit">Masukkan Buku ke rak <span>Belum selesai dibaca</span></button>
        </form>
      </div>
    </section>

    <div class="daftarBuku">
      <section class="book_shelf">
        <h2>Belum selesai dibaca</h2>

        <div id="incompleteBookshelfList" class="book_list">
        </div>
      </section>

      <section class="book_shelf">
        <h2>Selesai dibaca</h2>

        <div id="completeBookshelfList" class="book_list">
        </div>
      </section>
    </div>

    <div id="confirm-remove" class="confirm-remove">
      <div class="remove-content">
        <h3>Yakin Menghapus Buku?</h3>
        <div class="button-confirm">
          <button id="jadi-remove" class="jadi-remove">Yes</button>
          <button id="batal-remove" class="batal-remove">Cancel</button>
        </div>
      </div>
    </div>

  </main>

  <script src="main.js"></script>

</body>

</html>
```

### Css

```
* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body,
input,
button {
  font-family: "Open Sans", sans-serif;
}

input,
button {
  font-size: 16px;
}

.head_bar {
  padding: 12px;
  display: flex;
  align-items: center;
  background-color: cornflowerblue;
  color: white;
  display: flex;
  justify-content: space-between;
  padding-left: 40px;
  padding-right: 40px;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
}

main {
  max-width: 100%;
  width: 100%;
  margin: 0 auto;
  padding: 16px;
  margin-top: 110px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding-right: 100px;
}

.input_section .input-container {
  display: flex;
  flex-direction: column;
  border-radius: 10px;
  width: 30%;
  background-color: cornflowerblue;
  padding: 16px;
  margin-top: 20px;
  height: 390px;
  position: fixed;
  left: 50px;
}

.input_section .input-container > h2 {
  text-align: center;
  color: rgb(255, 255, 255);
}

.input_section .input-container > form > .input {
  margin: 8px 0;
}

.input_section .input-container > form > button {
  background-color: #0c9488ff;
  color: white;
  border: 0;
  border-radius: 5px;
  display: block;
  width: 100%;
  padding: 8px;
  cursor: pointer;
}
.input_section .input-container > form > button:hover {
  background-color: #207f7bff;
}

.input_section .input-container > form > button > span {
  font-weight: bold;
}

.input_section .input-container > form > .input > input {
  display: block;
  width: 100%;
  padding: 8px;
  border-radius: 5px;
}

.input_section .input-container > form > .input > label {
  color: rgb(255, 255, 255);
  font-weight: bold;
}

.input_section .input-container > form > .input_inline {
  margin: 12px 0;
  display: flex;
  align-items: center;
}

.input_section .input-container > form > .input_inline > label {
  color: rgb(255, 255, 255);
  font-weight: bold;
  margin-right: 10px;
}

.search_section > form {
  padding: 16px;
  width: 100%;
  display: grid;
  grid-template-columns: auto 1fr 0.5fr;
  grid-gap: 10px;
  width: 500px;
}

.search_section > form > label {
  display: flex;
  align-items: center;
}

.search_section > form > input {
  padding: 5px;
  border-radius: 5px;
}

.search_section > form > button {
  background-color: #0c9488ff;
  color: #fff;
  font-weight: bold;
  border: 2;
  border-radius: 5px;
  cursor: pointer;
  border-color: #fff;
}
.search_section > form > button:hover {
  background-color: #207f7bff;
}

.book_shelf {
  margin: 16px 0 0 0;
  border: 1px solid black;
  padding: 16px;
  border-radius: 10px;
  width: 600px;
}

.book_shelf > h2 {
  color: cornflowerblue;
}

.book_shelf > .book_list {
  padding: 16px;
}

.book_shelf > .book_list > .book_item {
  padding: 8px 16px 16px 16px;
  border: 1px solid black;
  border-radius: 5px;
  margin: 10px 0;
}

.book_shelf > .book_list > .book_item > h3,
p {
  margin: 8px 0;
}

.book_shelf > .book_list > .book_item > .action > button {
  border: 0;
  padding: 5px;
  margin: 0 5px 0 0;
  border-radius: 5px;
  cursor: pointer;
}

.book_shelf > .book_list > .book_item > .action > .green {
  background-color: darkgreen;
  color: white;
}

.book_shelf > .book_list > .book_item > .action > .red {
  background-color: darkred;
  color: white;
}

.book_shelf > .book_list > .book_item > .action > .orange {
  background-color: rgb(255, 119, 8);
  color: white;
}

.confirm-remove {
  display: none;
  position: fixed;
  z-index: 3;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.484);
}

.remove-content {
  background-color: #fff;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  padding: 20px;
  width: 300px;
  height: 150px;
  text-align: center;
}

.remove-content .button-confirm {
  margin-top: 50px;
  display: flex;
  justify-content: space-around;
}
.remove-content .button-confirm button {
  width: 90px;
  height: 35px;
  color: #fff;
  border: none;
  border-radius: 7px;
  cursor: pointer;
}
.remove-content .button-confirm #jadi-remove {
  background-color: darkgreen;
}
.remove-content .button-confirm #batal-remove {
  background-color: darkred;
}

```

### JavaScript

```
const SAVED_EVENT = "saved-book";
const STORAGE_KEY = "BOOKSHELF_APPS";

function isStorageExist() /* boolean */ {
  if (typeof Storage === undefined) {
    alert("Browser kamu tidak mendukung local storage");
    return false;
  }
  return true;
}
const daftarBook = [];
const RENDER_EVENT = "render-book";
document.addEventListener("DOMContentLoaded", function () {
  const submitForm = document.getElementById("inputBook");
  submitForm.addEventListener("submit", function (event) {
    event.preventDefault();
    addBuku();
  });
  if (isStorageExist()) {
    loadDataFromStorage();
  }
});
function addBuku() {
  const titleBook = document.getElementById("inputBookTitle").value;
  const authorBook = document.getElementById("inputBookAuthor").value;
  const yearBook = document.getElementById("inputBookYear").value;
  const isCompletedBook = document.getElementById(
    "inputBookIsComplete"
  ).checked;
  const generatedID = generateId();
  const bookObject = generateBookObject(
    generatedID,
    titleBook,
    authorBook,
    yearBook,
    isCompletedBook
  );
  daftarBook.push(bookObject);
  document.dispatchEvent(new Event(RENDER_EVENT));
  saveData();
}
function generateId() {
  return +new Date();
}
function generateBookObject(id, titleBook, authorBook, yearBook, isCompleted) {
  return {
    id,
    titleBook,
    authorBook,
    yearBook: parseInt(yearBook),
    isCompleted,
  };
}
document.addEventListener(RENDER_EVENT, function () {
  const uncompletedBookList = document.getElementById(
    "incompleteBookshelfList"
  );
  uncompletedBookList.innerHTML = "";
  const completedBookList = document.getElementById("completeBookshelfList");
  completedBookList.innerHTML = "";

  for (const bookItem of daftarBook) {
    const bookElement = makeBuku(bookItem);
    if (!bookItem.isCompleted) {
      uncompletedBookList.append(bookElement);
    } else {
      completedBookList.append(bookElement);
    }
  }
});
function makeBuku(bookObject) {
  const textTitle = document.createElement("h3");
  textTitle.innerText = bookObject.titleBook;
  const textAuthor = document.createElement("p");
  textAuthor.innerText = "Penulis: " + bookObject.authorBook;
  const textYear = document.createElement("p");
  textYear.innerText = "Tahun: " + bookObject.yearBook;
  const textContainer = document.createElement("div");
  textContainer.classList.add("inner");
  textContainer.append(textTitle, textAuthor, textYear);
  const container = document.createElement("article");
  container.classList.add("book_item");
  container.append(textContainer);
  container.setAttribute("id", `book-${bookObject.id}`);
  if (bookObject.isCompleted) {
    const undoButton = document.createElement("button");
    undoButton.classList.add("green");
    undoButton.innerText = "Belum Selesai dibaca";
    undoButton.addEventListener("click", function () {
      undoBook(bookObject.id);
    });
    const trashButton = document.createElement("button");
    trashButton.classList.add("red");
    trashButton.innerText = "Hapus buku";
    trashButton.addEventListener("click", function () {
      const confirmRemove = document.getElementById("confirm-remove");
      const jadiRemove = document.getElementById("jadi-remove");
      const batalRemove = document.getElementById("batal-remove");
      confirmRemove.style.display = "block";
      jadiRemove.addEventListener("click", () => {
        removeBook(bookObject.id);
        confirmRemove.style.display = "none";
      });
      batalRemove.addEventListener("click", () => {
        confirmRemove.style.display = "none";
      });
    });
    const buttonAction = document.createElement("div");
    buttonAction.classList.add("action");
    buttonAction.append(undoButton, trashButton);
    container.append(buttonAction);
  } else {
    const checkButton = document.createElement("button");
    checkButton.classList.add("green");
    checkButton.innerText = "Selesai dibaca";

    checkButton.addEventListener("click", function () {
      addTaskToCompleted(bookObject.id);
    });
    const trashButton = document.createElement("button");
    trashButton.classList.add("red");
    trashButton.innerText = "Hapus buku";
    trashButton.addEventListener("click", function () {
      const confirmRemove = document.getElementById("confirm-remove");
      const jadiRemove = document.getElementById("jadi-remove");
      const batalRemove = document.getElementById("batal-remove");
      confirmRemove.style.display = "block";
      jadiRemove.addEventListener("click", () => {
        removeBook(bookObject.id);
        confirmRemove.style.display = "none";
      });
      batalRemove.addEventListener("click", () => {
        confirmRemove.style.display = "none";
      });
    });
    const buttonAction = document.createElement("div");
    buttonAction.classList.add("action");
    buttonAction.append(checkButton, trashButton);
    container.append(buttonAction);
  }
  return container;
}
function addTaskToCompleted(bookId) {
  const bookTarget = findBook(bookId);
  if (bookTarget == null) return;
  bookTarget.isCompleted = true;
  document.dispatchEvent(new Event(RENDER_EVENT));
  saveData();
}
function findBook(bookId) {
  for (const bookItem of daftarBook) {
    if (bookItem.id === bookId) {
      return bookItem;
    }
  }
  return null;
}
function removeBook(bookId) {
  const bookTarget = findBookIndex(bookId);
  if (bookTarget === -1) return;
  daftarBook.splice(bookTarget, 1);
  document.dispatchEvent(new Event(RENDER_EVENT));
  saveData();
}
function undoBook(bookId) {
  const bookTarget = findBook(bookId);
  if (bookTarget == null) return;
  bookTarget.isCompleted = false;
  document.dispatchEvent(new Event(RENDER_EVENT));
  saveData();
}
function findBookIndex(bookId) {
  for (const index in daftarBook) {
    if (daftarBook[index].id === bookId) {
      return index;
    }
  }
  return -1;
}
function saveData() {
  if (isStorageExist()) {
    const parsed = JSON.stringify(daftarBook);
    localStorage.setItem(STORAGE_KEY, parsed);
    document.dispatchEvent(new Event(SAVED_EVENT));
  }
}
document.addEventListener(SAVED_EVENT, function () {
  console.log(localStorage.getItem(STORAGE_KEY));
});
function loadDataFromStorage() {
  const serializedData = localStorage.getItem(STORAGE_KEY);
  let data = JSON.parse(serializedData);
  if (data !== null) {
    for (const book of data) {
      daftarBook.push(book);
    }
  }
  document.dispatchEvent(new Event(RENDER_EVENT));
}
const formPencarian = document.getElementById("searchBook");
formPencarian.addEventListener("submit", function (event) {
  event.preventDefault();
  const searchInput = document.getElementById("searchBookTitle").value;
  searchBooks(searchInput);
});
function searchBooks(query) {
  const uncompletedBookList = document.getElementById(
    "incompleteBookshelfList"
  );
  const completedBookList = document.getElementById("completeBookshelfList");
  for (const bookItem of daftarBook) {
    const bookElement = document.getElementById(`book-${bookItem.id}`);
    if (bookItem.titleBook.toLowerCase().includes(query.toLowerCase())) {
      bookElement.style.display = "block";
    } else {
      bookElement.style.display = "none";
    }
  }
}
function showAllBooks() {
  const uncompletedBookList = document.getElementById(
    "incompleteBookshelfList"
  );
  const completedBookList = document.getElementById("completeBookshelfList");
  for (const bookItem of daftarBook) {
    const bookElement = document.getElementById(`book-${bookItem.id}`);
    bookElement.style.display = "block";
  }
}
formPencarian.addEventListener("reset", function () {
  showAllBooks();
});

```
