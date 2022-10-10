# Materi Minggu 3

## Daftar Isi

1. [JavaScript Array Method](#javascript-array-method)
2. [JavaScript Object](#javascript-object)
3. [Recursive Function](#recursive-function)
4. [Web Storage](#web-storage)
5. [Asynchronous JavaScript](#asycnhronous-javascript)

<br>

## JavaScript Array Method

### Array.prototype.map()

Array.prototype.map() digunakan untuk mengubah setiap elemen array menjadi
sesuatu yang baru. Berikut contoh penggunaan Array.prototype.map():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const newNumbers = numbers.map((number) => number * 2);
console.log(newNumbers);
```

### Array.prototype.filter()

Array.prototype.filter() digunakan untuk memfilter elemen array berdasarkan
kondisi tertentu. Berikut contoh penggunaan Array.prototype.filter():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const newNumbers = numbers.filter((number) => number > 3);
console.log(newNumbers);
```

### Array.prototype.reduce()

Array.prototype.reduce() digunakan untuk mengurangi elemen array menjadi satu
nilai. Berikut contoh penggunaan Array.prototype.reduce():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce((total, number) => total + number, 0);
console.log(sum);
```

### Array.prototype.forEach()

Array.prototype.forEach() digunakan untuk melakukan sesuatu pada setiap elemen
array. Berikut contoh penggunaan Array.prototype.forEach():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
numbers.forEach((number) => console.log(number));
```

### Array.prototype.find()

Array.prototype.find() digunakan untuk mencari elemen array berdasarkan kondisi
tertentu. Berikut contoh penggunaan Array.prototype.find():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const number = numbers.find((number) => number > 3);
console.log(number);
```

### Array.prototype.findIndex()

Array.prototype.findIndex() digunakan untuk mencari indeks elemen array
berdasarkan kondisi tertentu. Berikut contoh penggunaan
Array.prototype.findIndex():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const index = numbers.findIndex((number) => number > 3);
console.log(index);
```

### Array.prototype.some()

Array.prototype.some() digunakan untuk mengecek apakah ada elemen array yang
memenuhi kondisi tertentu. Berikut contoh penggunaan Array.prototype.some():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const isSomeNumberGreaterThan3 = numbers.some((number) => number > 3);
console.log(isSomeNumberGreaterThan3);
```

### Array.prototype.every()

Array.prototype.every() digunakan untuk mengecek apakah semua elemen array
memenuhi kondisi tertentu. Berikut contoh penggunaan Array.prototype.every():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const isEveryNumberGreaterThan3 = numbers.every((number) => number > 3);
console.log(isEveryNumberGreaterThan3);
```

### Array.prototype.includes()

Array.prototype.includes() digunakan untuk mengecek apakah elemen array ada atau
tidak. Berikut contoh penggunaan Array.prototype.includes():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const isNumber3Included = numbers.includes(3);
console.log(isNumber3Included);
```

### Array.prototype.sort()

Array.prototype.sort() digunakan untuk mengurutkan elemen array. Berikut contoh
penggunaan Array.prototype.sort():

```JavaScript
const numbers = [5, 4, 3, 2, 1];
const sortedNumbers = numbers.sort();
console.log(sortedNumbers);
```

### Array.prototype.reverse()

Array.prototype.reverse() digunakan untuk membalik urutan elemen array. Berikut
contoh penggunaan Array.prototype.reverse():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const reversedNumbers = numbers.reverse();
console.log(reversedNumbers);
```

### Array.prototype.join()

Array.prototype.join() digunakan untuk menggabungkan elemen array menjadi
string. Berikut contoh penggunaan Array.prototype.join():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const joinedNumbers = numbers.join();
console.log(joinedNumbers);
```

### Array.prototype.slice()

Array.prototype.slice() digunakan untuk mengambil elemen array berdasarkan
indeks. Berikut contoh penggunaan Array.prototype.slice():

```JavaScript
const numbers = [1, 2, 3, 4, 5];
const slicedNumbers = numbers.slice(2, 4);
console.log(slicedNumbers);
```

## JavaScript Object

Javascript object adalah sebuah kumpulan properti yang memiliki nama dan nilai.

Properti dapat berupa fungsi, array, string, number, boolean, dan lain-lain.

### Membuat Object

```JavaScript
const person = {
  name: "Ersan Karimi",
  age: 20,
  hobbies: ["music", "movies", "sports"],
  address: {
    street: "Soekarno-Hatta",
    city: "Balikpapan",
    state: "Balikpapan Utara",
  },
};

console.log(person);
```

### Mengakses Object

```JavaScript
const person = {
  name: "Ersan Karimi",
  age: 20,
  hobbies: ["music", "movies", "sports"],
  address: {
    street: "Soekarno-Hatta",
    city: "Balikpapan",
    state: "Balikpapan Utara",
  },
};

console.log(person.name);
console.log(person.hobbies[1]);
console.log(person.address.city);
```

### Mengubah Object

```JavaScript

const person = {
  name: "Ersan Karimi",
  age: 20,
  hobbies: ["music", "movies", "sports"],
  address: {
    street: "Soekarno-Hatta",
    city: "Balikpapan",
    state: "Balikpapan Utara",
  },
};

person.email = "example@gmail.com"

console.log(person);
```

### Menghapus Object

```JavaScript
const person = {
  name: "Ersan Karimi",
  age: 20,
  hobbies: ["music", "movies", "sports"],
  address: {
    street: "Soekarno-Hatta",
    city: "Balikpapan",
    state: "Balikpapan Utara",
  },
};

delete person.age;

console.log(person);
```

### Array of Object

```JavaScript
const todos = [
  {
    id: 1,
    text: "Take out trash",
    isCompleted: true,
  },
  {
    id: 2,
    text: "Meeting with boss",
    isCompleted: true,
  },
  {
    id: 3,
    text: "Dentist appointment",
    isCompleted: false,
  },
];

console.log(todos);
console.log(todos[1].text);
```

## Recursive Function

Recursive function adalah fungsi yang memanggil dirinya sendiri.

### Contoh Recursive Function

```JavaScript
function factorial(n) {
  if (n === 0) {
    return 1;
  } else {
    return n * factorial(n - 1);
  }
}

console.log(factorial(5));
```

## Web Storage

Web storage adalah cara untuk menyimpan data di browser. Web storage terdiri
dari 2 jenis, yaitu localStorage dan sessionStorage. Web storage ini dapat
digunakan untuk menyimpan data sementara atau permanen. Web storage ini dapat
digunakan untuk menyimpan data sementara atau permanen.

### localStorage

localStorage adalah web storage yang dapat digunakan untuk menyimpan data secara
permanen. Data yang disimpan di localStorage akan tetap ada meskipun browser
ditutup.

### sessionStorage

sessionStorage adalah web storage yang dapat digunakan untuk menyimpan data
sementara. Data yang disimpan di sessionStorage akan hilang jika browser
ditutup.

### Membuat localStorage

```JavaScript
localStorage.setItem("name", "Ersan Karimi");
```

### Membuat sessionStorage

```JavaScript
sessionStorage.setItem("name", "Ersan Karimi");
```

### Menghapus localStorage

```JavaScript
localStorage.removeItem("name");
```

### Menghapus sessionStorage

```JavaScript
sessionStorage.removeItem("name");
```

### Menghapus semua localStorage

```JavaScript
localStorage.clear();
```

### Menghapus semua sessionStorage

```JavaScript
sessionStorage.clear();
```

### Mengambil localStorage

```JavaScript
const name = localStorage.getItem("name");
```

### Mengambil sessionStorage

```JavaScript
const name = sessionStorage.getItem("name");
```

## Asycnhronous JavaScript

Asynchronous JavaScript adalah JavaScript yang dapat melakukan proses secara
paralel. Asynchronous JavaScript menggunakan callback function untuk menangani
proses yang dilakukan secara asynchronous.

### Contoh Asynchronous JavaScript

```JavaScript
console.log("Start");

setTimeout(() => {
  console.log("Callback function fired");
}, 2000);

console.log("End");
```

### Contoh Asynchronous JavaScript dengan Callback

```JavaScript
console.log("Start");

function getUser(id, callback) {
  setTimeout(() => {
    console.log("Reading a user from a database...");
    callback({ id: id, gitHubUsername: "ersankarimi" });
  }, 2000);
}

function getRepositories(username, callback) {
  setTimeout(() => {
    console.log("Calling GitHub API...");
    callback(["repo1", "repo2", "repo3"]);
  }, 2000);
}

getUser(1, (user) => {
  console.log("User", user);
  getRepositories(user.gitHubUsername, (repos) => {
    console.log("Repos", repos);
  });
});

console.log("End");
```

## Promise

Promise adalah sebuah objek yang merepresentasikan keberhasilan atau kegagalan
sebuah event yang asynchronous di masa yang akan datang. Promise memiliki 3
state, yaitu pending, fulfilled, dan rejected. Promise juga memiliki 2 callback,
yaitu resolve dan reject. Resolve digunakan untuk mengubah state dari pending
menjadi fulfilled. Reject digunakan untuk mengubah state dari pending menjadi
rejected. Promise juga memiliki method, yaitu then dan catch. Then digunakan
untuk menangani state fulfilled. Catch digunakan untuk menangani state rejected.

### Contoh Promise

```JavaScript
const p = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve(1);
    reject(new Error("message"));
  }, 2000);
});

p.then((result) => console.log("Result", result)).catch((err) =>
  console.log("Error", err.message)
);
```

### Contoh Promise dengan Asynchronous JavaScript

```JavaScript
console.log("Start");

function getUser(id) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log("Reading a user from a database...");
      resolve({ id: id, gitHubUsername: "ersankarimi" });
    }, 2000);
  });
}

