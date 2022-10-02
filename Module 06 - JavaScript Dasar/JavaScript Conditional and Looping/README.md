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

    Operator aritmatikan digunakan pada operasi matematika yang melibatkan tipe data number. 
    
    Operator | Deskripsi
    --- | ---
    | + | Penjumlahan
    | - | Pengurangan
    | * | Perkalian
    | / | Pembagian
    | ** | Eksponen (pangkat)
    | % | Modulus
    | ++ | Increment (menambah 1)
    | -- | Decrement (mengurangi 1)
    
  - **Assignment Operator**

    Assignment Operator digunakan untuk memberikan nilai pada variabel
    
    Assignment | Operator | Contoh Penggunaan | Setara Dengan 
    --- | --- | --- | --- 
    = |  | x = y | x = y
    = | + | x += y | x = x + y
    = | - | x -= y | x = x - y
    = | * | x * = y | x = x * y
    = | / | x /= y | x = x / y
    = | % | x %= y | x = x % y
    = | ** | x ** = y | x = x ** y
    
  - **String Operator**

    String operator digunakan untuk menggabungkan dua atau lebih data string.
    
    Terdapat 2 macam string operator, yaitu:
    
      - **Operator `+`**
        
        Contoh:
        
        ```
        let namaDepan = "John";
        let namaBelakang = "Kennedy";
        
        console.log(namaDepan + " " + namaBelakang); // Output: John Kennedy
        ```
        
      - **Operator `+=`**
        
        Contoh:
        
        ```
        let kata = "Selamat";
        kata += "Pagi";
        
        console.log(kata); // Output: Selamat Pagi
        ```
        
  - **Operator Perbandingan**
    
    Operator perbandingan digunakan untuk membandingkan 2 data atau 2 nilai.
    
    Operator | Deskripsi
    --- | ---
    | == | Sama dengan (cek nilai)  
    | === | Sama dengan (cek nilai dan tipe data) 
    | != | Tidak sama dengan (cek nilai) 
    | !== | Tidak sama dengan (cek nilai dan tipe data)
    | > | Lebih dari 
    | < | Kurang dari 
    | >= | Lebih dari sama dengan 
    | <= | Kurang dari sama dengan 
    | ? : | Ternary Operator
    
  - **Operator Logika**

    Operator logika digunakan untuk menentukan logika antara 2 kondisi atau nilai.
    
     | Operator | Deskripsi 
     | --- | --- 
     | && | AND
     |  | OR 
     | ! | NOT 
     
     Bentuk operator dari `OR` adalah `||`.

## JavaScript Conditional

Conditional merupakan statement percabangan yang menggambarkan suatu kondisi tertentu. Conditional statement akan mengecek kondisi spesifik dan menjalankan perintah berdasarkan kondisi tersebut. Jika kondisi bernilai `true` maka kode yang terdapat di dalam kondisi akan dijalankan.
    
  - **If Statement**
    
    If Statement digunakan jika hanya ada 1 kondisi dan 1 keputusan yang dijalankan.
    
    ```
    if (kondisi){
      //kode yang akan dijalankan jika kondisi tercapai
    }
    ```
    
  - **If...Else Statement**

    If...Else Statement digunakan jika terdapat 1 kondisi dan 2 keputusan yang dijalankan.
    
    ```
    if (kondisi){
      //kode yang akan dijalankan jika kondisi tercapai (bernilai `true`)
    }
    else{
      //kode yang dijalankan jika kondisi tidak tercapai (bernilai `false`)
    }
    ```
    
  - **If...Else If... Statement**
    
    If...Else If... Statement digunakan jika terdapat beberapa kondisi dan beberapa keputusan yang dijalankan.
    
    ```
    if (kondisi_1){
      //kode yang dijalankan jika kondisi_1 tercapai
    }
    else if (kondisi_2){
      //kode yang dijalankan jika kondisi_2 tercapai
    }
    else{
      //kode yang dijalankan jika kondisi_1 dan kondisi_2 tidak tercapai
    }
    ```
    
  - **Switch Case**
    
    Switch Case digunakan jika kondisi dan percabangan terlalu banyak.
    
    ```
    switch (pernyataan){
      case kondisi1:
        //keputusan yang dijalankan ketika kondisi1 tercapai
        break;
      case kondisi2:
        //keputusan yang dijalankan ketika kondisi2 tercapai
        break;
      case kondisi3:
        //keputusan yang dijalankan ketika kondisi3 tercapai
        break;
      case kondisi4:
        //keputusan yang dijalankan ketika kondisi4 tercapai
        break;
      default:
        //keputusan yang dijalankan jika tidak ada kondisi yang tercapai
    }
    ```
    
## JavaScript Looping

Looping adalah sekumpulan kode yang akan dijalankan berulang kali hingga kondisi terpenuhi atau kondisi stop tercapai.

- **For Loop**
  
  Jika banyak perulangan yang diinginkan telah diketahui secara pasti, maka kita dapat menggunakan for loop.
  
  ```
  for (pernyataan1; pernyataan2; pernyataan3;){
    //kode yang akan dijalankan jika pernyataan-pernyataan tersebut bernilai true
  }
  ```
  
  Keterangan:
  
    - `pernyataan1` digunakan untuk menentukan nilai awal berjalannya loop
    - `pernyataan2` digunakan untuk kondisi berjalannya suatu loop. Jika kondisi `false`, maka loop berakhir
    - `pernyataan3` digunakan untuk menambah atau mengurangi nilai awal dari `pernyataan1` setiap loop dijalankan
   
  Contoh:
  
  ```
  for (let i=1; i<=5; i++){
    console.log(i);
  }
  ```
  
  Output dari kode di atas adalah:
  
  ```
  1
  2
  3
  4
  5
  ```
  
- **While Loop**

  While Loop adalah perulangan yang tidak diketahui secara pasti perulangannya sampai kapan. Perulangan berdasarkan kondisi.
  
  ```
  while (kondisi){
    //kode yang dijalankan jika kondisi bernilai benar (true)
  }
  ```

- **Do While Loop**

  Perulangan dilakukan hingga kondisinya terpenuhi. Syntax penulisan mirip seperti if, tetapi if hanya sekali dijalankan tetapi do while akan berulang.
  
  ```
    Do{
      //kode yang akan dijalankan Ketika kondisi benar
    }
    While (kondisi);
    ```

- **Penggunaan Looping**

  Kriteria | Looping yang Digunakan
  --- | ---
  Saat jumlah perulangan telah diketahui secara pasti | For Loop
  Jumlah perulangan belum diketahui dan kondisi ditanyakan terlebih dahulu (sebelum perulangan) | While Loop
  Jumlah perulangan belum diketahui dan kondisi ditanyakan terakhir (setelah eksekusi/perulangan) | DO While Loop
