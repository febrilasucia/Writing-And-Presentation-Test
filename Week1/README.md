# **Writing and Presentation Test**

## **DAY 1**

---

### **Unix Command Line**

- Shell merupakan program khusus yang menyediakan komunikasi langsung antara pengguna dan sistem operasi
- Shell terbagi menjadi dua, Shell yang berbasis teks disebut dengan _Command Line Interface_ (CLI) dan shell berbasis grafis disebut dengan _Graphical user interface_ (GUI)
- Contoh dari CLI yaitu `sh, bash, zsh, cmd.exe` . Biasanya yang sering digunakan adalah `bash`.
- Dalam mengakses _Command Line Interface_ dibutuhkan sebuah program yang disebut dengan `Terminal Emulator`.
- Struktur sistem file
  Sebuah filesystem mengatur bagaimana data disimpan di dalam sebuah system. OS seperti Windows menyusun file dan direktori menggunakan struktur seperti tree
  Beberapa Perintah CLI

  - Untuk melihat _Current Working Directory_ dapat mengetikkan

    ```
    $ pwd
    ```

    Contohnya :

    ```
    $ pwd
    /d/skilvul2/Writing-and-Presentation-Test
    ```

  - Untuk melihat isi sebuah directory

    ```
    $ ls
    $ ls -a //melihat semua file termasuk file yang tersembunyi
    ```

    Contohnya :

    ```
    $ ls
    Week1/  Week2/
    ```

  - Untuk berpindah directory

    ```
    $ cd <nama direktori>
    ```

    Contohnya :

    ```
    $ cd Week1
    ```

  - Untuk membuat file

    ```
    $ touch <nama file>
    ```

    Contohnya :

    ```
    $ touch catatan.txt
    ```

  - Untuk membuat direktori

    ```
    $ mkdir <nama direktori>
    ```

    Contohnya :

    ```
    $ mkdir Week3
    ```

  - Untuk melihat isi files

    ```
    $ nano <nama-files>
    ```

    Contohnya :

    ```
    $ nano catatan.txt
    ```

  - Untuk menyalin file dan direktori
    ```
    $ cp <asal> <tujuan>
    ```
    Contohnya :
    ```
    $ cp catatan.txt catatan1.txt
    ```
  - Untuk memindahkan atau me-rename file dan direktori
    ```
    $ mv <asal> <tujuan>  //me-rename
    $ mv <old name> <new name>  //me-rename
    ```
    Contohnya :
    ```
    $ mv catatan.txt /Week2
    $ mv Week1 Minggu1
    ```
  - Untuk menghapus file & direktori
    ```
    $ rm <nama file/direktori>
    ```
    Contohnya :
    ```
    $ rm catatan1.txt
    ```

### **Git dan Github**

- Git dan Github merupakan tools yang biasanya digunakan oleh para programmer sebagai tempat penyimpanan file pemrograman mereka, karena lebih efektif.
- Git dan Github berbeda. Developer yang menggunakan Git dapat menggunakan command-line tool, yaitu pengubah kode dan dapat digabungkan menuju perangkat lokal. Sedangkan, GitHub menyediakan interface grafis berbasis cloud sebagai tempat untuk melakukan seluruh tugas
- Alur kerja dari Git dan Github
  - Download git pada PC/Laptop dan lakukan instalasi.
  - Buatlah folder baru setela
  - Lakukan set up awal
    ```
    git config global user.name "suca"
    git config global user.email febrilasucia@gmail.com
    ```
  - Untuk hasil konfigurasi dapat dilihat dengan
    ```
    git config --list Config list
    ```
  - Membuat Repository Git
    ```
    git init <Nama Projek>
    ```
  - Melihat perubahan pada Git
    ```
    git status
    ```
  - Menambahkan file pada
    ```
    git add
    ```
  - Menghubungkan repository dengan project yang sedang dibuat
    ```
    git remote
    ```
  - Menyimpan perubahan pada Git
    ```
    git commit -m "Commit Message"
    ```
  - Mengirimkan file ke remote repository
    ```
    git push -u origin master
    ```
- Cara Cloning Github ke lokal
  - Cari Repository Github yang ingin di clone ke direktori
  - Pada halama repositori, klik tombol **_Clone or Download_**, lalu _copy link_
  - Setelah itu tetapkan lokasi direktori, lalu klik kanan pilih opsi **_Git Bash Here_**
  - Masukan perintah berikut
  ```
  git clone LINK_REPOSITORI
  ```
  - Jika link dapat terbaca oleh server Github, nantinya semua file yang berkaitan dengan link tersebut akan di unduh menuju lokasi yang telah kita tetapkan sebelumnya. Lama proses pengunduhan menyesuaikan dengan jumlah serta ukuran file yang terdapat pada repositori Github.
  - Jika proses pengunduhan telah selesai dilakukan, nantinya pada direktori yang di tuju, akan terdapat sebuah direktori yang memiliki nama yang sama dengan nama dari repositori yang kita clone. Artinya, file hasil clone telah siap untuk digunakan.

