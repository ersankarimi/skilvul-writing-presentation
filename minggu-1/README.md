# Materi Minggu 1

## Daftar Isi

1. [UNIX Command Line](#unix-command-line)
2. [Git dan Github Dasar](#git-dan-github-dasar)
3. [HTML](#html)

<br>

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
