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

        let productTeam = ['Product Manager','Front End Developer','Back End Developer'];
        console.log(productTeam);
```
```javascript
let arrBuah = ["anggur", "jeruk"]
console.log(arrBuah); // 'anggur','jeruk'
```
#### **Membuat Array**
- Array didefinisikan menggunakan square brackets
```javascript
// Square Bracket
[]
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
let arrBuah = ["anggur", "jeruk"]
console.log(arrBuah); // 'anggur','jeruk'

push.arrBuah["apel"]; //'anggur','jeruk','apel'
```
#### pop()
.pop() adalah method yang menghapus item array index terakhir.
Contoh :
```javascript
let arrBuah = ["anggur", "jeruk"]
pop.arrBuah["jeruk"]; //'anggur'
```
#### shift()
.shift() adalah method untuk menghapus item Array pada index pertama.
Contoh :
```javascript
let arrBuah = ["anggur", "jeruk"]
arrBuah.shift();
console.log(arrBuah); //"jeruk"
```

#### unshift()
.unshift() adalah method untuk menambahkan item Array pada index pertama
Contoh :
```javascript
let arrBuah = ["anggur", "jeruk"]
arrBuah.shift['apel'];
console.log(arrBuah); //"apel","anggur", "jeruk"
```

#### sort()
.sort() adalah method untuk mengurutkan secara Ascending atau Descending Alphanumeric
```javascript
let numbers = [1,9,6,7];
number.sort();
console.log(numbers); //1,6,7,9
```
#### **Looping Array Elements**
Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach()
**.forEach()**
.forEach() adalah method untuk melakukan looping pada setiap elemen array.
Contoh :
```javascript
let arrBuah = ["anggur", "jeruk"]
arrBuah.forEach(elements => {
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
let arr = [1,2,3,4,5];
let doubled = arr.map(num => {
    return num * 2;
});
```
console.log(doubled);[2,4,6,8,10]

- Gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database.
- Gunakan .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.
---
## **DAY 2**

---

### **Java Script Advance**

---