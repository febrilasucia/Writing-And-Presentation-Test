# **Writing and Presentation Test**
![image](https://user-images.githubusercontent.com/82355658/192155172-514ef809-b1c1-427f-9bc0-9c695df48e4a.png)

## **DAY 1**

---

### **Java Script**
#### SCOPE
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
    ```
    let myName = 'Raisha';
    function greeting(){
        return myName;
    }

    console.log(myName); //Raisha
    ```
    > Variabel myName dideklarasikan secara global scope

#### 3. Local Scope
##### Pengertian 
- Local scope berarti mendeklarasikan variabel didalam blocks seperti funciton, conditional dan looping. Artinya variabel hanya bisa diakses didalam blocks saja dan tidak bisa diakses diluar blocks.
    Contoh :
    ```
    function greeting(){
        let myName = 'Raisha';
        return myName;
    }

    console.log(greeting()) //Raisha
    console.log(myName); //Uncaught ReferenceError: myNAme is not defined local scope

    ```
#### FUNCTION
##### 1. Pengertian
- Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task/1 fitur.
- Penggunaannya dapat digunakan berkali kali
##### 2. Membuat Function
    ```
    function greeting(){
        return 'Hello World';
    };
    ```
##### 3. Pemanggilan Function
    ```
    greeting() // Call the function name
    console.log(greeting()) //Output: 'Hello World'

    function getGreeting(){
        console.log("Hello, World!");
    }

    getGreeting();

    // Code after function call
    ```
##### 4. Parameter dan Argumen
- Parameter berfungsi agar dunction dapat menerima sebuah inputan data dan menggunakannya untuk melakukan sebuah task.
    Contoh :
    ```
    function penambahan(a,b){
        return a + b;
    }
    ```
    > a,b => parameters

- Argumen adalah nilai yang digunakan saat memanggil function
- Jumlah argumen harus sama dengan jumlah parameternya
    Contoh :
    ```
    function penambahan(a,b){
        return a + b;
    }
    console.log(penambahan(5, 5)) // 10
    ```
    > penambahan() => identifier
    > 5,5 => argument as values
- Default Parameters
    - Digunakan memberikan nilai awal/default pada parameter function.
    - Digunakan jika ingin menjaga function agar tidak error saat dipanggil tanpa argumen

    ```
    function greetOnWebsite(name= 'Stranger'){
        return 'Hello ' + name;
    }

    console.log(greetOnWebsite('David')); //Hello David
    console.log(greetOnWebsite()); //Hello Stranger   
    ```
 
  - Function Helper
        ```
        function multiplyByNineFifths(number){
          return number * (9/5);
        };
    
        function getFahtenheit(celsius){
          return multiplyByNineFifths(celcius) + 32);
        };
        
        getFahrenheit(15); ///Prints : 59
        ```
  
  - Arrow Function, cara lain menuliskan function.
         ```
         const greeting = () => {
          return 'Hello World'
         }
         ```
  - Short Syntax Function
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
#### ERROR & DEBUGGING
##### Jenis-jenis Error Message  
- Biasanya pesan kesalahan muncul di konsol yang digunakan developer.

1. Reference Errors (Kesalahan Referensi)
    - ketika mencoba menggunakan variabel yang belum dideklarasikan, maka akan mendapatkan kesalahan seperti berikut 
    
    ```
    console.log(foo) // Uncaught ReferenceError: foo is not defined
    ```
    - Ketika menggunakan const dan let, mereka seperti var dan function tapi ada waktu ketika dideklarasikan sehingga ketika ingin mengaksesnya terjadi kesalahan referensi
    ```
    foo = 'Hello' // Uncaught ReferenceError: foo is not defined
    let foo
    ```
    - Apapun yang sedang digunakan baik itu var, let atau const, untuk perbaikannya hanya mendeklarasikan variabel sebelum pendeklarasian dibuat
    ```
    let foo;
    foo = 'Hello'
    ```
2. Syntax Errors (Kesalahan Sintaks)
    - Syntax error adalah kesalahan penulisan kode dalam sebuah program. Biasanya salah memasukkan angka, kata, atau tanda baca sehingga format atau informasi tersebut tidak bisa dikenali oleh sistem komputer.
    - Seperti ketika mencoba mengurai objek yang tidak valid menggunakan JSON.parse
    ```
    JSON.parse( {'foo': 'bar'} ) // Uncaught SyntaxError: Unexpected token o in JSON at position 1
    ```
    - Ini dapat diselesaikan dengan memperbaiki sintaks dimana objek harus JSON
    ```
    JSON.parse('{"foo":"bar"}')
    ```
    
3. Range Errors
- Cobalah untuk memanipulasi obek dengan panjang tertentu dan berikan panjanga yang tidak valid dan kesalahan seperti ini akan muncul.
    ```
    var foo= [] 
    foo.length = foo.length -1 // Uncaught RangeError: Panjang array tidak valid
    ```

4. Type Errors
- Kesalahan ini muncul ketika jenis (angka, string dll) yang anda coba gunakan atau akses tidak kompatibel seperti mengakses properti dalam jenis variabel yang tidak ditentukan.
```

```
- Ini merupakan kesalahan yang sering terjadi di JS, mencoba mengakses properti/metode dengan berfikir bahwa bar adalah objek tipe
    
5. Debug
Untuk mendebug kode JSm adalah dengan console.log() variabel yang ingin anda periksa atau dengan menggunakan chorme

6. Handling Errors
- ???







Perulangan
- FOR
```
funstion cariAngka (x){
    for (let i = 1; i <= 20; i++){
        if (i == x) {
            consol.log(i)
        }
    }
}

cariAngka(3) /// 3
cariAngka(5) /// 5
cariAngka(11) /// 11
cariAngka(16) /// 16
cariAngka(22) /// tidak menampilkan apa2

-----

funstion cariAngka (x){
    let isKetemu = false
    for (let i = 1; i <= 20; i++){
        if (i == x) {
            consol.log(i)
            isKetemu = true
        }
    }

    if (!isKetemu) {
        console.log("data tidak ditemukan")
    }
}

cariAngka(3) /// 3
cariAngka(5) /// 5
cariAngka(11) /// 11
cariAngka(16) /// 16
cariAngka(22) /// tidak menampilkan apa2
```
- WHILE
```
    let i = 1
    let isKEtemu = false

    while (!isKetemu){
        if (i % 2 == 0 && 
            i % 3 == 0 && 
            i % 4 == 0 && 
            i % 5 == 0 && 
            i % 6 == 0)
        {
            console.log(i);
            isKetemu = true
        }

        i++
    }

    Hasil :
    60
```