## **DAY 2**

---

### **HTML**
- HTML ada singkatan dari Hypertext Markup Language
- Pada sebuah Website, HTML adalah sebagai 'kerangka' yang memberi struktur pada website. Html juga dapat menampilkan beberapa konten seperti gambar, video, audio, teks dan masih banyak lagi
- Tools Pendukung dalam menggunakan HTML
  - Browser 
  - Code Editor
-  HTML Tag
    ```
    <p>My First Paragraph</p>

    ```
    ```<p>``` => Opening Tag<br>
    ```</p>``` => Closing Tag <br>
    ```My First Paragraph``` => Html Content
- Struktur Dokumen HTML
    ```
    <!DOCTYPE html>
    <html>
      <head>
        ...
      </head>
      <body>
        ...
      </body>
    </html>
    ```
- Contoh HTML sederhana 
  ```
  <!DOCTYPE html>
  <html lang="en">
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>My Website</title>
      <link href="coba.css" type="text/css" rel="stylesheet"/>
  </head>
      <body>
          <div>
              <h1 class="header">Hi! This is my Website</h1>
              <p>I love learning and sharing</p>
          </div>
      </body>
  </html>
  ```
  Hasilnya :

- Live Server dari Visual Studio Code 
  - Dalam menjalankan HTML diperlukan lokasi file html untuk membukanya dalam via browser. Tapi setiap melakukan perubahan , perlu melakukan refresh halaman. 
  - Pada Visual Studio Code terdapat Extention bernama Live Server. Fungsinya, programmer dapat melihat perubahan html tanpa merefresh halaman karena sudah auto reload 

  Contoh :

- Tag HTML
  - Gambar
    - Src atau source adalah  attribute untuk memberitahukan sumber gambar 
    - Alt atau alternative adalah dalah satu atribut alternatif apaliba gambar yang tidak bisa ditampilkan maka akan digantikan dengan kalimat alternatif.
    - Dalam menampilkan gambar bisa melalui file lokal komputer atau menggunakan link dari internet

    Contoh : 
    ```
    <img src="image/logo.jpg" alt="logo">
    ```
  - Video
    - Video merupakan double closing tag sehingga kita menaruh konten di antara opening dan closing
    - Controls berguna untuk kita bisa mengatur videonya di play / pause dan indikator menit
    Contoh :
    ```
    <video>
      <source src="movie.mp4" type="video/mp4">
    </video>
    ```
  - Table
    - Sebuah tabel terdiri dari baris dan kolom
    - Ada 3 tag untuk membuat tabel
      - ```<table>```  elemen utama
      - ```<tr>``` table row tag
      - ```<td>``` table data tag
    Contoh :
    ```
    <table>
      <tr>
        <th>Nama</th>
        <th>Nomor Telpon</th>
        <th>Negara</th>
      </tr>
      <tr>
        <td>Sarah</td>
        <td>0811111111</td>
        <td>Indonesia</td>
      </tr>
      <tr>
        <td>Sophia</td>
        <td>0822222222</td>
        <td>Indonesia</td>
      </tr>
    </table>
    ```
    Hasilnya :
- Semantic HTML 
  - Semantic artinya element html yang sesuai dengan kebutuhan konten.
  - Meningkatkan Accessibility
  - Meningkatkan SEO
  - Lebih mudah di maintain
  
  Contohnya :
  ```
  <div class="header"> ==> <header>

  <article>
  <aside>
  <details>
  <figcaption>
  <figure>
  <footer>
  <header>
  <main>
  <mark>
  <nav>
  <section>
  <summary>
  <time>
  ```
  
- DEPLOY
  - Deploy adalah sebuah proses untuk menyebarkan aplikasi yang sudah dibuat dengan tujuan dapat digunakan oleh orang-orang.  
  - Apabila aplikasi berbentuk mobule, maka perlu mendeploy ke Google Play Store/App Store
  - Apabila aplikasi berbentuk Web App maka perlu mendeploy ke server. Kita dapat menggunakan tools seperti **Netlify**
  - Masuk pada netlify.com 
  - Masuk ke tab Sites, lalu drag n drop seluruh folder html

  

