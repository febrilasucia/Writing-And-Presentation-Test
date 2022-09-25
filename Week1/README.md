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
