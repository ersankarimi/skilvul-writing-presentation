# Materi Minggu 4

## Daftar Isi

1. [Asynchronous JavaScript](#asycnhronous-javascript)
2. [Git & Github Advanced](#git--github-advanced)
3. [Responsive Web Design](#responsive-web-design)
4. [Bootstrap](#bootstrap)

<br>

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

### Promise

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

### Async and Await

Async dan await adalah cara untuk menangani proses asynchronous dengan cara yang
lebih mudah. Async digunakan untuk membuat function menjadi asynchronous. Await
digunakan untuk menunggu proses asynchronous selesai. Await hanya dapat
digunakan di dalam function yang memiliki async. Await hanya dapat digunakan
untuk menangani promise.

#### Contoh Async and Await

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

### Fetch API

Fetch API adalah API yang digunakan untuk mengambil data dari server. Fetch API
menggunakan promise. Fetch API memiliki 2 method, yaitu GET dan POST. Method GET
digunakan untuk mengambil data dari server. Method POST digunakan untuk mengirim
data ke server.

#### Contoh Fetch API

```JavaScript
fetch("https://jsonplaceholder.typicode.com/posts")
  .then((response) => response.json())
  .then((json) => console.log(json));
```

#### Contoh Fetch API dengan Async and Await

```JavaScript
async function displayPosts() {
  const response = await fetch("https://jsonplaceholder.typicode.com/posts");
  const json = await response.json();
  console.log(json);
}

displayPosts();
```

## Git & Github Advanced

### Branch

Branch adalah sebuah cabang dari repository. Branch digunakan untuk
mengembangkan fitur baru tanpa mengganggu branch utama. Branch juga digunakan
untuk mengembangkan fitur baru secara bersamaan. Branch juga digunakan untuk
mengembangkan fitur baru secara bersamaan.

### Merge

Merge adalah sebuah proses untuk menggabungkan branch yang berbeda. Merge hanya
dapat dilakukan jika branch yang akan digabungkan memiliki parent. Merge hanya
dapat dilakukan jika branch yang akan digabungkan memiliki parent.

### Merge Conflict

Merge conflict adalah sebuah kondisi dimana branch yang akan digabungkan
memiliki parent yang berbeda. Merge conflict dapat diatasi dengan menghapus kode
yang tidak diperlukan.

### Rebase

Rebase adalah sebuah proses untuk menggabungkan branch yang berbeda. Rebase
tidak memiliki parent. Rebase tidak memiliki parent.

### Rebase Conflict

Rebase conflict adalah sebuah kondisi dimana branch yang akan digabungkan
memiliki parent yang berbeda. Rebase conflict dapat diatasi dengan menghapus
kode yang tidak diperlukan.

### Pull Request

Pull request adalah sebuah proses untuk menggabungkan branch yang berbeda. Pull
request hanya dapat dilakukan jika branch yang akan digabungkan memiliki parent.
Pull request hanya dapat dilakukan jika branch yang akan digabungkan memiliki
parent.

### Pull Request Conflict

Pull request conflict adalah sebuah kondisi dimana branch yang akan digabungkan
memiliki parent yang berbeda. Pull request conflict dapat diatasi dengan
menghapus kode yang tidak diperlukan.

### Fork

Fork adalah sebuah proses untuk menggabungkan branch yang berbeda. Fork tidak
memiliki parent. Fork tidak memiliki parent.

### Fork Conflict

Fork conflict adalah sebuah kondisi dimana branch yang akan digabungkan memiliki
parent yang berbeda. Fork conflict dapat diatasi dengan menghapus kode yang
tidak diperlukan.

### Clone

Clone adalah sebuah proses untuk menggabungkan branch yang berbeda. Clone tidak
memiliki parent. Clone tidak memiliki parent.

### Clone Conflict

Clone conflict adalah sebuah kondisi dimana branch yang akan digabungkan
memiliki parent yang berbeda. Clone conflict dapat diatasi dengan menghapus kode
yang tidak diperlukan.

### Remote

Remote adalah sebuah proses untuk menggabungkan branch yang berbeda. Remote
tidak memiliki parent. Remote tidak memiliki parent.

### Remote Conflict

Remote conflict adalah sebuah kondisi dimana branch yang akan digabungkan
memiliki parent yang berbeda. Remote conflict dapat diatasi dengan menghapus
kode yang tidak diperlukan.

### Push

Push adalah sebuah proses untuk menggabungkan branch yang berbeda. Push tidak
memiliki parent. Push tidak memiliki parent.

### Push Conflict

Push conflict adalah sebuah kondisi dimana branch yang akan digabungkan memiliki
parent yang berbeda. Push conflict dapat diatasi dengan menghapus kode yang
tidak diperlukan.

### Pull

Pull adalah sebuah proses untuk menggabungkan branch yang berbeda. Pull tidak
memiliki parent. Pull tidak memiliki parent.

### Pull Conflict

Pull conflict adalah sebuah kondisi dimana branch yang akan digabungkan memiliki
parent yang berbeda. Pull conflict dapat diatasi dengan menghapus kode yang
tidak diperlukan.

### Fetch

Fetch adalah sebuah proses untuk menggabungkan branch yang berbeda. Fetch tidak
memiliki parent. Fetch tidak memiliki parent.

### Fetch Conflict

Fetch conflict adalah sebuah kondisi dimana branch yang akan digabungkan
memiliki parent yang berbeda. Fetch conflict dapat diatasi dengan menghapus kode
yang tidak diperlukan.

### Checkout

Checkout adalah sebuah proses untuk menggabungkan branch yang berbeda. Checkout
tidak memiliki parent. Checkout tidak memiliki parent.

### Checkout Conflict

Checkout conflict adalah sebuah kondisi dimana branch yang akan digabungkan
memiliki parent yang berbeda. Checkout conflict dapat diatasi dengan menghapus
kode yang tidak diperlukan.

### Reset

Reset adalah sebuah proses untuk menggabungkan branch yang berbeda. Reset tidak
memiliki parent. Reset tidak memiliki parent.

### Reset Conflict

Reset conflict adalah sebuah kondisi dimana branch yang akan digabungkan
memiliki parent yang berbeda. Reset conflict dapat diatasi dengan menghapus kode
yang tidak diperlukan.

### Revert

Revert adalah sebuah proses untuk menggabungkan branch yang berbeda. Revert
tidak memiliki parent. Revert tidak memiliki parent.

### Revert Conflict

Revert conflict adalah sebuah kondisi dimana branch yang akan digabungkan
memiliki parent yang berbeda. Revert conflict dapat diatasi dengan menghapus
kode yang tidak diperlukan.

### Squash

Squash adalah sebuah proses untuk menggabungkan branch yang berbeda. Squash
tidak memiliki parent. Squash tidak memiliki parent.

### Squash Conflict

Squash conflict adalah sebuah kondisi dimana branch yang akan digabungkan
memiliki parent yang berbeda. Squash conflict dapat diatasi dengan menghapus
kode yang tidak diperlukan.

## Responsive Web Design

Responsive web design adalah sebuah desain web yang dapat menyesuaikan ukuran
layar yang digunakan oleh pengguna. Responsive web design dapat dibuat dengan
menggunakan CSS.

### Media Query

Media query adalah sebuah kode CSS yang dapat menyesuaikan ukuran layar yang
digunakan oleh pengguna. Media query dapat digunakan untuk membuat responsive
web design.

### Mobile First

Mobile first adalah sebuah desain web yang memprioritaskan penggunaan layar
mobile. Mobile first dapat dibuat dengan menggunakan media query.

### Desktop First

Desktop first adalah sebuah desain web yang memprioritaskan penggunaan layar
desktop. Desktop first dapat dibuat dengan menggunakan media query.

### Breakpoint

Breakpoint adalah sebuah titik dimana media query akan berjalan. Breakpoint
dapat dibuat dengan menggunakan media query.

### Contoh Media Query

```
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

### Contoh Breakpoint

```
@media (max-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

## Bootstrap

Bootstrap adalah sebuah framework CSS yang dapat digunakan untuk membuat
responsive web design. Bootstrap dapat digunakan untuk membuat responsive web
design.

### Grid System

Grid system adalah sebuah sistem yang dapat digunakan untuk membuat responsive
web design. Grid system dapat digunakan untuk membuat responsive web design.

### Container

Container adalah sebuah elemen yang dapat digunakan untuk membuat responsive web
design. Container dapat digunakan untuk membuat responsive web design.

### Row

Row adalah sebuah elemen yang dapat digunakan untuk membuat responsive web
design. Row dapat digunakan untuk membuat responsive web design.

### Column

Column adalah sebuah elemen yang dapat digunakan untuk membuat responsive web
design. Column dapat digunakan untuk membuat responsive web design.

### Contoh Grid System

```
<div class="container">
  <div class="row">
    <div class="col-sm-4">
      One of three columns
    </div>
    <div class="col-sm-4">
      One of three columns
    </div>
    <div class="col-sm-4">
      One of three columns
    </div>
  </div>
</div>
```

### Contoh Container

```
<div class="container">
  <h1>My First Bootstrap Page</h1>
  <p>This is some text.</p>
</div>
```

### Contoh Row

```


<div class="container">
  <div class="row">
    <div class="col-sm-4">
      One of three columns
    </div>
    <div class="col-sm-4">
      One of three columns
    </div>
    <div class="col-sm-4">
      One of three columns
    </div>
  </div>
</div>
```

### Contoh Column

```
<div class="container">
  <div class="row">
    <div class="col-sm-4">
      One of three columns
    </div>
    <div class="col-sm-4">
      One of three columns
    </div>
    <div class="col-sm-4">
      One of three columns
    </div>
  </div>
</div>
```

### Contoh Grid System

```
<div class="container">
  <div class="row">
    <div class="col-sm-4">
      One of three columns
    </div>
    <div class="col-sm-4">
      One of three columns
    </div>
    <div class="col-sm-4">
      One of three columns
    </div>
  </div>
</div>
```
