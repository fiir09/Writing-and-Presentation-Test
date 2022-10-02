# JavaScript Dasar

## JavaScript Function

### Definisi

Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task atau 1 fitur. Function dapat dianalogikan seperti mesin cuci yang diberi inputan (berupa baju, detergen, air, dll) kemudian diatur atau diberi perintah (melalui tombol) untuk mengerjakan sesuatu yang diinginkan.

### Syntax Function

Function dapat dituliskan dengan beberapa cara seperti berikut ini:

- **Cara Pertama (Function Classic)**

  ```
  Function namaFungsi (kondisi){
    //statement
  }
  ```

- **Cara Kedua (Function Variable)**

  ```
  Let namaFungsi = function () {
    //statement
  }
  ```

- **Cara Ketiga (Arrow Function)**

  ```
  Let namaFungsi = () => {
    //statement
  }
  ```
  
 ### Pemanggilan Function
  
 Untuk memanggil function, cukup dengan menambahkan tanda kurung `()` setelah nama function tersebut. Contohnya adalah sebagai berikut:
  
 ```
 Function namaFungsi (kondisi){
   //statement
 }
  
 namaFungsi()
 console.log (namaFungsi())
 ```
  
 Pada kode di atas, console.log akan menampilkan informasi ke dalam tab console JavaScript.
 
 - **Contoh Function**
   
   ```
   function penjumlahan(a, b){
    a + b
   }

   console.log(penjumlahan(2, 3))   //undefined
   ```

   Pada contoh di atas dihasilkan output `undefined` dikarenakan function tersebut tidak memiliki perintah `return` di dalamnya. Pada JavaScript, jika tidak ada perintah `renturn` maka secara default function tersebut akan mengembalikan nilai `undefined. 
   
   Perlu diketahui juga bahwa `console.log` berbeda dengan `return`. `console.log` hanya akan menampilkan informasi ke dalam tab console di JavaScript, sedangkan `return` akan mengembalikkan nilai ke tempat dimana function dipanggil.
   
   Jika kita menambahkan perintah return ke dalam kode contoh di atas, maka hasilnya akan seperti berikut:
   
   ```
   function penjumlahan(a, b){
    return a + b
   }

   console.log(penjumlahan(2, 3))   //Output: 5
   ```
   
   Selain cara di atas, kita dapat juga melakukan pemanggilan function sebagai berikut:
   
   ```
   function sapa(nama){
      console.log (`Selamat pagi ${nama}`)
    }

    sapa ("Ani")
    sapa ("Budi")
    sapa ("Anton")
   ```
   
   Output dari kode di atas adalah:
   
   ![function](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2006%20-%20JavaScript%20Dasar/function.png)
   
 ### Parameter dan Argument
 
 - **Definisi**
    
   Parameter adalah syarat input yang harus dimasukkan ke dalam suatu function dan dideklarasikan bersama dengan deklarasi function. Dengan parameter, function dapat menerima inputan data dan menggunakannya untuk menjalankan tugas. Saat membuat function, kita harus mengetahui data-data yang dibutuhkan. Misalnya saat ingin membuat function penjumlahan 2 nilai, maka data yang dibutuhkan adalah data 2 nilai tersebut.
   
    Argument adalah nilai yang dimasukkan ke dalam suatu function sesuai dengan persyaratan parameter. Argument dituliskan bersamaan dengan pemanggilan function. Jumlah dari argument harus sama dengan jumlah parameter. Jadi jika kita mempunyai function penjumlahan dengan 2 parameter, maka kita juga harus menggunakan 2 buah argumen saat memanggil function tersebut.
    
    ```
    function penjumlahan(a, b){
      return a + b
    }

    console.log(penjumlahan(2, 3))
    ```
    
    Pada kode di atas, `a` dan `b` adalah parameter, sedangkan `2` dan `3` adalah argument.
   
 - **Default Parameter**
 
   Default parameter digunakan untuk memberikan nilai awal atau nilai default pada parameter function. Penggunaan default parameter ini juga akan menghindari hasil error apabila jumlah argument kurang dari jumlah parameter dimana parameter yang tidak memiliki argument tersebut akan diberi nilai default sesuai yang telah ditentukan pada bagian awal kode.
   
   Contoh:
   
   ```
   function penjumlahan (a, b, c = 4){
      return a + b + c
   }

   console.log (penjumlahan (2, 5, 1))    //Output: 8
   console.log (penjumlahan (5, 2))      //Ouput: 11
   ```
   
   Pada kode di atas, untuk `console.log (penjumlahan (5, 2))` menghasilkan output 2 meskipun hanya memiliki 2 argument. Hal tersebut dikarenakan pada penulisan parameter di bagian atas kode, kita telah menuliskan default parameternya sehingga nilai argumen yang belum didefinisikan tersebut akan digantikan dengan defaultnya.

## JavaScript Scope

Scope adalah konsep dalam flow data variabel yang menentukan suatu variabel dapat diakses pada scobe tertentu atau tidak.

 ### Block

   Block adalah kode yang terdapat di dalam kurung kurawal `{}`. Block ini biasanya digunakan pada conditional, looping, dan function.
    
 ### Global Scope

   Pada global scope, variabel dapat diakses dimana saja baik di luar maupun di dalam function atau block kode. Agar suatu variabel dapat menjadi global scope, maka variabel tersebut harus dideklarasikan di luar block.
   
   Contoh:
   
   ```
   let a = 4
   let b = 7

   function penjumlahan (){
     return a + b
   }

   console.log(a + b);    //Output: 11
   ```
   
   Pada contoh di atas, variabel `a` dan `b` dideklarasikan secara global scope.
   
 ### Local Scope

   Pada local scope, variabel dideklarasikan di dalam block sehingga variabel tersebut hanya dapat diakses di dalam block saja.
   
   Contoh:
   
   ```
   function penjumlahan (){
      let a = 4
      let b = 7
      return a + b

      console.log(a+b);
   }

   console.log(penjumlahan());    //Output: 11
   console.log(a + b);           //Output: Uncaught ReferenceError: a is not defined
   ```
   
   