function getRepositories(username) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log("Calling GitHub API...");
      resolve(["repo1", "repo2", "repo3"]);
    }, 2000);
  });
}

getUser(1)
  .then((user) => getRepositories(user.gitHubUsername))
  .then((repos) => console.log("Repos", repos))
  .catch((err) => console.log("Error", err.message));

console.log("End");

```

## Async and Await

Async dan await adalah cara untuk menangani proses asynchronous dengan cara yang
lebih mudah. Async digunakan untuk membuat function menjadi asynchronous. Await
digunakan untuk menunggu proses asynchronous selesai. Await hanya dapat
digunakan di dalam function yang memiliki async. Await hanya dapat digunakan
untuk menangani promise.

### Contoh Async and Await

```JavaScript
console.log("Start");

function getUser(id) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log("Reading a user from a database...");
      resolve({ id: id, gitHubUsername: "ersankarimi" });
    }, 2000);
  });
}

function getRepositories(username) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log("Calling GitHub API...");
      resolve(["repo1", "repo2", "repo3"]);
    }, 2000);
  });
}

async function displayRepositories() {
  try {
    const user = await getUser(1);
    const repos = await getRepositories(user.gitHubUsername);
    console.log("Repos", repos);
  } catch (err) {
    console.log("Error", err.message);
  }
}

displayRepositories();

console.log("End");
```

## Fetch API

Fetch API adalah API yang digunakan untuk mengambil data dari server. Fetch API
menggunakan promise. Fetch API memiliki 2 method, yaitu GET dan POST. Method GET
digunakan untuk mengambil data dari server. Method POST digunakan untuk mengirim
data ke server.

### Contoh Fetch API

```JavaScript
fetch("https://jsonplaceholder.typicode.com/posts")
  .then((response) => response.json())
  .then((json) => console.log(json));
```

### Contoh Fetch API dengan Async and Await

```JavaScript
async function displayPosts() {
  const response = await fetch("https://jsonplaceholder.typicode.com/posts");
  const json = await response.json();
  console.log(json);
}

displayPosts();
```
