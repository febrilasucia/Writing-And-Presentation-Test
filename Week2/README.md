# **Writing and Presentation Test**

![image](https://user-images.githubusercontent.com/82355658/192155172-514ef809-b1c1-427f-9bc0-9c695df48e4a.png)

## **DAY 1**

---

### **Java Script**

---

### **JS SCOPE**

##### Pengertian

- Scope adalah konsep dalam flow data variabel

#### 1. BLOCK

##### Pengertian

- Blocks adalah code yang berada di dalam curly braces{}
- Conditional, function dan looping menggunakan blocks

#### 2. Global Scope

##### Pengertian

- Variabel yang kita buat dapat diakses dimanapun dalam suatu file.
- Agar menjadi Global Scope suatu variabel harus dideklarasikan diluar Blocks.

  Contoh :

  ```javascript
  let myName = "Raisha";
  function greeting() {
    return myName;
  }

  console.log(myName); //Raisha
  ```

  > Variabel myName dideklarasikan secara global scope

#### 3. Local Scope

##### Pengertian

- Local scope berarti mendeklarasikan variabel didalam blocks seperti funciton, conditional dan looping. Artinya variabel hanya bisa diakses didalam blocks saja dan tidak bisa diakses diluar blocks.
  Contoh :

  ```javascript
  function greeting() {
    let myName = "Raisha";
    return myName;
  }

  console.log(greeting()); //Raisha
  console.log(myName); //Uncaught ReferenceError: myNAme is not defined local scope
  ```

---

#### **JS FUNCTION**

---

##### 1. Pengertian

- Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur.
- Penggunaannya dapat digunakan berkali kali

##### 2. Membuat Function

```javascript
function greeting() {
  return "Hello World";
}
```

##### 3. Pemanggilan Function

```javascript
greeting(); // Call the function name
console.log(greeting()); //Output: 'Hello World'

function getGreeting() {
  console.log("Hello, World!");
}

getGreeting();
// Code after function call
```

##### 4. Parameter dan Argumen

- Parameter berfungsi agar dunction dapat menerima sebuah inputan data dan menggunakannya untuk melakukan sebuah task.
  Contoh :

  ```javascript
  function penambahan(a, b) {
    return a + b;
  }
  ```

  > `a,b` => parameters

- Argumen adalah nilai yang digunakan saat memanggil function
- Jumlah argumen harus sama dengan jumlah parameternya
  Contoh :
  ```javascript
  function penambahan(a, b) {
    return a + b;
  }
  console.log(penambahan(5, 5)); // 10
  ```
  > `penambahan()` => identifier<br> > `5,5` => argument as values
- Default Parameters

  - Digunakan memberikan nilai awal/default pada parameter function.
  - Digunakan jika ingin menjaga function agar tidak error saat dipanggil tanpa argumen

  ```javascript
  function greetOnWebsite(name = "Stranger") {
    return "Hello " + name;
  }

  console.log(greetOnWebsite("David")); //Hello David
  console.log(greetOnWebsite()); //Hello Stranger
  ```

  - Function Helper

    ```javascript
        function multiplyByNineFifths(number){
          return number * (9/5);
        };

        function getFahtenheit(celsius){
          return multiplyByNineFifths(celcius) + 32);
        };

        getFahrenheit(15); ///Prints : 59
    ```

  - Arrow Function, cara lain menuliskan function.
    ```javascript
    const greeting = () => {
      return "Hello World";
    };
    ```
  - Short Syntax Function
    - Zero Parameters
      ```java
      const functionName = () => {};
      ```
    - One Parameter
      ```java
      const functionName = paramOne => {};
      ```
    - Two or More Parameters
      ```java
      const functionName = (paramOne, paramTwo) => {};
      ```
    - Single-Line Block
      ```java
      const sumNumbers = number => number + number;
      ```
    - Multi Line Block
      ```java
      const sumNumbers = number => {
       const sum = number + number;
       return sum;
      };
      ```

#### **ERROR & DEBUGGING**

##### Jenis-jenis Error Message

- Biasanya pesan kesalahan muncul di konsol yang digunakan developer.

1. Reference Errors (Kesalahan Referensi)

   - ketika mencoba menggunakan variabel yang belum dideklarasikan, maka akan mendapatkan kesalahan seperti berikut

     ```javascript
     console.log(foo); // Uncaught ReferenceError: foo is not defined
     ```

   - Ketika menggunakan const dan let, mereka seperti var dan function tapi ada waktu ketika dideklarasikan sehingga ketika ingin mengaksesnya terjadi kesalahan referensi
     ```javascript
     foo = "Hello"; // Uncaught ReferenceError: foo is not defined
     let foo;
     ```
   - Apapun yang sedang digunakan baik itu var, let atau const, untuk perbaikannya hanya mendeklarasikan variabel sebelum pendeklarasian dibuat
     ```javascript
     let foo;
     foo = "Hello";
     ```

2. Syntax Errors (Kesalahan Sintaks)
   - Syntax error adalah kesalahan penulisan kode dalam sebuah program. Biasanya salah memasukkan angka, kata, atau tanda baca sehingga format atau informasi tersebut tidak bisa dikenali oleh sistem komputer.
   - Seperti ketika mencoba mengurai objek yang tidak valid menggunakan JSON.parse
     ```javascript
     JSON.parse({ foo: "bar" }); // Uncaught SyntaxError: Unexpected token o in JSON at position 1
     ```
   - Ini dapat diselesaikan dengan memperbaiki sintaks dimana objek harus JSON
     ```javascript
     JSON.parse('{"foo":"bar"}');
     ```
3. Range Errors

- Cobalah untuk memanipulasi obek dengan panjang tertentu dan berikan panjanga yang tidak valid dan kesalahan seperti ini akan muncul.
  ```java
  var foo= []
  foo.length = foo.length -1 // Uncaught RangeError: Panjang array tidak valid
  ```

4. Type Errors

- Kesalahan ini muncul ketika jenis (angka, string dll) yang anda coba gunakan atau akses tidak kompatibel seperti mengakses properti dalam jenis variabel yang tidak ditentukan.
- Ini merupakan kesalahan yang sering terjadi di JS, mencoba mengakses properti/metode dengan berfikir bahwa bar adalah objek tipe

5. Debug

   Untuk mendebug kode JSm adalah dengan console.log() variabel yang ingin anda periksa atau dengan menggunakan chorme

---

## **DAY 2**

---

### **Data Type And Structure**

---

##### **Pengertian**

- JavaScript adalah bahasa dinamis dengan tipe dinamis.
- Variabel dalam JS tidak secara langsung terkait dengan jenis nilai tertentu dan variabel apapun dapat diberi nilai dari semua jenis

Contoh :

```javascript
let foo = 42; // foo is now a number
foo = "bar"; // foo is now a string
foo = true; // foo is now a boolean
```

### **Jenis-jenis JavaScript**

#### 1. Nilai Primitif

Adalah data yang tidak dapat diubah diwakili pada tingkat bahasa terendah

- **Boolean**
  - mempunyai dua nilai : `true` dan `false`
- **Null** 
    - memiliki tepat satu nilai: `null`
- Undefined 
    - sebuah variabel yang belum diberi nilai
- **Number**
    - ECSMASCRIPT memiliki dua tipe yaitu number dan BigInt
- **Bigint** 
    - Tipe BigInt adalah primitif numberik dalam JS yang dapat mewakili bilangan bulat denan presisi arbitrer. - Dengan BigInts, Anda dapat dengan aman menyimpan dan mengoperasikan bilangan bulat besar bahkan di luar batas bilangan bulat aman untuk Numbers. - BigInt dibuat dengan menambahkan nke akhir bilangan bulat atau dengan memanggil konstruktor. - Anda dapat memperoleh nilai aman terbesar yang dapat ditambahkan dengan Numbers dengan menggunakan konstanta Number.MAX_SAFE_INTEGER. Dengan diperkenalkannya BigInts, Anda dapat beroperasi dengan angka di luar Number.MAX_SAFE_INTEGER.
    Contoh :
    ```java
        // BigInt
        const x = BigInt(Number.MAX_SAFE_INTEGER); 
        // 9007199254740991n
        x + 1n === x + 2n; 
        // false because 9007199254740992n and 9007199254740993n are unequal

        // Number
        Number.MAX_SAFE_INTEGER + 1 === Number.MAX_SAFE_INTEGER + 2; 
        // true because both are 9007199254740992
    ```
    > Keterangan
    > > - Anda dapat menggunakan operator +, *, -, **, dan %dengan BigInts—seperti halnya dengan Numbers. BigInt tidak sepenuhnya sama dengan Angka, tetapi secara longgar begitu.
    > > - BigInt berperilaku seperti Angka jika diubah menjadi boolean: if, ||, &&, Boolean, !.
    > > - BigInts tidak dapat dioperasikan secara bergantian dengan Numbers. Sebaliknya a TypeErrorakan dilempar.

- **String** - Jenis String JavaScript digunakan untuk mewakili data tekstual. Ini adalah satu set "elemen" dari nilai integer 16-bit unsigned. - Gunakan string untuk data tekstual. Saat mewakili data kompleks, parsing string, dan gunakan abstraksi yang sesuai.
- **types of symbol** - Simbol adalah nilai primitif yang unik dan tidak dapat diubah dan dapat digunakan sebagai kunci dari properti Objek (lihat di bawah). Dalam beberapa bahasa pemrograman, Simbol disebut "atom".

#### **2. Objek (kumpulan properti)**

Dalam ilmu komputer, objek adalah nilai dalam memori yang mungkin dirujuk oleh pengidentifikasi

- **Properti**
  - Ada dua jenis properti objek: properti data dan properti pengakses .
  - Setiap properti memiliki atribut yang sesuai . Setiap atribut diakses secara internal oleh mesin JavaScript, tetapi Anda dapat mengaturnya melalui Object.defineProperty(), atau membacanya melalui Object.getOwnPropertyDescriptor().
  - **Data Property**
    Properti data mengaitkan kunci dengan nilai. Hal ini dapat dijelaskan dengan atribut berikut: - `value` => Nilai yang diambil oleh akses get properti. Dapat berupa nilai JavaScript apa pun. - `writeable` => Nilai boolean yang menunjukkan apakah properti dapat diubah dengan penugasan. - `enumerable` => Nilai boolean yang menunjukkan jika properti dapat dihitung dengan for...inloop. Lihat juga Enumerabilitas dan kepemilikan properti untuk mengetahui bagaimana enumerabilitas berinteraksi dengan fungsi dan sintaks lainnya. - `configurable` => Nilai boolean yang menunjukkan apakah properti dapat dihapus, dapat diubah menjadi properti pengakses, dan dapat mengubah atributnya.
  - **Accessor Property**
    - `get` => Fungsi yang dipanggil dengan daftar argumen kosong untuk mengambil nilai properti setiap kali akses get ke nilai dilakukan.
    - `set` => Fungsi yang dipanggil dengan argumen yang berisi nilai yang ditetapkan. Dieksekusi setiap kali properti tertentu dicoba untuk diubah.
    - `enumerable` => Nilai boolean yang menunjukkan jika properti dapat dihitung dengan for...inloop.
    - `configurable` => Nilai boolean yang menunjukkan apakah properti dapat dihapus, dapat diubah menjadi properti data, dan dapat mengubah atributnya.
  - **Date**
    - Saat mewakili tanggal, pilihan terbaik adalah menggunakan Dateutilitas bawaan dalam JavaScript.

##### Menentukan tipe menggunakan typeofoperator

- Operator `typeof` dapat membantu Anda menemukan tipe variabel Anda.

  Contoh :

  ```javascript
  console.log(typeof 42);
  // expected output: "number"

  console.log(typeof 'blubber');
  // expected output: "string"

  console.log(typeof true);
  // expected output: "boolean"

  console.log(typeof undeclaredVariable);
  // expected output: "undefined"

  ```
---
## **CONTOH DEMO**
---
### **STRING**
```javascript
  let hewan = "kAnciL"

  console.log("ini adalah "+ hewan); // kAnciL
  console.log(`ini adalah ${hewan}`); // kAnciL
  console.log(typeof hewan)

  //properties
  console.log(hewan.length); // 6

  //method
  console.log(hewan.toUpperCase()) // KANCIL
  console.log(hewan.toLowerCase()) //kancil
  console.log(hewan.charAt(1)) // A  
  console.log(hewan[1]) // A
  console.log(hewan.include("n"))//true
  console.log(hewan.include("n"))//true
  console.log(hewan.include("b"))//false
```
  String.prototype.includes()
  Method ini berfungsi untuk mencari sebuah string dalam kumpulan string. Jika ditemukan maka nilanya `true`, jikalau tida ditemukan maka `false`
  Contoh :

  ```javascript
  const sentence = 'The quick brown fox jumps over the lazy dog.';

  const word = 'fox';

  console.log(`The word "${word}" ${sentence.includes(word) ? 'is' : 'is not'} in the sentence`);
  // expected output: "The word "fox" is in the sentence"
  ```

  String.prototype.split()
  Method ini mengambil dan membagi sebuah string kedalam daftar substring terurut dengan mencari pola, menempatkan substring ini ke dalam array dan mengembalikan array.

  let kalimat = "dengan menggunakan split(), kita dapat";
  console.log("BEFORE", kalimat)
  console.log("AFTER", kalimat.split(" "));

---

# **DOM**

## HTML DOM Tree of Objects

![image](https://user-images.githubusercontent.com/82355658/193411555-0ff496a8-fd87-42e7-b441-267f884c5e3f.png)

## Pengertian

- "Model Objek Dokumen W3C (DOM) adalah platform dan antarmuka netral bahasa yang memungkinkan program dan skrip untuk mengakses dan memperbarui konten, struktur, dan gaya dokumen secara dinamis."
- Dengan DOM, JavaScript mendapatkan semua kebutuhan untuk membuat HTML dinamis

## DOM HTML

_HTML DOM_ adalah model objek standar dan antarmuka pemrograman untuk HTML.<br>
Ini mendefinisikan:

- Elemen HTML sebagai objek
- Properti dari semua elemen HTML
- Metode untuk mengakses semua elemen HTML
- Acara untuk semua elemen HTML

> **NOTE** : 
> Dengan kata lain: DOM HTML adalah standar untuk mendapatkan, mengubah, menambah, atau menghapus elemen HTML.

## Interface DOM

- *HTML DOM* dapat diakses dengan *JavaScript* (dan dengan bahasan pemograman lainnya).
- di DOM semua element HTML didefinisikan sebagai objek
- Antarmuka pemrograman adalah properti dan metode dari setiap objek.
- Properti adalah nilai yang bisa Anda dapatkan atau atur (seperti mengubah konten elemen HTML).
- Metode adalah tindakan yang dapat Anda lakukan (seperti menambah atau menghapus elemen HTML).

### Contoh :
Mengubah konten ( innerHTML) <p>elemen dengan id="demo":

```html
<!DOCTYPE html>
<html>
<body>

    <h2>My First Page</h2>
        <p id="demo"></p>

    <script>document.getElementById("demo").innerHTML = "Hello World!";</script>

</body>
</html>

```

### Hasil :
![image](https://user-images.githubusercontent.com/82355658/193412081-1f784149-aa1c-4632-a76a-265d9223a57c.png)

### Metode `getElementById`

- Cara paling umum untuk mengakses elemen HTML adalah dengan menggunakan idelemen.
- Pada contoh di atas getElementByIdmetode yang digunakan id="demo"untuk mencari elemen.

### Properti `innerHTML`

- Cara termudah untuk mendapatkan konten elemen adalah dengan menggunakan innerHTMLproperti.
- Properti innerHTMLini berguna untuk mendapatkan atau mengganti konten elemen HTML.
- Properti innerHTMLini dapat digunakan untuk mendapatkan atau mengubah elemen HTML apa pun, termasuk <html>dan <body>.

### Objek Dokumen DOM HTML

- Jika Anda ingin mengakses elemen apa pun di halaman HTML, Anda selalu mulai dengan mengakses objek dokumen.
- Di bawah ini adalah beberapa contoh bagaimana Anda dapat menggunakan objek dokumen untuk mengakses dan memanipulasi HTML.

### Menemukan Elemen HTML

| Method                                | Description                   |
| :------------------------------------ | :---------------------------- |
| document.getElementById(id)           | Find an element by element id |
| document.getElementsByTagName(name)   | Find elements by tag name     |
| document.getElementsByClassName(name) | Find elements by class name   |

### Mengubah Elemen HTML

| Property                             | Description                         |
| :----------------------------------- | :---------------------------------- |
| element.innerHTML = new html content | Change the inner HTML of an element |
| element.attribute = new value        | element.attribute = new value       |
| element.style.property = new style   | Change the style of an HTML element |

| Method                                 | Description                                   |
| :------------------------------------- | :-------------------------------------------- |
| element.setAttribute(attribute, value) | Change the attribute value of an HTML element |

### Menambah dan Menghapus Elemen

| Method                          | Description                       |
| :------------------------------ | :-------------------------------- | ----------------------- |
| document.createElement(element) | Create an HTML element            |
| document.removeChild(element)   | Remove an HTML element            |
| document.appendChild(element)   | Add an HTML element               |
| document.replaceChild(new, old) |                                   | Replace an HTML element |
| document.write(text)            | Write into the HTML output stream |

### Menambah Penanganan Acara

| Method                                                 | Description                                   |
| :----------------------------------------------------- | :-------------------------------------------- |
| document.getElementById(id).onclick = function(){code} | Adding event handler code to an onclick event |
