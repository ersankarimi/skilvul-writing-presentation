# Materi Minggu 2

## Daftar Isi

1. [JavaScript Looping](#javascript-looping)
2. [JavaScript Function](#javascript-function)
3. [JavaScript Data Type (Primitive and Non-Primitive)](#javascript-data-types-primitive-and-non-primitive)
4. [JavaScript Math Object](#javascript-math-object)
5. [JavaScript DOM](#javascript-dom)
6. [JavaScript DOM Events](#javascript-dom-events)
7. [JavaScript Form](#javascript-form)

<br>

## JavaScript Looping

### For Loop

For loop adalah salah satu cara untuk melakukan looping pada JavaScript. For
loop memiliki 3 bagian yaitu inisialisasi, kondisi, dan increment/decrement.
Berikut contoh penggunaan for loop:

```JavaScript
for (let i = 0; i < 10; i++) {
  console.log(i);
}
```

### While Loop

While loop adalah salah satu cara untuk melakukan looping pada JavaScript. While
loop memiliki 2 bagian yaitu kondisi dan increment/decrement. Berikut contoh
penggunaan while loop:

```JavaScript
let i = 0;
while (i < 10) {
  console.log(i);
  i++;
}
```

### Do While Loop

Do while loop adalah salah satu cara untuk melakukan looping pada JavaScript. Do
while loop memiliki 2 bagian yaitu kondisi dan increment/decrement. Berikut
contoh penggunaan do while loop:

```JavaScript
let i = 0;
do {
  console.log(i);
  i++;
} while (i < 10);
```

## JavaScript Function

### Function Declaration

Function declaration adalah cara untuk membuat function pada JavaScript. Berikut
contoh penggunaan function declaration:

```JavaScript
function sayHello() {
  console.log("Hello");
}
```

### Function Expression

Function expression adalah cara untuk membuat function pada JavaScript. Berikut
contoh penggunaan function expression:

```JavaScript
const sayHello = function () {
  console.log("Hello");
};
```

### Arrow Function

Arrow function adalah cara untuk membuat function pada JavaScript. Berikut
contoh penggunaan arrow function:

```JavaScript
const sayHello = () => {
  console.log("Hello");
};
```

### Function Parameter

Function parameter adalah cara untuk mengirimkan data ke dalam function. Berikut
contoh penggunaan function parameter:

```JavaScript
function sayHello(name) {
  console.log(`Hello ${name}`);
}
```

### Default Parameter

Default parameter adalah cara untuk memberikan nilai default pada function
parameter. Berikut contoh penggunaan default parameter:

```JavaScript
function sayHello(name = "Ersan") {
  console.log(`Hello ${name}`);
}
```

### Return Value

Return value adalah cara untuk mengembalikan nilai dari function. Berikut contoh
penggunaan return value:

```JavaScript
function sayHello(name = "Ersan") {
  return `Hello ${name}`;
}
```

### Rest Parameter

Rest parameter adalah cara untuk mengirimkan banyak data ke dalam function.
Berikut contoh penggunaan rest parameter:

```JavaScript
function sayHello(...names) {
  console.log(names);
}
```

### Function Scope

Function scope adalah cara untuk membuat variable yang hanya bisa diakses di
dalam function. Berikut contoh penggunaan function scope:

```JavaScript
function sayHello() {
  const name = "Ersan";
  console.log(name);
}
```

### Block Scope

Block scope adalah cara untuk membuat variable yang hanya bisa diakses di dalam
block. Berikut contoh penggunaan block scope:

```JavaScript
if (true) {
  const name = "Ersan";
  console.log(name);
}
```

## JavaScript Data Types (Primitive and Non-Primitive)

### Primitive Data Types

Primitive data types adalah tipe data yang tidak memiliki method dan tidak bisa
diubah. Berikut contoh penggunaan primitive data types:

```JavaScript
const name = "Ersan";
const age = 20;
const isMarried = false;
```

### Non-Primitive Data Types

Non-primitive data types adalah tipe data yang memiliki method dan bisa diubah.
Berikut contoh penggunaan non-primitive data types:

```JavaScript
const person = {
  name: "Ersan",
  age: 20,
  isMarried: false,
};
const fruits = ["Apple", "Banana", "Orange"];
```

## JavaScript Math Object

### Math Object

Math object adalah object yang berisi method-method untuk melakukan operasi
matematika. Berikut contoh penggunaan math object:

```JavaScript
const number = 10;
console.log(Math.PI);
console.log(Math.abs(number));
console.log(Math.ceil(number));
console.log(Math.floor(number));
console.log(Math.round(number));
console.log(Math.max(1, 2, 3, 4, 5));
console.log(Math.min(1, 2, 3, 4, 5));
console.log(Math.random());
```

## JavaScript DOM

### DOM

DOM adalah singkatan dari Document Object Model. DOM adalah object yang berisi
semua element HTML. Berikut contoh penggunaan DOM:

### DOM Tree

DOM tree adalah object yang berisi semua element HTML. Berikut contoh penggunaan
DOM tree:

```JavaScript
const body = document.body;
const div = document.getElementById("div");
const divs = document.getElementsByTagName("div");
const divs = document.getElementsByClassName("div");
const divs = document.querySelectorAll("div");
const divs = document.querySelectorAll(".div");
const divs = document.querySelectorAll("#div");
```

### DOM Traversal

DOM traversal adalah cara untuk mengakses element HTML. Berikut contoh
penggunaan DOM traversal:

```JavaScript
const div = document.getElementById("div");
const divParent = div.parentElement;
const divChildren = div.children;
const divFirstChild = div.firstElementChild;
const divLastChild = div.lastElementChild;
const divNextSibling = div.nextElementSibling;
const divPreviousSibling = div.previousElementSibling;
```

### DOM Manipulation

DOM manipulation adalah cara untuk mengubah element HTML. Berikut contoh
penggunaan DOM manipulation:

```JavaScript
const div = document.getElementById("div");
div.innerHTML = "Hello";
div.style.color = "red";
div.style.backgroundColor = "blue";
div.classList.add("class");
div.classList.remove("class");
div.classList.toggle("class");
```

### NodeList

NodeList adalah object yang berisi semua element HTML. Berikut contoh penggunaan
NodeList:

```JavaScript
const divs = document.querySelectorAll("div");
divs.forEach((div) => {
  div.innerHTML = "Hello";
});
```

### HTMLCollection

HTMLCollection adalah object yang berisi semua element HTML. Berikut contoh
penggunaan HTMLCollection:

```JavaScript
const divs = document.getElementsByClassName("div");
divs[0].innerHTML = "Hello";
```

## JavaScript DOM Events

### DOM Events

DOM events adalah cara untuk menangani event pada element HTML. Berikut contoh
penggunaan DOM events:

```JavaScript
const button = document.getElementById("button");
button.addEventListener("click", () => {
  console.log("Hello");
});
```

### Event Bubbling

Event bubbling adalah cara untuk menangani event pada element HTML. Berikut
contoh penggunaan event bubbling:

```JavaScript
const div = document.getElementById("div");
div.addEventListener("click", () => {
  console.log("Hello");
});
```

### Event Delegation

Event delegation adalah cara untuk menangani event pada element HTML. Berikut
contoh penggunaan event delegation:

```JavaScript
const div = document.getElementById("div");
div.addEventListener("click", (event) => {
  if (event.target.tagName === "BUTTON") {
    console.log("Hello");
  }
});
```

## JavaScript Form

### Form

Form adalah cara untuk mengambil data dari user. Berikut contoh penggunaan form:

```HTML
<form>
  <input type="text" name="name" />
  <input type="text" name="age" />
  <input type="submit" value="Submit" />
</form>
```

### Form Validation

Form validation adalah cara untuk memvalidasi data dari user. Berikut contoh
penggunaan form validation:

```JavaScript
const form = document.getElementById("form");
form.addEventListener("submit", (event) => {
  event.preventDefault();
  const name = document.getElementById("name").value;
  const age = document.getElementById("age").value;
  if (name === "") {
    alert("Name is required");
  } else if (age === "") {
    alert("Age is required");
  } else {
    alert("Success");
  }
});
```
