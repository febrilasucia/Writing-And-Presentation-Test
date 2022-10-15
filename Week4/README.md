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

**Hasil** :
![image](https://user-images.githubusercontent.com/82355658/195758940-261e7206-5162-4f9f-9b5b-0d69f8d23185.png)

Kalo dalam bentuk mobile
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

**Hasil** :
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
