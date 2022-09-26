# Materi Minggu 1

## Daftar Isi

1. [UNIX Command Line](#unix-command-line)
2. [Git dan Github Dasar](#git-dan-github-dasar)

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
