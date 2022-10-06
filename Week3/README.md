# **Writing and Presentation Test**

![image](https://user-images.githubusercontent.com/82355658/192155172-514ef809-b1c1-427f-9bc0-9c695df48e4a.png)

## **DAY 1**

---

### **Java Script Advance**

---

### Array

#### **Pengertian**

**Array** adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya.

Contoh :

```javascript
//Product Team
//1. Product Manager
//2. Front End Developer
//3. Back End Developer

let productTeam = [
  "Product Manager",
  "Front End Developer",
  "Back End Developer",
];
console.log(productTeam);
```

```javascript
let arrBuah = ["anggur", "jeruk"];
console.log(arrBuah); // 'anggur','jeruk'
```

#### **Membuat Array**

- Array didefinisikan menggunakan square brackets

```javascript
// Square Bracket
[];
```

#### **Mengakses Array**

- Array pada javascript dihitung dari index data ke-0
- Data pertama adalah index ke-0
  Contoh :

```javascript
const cars = ["Saab", "Volvo", "BMW"];
let car = cars[0];

console.log(car); //Saab
```

#### **Mengubah Element Array**

- Seperti tipe data dan variabel pada umumnya, kita dapat mengupdate data pada Array
  Contoh :

```javascript
const cars = ["Saab", "Volvo", "BMW"];
cars[0] = "Opel";
console.log(cars); //'Opel', 'Volvo', 'BMW'
```

#### **Const dalam Array**

- Jika menggunakan let, kita dapat mengubah array dengan array batu dan konten nilai yang ada didalam array dengan nilai lain
- Tapi const tidak bisa update data. Tapi dapat dilakukan **update konten nilai** didalam array
- Yang **tidak bisa** adalah **mengubah arrray** dengan **array yang baru** jika menggunakan const

Contoh :

```javascript
const cars = ["Saab", "Volvo", "BMW"];
cars = ["Opel"];
console.log(cars); //Uncaught TypeError: Assignment to constant variable

const cars = ["Saab", "Volvo", "BMW"];
cars[0] = "Opel";
console.log(cars); //'Opel', 'Volvo', 'BMW'
```

#### **Array Properties**

- **Properties** adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.
- Array memiliki 5 properti yang sering digunakan yaitu **constructor**, **length**, **index**, **input**, dan **prototype**.

#### **.length**

length akan mengembalikan nilai dari jumlah panjang data suatu array.

Contoh:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let length = fruits.length;
console.log(length); // 4
```

#### **Array Method**

- Array memiliki method atau built-in methods
  Contoh :

#### push()

```javascript
let arrBuah = ["anggur", "jeruk"];
console.log(arrBuah); // 'anggur','jeruk'

push.arrBuah["apel"]; //'anggur','jeruk','apel'
```

#### pop()

.pop() adalah method yang menghapus item array index terakhir.
Contoh :

```javascript
let arrBuah = ["anggur", "jeruk"];
pop.arrBuah["jeruk"]; //'anggur'
```

#### shift()

.shift() adalah method untuk menghapus item Array pada index pertama.
Contoh :

```javascript
let arrBuah = ["anggur", "jeruk"];
arrBuah.shift();
console.log(arrBuah); //"jeruk"
```

#### unshift()

.unshift() adalah method untuk menambahkan item Array pada index pertama
Contoh :

```javascript
let arrBuah = ["anggur", "jeruk"];
arrBuah.shift["apel"];
console.log(arrBuah); //"apel","anggur", "jeruk"
```

#### sort()

.sort() adalah method untuk mengurutkan secara Ascending atau Descending Alphanumeric

```javascript
let numbers = [1, 9, 6, 7];
number.sort();
console.log(numbers); //1,6,7,9
```

#### **Looping Array Elements**

Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach()
**.forEach()**
.forEach() adalah method untuk melakukan looping pada setiap elemen array.
Contoh :

```javascript
let arrBuah = ["anggur", "jeruk"];
arrBuah.forEach((elements) => {
  console.log(elements); //"anggur", "jeruk"
});
```

Salah satu jalan untuk looping sebuah array menggunakan `for`
Contoh :

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fLen = fruits.length;

let text = "<ul>";
for (let i = 0; i < fLen; i++) {
  text += "<li>" + fruits[i] + "</li>";
}
text += "</ul>";

//You can also use the Array.forEach() function:

const fruits = ["Banana", "Orange", "Apple", "Mango"];

let text = "<ul>";
fruits.forEach(myFunction);
text += "</ul>";

function myFunction(value) {
  text += "<li>" + value + "</li>";
}
```

**.map()**
.map() melakukan perulangan/looping dengan membuat array baru.

```javascript
let arr = [1, 2, 3, 4, 5];
let doubled = arr.map((num) => {
  return num * 2;
});
```

console.log(doubled);[2,4,6,8,10]

- Gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database.
- Gunakan .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.

---

## **DAY 2**

---

### **JavaScript Object**

---

#### **Pengertian**

- Objek adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method).
- Properti adalah data lengkap dari sebuah object.
- Method adalah action dari sebuah object.

#### **Tipe Data**

- number
- string
- boolean
- null
- undefined
- array
- **object**

Contoh Properti dan nilai dalam suatu object
Objek = Mobil
|Properti|Nilai|
|:--------:|:--------:|
|name|'Fiat'|
|model|'500'|
|weight|850kg|
|color|white|

| Method  |
| :-----: |
| start() |
| drive() |
| brake() |
| stop()  |

#### **Membuat sebuah object**

