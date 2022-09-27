# **Writing and Presentation Test**
![image](https://user-images.githubusercontent.com/82355658/192155172-514ef809-b1c1-427f-9bc0-9c695df48e4a.png)

## **DAY 1**

---

### **Java Script**
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