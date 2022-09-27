# **Writing and Presentation Test**

![image](https://user-images.githubusercontent.com/82355658/192155172-514ef809-b1c1-427f-9bc0-9c695df48e4a.png)

## **DAY 1**

---

### **Unix Command Line**

![image](https://user-images.githubusercontent.com/82355658/192155241-490e8d04-cbae-48d2-b61e-1f59fe2b66d6.png)

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

![image](https://user-images.githubusercontent.com/82355658/192155327-8c576490-f8c2-4154-9183-d1c0d7c5c19c.png)

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
- HTML Tag
  ```
  <p>My First Paragraph</p>
  ```
  `<p>` => Opening Tag<br>
  `</p>` => Closing Tag <br>
  `My First Paragraph` => Html Content
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

  > `<!DOCTYPE html> ` => Tag yang menyatakan dokumen html<br> > `<html>` => root elemen yang mana membungkus dari keseluruhan dokumen html <br> > `<head> ` => elemen untuk memanggil css, judul website, dll <br> > `<body>` => elemen yang tampak dan merupakan konten seperti gambar, video, teks dll
  > ` `

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

  ![image](https://user-images.githubusercontent.com/82355658/192154359-f3f7731d-f632-458c-9ace-187b9fd08985.png)

- Live Server dari Visual Studio Code

  - Dalam menjalankan HTML diperlukan lokasi file html untuk membukanya dalam via browser. Tapi setiap melakukan perubahan , perlu melakukan refresh halaman.
  - Pada Visual Studio Code terdapat Extention bernama Live Server. Fungsinya, programmer dapat melihat perubahan html tanpa merefresh halaman karena sudah auto reload
  - Klik extensions > search _Live server_ > install
    ![image](https://user-images.githubusercontent.com/82355658/192154455-9db3de6b-9c04-4bc0-ba30-fd5a3a5866b9.png)
  - untuk melihatnya, klik kanan pada file > open with live server, maka hasilnya
    ![image](https://user-images.githubusercontent.com/82355658/192154632-05b09415-ad9c-4b97-aba7-ec657d4ad3a5.png)

- Tag HTML

  - Gambar

    - Src atau source adalah attribute untuk memberitahukan sumber gambar
    - Alt atau alternative adalah dalah satu atribut alternatif apaliba gambar yang tidak bisa ditampilkan maka akan digantikan dengan kalimat alternatif.
    - Dalam menampilkan gambar bisa melalui file lokal komputer atau menggunakan link dari internet
      Contoh :

    ```
    <img src="image/logo.jpg" alt="logo">
    ```

    Hasil :
    ![image](https://user-images.githubusercontent.com/82355658/192154799-30ec4c72-ea27-4b48-85b4-5d2bf0cd614f.png)

  - Video

    - Video merupakan double closing tag sehingga kita menaruh konten di antara opening dan closing
    - Controls berguna untuk kita bisa mengatur videonya di play / pause dan indikator menit
      Contoh :

    ```
    <video>
      <source src="movie.mp4" type="video/mp4">
    </video>
    ```

    Hasil :

    ![image](https://user-images.githubusercontent.com/82355658/192154869-0a7e8a47-8b4c-434e-96ff-990d01ba177a.png)

  - Table

    - Sebuah tabel terdiri dari baris dan kolom
    - Ada 3 tag untuk membuat tabel
      - `<table>` elemen utama
      - `<tr>` table row tag
      - `<td>` table data tag
        Contoh :

    ```
    <table border="1">
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

    ![image](https://user-images.githubusercontent.com/82355658/192154977-7dadeb3f-5ac0-467d-96db-5a928165300f.png)

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

## **DAY 3**

---

### **Cascading Style Sheets**

#### **CSS Foundation**

- CSS adalah bahasa yang digunakan untuk mendesain halaman website.
- Dengan CSS, kita bisa mengubah warna, menggunakan font custom, editing text format, mengatur tata letak, dan lainnya.

#### **Menyisipkan CSS ke dalam HTML**

1.  Inline CSS, yaitu menggunakan attribute style untuk menyisipkan kode CSS langsung di dalam HTML element.
    Contoh :

    ```
    <!DOCTYPE html>
      <html>
      <head>
        <title>
          Website Pertamaku
        </title>
      </head>
      <body>
        <h1 style="color:blue;">Selamat Datang</h1>
      </body>
      </html>
    ```

    Hasil :
    ![image](https://user-images.githubusercontent.com/82355658/192409206-ed3629e1-37d4-4e0a-b0aa-6e9601972de7.png)

2.  Internal CSS, yaitu menggunakan element <style> untuk menyisipkan kode CSS. Element <style> diletakkan di dalam element <head>.
    Contoh:

    ```
    <!DOCTYPE html>
    <html>
      <head>
      <title>Website Pertamaku</title>
        <style>
        body { background-color: yellow; }
        h1 { color: blue; }
        p { color: red; }
        </style>
      </head>
      <body>
      <h1>Website Pertamaku</h1>
      <p>Selamat Datang</p>
      </body>
    </html>
    ```

    Hasil :
    ![image](https://user-images.githubusercontent.com/82355658/192409505-62fdec76-7eaf-48e5-ac1f-1a433f3346fe.png)

3.  External CSS, adalah cara menyisipkan kode CSS dengan cara membuat file CSS terpisah, dan lalu menyambungkannya dengan file HTML dengan menggunakan element <link>. Element <link> tersebut diletakkan di dalam element <head>.
    Contoh :

    ```
    <!-- File index.html -->
    <!DOCTYPE html>
    <html>
    <head>
      <title>Website Pertamaku</title>
      <link rel="stylesheet" href="styles.css" />
    </head>
    <body>
      <h1>Website Pertamaku</h1>
      <p>Selamat Datang</p>
    </body>
    </html>
    /* File styles.css */
    body {
    background-color: pink;
    }
    h1 {
    color: blue;
    }
    p {
    color: black;
    }
    ```

    Hasil :
    ![image](https://user-images.githubusercontent.com/82355658/192410150-f7769530-f5ad-4608-9d6a-b4c7f661e9cf.png)

#### **CSS Syntac**

```
selector{
  property: value;
}
```

> **Selector** adalah elemen atau tag HTML yang akan didefinisikan.
> **Property** adalah atribut yang akan diganti dengan “nilai” tertentu. Properti dan nilai dipisahkan dengan tanda titik dua (:) dan keduanya diapit oleh tanda kurung kurawal ({).
> **Value** adalah nilai yang diberikan kepada selector.

#### **Pemberian Style pada Element**

```
  <body>
    <h1>Selamat Datang di Website Pertamaku</h1>

    <div>
      <p>Namaku Sarah</p>
      <p>Saya tinggal di Indonesia</p>
    </div>

    <p>Saya tinggal bersama orang tua saya</p>
  </body>

  /* Pada File CSS */
  p {
    font-size: 20px;
  }
  div * {
    background-color: yellow;
  }
```

Hasil :
![image](https://user-images.githubusercontent.com/82355658/192411372-97b52878-a50f-424e-a858-8f6ccf967142.png)

    > Pada kode di atas, ada 2 element yang akan diberi latar belakang berwarna kuning:
    > element <p> yang berisi "Namaku"
    > element <span> yang berisi "Sarah"
    > Kode CSS di atas akan mengubah ukuran huruf dari semua element <p> menjadi sebesar 20px.

```
<!-- Pada File HTML -->
<body>
  <div id="container">
    <p>Selamat Datang di Website Kami</p>
    <div>
        <p>Semoga pengalaman kalian menyenangkan</p>
    </div>
  </div>
</body>

/* Pada File CSS */
#container p {
  background-color: yellow;
}
```

Hasil :
![image](https://user-images.githubusercontent.com/82355658/192412343-c4191e6c-dadc-4afc-9df0-07c3e63567db.png)

> Pada kode CSS di atas, ada dua buah selector:
> #container yang menunjuk kepada element <div> yang memiliki id bernilai container.
> p yang menunjuk kepada element <p>.

#### Metode responsive web design menggunakan CSS

- Mobile browser biasanya akan mengatur skala halaman html sesuai lebar viewport, sehingga website tampil di layar mobile. Kamu bisa menggunakan tag meta viewport untuk mereset ulang ini. Tag viewport sendiri digunakan untuk memberitahu browser agar menonaktifkan skala awal. Kamu bisa menyertakan meta tag seperti berikut ini dibagian <head>

```
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

- Tentukan Struktur HTML
  Langkah kedua yang bisa kamu lakukan yaitu menentukan struktur HTML Website, yang biasanya terdiri dari header, content, sidebar serta footer. Untuk header biasanya dibuat dengan ukuran lebar yang full dan tinggi disesuaikan dengan kebutuhan. Sedangkan content bisa ditentukan misalnya lebar 660px dan sidebar 300px, sehingga lebar keseluruhan adalah 960px.

- Membuat Media Query di CSS untuk memerintahkan Browser

  - Ketika lebar layar berukuran 960px atau kurang dari itu, maka jalankan script, atur lebar sesuai script. Disini lebar wrapper diatur menjadi 96% saja dari lebar layarnya. Sedangkan konten diatur agar lebarnya 66% saja dari lebar layar, dan sidebar lebarnya menjadi 30%. Perhatikan kode dibawah ini.

    ```
    /* Jika ukuran layar 680px atau kurang dari itu */

      @media screen and (max-width:680px){

        #maincontent{
          width: auto;
          float: none;
        }
        #sidebar{
          width: auto;
          float: none;
        }
      }

    ```

  - Selanjutnya jika ukuran layar 480px atau kurang dari itu (biasanya ini ukuran untuk ponsel/ smartphone), maka kamu bisa sembunyikan sidebar dan atur agar tinggi header menjadi auto. Semua kondisi bisa kamu tentukan sendiri berdasarkan kebutuhan.

  ```
  /* Jika ukuran layar 480px atau kurang */
  @media screen and (max-width: 480px) {
    #header{ height: auto; }
    #sidebar{ display: none; }
  }
  ```

#### Flexbox

- Flexbox bertujuan untuk menyediakan cara yang lebih efisien untuk menata, menyelaraskan dan mendistribusikan ruang di antara item dalam wadah.
- Membuat Layout Flexbox
  Ada dua komponen utama sebuah layout Flexbox yaitu container dan item.

  - Berikut ini HTML untuk contoh kita yang memiliki sebuah container dan tiga item:

  ```
    <nav class="container">
      <div>Home</div>
      <div>Search</div>
      <div>Logout</div>
    </nav>
  ```

  - Sebelum diatur untuk menggunakan Flexbox, setiap div di atas akan saling menumpuk seperti pada gambar (contoh di bawah sudah diberikan style default untuk mempermudah pembaca dan tidak ada hubungannya dengan Flexbox secara langsung):
    ![image](https://user-images.githubusercontent.com/82355658/192432260-eca96adc-a85e-46fa-b7e1-4d836a41205f.png)
  - Untuk mengubah layout ini untuk menggunakan Flexbox, cukup berikan kelas container properti CSS berikut:

  ```
  .container {
    display: flex;
  }
  ```

  ![image](https://user-images.githubusercontent.com/82355658/192432373-f70e2474-803a-49e3-86f2-afd2c777cb6f.png)

  - Justify Content dan ALign Items
    Justify-content dan align-items adalah dua properti CSS yang membantu kita mendistribusikan item-item di dalam container. Mereka mengontrol bagaimana item diposisikan secara horizontal (main axis) maupun vertikal (cross axis).
    ![image](https://user-images.githubusercontent.com/82355658/192432482-4806779a-44f5-482b-85f1-b78db8081542.png)

  ```
  .container {
    display: flex;
    justify-content: center;
  }
  ```

  ![image](https://user-images.githubusercontent.com/82355658/192432558-2a5b1c98-a2a5-4833-9e5c-90ed996729c2.png)

  - Berikut ini beberapa nilai lain yang bisa dipakai untuk justify-content:

    - flex-start (default)
    - flex-end
    - center
    - space-between
    - space-around
    - space-evenly

  - Align-items
    Digunakan untuk digunakan untuk menyelaraskan item fleksibel
    Contoh :

    ```
    .flex-container {
      display: flex;
      height: 200px;
      align-items: stretch;
    }
    ```

    ![image](https://user-images.githubusercontent.com/82355658/192438891-e3df5197-92b5-4638-9f5c-2f08c9691f69.png)

  - Nilai centermenyelaraskan item fleksibel di tengah wadah:

  ```
  .flex-container {
    display: flex;
    height: 200px;
    align-items: center;
  }
  ```

  ![image](https://user-images.githubusercontent.com/82355658/192433231-78dbad72-c04f-4dc2-b2bc-17ff5aa3e7bb.png)

## **DAY 4**

---

### **Algoritma dan Pseudocode**

#### **Algoritma**

- Algoritma adalah deskripsi berupa step by step yang dibutuhkan untuk menyelesaikan suatu masalah

  ##### Perbedaan Data Struktur dengan Algoritma

  - Data Struktur digunakan untuk menglola/manajemen sebuah data
  - Algotitma digunakan untuk menyelesaikan suatu permasalahan menggunakan data tersebut.

  ##### Contoh Algoritma Sederhana

  ```
    Step 1 : Start
    Step 2 : Declare variables num1, num2, and sum
    Step 3 : Read values num1 and num2
    Step 4 : Add num1 and num2 and assign the result tu sum
              sum <- num1 + num2
    Step 5 : Start Display sum
    Step 6 : Stop

  ```

  Dalam bahasa pemograman

  ```
  int num1, num2, sum;
    num1 = 10;
    num2 = 20;
  sum = num1 + num2;
    print(sum);
  ```

#### **Pseudocode**

- Pseudocode adalah menuliskan algoritma dengan umumnya bahasa inggris sebelum kita implementasikan ke bahasa pemograman tertentu.

#### **Big O notation**

- Definisi
  Bahasa & metrik untuk menentukan efisiensi sebuah algoritma
- Tujuan
  - Untuk membangun algoritma
  - mengoptimalkan algoritma ketika menjadi semakin lambat
- Kategori Big O Notation

  - Time Complexity
    Analogi
    ![image](https://user-images.githubusercontent.com/82355658/192273981-58bd5b20-b6f7-4d54-9d7c-3d7e8e6b9aeb.png)

    > Bayangkan kita akan mengirimkan paket pada teman kita di Bandung dimana proses pengiriman efisien saat ini menggunakan motor dengan waktu perjalanan 1 jam.
    > Paket = parameter
    > Proses = runtime
    > Time complexity = O(1), Konstan

    Bagaimana dengan 3 paket yang berbeda sedeangkan motor hanya menampung maksimal 1 paket.

    > Waktu perjalanan = 3 jam
    > Time complexity = O(n), Linear
    > Atau mengulangi proses sejumlah paket kita

  - Space Complexity
    Analogi
    Bagaimana kita mengirimkan 3 paket dalam satu waktu yang sama.
    > - menggunakan truk atau transportasi dengan ruang yg lebih luas
    > - Maka space complexitynya O(n), Linear
    > - Sehingga dapat mengirimkan barang-barang dalam satu waktu
    >   ![image](https://user-images.githubusercontent.com/82355658/192318358-7d2e0b0c-1bbe-4fef-ad01-417511e2e9f2.png)

- Mengukur Big O Notation

  - O(1), Konstan
  - O(n), Linear
  - O(log n), Logaritma N
  - O(n^2), Kuadrat 2
  - O(n^N), N Kuadrat N

- Contoh Kasus
  Brute Force
  Tidak Efisien namu efektif

  - Sangat mudah diterapkan
  - Tidak berarti buruk
  - Langkah awsal untuk mengoptimalkan program
  - Time complexity O(N^2)

  ```
    2, 1, 3, 1

   public boolean checkDuplication(int[] arr){
    for(int i = 0; i <arr.length; i++){
      for (int j = i + 1; j < arr.length; j++){
        if(arr[i] == arr[j]) return true;
      }
    }
    return false;
  }
  ```

  > **Optimize**
  > Negosiasi & kebutuhan
  >
  > - Bertanya kebutuhan dan ketebatasan
  > - menggunakan sortung
  > - time complexity O(N log N)

  ```
    2, 1, 3, 1
   public boolean checkDuplication(int[] arr){
    Arrays.sort(arr);
    for(int i = 0; i <arr.length; i++){
        if(arr[i] == arr[i +1]) return true;
    }
    return false;
  }
  ```

## **DAY 5**

---

Peserta mampu memahami dan membedakan control flow (conditional dan looping)

### **Java Script**

#### **Intro JavaScript**

1. Pengertian

- Javascript adalah bahasa pemograman yang sangat powerful yang digunakan untuk logic pada sebuah website
- Javascript juga dapat membuat website menjadi interaktif dan dinamis

2. Menjalankan JavaScript

- Dijalankan memlalui browser

3. Syntax dan Statement JavaScript

- Alert()
- Prompt()
- Confirm()
- Console Log
  - Console log adalah tempat kita untuk cek logic pemograman web yang kita kembangkan
  - Console log juga tempat kita untuk melakukan debugging (mengetahui error pada code) pada pemograman web
- Comment
  - Comments adalah sintaks yang digunakan untuk memberi keterangan tentang suatu statement. Menggunakan bahasa inggris atau bahasa indonesia.
  - Jenis-jenis Comment
    - Single Comments
      ```
      // Prints 5 to the console
      ```
    - Multiline Comments
      /_
      This is all commented
      console.log(10);
      None of this is going to run!
      console.log(99);
      _/

4. Tipe Data (Data Types)

- Pengertian
  Tipe data adalah klasifikasi yang kita berikan untuk berbagai macam data yang digunakan dalam programming.
- Jenis-jenis
  - number => mengandung semua angka termasuk desimal
  - string => gup karakter yang ada pada keyboadr laptio/PC seperti hurud, angka, spasi dan symbol
  - boolean => mempunyai 2 nilai yaitu `TRUE` or `FALSE`
  - null => data tidak memiliki nilai
  - undefined => tipe data yang merepresentasikan variabel/data yang tidak memiliki nilai, biasanya terjadi karena eror, atau tidak disengajakan
  - object => dapat menyimpan data dengan tipe data apapun

5. Variabel
   - Var
   - Let
   - Const
6. Operator

- Assignment Operator, digunakan untu menyimpan sebuah nilai pada variabel
  Contoh :
- Increment dan Decrement
  Contoh:

- Operator Aritmatika

  - Tambah(+)
  - Kurang(-)
  - Perkalian(\*)
  - Pembagian(/)
  - Modulus(%)
    Contoh:

- Comparison Operator
  Comparison operator adalah operator yang membandingkan satu nilai dengan yang lain, hasil operasi berupa `true` or `false`

  - <
  - >
  - <=
  - > =
  - ===
  - !==
    Contoh:

- Operator Logika, biasa digunakan untuk sebuah conditional pada pemograman, hasilnya berupa `true` or `false`
- AND &&
- OR !!
- NOT !
  Contoh:
#### CONDITIONAL
1. Pengenalan
   Conditional merupakan statemen percabangan yang menggambarkan suatu kondisi. Apakah kondisi tersebut TRUE (benar) atau FALSE (salah). Apabila TRUE maka code akan dijalankan
   Contoh :
   - IF Statement
      ```
      if(true){
        console.log('This message will print!');
      };
      //Prints "This message will print"

      let lapar = true;
      if(lapar){
        console.log('Yuk makan');
      };
      ```
    - IF ELSE Statement
      ```
      let lapar = false;
      if(lapar){
        console.log('Yuk makan');
      }else{
        console.log('Tidak makan'); 
      };
      //Program akan menampilkan statement pada else
      ```
    - IF.. ELSE IF Statement
      let lapar = false;
      if(lapar){
        console.log('Yuk makan nasi');
      }else if{
        console.log('Yuk beli cemilan'); 
      }else if{
        console.log('Yuk buat gorengan'); 
      }else{
        console.log('Males makan'); 
      };
      
      ```
  - TRUTHY AND FALSY ASSIGNMENT
    Jika kita memiliki sebuah website dan meminta inputan username lalu menampilkannya. Jisa usernamenya kosong kita bisa isi nilai tersebut.
    Contoh :
    let defaultName;
    if (username) {
      defaultName = username;
    }else {
      defaultName = 'Stranger'
    }
  
  - SWITCH CASE CONDITIONAL
    Biasanya digunakan untuk kondisi dan percabanyan terlalu banyak.
    ```
    var buttonPushed = 1;
    switch(buttonPushed){
      case  1;
            console.log('matikan TV!);
            break;
      case  2;
            console.log('turunkan volume TV!);
            break;
      case  3;
            console.log('tingkatkan TV!);
            break;
      case  4;
            console.log('matikan suara TV!);
            break;
      default;
            console.log('Tidak terjadi apa-apa');
            break; 
    }
    ```
  - Ternary Operator
    Ternary Operator merupakan short-syntax dari statement if ... else.
    Contoh :
    ```
    let isNowSale = true;
    isNowSale ? console.log('Lest shopping now') : console.log('Sjopping Later');
    ```
#### FUNCTION
 1. Function adalah sebuah blok kode sebuah grup untuk menyelesaikan 1 task/1 fitur.
    Contoh :
    ```
    function greeting(){
      return 'Hello Beban Keluarga';
    }
    ```
    > ```function``` function keyword
    > ```greeting``` identifier
    > ```return'...';``` function body

  2. Default Parameters, digunakan untuk memberikan nilai awal/default pada parameter function
    Contoh :
    ```
    function greetOnWebsite(name = 'Stranger') {
      return 'Hello ' + name;
    }

    console.log(greetOnWebsite('David')); //Prints : 'Hello David'
    console.log(greetOnWebsite()); //Prints : 'Hello Stranger'
    ```
  
  3. Function Helper
    ```
    function multiplyByNineFifths(number){
      return number * (9/5);
    };

    function getFahtenheit(celsius){
      return multiplyByNineFifths(celcius) + 32);
    };
    
    getFahrenheit(15); ///Prints : 59
    ```
  
  4. Arrow Function, cara lain menuliskan function.
     ```
     const greeting = () => {
      return 'Hello World'
     }
     ```
  5. Short Syntax Function
     - Zero Parameters
       ```
       const functionName = () => {};
       ```
     - One Parameter
       ```
       const functionName = paramOne => {};
       ```
     - Two or More Parameters
       ```
       const functionName = (paramOne, paramTwo) => {};
       ```
     - Single-Line Block
       ```
       const sumNumbers = number => number + number;
       ```
     - Multi Line Block
       ```
       const sumNumbers = number => {
        const sum = number + number;
        return sum;
       };
       ```





