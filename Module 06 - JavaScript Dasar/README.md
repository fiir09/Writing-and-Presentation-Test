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
  
  Tipe data string merupakan deretan karakter seperti huruf, angka, spasi, simbol, dan lainnya yang diapit oleh single quotes ('...') atau double quotes ("...").
  
  Contoh:
  
  ```
  let string = "Selamat Pagi";
  ```
  
  Pada contoh di atas "Selamat Pagi" memiliki tipe data string.
  
- **Boolean**

  Tipe data boolean merupakan nilai kebenaran dari sebuah pernyataan yang dituliskan sebagai `true` atau `false`.
  
  Contoh:
  
  ```
  let benar = true;
  let salah = false;
  ```
  
- **Null**

  Tipe data null adalah tipe data yang diartikan bahwa sebuah variabel/data tidak memiliki nilai. Null berbeda dengan string kosong karena string kosong masih memiliki tipe data yaitu string.
  
  Contoh:
  
  ```
  let dataPertama = null;
  let dataKedua = "";
  ```
  
  Jika contoh di atas ditampilkan, maka hasilnya adalah dataPertama memiliki nilai null dan dataKedua memiliki nilai kosong dengan tipe datanya adalah string.
  
- **Undefined**

  Tipe data undefined adalah tipe data yang merepresentasikan sebuah variable/data yang tidak memiliki nilai. Berbeda dengan tipe data null yang akan menghasilkan null ketika ditampilkan, tipe data undefined akan menghasilkan hasil seperti berikut ini:
  
  ```
  Nilai belum didefinisikan
  element array tidak ada
  ```
  Tipe data undefined ini biasanya dihasilkan karena adanya error pada program ataupun kelalaian programmer. Dengan kata lain, tipe data ini tidak direncanakan kemunculannya.
  
- **Object**

  Tipe data object adalah kumpulan pasangan property dan nilai. Tipe data ini dapat menyimpan data dengan tipe data apapun.
  
  Contoh:
  ```
  var person = {
    fistName: "John",
    lastName: "Kennedy"
  };
  ```

## Variabel JavaScript

Variabel merupakan tempat untuk menyimpan nilai. Hal-hal yang dapat dilakukan pada variabel adalah sebagai berikut:

  - Membuat variabel dengan nama yang jelas dan menggambarkan tentang data tersebut
  - Menyimpan dan mengupdate informasi atau data yang disimpan
  - Mendapatkan atau menampilkan data yang tersimpan

Untuk mendefinisikan variabel, terdapat 3 cara yaitu:

  - **var**
    
    Pendefinisikan dengan menggunakan `var` digunakan untuk variabel dengan nilai yang dapat berubah, namun saat ini `var` sudah jarang digunakan. Hal tersebut dikarenakan pendefinisian dengan `var` tidak akan memunculkan error meskipun variabel dengan nama yang sama telah didefinisikan sebelumnya sehingga nilai dari variabel pertama akan ditimpa dengan nilai dari variabel yang baru.
    
  - **let**

    Pendefinisian variabel dengan menggunakan `let` cocok untuk variabel dengan nilai yang dapat berubah-ubah.
    
  - **const**

    Berbeda dengan `let`, pendefinisian dengan menggunakan `const` dilakukan untuk variabel dengan nilai yang tidak dapat diubah.

## Operator JavaScript

Operator digunakan untuk menyimpan sebuah nilai pada variabel.

  - **Operator Aritmatika**
  - **Assignment Operator**
  - **String Operator**
  - **Operator Perbandingan**
  - **Operator Logika**

## JavaScript Conditional

## JavaScript Looping (For Loop)