```javascript
let person = {};
```

> Penjelasan :
> person adalah object

```javascript
let person = {
  name: "John Doe",
  age: 25,
  isVerified: true,
};
```

#### **Mengakses Object dan Property Object**

```javascript
let person = {
  name: "John Doe",
  age: 25,
  isVerified: true,
  "current address": "Cambrridge, UK", //gunakan single quote pada key jika menggunakan spasi
};
//Pemanggilan nama variabel untuk akses object
console.log(person); // mengakses seluruh object
console.log(person.name); // mengakses properti object
```

#### **Bracket Notation**

```javascript
let person = {
  name: "John Doe",
  age: 25,
  isVerified: true,
  "current address": "Cambrridge, UK", //gunakan single quote pada key jika menggunakan spasi
};
//Pemanggilan nama variabel untuk akses object
console.log(person["name"]);
console.log(person["current address"]);
```

#### **Update Object**

- Object dapat **mengupdate value** dari key yang sudah tersedia
- Object dapat **menambahkan key** dan **value baru**
  Contoh :

```javascript
let people = {
  name : 'John',
  age: 25,
  isVerified: true,
}

///Mengupdate key dengan value baru
people.age = 27;

///menambahkan properti dan value baru
people.address = 'Cambridge, UK';

console.log(people);
//Output
{
  name : 'John',
  age : 27,
  isVerified: true,
  address: 'Cambridge, UK',
}
```

- Jika menggunakan constant pada variable object. Kita tidak bisa mengganti seluruh data object dengan object yang baru.
- Jadi jika membutuhkan untuk update seluruh data object gunakan ‘let’ pada saat deklarasi variabel.

#### **Delete Object Property**

- Kita dapat menghapus properti dari object menggunakan delete operator.
  Contoh :

```javascript
let people = {
  name: "John",
  age: 25,
  isVerified: true,
};

delete people.age;
console.log(people);
```

#### **Method**

- Method adalah value yang dimasukkan pada property berupa function.
  Contoh :

```javascript
const greeting = {
  welcome: function () {
    return "Halo selamat datang";
  },
  afterTransaction: function () {
    return "Terimakasih sudah membeli";
  },
};

console.log(greeting.welcome()); // 'Halo selamat datang'
```

> Catatan :
> Ada 2 method pada object `greeting`
>
> > `welcome()` dan `afterTransaction()`

#### **Nested Object**

- Pada real applicaton, nantinya akan menemukan data object yang kompleks
- data objek seringkali berasal dari turunan objek lainnya.
  Contoh :

```javascript
  const news ={
    title: 'Impact Byte menjadi Unicorn'
    desc: 'Berita ini sangat popler'
    author: {
      people: {
        name: 'David'
        age: 25,
        city: 'Bandung',
      }
    }
  };

  console.log('News:', news.title);
  console.log('Article published by:', news.author.people.name);

```

#### **Pass by reference**

- Mengbah data pada object melalui function dan memasukkan object sebagai parameter function

```javascript
let number = {
  originA: 2,
  originB: 3,
};

funtion chageData (obj){
  obj.originA = 4;
  obj.originB = 6;

};

chageData(number)
console.log(number.originA); //4
console.log(number.originb); //6

```

> Penjelasan :
> Mengubah data object number dengan sebuah function chageData()

#### **Looping Object**

- Looping berfungsi untuk menampilkan seluruh object properti tanpa harus akses secara manual

```javascript
  for(let key in object){
    //...
  }
  //......................
  const news ={
    title: 'Impact Byte menjadi Unicorn'
    desc: 'Berita ini sangat popler'
    author: {
      people: {
        name: 'David'
        age: 25,
        city: 'Bandung',
      }
    }
  };
  for(let data in news){
    console.log(news[data]);
  };

  for(let author in news.author.people){
    console.log(news.author.people[author]);
  };

```

#### **Array of Object**

- Untuk menyimpan data lebih dari satu bisa menggunakan array of object.
  Contoh :

```javascript
let students = [
  {
    name: 'febrila'
    age: 19,
    isVerified: true,
  },
  {
    name: 'sucia'
    age: 20,
    isVerified: false,
  },
  {
    name: 'dana'
    age: 21,
    isVerified: true,
  },
];

// gunakan forEach jika object berada didalam array
students.forEach(listStudent) => ]{
  console.log(listStudent);
}
```

## **DAY 3**

---

### **JavaScript Recursive**

---

#### **Pengertian**

- Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu.
- Recursive kebanyakan digunakan untuk case matematika, fisika, kimia dan berhubungan dengan calculator

#### **Struktur Recursive**

```javascript
function recursive() {
  recursive();
}

function recursive() {
  if (conditional) {
    // berhenti ketika memanggil dirinya sendiri
    // ..
  } else {
    recursive();
  }
}
```

#### **Ciri-ciri Rekrusif**

- selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti
- selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya

#### **Contoh Kasus**

```javascript
function countDown(fromNumber) {
  console.log(fromNumber);

  let nextNumber = fromNumber - 1;
  //jika kondisini ini bernilai false maka recursive berhenti

  if (nextNumber > 0) {
    countDown(nextNumber);
  }
}
countDown(3);

//mencari hasil dari nilai pangkat
function pow(m, n) {
  if (n == 1) {
    return m;
  } else {
    return m * pow(m, n - 1);
  }
}

console.log(pow(2, 3)); //8
```

## **DAY 4**

---

### **JavaScript Asynhronous**

---

#### **Pengertian**
