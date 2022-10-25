# Materi Minggu 5

## Daftar Isi

1. [Node JS](#node-js)
2. [Intro to React](#intro-to-react)
3. [JSX](#jsx)
4. [React Components](#react-components)

<br>

## Node JS

Node.js adalah sebuah runtime environment yang berjalan di atas engine V8 milik
Google. Node.js memungkinkan kita untuk menjalankan JavaScript di luar browser.
Node.js juga memungkinkan kita untuk membuat aplikasi web server, aplikasi CLI,
dan aplikasi desktop.

### Instalasi Node JS

Untuk menginstall Node JS, silahkan download terlebih dahulu di
[sini](https://nodejs.org/en/download/). Setelah itu, install sesuai dengan OS
yang digunakan.

### Inisialisasi Project Node JS

Untuk membuat project Node JS, silahkan buat folder baru dengan nama project
yang diinginkan. Setelah itu, buka terminal dan masuk ke dalam folder tersebut.
Kemudian, jalankan perintah berikut:

```bash
npm init
```

Perintah di atas akan membuat file `package.json` yang berisi informasi mengenai
project yang dibuat. File `package.json` ini akan dibutuhkan ketika kita ingin
menginstall package/package lainnya. Setelah itu, kita bisa menambahkan file
`index.js` yang berisi kode JavaScript yang akan dijalankan. Untuk menjalankan
kode JavaScript yang ada di dalam file `index.js`, silahkan jalankan perintah
berikut:

```bash
node index.js
```

### Menginstall Package

Untuk menginstall package/package, silahkan jalankan perintah berikut:

```bash
npm install <nama_package>
```

Contoh:

```bash
npm install tailwindcss
```

<br>

## Intro to React

React adalah sebuah library JavaScript yang digunakan untuk membuat user
interface. React dibuat oleh Facebook dan sekarang sudah menjadi salah satu
library JavaScript yang paling populer. React memungkinkan kita untuk membuat
aplikasi web dengan mudah dan cepat.

### Instalasi React JS

Untuk menginstall React JS, silahkan jalankan perintah berikut:

```bash
npm install -g create-react-app
```

### Membuat Project React JS

Untuk membuat project React JS, silahkan jalankan perintah berikut:

```bash
npx create-react-app <nama_project>
```

Contoh:

```bash
npx create-react-app my-app
```

### Menjalankan Project React JS

Untuk menjalankan project React JS, silahkan masuk ke dalam folder project
tersebut dan jalankan perintah berikut:

```bash
npm start
```

### Struktur Project React JS

Setelah menjalankan perintah `npm start`, maka akan muncul tampilan seperti
berikut:

![image](https://user-images.githubusercontent.com/25836292/136666909-4e4a4f4a-1b6f-4d4d-9d7a-4a9c9d6c7f2d.png)

Pada gambar di atas, terdapat beberapa folder dan file yang akan kita bahas satu
persatu:

1. `node_modules`: Folder ini berisi package-package yang dibutuhkan oleh
   project React JS. Folder ini akan dibuat ketika kita menjalankan perintah
   `npm install` atau `npm start`.
2. `public`: Folder ini berisi file-file yang akan diakses oleh browser. Folder
   ini akan dibuat ketika kita menjalankan perintah
   `npx create-react-app <nama_project>`.
3. `src`: Folder ini berisi file-file yang akan diakses oleh browser. Folder ini
   akan dibuat ketika kita menjalankan perintah
   `npx create-react-app <nama_project>`.
4. `package.json`: File ini berisi informasi mengenai project React JS. File ini
   akan dibuat ketika kita menjalankan perintah `npm init` atau
   `npx create-react-app <nama_project>`.
5. `package-lock.json`: File ini berisi informasi mengenai package-package yang
   dibutuhkan oleh project React JS. File ini akan dibuat ketika kita
   menjalankan perintah `npm install` atau `npm start`.
6. `README.md`: File ini berisi informasi mengenai project React JS. File ini
   akan dibuat ketika kita menjalankan perintah
   `npx create-react-app <nama_project>`.

## JSX

JSX adalah sintaks yang digunakan untuk menuliskan kode React. JSX adalah
gabungan dari HTML dan JavaScript. JSX memungkinkan kita untuk menuliskan kode
React dengan lebih mudah dan cepat.

### Contoh JSX

Berikut adalah contoh kode JSX:

```jsx
import React from "react";

const App = () => {
  return (
    <div>
      <h1>Hello World</h1>
    </div>
  );
};

export default App;
```

### Render JSX

Untuk menampilkan kode JSX, kita bisa menggunakan fungsi `ReactDOM.render()`.
Fungsi `ReactDOM.render()` membutuhkan dua parameter, yaitu kode JSX dan elemen
HTML yang akan menampilkan kode JSX tersebut. Berikut adalah contoh penggunaan
fungsi `ReactDOM.render()`:

### JSX vs HTML

JSX mirip dengan HTML, namun ada beberapa perbedaan antara JSX dan HTML. Berikut
adalah perbedaan antara JSX dan HTML:

1. JSX menggunakan camelCase untuk penamaan atribut, sedangkan HTML menggunakan
   kebab-case.
2. JSX menggunakan tanda kurung kurawal `{}` untuk menuliskan JavaScript,
   sedangkan HTML tidak menggunakan tanda kurung kurawal `{}` untuk menuliskan
   JavaScript.
3. JSX menggunakan tanda kurung kurawal `{}` untuk menuliskan JavaScript
   expression, sedangkan HTML tidak menggunakan tanda kurung kurawal `{}` untuk
   menuliskan JavaScript expression.
4. JSX menggunakan tanda kurung kurawal `{}` untuk menuliskan JavaScript
   statement, sedangkan HTML tidak menggunakan tanda kurung kurawal `{}` untuk
   menuliskan JavaScript statement.
5. JSX menggunakan tanda kurung kurawal `{}` untuk menuliskan JavaScript object,
   sedangkan HTML tidak menggunakan tanda kurung kurawal `{}` untuk menuliskan
   JavaScript object.
6. JSX menggunakan tanda kurung kurawal `{}` untuk menuliskan JavaScript array,
   sedangkan HTML tidak menggunakan tanda kurung kurawal `{}` untuk menuliskan
   JavaScript array.

## React Component

React Component adalah sebuah fungsi atau kelas yang mengembalikan kode JSX.
React Component memungkinkan kita untuk memisahkan kode JSX menjadi beberapa
bagian yang lebih kecil. React Component memungkinkan kita untuk membuat
komponen-komponen yang dapat digunakan kembali.

### Membuat React Component

Untuk membuat React Component, kita bisa menggunakan fungsi atau kelas. Berikut
adalah contoh penggunaan fungsi dan kelas untuk membuat React Component:

#### Fungsi

```jsx
import React from "react";

const App = () => {
  return (
    <div>
      <h1>Hello World</h1>
    </div>
  );
};

export default App;
```

#### Kelas

```jsx
import React from "react";

class App extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello World</h1>
      </div>
    );
  }
}

export default App;
```

### Menggunakan React Component

Untuk menggunakan React Component, kita bisa menggunakan tag HTML. Berikut
adalah contoh penggunaan React Component:

```jsx
import React from "react";
import App from "./App";

const Main = () => {
  return (
    <div>
      <App />
    </div>
  );
};

export default Main;
```

## Props

Props adalah sebuah object yang berisi data yang akan digunakan oleh React
Component. Props memungkinkan kita untuk mengirimkan data dari React Component
ke React Component lainnya. Props memungkinkan kita untuk membuat React
Component yang dapat digunakan kembali.

### Mengirimkan Props

Untuk mengirimkan Props, kita bisa menggunakan atribut HTML. Berikut adalah
contoh penggunaan Props:

```jsx
import React from "react";
import App from "./App";

const Main = () => {
  return (
    <div>
      <App title="Hello World" />
    </div>
  );
};

export default Main;
```

### Menerima Props

Untuk menerima Props, kita bisa menggunakan parameter fungsi atau parameter
kelas. Berikut adalah contoh penggunaan Props:

#### Fungsi

```jsx
import React from "react";

const App = (props) => {
  return (
    <div>
      <h1>{props.title}</h1>
    </div>
  );
};

export default App;
```

#### Kelas

```jsx
import React from "react";

class App extends React.Component {
  render() {
    return (
      <div>
        <h1>{this.props.title}</h1>
      </div>
    );
  }
}

export default App;
```

## State

State adalah sebuah object yang berisi data yang akan digunakan oleh React
Component. State memungkinkan kita untuk membuat React Component yang dapat
berubah-ubah. State memungkinkan kita untuk membuat React Component yang
interaktif.

### Membuat State

Untuk membuat State, kita bisa menggunakan fungsi `useState()`. Fungsi
`useState()` membutuhkan satu parameter, yaitu nilai awal dari State. Berikut
adalah contoh penggunaan fungsi `useState()`:

```jsx
import React, { useState } from "react";

const App = () => {
  const [count, setCount] = useState(0);

  return (
    <div>
      <h1>{count}</h1>
    </div>
  );
};

export default App;
```

### Mengubah State

Untuk mengubah State, kita bisa menggunakan fungsi `setCount()`. Fungsi
`setCount()` membutuhkan satu parameter, yaitu nilai baru dari State. Berikut
adalah contoh penggunaan fungsi `setCount()`:

```jsx
import React, { useState } from "react";

const App = () => {
  const [count, setCount] = useState(0);

  return (
    <div>
      <h1>{count}</h1>
      <button onClick={() => setCount(count + 1)}>Tambah</button>
    </div>
  );
};

export default App;
```

## Lifecycle

Lifecycle adalah sebuah proses yang berjalan secara otomatis pada React
Component. Lifecycle memungkinkan kita untuk melakukan sesuatu pada React
Component sebelum React Component ditampilkan pada layar, sesudah React
Component ditampilkan pada layar, sebelum React Component dihapus dari layar,
dan sesudah React Component dihapus dari layar.

### Lifecycle pada Fungsi

Lifecycle pada fungsi mempunyai 3 fase, yaitu:

1. Mounting
2. Updating
3. Unmounting

#### Mounting

Mounting adalah sebuah proses yang berjalan secara otomatis pada React Component
sebelum React Component ditampilkan pada layar. Mounting mempunyai 3 fase,
yaitu:

1. Fase pertama: `constructor()`
2. Fase kedua: `render()`
3. Fase ketiga: `componentDidMount()`

#### Updating

Updating adalah sebuah proses yang berjalan secara otomatis pada React Component
sesudah React Component ditampilkan pada layar. Updating mempunyai 3 fase,
yaitu:

1. Fase pertama: `render()`
2. Fase kedua: `componentDidUpdate()`
3. Fase ketiga: `componentDidUpdate()`

#### Unmounting

Unmounting adalah sebuah proses yang berjalan secara otomatis pada React
Component sebelum React Component dihapus dari layar. Unmounting mempunyai 1
fase, yaitu:

1. Fase pertama: `componentWillUnmount()`
