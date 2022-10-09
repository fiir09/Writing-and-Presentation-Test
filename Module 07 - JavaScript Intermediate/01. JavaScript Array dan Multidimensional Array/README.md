# JavaScript Array dan Multidimensional Array

## Array

### Definisi

Array di dalam JavaScript merupakan suatu tipe data yang dapat menampung banyak data dimana data-data yang ditampung dalam array tersebut dapat memiliki tipe data yang berbeda-beda.

Contoh:

```
let array = ["apel", "jambu", 23, true]

console.log(array);     //Output: ['apel', 'jambu', 23, true]
```

Pada contoh di atas, data `apel` dan `jambu` memiliki tipe data string, data `23` memiliki tipe data number, dan data `true` memiliki tipe data boolean.

### Deklarasi dan Pemanggilan Array

- **Deklarasi Array**

  Array didefinisikan dengan menggunakan square brackets `[]` dan setiap data yang ada di dalamnya dipisahkan dengan tanda koma `,`.

  ```
  let namaArray = [data1, data2, data3]
  ```
  
  Array dihitung dari index data ke-0. Pada contoh di atas, `data1` memiliki index 0, `data2` memiliki index 1, dan `data3` memiliki index 2.
  
- **Pemanggilan Array**

  Pemanggilan array dilakukan dengan menuliskan nama array yang akan dipanggil. Jika kita ingin memanggil suatu data yang ada di dalam array, maka pemanggilannya adalah dengan cara menuliskan nama array yang diikuti dengan index data yang akan dipanggil.
  
  Contoh:
  
  ```
  let buah = ["mangga", "jambu", "pisang"]

  console.log(buah);        //Output: ['mangga', 'jambu', 'pisang']
  ```
  
  Misal kita ingin memanggil data `jambu` pada array `buah`. Maka kita harus menuliskan index dari data `jambu`.
  
  ```
  ...
  console.log(buah[1]);     //Output: jambu
  ```
  
  Index dari data `jambu` adalah 1, sehingga saat kita menuliskan `buah[1]`, maka data jambu akan terpanggil.

### Property Array.length

Property merupakan fitur yang telah disediakan oleh JavaScript untuk memudahkan developer. Salah satu property dalam array yang sering digunakan adalah property `.length`. Property `.length` digunakan untuk mengembalikan nilai dari jumlah panjang data dari suatu array. Singkatnya, jika kita ingin mengetahui panjang data yang ada dalam suatu array, maka kita dapat menggunakan property `.length`.

Contoh:

```
let buah = ["mangga", "jambu", "pisang"]

console.log(buah.length);       //Output: 3
```

Pada contoh di atas diketahui bahwa panjang data pada array `buah` adalah 3.

### Array Method

Array memiliki method atau biasa juga disebut dengan built-in methods. Jika method yang dibutuhkan telah tersedia, maka tidak perlu lagi menggunakan function. Berikut adalah beberapa array method yang telah tersedia dalam JavaScript.

- **.push()**

  Method `.push()` digunakan untuk menambahkan item array pada urutan terakhir.
  
  Contoh:
  
  ```
  let buah = ["mangga", "jambu", "pisang"]
  
  console.log(buah);        //Output: (3) ['mangga', 'jambu', 'pisang']
  ```
  
  Misal kita ingin menambahkan item `apel` pada bagian akhir array `buah`, maka dapat menambahkan kode berikut:
  
  ```
  ...
  buah.push ("apel")
  console.log(buah);      //Output: (4) ['mangga', 'jambu', 'pisang', 'apel']
  ```
  
- **.unshift()**

  Method `.unshift()` digunakan untuk menambahkan item array pada bagian awal atau pada index pertama array.
  
  Contoh: 
  
  ```
  let buah = ["mangga", "jambu", "pisang", "apel"]
  
  console.log(buah);        //Output: (4) ['mangga', 'jambu', 'pisang', 'apel']
  ```
  
  Misal kita akan menambahkan item `manggis` pada index pertama array `buah`, maka dapat menambahkan kode berikut:
  
  ```
  buah.unshift("manggis")
  console.log(buah);        //Output: (5) ['manggis', 'mangga', 'jambu', 'pisang', 'apel']
  ```
  
- **.pop()**

  Method `.pop()` digunakan untuk menghapus item array yang ada pada bagian akhir array atau index terakhir.
  
  Contoh:
  
  ```
  let buah = ['manggis', 'mangga', 'jambu', 'pisang', 'apel']
  
  console.log(buah);        //Output: ['manggis', 'mangga', 'jambu', 'pisang', 'apel']
  ```
  
  Misal kita ingin menghapus item `apel` dimana item tersebut terletak pada index terakhir array `buah`, maka dapat menambahkan kode berikut:
  
  ```
  buah.pop()
  console.log(buah);        //Output: (4) ['manggis', 'mangga', 'jambu', 'pisang']
  ```

- **.shift()**

  Method `.shift()` menghapus item array pada index pertama array.
  
  Contoh:
  
  ```
  let buah = ["manggis", "mangga", "jambu", "pisang"]
  
  console.log(buah);        //Output: (4) ['manggis', 'mangga', 'jambu', 'pisang']
  ```
  
  Misal akan dihapus item `manggis` dimana item tersebut terletak pada index pertama array `buah`, maka dapat menambahkan kode berikut:
  
  ```
  buah.shift()
  console.log(buah);        //Output: (3) ['mangga', 'jambu', 'pisang']
  ```

### Array Loop

Untuk melakukan looping, array memiliki built in methods `.forEach()` dan `.map()`.

- **.forEach()**

  Method `.forEach()` digunakan untuk melakukan looping pada setiap element array.
  
  Contoh:
  
  ```
  let number = [2, 3, 5, 7];
  
  number.forEach (element => {
    console.log(element);
  })
  
  //Output: 2, 3, 5, 7
  ```
  
  Pada `.forEach()` output yang dihasilkan tidak berbentuk array.
  
- **.map()**

  Method `.map()` digunakan untuk melakukan looping dengan membuat array baru.
  
  Contoh:
  
  ```
  let number = [2, 3, 5, 7];
  
  let double = number.map(num => {
    return num * 2
  })

  console.log(double);        //Output: (4) [4, 6, 10, 14]
  ```

## Multidimensional Array

### Definisi

Multidimensional array merupakan array yang menampung data array atau dapat dianalogikan dengan array of array.

Contoh:

```
let array = [
    ["manggis", "apel", "pisang"],
    ["daffodil", "anggrek"],
    ["bayam", "sawi"],
]
```

### Pemanggilan Multidimensional Array

Untuk memanggil atau mengakses data yang diinginkan pada multidimensional array, maka dapat dilakukan dengan menuliskan index data seperti saat mengakses data pada array. Namun, jika pada array kita hanya perlu memberikan satu index data saja (index data yang ingin diakses), pada multidimensional array kita harus menuliskan 2 index data (index data array tempat data berada dan index data yang ingin diakses).

Contoh:

```
let array = [
    ["manggis", "apel", "pisang"],
    ["daffodil", "anggrek"],
    ["bayam", "sawi"],
]
```

Pada contoh di atas, data ` ["manggis", "apel", "pisang"]` memiliki index data 0, data `["daffodil", "anggrek"]` memiliki index data 1, dan data `["bayam", "sawi"]` memiliki index data 2.

Jika kita ingin mengakses data `daffodil`, maka kita dapat menuliskannya seperti berikut:

```
...
console.log(array[1][0]);       //Output: daffodil
```

Pada contoh di atas `[1]` merupakan index array tempat data `daffodil` berada. Sedangkan `[0]` merupakan index dari `daffodil`.
