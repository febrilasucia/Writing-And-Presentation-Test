# **Writing and Presentation Test**

![image](https://user-images.githubusercontent.com/82355658/192155172-514ef809-b1c1-427f-9bc0-9c695df48e4a.png)

## **DAY 1**

---

### **JavaScript Intermediate**

---

### Asynchronous - Fetch

#### **Pengertian**

- Tugas lain yang sangat umum di situs web dan aplikasi modern adalah mengambil item data individual dari server untuk memperbarui bagian halaman web tanpa harus memuat seluruh halaman baru.
- Detail yang tampaknya kecil ini memiliki dampak besar pada kinerja dan perilaku situs, jadi dalam artikel ini, kami akan menjelaskan konsep dan melihat teknologi yang memungkinkan: khususnya, **Fetch API** .
- Untuk memperlajari cara mengambil data dari server dan menggunakannya untuk memperbarui konten halaman web.

#### **Ambil API**

Contoh :

```javascript
fetch(file)
  .then((x) => x.text())
  .then((y) => myDisplay(y));
```

#### **Sintaksis**

```javascript
fetch(file);
```

#### **Parameter**

| Parameter | Description |
| :-------: | :---------: |
|   file    |  Optional   |

#### **Return Value**

|  Type   |               Description               |
| :-----: | :-------------------------------------: |
| Promise | Promise yang memutuskan ke objek Respon |

### **Asynchronous - Async Await **

- Async dan await membuat promise lebih mudah untuk ditulis
- **Async** membuat fungsi mengembalikan promise
- **Await** membuat fungsi menunggu promise

#### **Sintaks Asinkron**

**Contoh**

```javascript
async function myFunction() {
  return "Hello";
}
```

Sama dengan :

```javascript
function myFunction() {
  return Promise.resolve("Hello");
}
```

Berikut cara menggunakan promise

```javascript
myFunction().then(
  function (value) {
    /* code if successful */
  },
  function (error) {
    /* code if some error */
  }
);
```

#### **Sintaks Await**

```javascript
let value = await promise;
```

- Kata awaitkunci hanya dapat digunakan di dalam suatu asyncfungsi.

```javascript
async function myDisplay() {
  let myPromise = new Promise(function (resolve, reject) {
    resolve("I love You !!");
  });
  document.getElementById("demo").innerHTML = await myPromise;
}

myDisplay();
```

**Menunggu Waktu Habis**

```javascript
async function myDisplay() {
  let myPromise = new Promise(function (resolve) {
    setTimeout(function () {
      resolve("I love You !!");
    }, 3000);
  });
  document.getElementById("demo").innerHTML = await myPromise;
}

myDisplay();
```

**Menunggu File**

```javascript
async function getFile() {
  let myPromise = new Promise(function (resolve) {
    let req = new XMLHttpRequest();
    req.open("GET", "mycar.html");
    req.onload = function () {
      if (req.status == 200) {
        resolve(req.response);
      } else {
        resolve("File not Found");
      }
    };
    req.send();
  });
  document.getElementById("demo").innerHTML = await myPromise;
}

getFile();
```

---

## **DAY 2**

---

### **GIT & GITHUB LANJUTAN**

---

- GitHub telah menjadi batu penjuru untuk semua software open source. Para pengembang menyukainya, berkolaborasi, dan terus-menerus membangun proyek-proyek hebat melaluinya

#### **Kolaborasi Github**

1. Menambahkan Anggota Tim
   Biasanya ada dua cara menyiapkan Github untuk kolaborasi tim:

- **_Organizations_** - Pemilik organisasi dapat membuat banyak tim dengan tingkat izin yang berbeda untuk berbagai repositori
- **_Collaborators_** - Pemilik repositori dapat menambahkan kolaborator dengan akses Baca + Tulis untuk satu repositori

- Organizations
- Untuk mengakses halaman tim untuk Organization Anda, Anda cukup pergi ke http://github.com/organizations/[organization-name]/teams untuk melihatnya atau bahkan mengunjungi https://github.com/organizations/[organization-name]/teams/new untuk membuat tim baru dengan anggota dari 3 tingkat izin yang berbeda seperti:

  - **Pull Only**: Fetch and Merge dengan repositori lain atau salinan lokal. Akses hanya baca.
  - **Push and Pull**: (1) bersama dengan pembaruan reparasi jarak jauh. Baca + Akses tulis.
  - **Push, Pull & Administrative**: (1), (2) bersama dengan hak atas info penagihan, membuat tim serta membatalkan akun Organization. Baca + Tulis + akses Admin

- Colaborators
  Collaborators digunakan untuk memberikan akses Read + Write access ke satu repositori yang dimiliki oleh akun pribadi. Untuk menambahkan Collaborators, (akun pribadi Github lainnya), cukup buka https://github.com/[username]/[repo-name]/settings/collaboration:

  Collaborators digunakan untuk memberikan akses Read + Write access ke satu repositori yang dimiliki oleh akun pribadi. Untuk menambahkan Collaborators, (akun pribadi Github lainnya), cukup buka https://github.com/[username]/[repo-name]/settings/collaboration:

  - Fork target repo ke akun Anda sendiri.
  - Klon repo ke mesin lokal Anda.
  - Lihat "cabang topik" baru dan buat perubahan.
  - Dorong cabang topik Anda ke garpu Anda.
  - Gunakan penampil diff pada GitHub untuk membuat permintaan tarik melalui diskusi.
  - Lakukan perubahan apa pun yang diminta.
  - Permintaan tarik kemudian digabungkan (biasanya ke dalam cabang master) dan cabang topik dihapus dari repo hulu (target).

---

## **DAY 3**

---

### **RESPONSIVE WEB DESIGN**

---

#### **Pengertian**

- Responsive Web Design (RWD) adalah bertujuan membuat desain membuat desain website kita dapat diakses dalam device apapun.
- Dalam membuat aplikasi kita harus memikirkan user yang akan menggunakannya
- Device yang umumnya digunakan adalah laptop/PC, smartphone dan tablet.

#### **Setting Up Chrome Dev Tools**

- Setiap developer website wajib menggunakan tools
  bawaan dari setiap browser yang memudahkan proses development website
- Pada browser chrome biasa disebut denga Chrome Dev Tools

#### **Add Viewport in HTML**

```javascript
<meta name="viewport" content= "width=device-width, initial-scale=1.0">
```

#### **Use MAx-width Element**

- Properti max-widthmendefinisikan lebar maksimum elemen.
- Jika konten lebih besar dari lebar maksimum, itu akan secara otomatis mengubah tinggi elemen.
- Jika konten lebih kecil dari lebar maksimum, max-widthproperti tidak berpengaruh.

> **Note**: Ini mencegah nilai properti lebar menjadi lebih besar dari max-width. Nilai max-widthproperti menimpa properti lebar.

**Contoh** :

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=<device-width>, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <img
      style="max-width: 100%;"
      src="image/pemandangan.jpg"
      alt=""
      srcset=""
    />
  </body>
</html>
```

**Hasil** : <br>
![image](https://user-images.githubusercontent.com/82355658/195758940-261e7206-5162-4f9f-9b5b-0d69f8d23185.png)

Kalo dalam bentuk mobile <br>
![image](https://user-images.githubusercontent.com/82355658/195758971-2fccda05-d029-42ad-9308-242ce8d3fb5b.png)

#### **Your RWD Friends - Media Query**

Media query adalah teknik CSS yang diperkenalkan di CSS3.

Ini menggunakan @mediaaturan untuk menyertakan blok properti CSS hanya jika kondisi tertentu benar.

**Contoh** :
Jika jendela browser berukuran 600 piksel atau lebih kecil, warna latar belakang akan menjadi biru muda:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <style>
      body {
        background-color: lightgreen;
      }

      @media only screen and (max-width: 600px) {
        body {
          background-color: lightblue;
        }
      }
    </style>
  </head>
  <body>
    <p>
      Resize the browser window. When the width of this document is 600 pixels
      or less, the background-color is "lightblue", otherwise it is
      "lightgreen".
    </p>
  </body>
</html>
```

**Hasil** :<br>
![image](https://user-images.githubusercontent.com/82355658/195759532-54b2a423-3a33-4fa6-b5ac-b223c974d008.png)

![image](https://user-images.githubusercontent.com/82355658/195759549-b96d834c-72fc-494f-92b0-272aa755b263.png)

#### **Add Breakpoint**

- Kueri media dapat membantu dengan itu. Kita dapat menambahkan breakpoint di mana bagian tertentu dari desain akan berperilaku berbeda di setiap sisi breakpoint.

![image](https://user-images.githubusercontent.com/82355658/195759786-4da645e9-a0b1-4987-9953-38b65093f7d9.png)

Gunakan kueri media untuk menambahkan breakpoint pada 768px:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <style>
      * {
        box-sizing: border-box;
      }

      .row::after {
        content: "";
        clear: both;
        display: block;
      }

      [class*="col-"] {
        float: left;
        padding: 15px;
      }

      html {
        font-family: "Lucida Sans", sans-serif;
      }

      .header {
        background-color: #9933cc;
        color: #ffffff;
        padding: 15px;
      }

      .menu ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
      }

      .menu li {
        padding: 8px;
        margin-bottom: 7px;
        background-color: #33b5e5;
        color: #ffffff;
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
      }

      .menu li:hover {
        background-color: #0099cc;
      }

      .aside {
        background-color: #33b5e5;
        padding: 15px;
        color: #ffffff;
        text-align: center;
        font-size: 14px;
        box-shadow: 0 1px 3px rgba(0, 0, 0, 0.12), 0 1px 2px rgba(0, 0, 0, 0.24);
      }

      .footer {
        background-color: #0099cc;
        color: #ffffff;
        text-align: center;
        font-size: 12px;
        padding: 15px;
      }

      /* For desktop: */
      .col-1 {
        width: 8.33%;
      }
      .col-2 {
        width: 16.66%;
      }
      .col-3 {
        width: 25%;
      }
      .col-4 {
        width: 33.33%;
      }
      .col-5 {
        width: 41.66%;
      }
      .col-6 {
        width: 50%;
      }
      .col-7 {
        width: 58.33%;
      }
      .col-8 {
        width: 66.66%;
      }
      .col-9 {
        width: 75%;
      }
      .col-10 {
        width: 83.33%;
      }
      .col-11 {
        width: 91.66%;
      }
      .col-12 {
        width: 100%;
      }

      @media only screen and (max-width: 768px) {
        /* For mobile phones: */
        [class*="col-"] {
          width: 100%;
        }
      }
    </style>
  </head>
  <body>
    <div class="header">
      <h1>Chania</h1>
    </div>

    <div class="row">
      <div class="col-3 menu">
        <ul>
          <li>The Flight</li>
          <li>The City</li>
          <li>The Island</li>
          <li>The Food</li>
        </ul>
      </div>

      <div class="col-6">
        <h1>The City</h1>
        <p>
          Chania is the capital of the Chania region on the island of Crete. The
          city can be divided in two parts, the old town and the modern city.
        </p>
      </div>

      <div class="col-3 right">
        <div class="aside">
          <h2>What?</h2>
          <p>Chania is a city on the island of Crete.</p>
          <h2>Where?</h2>
          <p>Crete is a Greek island in the Mediterranean Sea.</p>
          <h2>How?</h2>
          <p>You can reach Chania airport from all over Europe.</p>
        </div>
      </div>
    </div>

    <div class="footer">
      <p>
        Resize the browser window to see how the content respond to the
        resizing.
      </p>
    </div>
  </body>
</html>
```

**Hasil** :
Size result : 839 x 585
![image](https://user-images.githubusercontent.com/82355658/195760019-3aea0aa6-3a9e-4a97-b05c-0fd451fe25ed.png)

Size result : 411 x 573
![image](https://user-images.githubusercontent.com/82355658/195760219-e2c9a0e6-e212-4cf4-9197-62c730a92649.png)

---

### **BOOTSTRAP 5**
#### **Pengenalan Bootstrap**
- Bootstrap adalah CSS Framework
- Bootstrap adalah sebuah CSS Framework yang di gunakan untuk membuat halaman HTML pada situs internet. Sebuah framework yang sangat populer saat ini dan banyak di gunakan para web designer dan website developer.

#### **Penggunaan Bootstrap 5**
- **Menggunakan Editor Halaman**
  Pastikan terlebih dahulu sebelum belajar anda memiliki editor halaman web yang bisa mengubah berkas html, css, dan js.

- **Instalasi Bootstrap 5**
  Menggunakan framework ini mengharuskan instalasi terlebih dahulu dengan download bahan-bahan yang akan di gunakan. Unduh bisa langsung dengan mengunjungi halaman web Bootstrap.

- **Download Bootstrap 5**
  Anda di berikan kemudahan dalam download dengan pilihan sumber yang telah di kompres atau tanpa kompres.

- **Compiled CSS & JS**

#### **Penggunaan Bootstrap 5 Online**
- Untuk versi Online menggunakan CDN, pastikan komputer terhubung dengan internet untuk melihat hasil halaman.Cara penggunaan Bootstrap 5 secara Online tanpa menyimpan data pada folder bisa dengan membuat link melalui versi CDN. Tentunya hal ini perlu menyimpan baris link css dan js pada halaman html yang anda miliki.


- Cascading Style Sheet
Bisa menggunakan CSS versi CDN dengan menyisipkan baris kode.

- Javascript
Untuk JS versi CDN, bisa di sisipkan baris kode dan tempatkan di bagian bawah halaman html. Penempatan javascript disarankan disimpan sebelum kode penutup ```</body>```.
```html
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-ka7Sk0Gln4gmtz2MlQnikT1wXgYsOg+OMhuP+IlRH9sENBO0LRn5q+8nbTov4+1p" crossorigin="anonymous"></script>
```

#### **Contoh Penggunaan Bootstrap 5**
```html
<header class="site-header">
  <nav class="navbar navbar-expand-lg navbar-light bg-light fixed-top" aria-label="navigation">
    <div class="container-fluid">
      <a class="navbar-brand" href="https://reezhdesign.com" target="_blank" rel="noopener">ReeZh Design</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarMain" aria-controls="navbarMain" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarMain">
        <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
          <li class="nav-item active">
            <a class="nav-link" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Link</a>
          </li>
          <li class="nav-item">
            <a class="nav-link disabled" href="#" tabindex="-1" aria-disabled="true">Disabled</a>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="dropdown05" data-bs-toggle="dropdown" aria-expanded="false">Dropdown</a>
            <ul class="dropdown-menu dropdown-menu-light dropdown-menu-end" aria-labelledby="dropdown05">
              <li><a class="dropdown-item" href="#">Action</a></li>
              <li><a class="dropdown-item" href="#">Another action</a></li>
              <li><a class="dropdown-item" href="#">Something else here</a></li>
            </ul>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</header>
<main class="site-content">
  <article class="hentry">
    <header class="entry-header">
      <div class="starter-template text-center py-5 px-3">
        <h1>Bootstrap 5 Starter Template</h1>
        <p class="lead">Use this document as a quick way to start a new project.
          This pen is an example of using the Bootstrap 5 Framework.</p>
        <p>current version Bootstrap 5.1.3</p>
      </div>
      <div class="sekrol d-none d-lg-block">
        <div class="tikus">
          <div class="pemutar"></div>
        </div>
      </div>
    </header>
    <section class="entry-content">
      <div class="container alignfull d-flex justify-content-center align-items-center vh-100">
        <h2>Work Canvas</h2>
      </div>
      <h2>Description</h2>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus laudantium nam aliquid officiis dignissimos totam sequi ipsam velit et. Deserunt soluta est voluptates corporis molestias quo eveniet inventore neque error.</p>
      <h3>How's To?</h3>
      <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Optio neque animi eveniet nihil consectetur ea, quod nulla totam eius error dolore id sunt quis repudiandae repellendus non saepe aut, numquam corporis, amet aliquid ullam illo. Voluptatem asperiores harum, magni nobis voluptatibus distinctio illum dolorem itaque expedita laudantium praesentium blanditiis autem.</p>
      <ul>
        <li>Lorem ipsum dolor sit amet.</li>
        <li>Facere numquam neque minima odit.</li>
        <li>Ratione veniam eum accusantium debitis!</li>
        <li>Magnam, nobis. Nulla, doloribus reprehenderit.</li>
        <li>Culpa commodi cum ipsa provident!</li>
      </ul>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Ratione fugit nostrum molestiae omnis repellat distinctio quos. Officia optio, ad id totam delectus rerum exercitationem voluptatum error mollitia magnam debitis accusamus.</p>
      <h4>Conclusion</h4>
      <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos ipsum numquam doloribus, alias aliquid eligendi natus quod iusto distinctio, in cum eos nam reiciendis? Voluptates dolore hic corporis. Aperiam, quibusdam.</p>
    </section>
    <footer class="entry-footer">
      <div class="container py-5">
        <div class="row">
          <div class="col-12 col-md-6 text-start">
            <p class="publish-on">Published: February 20<sup>th</sup>, 2020
            </p>
          </div>
          <div class="col-12 col-md-6 text-end">
            <p class="writer">Created by: ReeZh Design
            </p>
          </div>
        </div>
      </div>
    </footer>
  </article>
</main><!-- /.container -->
<footer class="site-footer">
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2 row-cols-lg-4 g-5">
      <div class="col">
        <div class="card border-0 h-100">
          <div class="card-body">
            <h4 class="card-title">About</h4>
            <p class="card-text">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cumque, enim officiis quas beatae molestiae, nisi porro quia numquam sint, officia vel amet quos. Nemo quasi repellat cupiditate! Vero, nobis exercitationem.</p>
            <a href="https://reezhdesign.com/" class="btn btn-sm btn-outline-primary" target="_blank" rel="noopener">More About Us</a>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-0 h-100">
          <div class="card-body">
            <h4 class="card-title">Services</h4>
            <p class="card-text">Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
            <ul>
              <li><a href="#">User Interface & Experience</a></li>
              <li><a href="#">Website Development</a></li>
              <li><a href="#">Search Engine Optimization</a></li>
            </ul>
            <a href="https://reezhdesign.com/kontak/" class="btn btn-sm btn-outline-success" target="_blank" rel="noopener">Let's Talk</a>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-0 h-100">
          <div class="card-body">
            <h4 class="card-title">Latest Posts</h4>
            <ul>
              <li><a href="#">Lorem ipsum dolor sit amet.</a></li>
              <li><a href="">Necessitatibus, cumque? Laborum, at iusto.</a></li>
              <li><a href="#">Minus nam natus pariatur cupiditate!</a></li>
              <li><a href="#">Optio et deserunt maxime maiores.</a></li>
              <li><a href="#">Quia sit repudiandae aperiam numquam.</a></li>
            </ul>
          </div>
        </div>
      </div>
      <div class="col">
        <div class="card border-0 h-100">
          <div class="card-body">
            <h4 class="card-title">Address</h4>
            <p class="card-text">Beverly Hills 5150, CA 90210</p>
            <p class="card-text">Visit and connect with social media:</p>
            <ul class="social-media list-inline fs-5">
              <li class="list-inline-item"><a href="https://www.facebook.com/reezh" target="_blank" rel="noopener"><i class="bi-facebook"></i><span> Facebook</span></a></li>
              <li class="list-inline-item"><a href="https://twitter.com/reezhdesign" target="_blank" rel="noopener"><i class="bi-twitter"></i><span>Twitter</span></a></li>
              <li class="list-inline-item"><a href="https://www.instagram.com/reezhdesign" target="_blank" rel="noopener"><i class="bi-instagram"></i><span>Instagram</span></a></li>
              <li class="list-inline-item"><a href="https://pinterest.com/reezhdesign" target="_blank" rel="noopener"><i class="bi-pinterest"></i><span>Pinterest</span></a></li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="container py-3 text-center">
    <a href="https://reezhdesign.com" target="_blank" title="Jasa Website Bandung" rel="noopener">ReeZh Design</a>
  </div>
  <div class="container">
    <div class="hstack w-100 justify-content-center">
      <div class="form-check form-switch">
        <label class="form-check-label ms-3" for="lightSwitch">
        </label>
        <input class="form-check-input" type="checkbox" id="lightSwitch" />
      </div>
    </div>
  </div>
</footer>
```

Hasil :<br>
![image](https://user-images.githubusercontent.com/82355658/196041304-35ddca01-4152-4f3f-b856-54035710b137.png)
Atau lebih lengkap
[lihat disini](https://codepen.io/reezhdesign/pen/PoGPZJZ)