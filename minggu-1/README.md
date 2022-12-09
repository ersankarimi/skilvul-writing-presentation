# Materi Minggu 1

## Daftar Isi

1. [Algorithm and Data Structure](#algorithm-and-data-structure)
2. [UNIX Command Line](#unix-command-line)
3. [Git dan Github Dasar](#git-dan-github-dasar)
4. [HTML](#html)
5. [CSS](#css)
6. [JavaScript](#javscript)

<br>

## Algorithm and Data Structure

### Algorithm

Algorithm atau Algoritma adalah sebuah langkah-langkah yang digunakan untuk
menyelesaikan suatu masalah. Algoritma berfungsi untuk mengubah masalah yang
kompleks menjadi masalah yang lebih sederhana sehingga lebih mudah untuk
diselesaikan. Algoritma juga dapat digunakan untuk menyelesaikan masalah yang
sama secara berulang-ulang.

Contoh algoritma sederhana adalah algoritma untuk menyelesaikan masalah
perhitungan sederhana seperti penjumlahan, pengurangan, perkalian, dan
pembagian.

```
1. Mulai
2. Masukkan angka pertama
3. Masukkan angka kedua
4. Tampilkan hasil penjumlahan dari kedua angka
5. Selesai
```

### Pseudocode

Pseudocode adalah sebuah cara untuk menulis algoritma dengan menggunakan bahasa
yang lebih mudah dimengerti. Pseudocode dapat digunakan untuk menulis algoritma
dengan menggunakan bahasa yang lebih sederhana sehingga lebih mudah dimengerti.
Pseudocode juga dapat digunakan untuk menulis algoritma dengan menggunakan
bahasa yang lebih dekat dengan bahasa manusia.

Contoh pseudocode sederhana adalah pseudocode untuk menyelesaikan masalah
perhitungan sederhana seperti penjumlahan, pengurangan, perkalian, dan
pembagian.

```
START
INPUT angka pertama
INPUT angka kedua
DISPLAY hasil penjumlahan dari kedua angka
END
```

Jenis-jenis Pseudocode :

-   Flowchart
-   Pseudocode

### Data Structure

Data Structure atau Struktur Data adalah sebuah cara untuk menyimpan dan
mengorganisir data. Data Structure dapat digunakan untuk menyimpan data secara
efisien dan mudah diakses. Data Structure juga dapat digunakan untuk
mengelompokkan data yang memiliki hubungan satu sama lain.

Contoh Data Structure sederhana adalah Array. Array adalah sebuah struktur data
yang digunakan untuk menyimpan data secara berurutan. Array dapat digunakan
untuk menyimpan data yang memiliki tipe data yang sama.

```js
var array = [1, 2, 3, 4, 5];

console.log(array[0]); // 1
console.log(array[1]); // 2

array[0] = 6;

console.log(array[0]); // 6

array.push(7);

console.log(array[5]); // 7

array.pop();

console.log(array[5]); // undefined
```

```js
class LinkedList {
    constructor() {
        this.head = null;
        this.tail = null;
    }

    append(value) {
        const newNode = { value: value, next: null };

        if (this.tail) {
            this.tail.next = newNode;
        }

        this.tail = newNode;

        if (!this.head) {
            this.head = newNode;
        }
    }

    prepend(value) {
        const newNode = { value: value, next: this.head };

        this.head = newNode;

        if (!this.tail) {
            this.tail = newNode;
        }
    }

    delete(value) {
        if (!this.head) {
            return;
        }

        while (this.head && this.head.value === value) {
            this.head = this.head.next;
        }

        let currentNode = this.head;

        while (currentNode.next) {
            if (currentNode.next.value === value) {
                currentNode.next = currentNode.next.next;
            } else {
                currentNode = currentNode.next;
            }
        }

        if (this.tail.value === value) {
            this.tail = currentNode;
        }
    }

    find(value) {
        if (!this.head) {
            return;
        }

        let currentNode = this.head;

        while (currentNode) {
            if (currentNode.value === value) {
                return currentNode;
            }

            currentNode = currentNode.next;
        }

        return null;
    }
}

const linkedList = new LinkedList();

linkedList.append(1);
console.log(linkedList.find(1)); // { value: 1, next: null }

linkedList.append(2);
console.log(linkedList.find(2)); // { value: 2, next: null }

linkedList.prepend(3);
console.log(linkedList.find(3)); // { value: 3, next: { value: 1, next: null } }

linkedList.delete(1);
console.log(linkedList.find(1)); // null
```

Jenis-jenis Data Structure :

-   Array
-   Linked List
-   Stack
-   Queue
-   Tree
-   Graph
-   Hash Table
-   Dan lain-lain

### Big O Notation

Big O Notation adalah sebuah cara untuk mengukur kompleksitas dari sebuah
algoritma. Big O Notation digunakan untuk mengukur kompleksitas dari sebuah
algoritma dengan menggunakan notasi matematika. Big O Notation juga digunakan
untuk mengukur kompleksitas dari sebuah algoritma dengan menggunakan notasi
bahasa pemrograman. Big O Notation dapat digunakan untuk mengukur kompleksitas
dari sebuah algoritma dengan menggunakan notasi bahasa pemrograman.

Jenis-jenis Big O Notation :

1.  O(1) : Constant, kompleksitas konstan

        ```
        function printFirstItem(items) {
             console.log(items[0]);
        }
        ```

        Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(1) karena
        tidak terdapat perulangan dan tidak terdapat operasi matematika yang
        kompleks.

2.  O(log n) : Logarithmic, kompleksitas logaritma

        ```
        function binarySearch(items, value) {
            var startIndex = 0,
                stopIndex = items.length - 1,
                middle = Math.floor((stopIndex + startIndex)/2);

            while(items[middle] != value && startIndex < stopIndex){

                //adjust search area
                if (value < items[middle]){
                    stopIndex = middle - 1;
                } else if (value > items[middle]){
                    startIndex = middle + 1;
                }

                //recalculate middle
                middle = Math.floor((stopIndex + startIndex)/2);
            }

            //make sure it's the right value
            return (items[middle] != value) ? -1 : middle;
        }
        ```

        Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(log n)
        karena terdapat perulangan dan operasi matematika yang kompleks.

3.  O(n) : Linear, kompleksitas linear

        ```
        function printAllItems(items) {
            items.forEach(function(item) {
                console.log(item);
            });
        }
        ```

        Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(n)
        karena terdapat perulangan dan operasi matematika yang sederhana.

4.  O(n log n) : Log Linear, kompleksitas log linear

        ```
        function mergeSort(items){

            //split the array into halves and merge them recursively
            if (items.length < 2) {
                return items;
            }

            var middle = Math.floor(items.length / 2),
                left   = items.slice(0, middle),
                right  = items.slice(middle);

            return merge(mergeSort(left), mergeSort(right));
        }

        //merges two sorted arrays
        function merge(left, right){
            var result = [];

            while (left.length && right.length) {
                if (left[0] <= right[0]) {
                    result.push(left.shift());
                } else {
                    result.push(right.shift());
                }
            }

            while (left.length)
                result.push(left.shift());

            while (right.length)
                result.push(right.shift());

            return result;
        }
        ```
        Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(n log n) karena terdapat perulangan dan operasi matematika yang kompleks. Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(n log n) karena terdapat perulangan dan operasi matematika yang kompleks.

5.  O(n^2) : Quadratic, kompleksitas kuadrat

        ```
        function printAllPossibleOrderedPairs(items) {
            items.forEach(function(firstItem) {
                items.forEach(function(secondItem) {
                    console.log(firstItem, secondItem);
                });
            });
        }
        ```
        Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(n^2) karena terdapat perulangan dan operasi matematika yang kompleks. Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(n^2) karena terdapat perulangan dan operasi matematika yang kompleks.

6.  O(2^n) : Exponential, kompleksitas eksponensial

        ```
        function fibonacci(n) {
            if (n < 2) {
                return n;
            }

            return fibonacci(n - 1) + fibonacci(n - 2);
        }
        ```
        Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(2^n) karena terdapat perulangan dan operasi matematika yang kompleks. Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(2^n) karena terdapat perulangan dan operasi matematika yang kompleks.

7.  O(n!) : Factorial, kompleksitas faktorial

        ```
        function printAllPermutations(items) {
            var permutationItems = items.slice(); //clone array

            //base case
            if (permutationItems.length === 0) {
                console.log(permutationItems);
            } else {
                //for each item in the array
                for (var i = 0; i < permutationItems.length; i++) {
                    var currentItem = permutationItems.splice(i, 1); //remove current item

                    //recurse over the rest of array
                    printAllPermutations(permutationItems.slice());

                    permutationItems.splice(i, 0, currentItem[0]); //put item back
                }
            }
        }
        ```
        Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(n!) karena terdapat perulangan dan operasi matematika yang kompleks. Pada contoh diatas, kompleksitas dari algoritma tersebut adalah O(n!) karena terdapat perulangan dan operasi matematika yang kompleks.

## Unix Command Line

### Command Line Interface

Command Line Interface (CLI) adalah sebuah antarmuka yang memungkinkan pengguna
untuk berinteraksi dengan sistem operasi menggunakan baris perintah.

### Shell

Shell adalah sebuah program yang membaca baris perintah yang dimasukkan oleh
pengguna dan menjalankannya. Shell juga dapat membaca baris perintah dari sebuah
file dan menjalankannya.

### Contoh-Contoh Command Line Interface

-   bash
-   zsh
-   cmd
-   sh

### Contoh Perintah Command Line Interface

Berikut beberapa perintah yang sering digunakan pada Command Line Interface,
antara lain :

#### Navigasi

-   `cd` : untuk berpindah direktori
-   `ls` : untuk melihat isi direktori
-   `pwd` : untuk melihat direktori yang sedang aktif

#### Manipulasi File

-   `touch` : untuk membuat file
-   `mkdir` : untuk membuat direktori
-   `rm` : untuk menghapus file

#### Melihat isi file

-   `cat` : untuk melihat isi file
-   `tail` : untuk melihat beberapa line awal dari sebuah file text
-   `head` : untuk melihat beberapa line awal dari sebuah file text
-   `grep` : untuk mencari kata pada sebuah file

## Tambahan

#### Relative Path

-   Relative path adalah path yang berhubungan dengan direktori yang sedang
    aktif.

    `/Users/user/Work/GitHub/skilvul/tugas`

#### Absolute Path

-   Absolute path adalah path yang berhubungan dengan root direktori.

    `./catatan`

## Git dan Github Dasar

### Version Control System

Version Control adalah sebuah system yang merekam perubahan pada file dari waktu
ke waktu, sehingga kita bisa melihat versi sebelumnya jika diinginkan.

Version Control sangat populer dikalangan programmer, karena programmer selalu
membuat kode program dalam bentuk kode tulisan. Dengan version control,
programmer bisa merekam semua perubahan yang terjadi, sehingga jika terjadi
kesalahan, programmer bisa dengan mudah kembali ke versi sebelumnya.

Ada beberapa contoh version control dan salah satu yang paling populer
dikalangan programmer adalah Git.

### Git

Git merupakan salah satu Version Control System (VCS) yang paling populer saat
ini. Git merupakan salah satu VCS yang bersifat distributed, artinya setiap
developer memiliki salinan lengkap dari repository.

### Github

Github merupakan layanan hosting untuk Git repository. Github menyediakan
layanan hosting gratis untuk repository publik dan berbayar untuk repository
pribadi. Github juga menyediakan fitur untuk kolaborasi antar developer yang
memudahkan tiap programmer untuk berkolaborasi dengan programmer lainnya.

## Alur Kerja Git

Alur kerja Git dapat dilihat pada gambar berikut:

1. Inisialisasi dulu folder proyek kita sebagai Git repository dengan perintah
   `git init`.
2. Kemudian kita buat file-file yang dibutuhkan untuk proyek kita.
3. Setelah itu kita tambahkan file-file tersebut ke dalam staging area dengan
   perintah `git add`.
4. Setelah itu kita commit file-file tersebut ke dalam repository dengan
   perintah `git commit`.
5. Setelah itu kita push file-file tersebut ke Github dengan perintah
   `git push`. Tapi sebelumnya kita harus membuat repository di Github terlebih
   dahulu lalu kita tambahkan remote repository dengan perintah
   `git remote add <nama-remote> <url-repository>`. Jika sudah, kita bisa push
   file-file tersebut ke Github dengan perintah
   `git push -u <nama-remote> <nama-branch>`.
6.

### Kenapa Git dan Github Penting

Git dan Github sangat penting untuk developer karena Git dan Github memudahkan
developer untuk berkolaborasi dengan programmer lainnya. Selain itu, Git dan
Github juga memudahkan developer untuk mengembangkan aplikasi dengan cara yang
terstruktur dan terorganisir.

### Cara Menggunakan Git dan Github

Berikut adalah langkah-langkah untuk menggunakan Git dan Github:

1. Pastikan git sudah terinstall di komputer kamu. Kamu bisa cek dengan
   mengetikkan perintah `git --version` di terminal. Jika sudah terinstall, maka
   akan muncul versi git yang terinstall di komputer kamu. Jika belum bisa
   mmenginstall git, kamu bisa mengikuti tutorial berikut ini:
   https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
2. Buat akun di Github. Kamu bisa mengikuti tutorial berikut ini:
   https://docs.github.com/en/github/getting-started-with-github/signing-up-for-a-new-github-account.
3. Buat repository baru di Github. Kamu bisa mengikuti tutorial berikut ini:
   https://docs.github.com/en/github/getting-started-with-github/create-a-repo
4. Clone repository yang sudah kamu buat di Github ke komputer kamu atau kita
   bisa push repository yang sudah ada di komputer kamu ke Github dengan
   mengintergrasikannya dengan repository yang sudah kita buat di Github
   menggunakan `git remote`.

## HTML

### HTML

HTML adalah singkatan dari HyperText Markup Language. HTML adalah bahasa yang
digunakan untuk membuat halaman web. HTML merupakan bahasa markup, artinya HTML
tidak memiliki fitur pemrograman seperti variabel, fungsi, dan lain sebagainya.
HTML hanya digunakan untuk menandai elemen-elemen yang ada di dalam halaman web.
HTML terdiri dari tag-tag yang digunakan untuk menandai elemen-elemen tersebut.

### Tag HTML

Tag HTML adalah sebuah elemen yang digunakan untuk menandai elemen-elemen yang
ada di dalam halaman web. Tag HTML terdiri dari tag pembuka dan tag penutup. Tag
pembuka digunakan untuk menandai awal dari sebuah elemen, sedangkan tag penutup
digunakan untuk menandai akhir dari sebuah elemen.

Ada 2 jenis tag HTML yaitu, tag yang bersifat self-closing dan tag yang tidak
bersifat self-closing. Tag yang bersifat self-closing adalah tag yang tidak
memiliki tag penutup. Tag yang tidak bersifat self-closing adalah tag yang
memiliki tag penutup.

Cara membuat tag html adalah sebagai berikut `<tagname> isi tag </tagname>`

### Attribute HTML

Atribut HTML adalah sebuah informasi tambahan yang diberikan pada sebuah tag
HTML. Atribut HTML diletakkan di dalam tag pembuka. Atribut HTML terdiri dari
nama atribut dan nilai atribut. Nama atribut digunakan untuk menandai informasi
apa yang akan diberikan, sedangkan nilai atribut digunakan untuk menandai nilai
dari informasi tersebut. Cara membuat atribut HTML adalah sebagai berikut
`<tagname atribut="nilai atribut"> isi tag </tagname>`.

Contoh atribut HTML adalah sebagai berikut:

-   `id` digunakan untuk menandai id dari sebuah elemen.
-   `class` digunakan untuk menandai kelas dari sebuah elemen.
-   `src` digunakan untuk menandai sumber dari sebuah elemen.
-   `href` digunakan untuk menandai link dari sebuah elemen.
-   `alt` digunakan untuk menandai alternatif dari sebuah elemen. Dan masih
    banyak lagi yang lainnya

### Basic Tag HTML

Ada basic tag HTML yang harus kamu ketahui, yaitu:

-   `<!DOCTYPE html>` mendefinisikan bahwa dokumen ini adalah dokumen HTML5
-   `<html></html>` digunakan untuk menandai awal dari sebuah halaman web.
-   `<head></head>` digunakan untuk menandai bagian dari halaman web yang tidak
    akan ditampilkan di browser.
-   `<title></title>` digunakan untuk menandai judul dari halaman web.
-   `<body></body>` digunakan untuk menandai bagian dari halaman web yang akan
    ditampilkan di browser.

Struktur dasar dari sebuah halaman web adalah sebagai berikut:

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Judul halaman</title>
    </head>
    <body>
        isi halaman
    </body>
</html>
```

### Contoh Tag HTML

#### Heading

Heading adalah sebuah tag yang digunakan untuk menandai judul dari sebuah
halaman web. Heading terdiri dari 6 jenis yaitu, h1, h2, h3, h4, h5, dan h6.
Heading memiliki tingkat kepentingan yang berbeda-beda. Heading dengan tingkat
kepentingan yang lebih tinggi akan memiliki ukuran font yang lebih besar
daripada heading dengan tingkat kepentingan yang lebih rendah.

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

#### Paragraph

Paragraph adalah sebuah tag yang digunakan untuk menandai sebuah paragraf.
Paragraph memiliki tingkat kepentingan yang sama dengan heading.

```html
<p>Paragraph</p>
```

#### Link

Link adalah sebuah tag yang digunakan untuk menandai sebuah link. Link memiliki
tingkat kepentingan yang sama dengan heading.

```html
<a href="https://google.com">Google</a>
```

#### Image

Image adalah sebuah tag yang digunakan untuk menandai sebuah gambar. Image
memiliki tingkat kepentingan yang sama dengan heading.

```html
<img
    src="https://www.google.com/images/branding/googlelogo/1x/googlelogo_color_272x92dp.png"
    alt="Google Logo"
/>
```

#### List

List adalah sebuah tag yang digunakan untuk menandai sebuah list. List memiliki
tingkat kepentingan yang sama dengan heading. List terdiri dari 2 jenis yaitu,
ordered list dan unordered list. Ordered list adalah list yang berurutan,
sedangkan unordered list adalah list yang tidak berurutan.

```html
<!-- Ordered List -->
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>

<!-- Unordered List -->
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

#### Table

Table adalah sebuah tag yang digunakan untuk menandai sebuah tabel. Table
memiliki tingkat kepentingan yang sama dengan heading. Table terdiri dari 2
jenis yaitu, table header dan table data. Table header adalah bagian dari tabel
yang berisi judul dari tabel, sedangkan table data adalah bagian dari tabel yang
berisi data dari tabel.

```html
<table>
    <tr>
        <th>Header 1</th>
        <th>Header 2</th>
        <th>Header 3</th>
    </tr>
    <tr>
        <td>Data 1</td>
        <td>Data 2</td>
        <td>Data 3</td>
    </tr>
</table>
```

#### Form

Form adalah sebuah tag yang digunakan untuk menandai sebuah form. Form memiliki
tingkat kepentingan yang sama dengan heading. Form terdiri dari 2 jenis yaitu,
input dan button. Input adalah sebuah elemen yang digunakan untuk menandai
sebuah inputan, sedangkan button adalah sebuah elemen yang digunakan untuk
menandai sebuah tombol.

```html
<form>
    <input type="text" placeholder="Input" />
    <button type="submit">Submit</button>
</form>
```

#### Div dan Span

Div mendefinisikan divisi atau bagian dalam dokumen HTML. Div tag digunakan
sebagai wadah untuk elemen HTML - yang kemudian ditata dengan CSS atau
dimanipulasi dengan JavaScript. Div tag is easily styled by using the class or
id attribute.

Span mendefinisikan sebuah bagian dalam dokumen HTML. Span tag digunakan untuk
mengelompokkan elemen inline dan untuk memberikan gaya CSS (dengan menggunakan
class atau id atribut) atau untuk manipulasi elemen dengan JavaScript.

```html
<div>Div</div>
<span>Span</span>
```

#### Semantic HTML

Semantic HTML adalah sebuah tag yang digunakan untuk menandai sebuah elemen
HTML. Tag HTML yang digunakan untuk menandai sebuah elemen HTML disebut dengan
tag HTML semantik. Tag HTML semantik memiliki tingkat kepentingan yang sama
dengan heading. Tag HTML semantik terdiri dari 5 jenis yaitu, header, footer,
main, section, dan article.

```html
<header>Header</header>
<footer>Footer</footer>
<main>Main</main>
<section>Section</section>
<article>Article</article>
```

### Deploy HTML

Untuk deploy HTML, kita bisa menggunakan beberapa cara, yaitu:

-   Deploy dengan menggunakan Github Pages
-   Deploy dengan menggunakan Netlify
-   Deploy dengan menggunakan Vercel

Dan masih banyak lagi cara deploy HTML lainnya.

<br>

## CSS

CSS adalah singkatan dari Cascading Style Sheets. CSS adalah sebuah bahasa yang
digunakan untuk mengatur tampilan dari sebuah halaman web.

### Peran CSS

CSS memiliki peran yang sangat penting dalam pembuatan sebuah halaman web. CSS
digunakan untuk mengatur tampilan dari sebuah halaman web. CSS memiliki 3 peran
yaitu,

-   Mengatur tampilan dari sebuah halaman web
-   Mengatur posisi dari sebuah halaman web
-   Mengatur animasi dari sebuah halaman web
-   Mengatur posisi dari sebuah halaman web

### Cara Menyisipkan CSS ke HTML

CSS memiliki 3 jenis yaitu, inline CSS, internal CSS, dan external CSS. Inline
CSS adalah CSS yang ditulis langsung di dalam tag HTML, internal CSS adalah CSS
yang ditulis di dalam tag HTML, dan external CSS adalah CSS yang ditulis di
dalam file terpisah.

### Sintaks Dasar CSS

CSS memiliki 3 jenis yaitu, selector, property, dan value. Selector adalah
sebuah elemen HTML yang akan diberikan style, property adalah sebuah style yang
akan diberikan ke sebuah elemen HTML, dan value adalah sebuah nilai dari sebuah
style.

```css
selector {
    property: value;
}
```

### Responsive Web Design CSS

Responsive Web Design adalah sebuah teknik yang digunakan untuk membuat sebuah
website agar dapat menyesuaikan dengan ukuran layar yang berbeda. Responsive Web
Design menggunakan 3 jenis yaitu, viewport, media query, dan flexbox.

#### Viewport

Viewport adalah sebuah elemen HTML yang digunakan untuk menentukan ukuran layar
yang akan digunakan untuk menampilkan sebuah website. Viewport memiliki 2 jenis
yaitu, viewport width dan viewport height. Viewport width adalah sebuah elemen
HTML yang digunakan untuk menentukan lebar layar yang akan digunakan untuk
menampilkan sebuah website, sedangkan viewport height adalah sebuah elemen HTML
yang digunakan untuk menentukan tinggi layar yang akan digunakan untuk
menampilkan sebuah website.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

#### Media Query

Media query adalah sebuah aturan CSS yang digunakan untuk menentukan ukuran
layar yang akan digunakan untuk menampilkan sebuah website. Media query memiliki
2 jenis yaitu, media query width dan media query height. Media query width
adalah sebuah aturan CSS yang digunakan untuk menentukan lebar layar yang akan
digunakan untuk menampilkan sebuah website, sedangkan media query height adalah
sebuah aturan CSS yang digunakan untuk menentukan tinggi layar yang akan
digunakan untuk menampilkan sebuah website.

```css
@media screen and (max-width: 600px) {
    body {
        background-color: red;
    }
}
```

#### Flexbox

Flexbox adalah sebuah aturan CSS yang digunakan untuk membuat sebuah elemen HTML
menjadi responsive. Flexbox memiliki 2 jenis yaitu, flex container dan flex
item. Flex container adalah sebuah elemen HTML yang digunakan untuk menentukan
sebuah elemen HTML menjadi responsive, sedangkan flex item adalah sebuah elemen
HTML yang digunakan untuk menentukan sebuah elemen HTML menjadi responsive.

```css
.flex-container {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    align-items: center;
    align-content: center;
}
```

<br>

## Javscript

Javascript adalah sebuah bahasa pemrograman yang digunakan untuk membuat sebuah
website menjadi interaktif. Javascript memiliki 3 jenis yaitu, DOM, event, dan
function.

### Variabel

Variabel adalah sebuah tempat untuk menyimpan sebuah nilai. Variabel memiliki 3
jenis yaitu, var, let, dan const. Var adalah sebuah variabel yang dapat
digunakan untuk menyimpan sebuah nilai, let adalah sebuah variabel yang dapat
digunakan untuk menyimpan sebuah nilai, dan const adalah sebuah variabel yang
dapat digunakan untuk menyimpan sebuah nilai.

```javascript
var nama = "Ersan Karimi";
let nama = "Ersan Karimi";
const nama = "Ersan Karimi";
```

### Operator

Operator adalah sebuah simbol yang digunakan untuk melakukan operasi matematika.
Operator memiliki 3 jenis yaitu, aritmatika, perbandingan, dan logika. Operator
aritmatika adalah sebuah simbol yang digunakan untuk melakukan operasi
matematika, operator perbandingan adalah sebuah simbol yang digunakan untuk
melakukan operasi perbandingan, dan operator logika adalah sebuah simbol yang
digunakan untuk melakukan operasi logika.

```javascript
var a = 10;
var b = 5;
var c = a + b;
var d = a - b;
var e = a * b;
var f = a / b;
var g = a % b;
var h = a == b;
var i = a != b;
var j = a > b;
var k = a < b;
var l = a >= b;
var m = a <= b;
var n = a && b;
var o = a || b;
```

### Array

Array adalah sebuah variabel yang dapat digunakan untuk menyimpan banyak nilai.
Array memiliki 3 jenis yaitu, array index, array length, dan array method. Array
index adalah sebuah variabel yang dapat digunakan untuk menyimpan banyak nilai,
array length adalah sebuah variabel yang dapat digunakan untuk menyimpan banyak
nilai, dan array method adalah sebuah variabel yang dapat digunakan untuk
menyimpan banyak nilai.

```javascript
var nama = ["Ersan", "Karimi"];
var nama = new Array("Ersan", "Karimi");
```

### Object

Object adalah sebuah variabel yang dapat digunakan untuk menyimpan banyak nilai.
Object memiliki 3 jenis yaitu, object property, object method, dan object
constructor. Object property adalah sebuah variabel yang dapat digunakan untuk
menyimpan banyak nilai, object method adalah sebuah variabel yang dapat
digunakan untuk menyimpan banyak nilai, dan object constructor adalah sebuah
variabel yang dapat digunakan untuk menyimpan banyak nilai.

```javascript
var nama = {
    namaDepan: "Ersan",
    namaBelakang: "Karimi",
};
```

### Looping

Looping adalah sebuah perulangan yang digunakan untuk melakukan perulangan.
Looping memiliki 3 jenis yaitu, for, while, dan do while. For adalah sebuah
perulangan yang digunakan untuk melakukan perulangan, while adalah sebuah
perulangan yang digunakan untuk melakukan perulangan, dan do while adalah sebuah
perulangan yang digunakan untuk melakukan perulangan.

```javascript
for (var i = 0; i < 10; i++) {
    console.log(i);
}

// while loop
var i = 0;
while (i < 10) {
    console.log(i);
    i++;
}

// do while loop
var i = 0;
do {
    console.log(i);
    i++;
} while (i < 10);
```

### Conditional

Conditional adalah sebuah kondisi yang digunakan untuk menentukan sebuah
kondisi. Conditional memiliki 3 jenis yaitu, if, else if, dan else. If adalah
sebuah kondisi yang digunakan untuk menentukan sebuah kondisi, else if adalah
sebuah kondisi yang digunakan untuk menentukan sebuah kondisi, dan else adalah
sebuah kondisi yang digunakan untuk menentukan sebuah kondisi.

```javascript
var a = 10;
var b = 5;
if (a > b) {
    console.log("a lebih besar dari b");
} else if (a < b) {
    console.log("a lebih kecil dari b");
} else {
    console.log("a sama dengan b");
}
```

### Ternary Operator

Ternary Operator adalah sebuah operator yang digunakan untuk menentukan sebuah
kondisi. Ternary Operator memiliki 3 jenis yaitu, if, else if, dan else. If
adalah sebuah operator yang digunakan untuk menentukan sebuah kondisi, else if
adalah sebuah operator yang digunakan untuk menentukan sebuah kondisi, dan else
adalah sebuah operator yang digunakan untuk menentukan sebuah kondisi.

```javascript
var a = 10;
var b = 5;
var c = a > b ? "a lebih besar dari b" : "a lebih kecil dari b";
```

### Short Circuit

Short Circuit adalah sebuah kondisi yang digunakan untuk menentukan sebuah
kondisi.

```javascript
var a = 10;
var b = 5;
var c = a > b && "a lebih besar dari b";

var d = a < b || "a lebih kecil dari b";
```

### Function

Function adalah sebuah fungsi yang digunakan untuk melakukan sebuah fungsi.
Function memiliki 3 jenis yaitu, function declaration, function expression, dan
arrow function. Function declaration adalah sebuah fungsi yang digunakan untuk
melakukan sebuah fungsi, function expression adalah sebuah fungsi yang digunakan
untuk melakukan sebuah fungsi, dan arrow function adalah sebuah fungsi yang
digunakan untuk melakukan sebuah fungsi.

```javascript
function nama() {
    console.log("Ersan Karimi");
}

var nama = function () {
    console.log("Ersan Karimi");
};

var nama = () => {
    console.log("Ersan Karimi");
};
```

### Scope

Scope adalah sebuah variabel yang digunakan untuk menentukan sebuah variabel.
Scope memiliki 3 jenis yaitu, global scope, local scope, dan block scope. Global
scope adalah sebuah variabel yang digunakan untuk menentukan sebuah variabel,
local scope adalah sebuah variabel yang digunakan untuk menentukan sebuah
variabel, dan block scope adalah sebuah variabel yang digunakan untuk menentukan
sebuah variabel.

```javascript
var a = 10;
function nama() {
    var b = 5;
    console.log(a);
    console.log(b);
}
nama();
console.log(a);
console.log(b);
```

### Data Type Built-in Function

Data Type Built-in Function adalah sebuah fungsi yang digunakan untuk menentukan
sebuah fungsi. Data Type Built-in Function memiliki 3 jenis yaitu, string,
number, dan boolean. String adalah sebuah fungsi yang digunakan untuk menentukan
sebuah fungsi, number adalah sebuah fungsi yang digunakan untuk menentukan
sebuah fungsi, dan boolean adalah sebuah fungsi yang digunakan untuk menentukan
sebuah fungsi.

```javascript
var a = "Ersan Karimi";
var b = 10;
var c = true;
console.log(a.length);
console.log(b.toFixed(2));
console.log(c.toString());
```

### DOM

DOM adalah sebuah fungsi yang digunakan untuk menentukan sebuah fungsi. DOM
memiliki 3 jenis yaitu, document, element, dan event. Document adalah sebuah
fungsi yang digunakan untuk menentukan sebuah fungsi, element adalah sebuah
fungsi yang digunakan untuk menentukan sebuah fungsi, dan event adalah sebuah
fungsi yang digunakan untuk menentukan sebuah fungsi.

```javascript
var a = document.getElementById("nama");
var b = document.getElementsByTagName("p");
var c = document.getElementsByClassName("nama");
var d = document.querySelector("#nama");
var e = document.querySelectorAll(".nama");
var f = document.createElement("p");
var g = document.createTextNode("Ersan Karimi");
var h = document.createAttribute("class");
```

### Event

Event adalah sebuah fungsi yang digunakan untuk menentukan sebuah fungsi. Event
memiliki 3 jenis yaitu, event listener, event handler, dan event object. Event
listener adalah sebuah fungsi yang digunakan untuk menentukan sebuah fungsi,
event handler adalah sebuah fungsi yang digunakan untuk menentukan sebuah
fungsi, dan event object adalah sebuah fungsi yang digunakan untuk menentukan
sebuah fungsi.

```javascript
var a = document.getElementById("nama");
a.addEventListener("click", function () {
    console.log("Ersan Karimi");
});
```
