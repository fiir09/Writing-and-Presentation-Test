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
    
   Parameter adalah syarat input yang harus dimasukkan ke dalam suatu function dan dideklarasikan bersama dengan deklarasi function. Sedangkan argument adalah nilai yang dimasukkan ke dalam suatu function sesuai dengan persyaratan parameter. Argument dituliskan bersamaan dengan pemanggilan function.
 - **Argument**
