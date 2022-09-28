# JavaScript Dasar

## Definisi

JavaScript adalah bahasa pemrograman yang sangat powerful yang digunakan untuk logic pada sebuah website. JavaScript membuat website menjadi lebih interaktif dan dinamis.

## Menyisipkan JavaScript ke HTML

Terdapat 2 cara untuk menyisipkan JavaScript ke dalam file HTML, yaitu

  - Internal JavaScript
    
    Untuk menyisipkan kode JavaScript di dalam file HTML, maka kita dapat menuliskannya di dalam tag `<script>`. Tag tersebut dapat ditulis di dalam `<head>` maupun di dalam bagian akhir dari `<body>`
    
  - Eksternal JavaScript

    Pada eksternal JavaScript, kita menggunakan tag `<script>` di dalam elemen `<body>`, hanya saja kita menambahkan attribute `src` di dalam `<script>` untuk menyambungkan dengan file eksternal JavaScript yang telah dibuat sebelumnya.
    
    ```
    <script src="coba.js"></script>
    ```
    
    Pada kode di atas, "coba.js" merupakan nama file JavaScript eksternal.
    
## Syntax JavaScript

Syntax dapat dianalogikan sebagai vocabulary dan tata cara pada bahasa pemrogramman. Syntax digunakan untuk membuat statement program, instruksi untuk dijalankan oleh web browser, compiler, ataupun intrepreter.

- **alert()**

  Perintah alert() merupakan perintah khusus untuk menampilkan kotak informasi. Fungsi ini sering digunakan dalam proses pembuatan kode JavaScript untuk menampilkan kode sederhana.
  
  Contoh:
  ```
  alert("Hello");
  ```
  
  Tampilan:
  
  ![alert()](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2006%20-%20JavaScript%20Dasar/alert().png)
  
  
- **prompt()**
  
  Dialog prompt() berfungsi untuk mengambil sebuah nilai input dari user.
  
  Contoh:
  ```
  var nama = prompt("Siapa nama kamu?", "");
  document.write("<p>Hello " + nama + "</p>");
  ```
  
  Tampilan:
  
  ![prompt().1](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2006%20-%20JavaScript%20Dasar/prompt().1.png)
  
- **confirm()**

  confirm() digunakan untuk melakukan konfirmasi dalam tindakan tertentu. Dialog confirm() akan mengembalikan nilai `true` ketika memilih "oke" dan mengembalikan nilai `false` ketika memilih "cancel".
  
  Contoh:
  ```
  confirm("Apakah anda akan menghapusnya?");
  ```
  
  Tampilan:
  
  ![confirm()](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2006%20-%20JavaScript%20Dasar/confirm().png)
  

## Tipe Data JavaScript

Tipe data adalah klasifikasi yang diberikan untuk berbagai macam data yang digunakan dalam programming. Berikut adalah tipe data fundamental pada JavaScript:

- **Number**

  Tipe data number merupakan tipe data yang mengandung semua angka/bilangan.
  
  Contoh:
  
  ```
  0, 10000, 3.14
  ```
  
- **String**

  
- **Boolean**
- **Null**
- **Undefined**
- **Object**

## Operator JavaScript

## JavaScript Conditional

## JavaScript Looping (For Loop)
