# Intro & Essential Node JS

## Definisi Node.js
Node.js adalah runtime environment untuk JavaScript yang bersifat open-source dan cross-platform. Dengan menggunakan node.js kita dapat menjalankan kode JavaScript dimanapun, tidak hanya terbatas pada lingkungan browser.

## Node.js Architecture

### Single Thread
Thread dalam ilmu komputer adalah eksekusi untuk menjalankan beberapa tugas atau program secara bersamaan. Setiap unit yang mampu mengeksekusi kode tersebut disebut dengan thread. Pada JavaScript konsep thread yang digunakan adalah single thread dimana hanya memiliki satu tumpukan panggilan yang digunakan untuk menjalankan program.

Untuk melakukan manajemen single thread, JavaScript menggunakan call stack. Ketika terdapat perintah baru, maka akan ditambahkan (push) dan akan dikeluarkan ketika perintah telah selesai (pop).

![single thread](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2012%20-%20Intro%20%26%20Essential%20Node%20JS/single%20thread.png)

### Even Loop
Dengan menggunakan konsep arsitektur JavaScript, kita dapat melihat JavaScript seperti menggunakan multi thread meskipun kita menggunakan single thread. Hal tersebut dikarenakan terdapat event queue yang berguna sebagai penampung ketika terdapat perintah baru yang akan dieksekusi. Kemudian event loop akan memeriksa kondisi secara terus menerus. Ketika antrian yang ada di call stack kosong, maka akan menambah antrian baru dari event queue hingga semua perintah selesai dieksekusi.

### Server side scripting
JavaScript merupakan bahasa pemrograman yang digunakan di front-end side sehingga kita hanya dapat mengerjakan JavaScript dengan menggunakan browser untuk menampilkan hasil eksekusinya. Namun, dengan menggunakan node.js kita dapat menjalankan JavaScript di server side dengan menggunakan terminal command line menggunakan perintah `node`.

## Node.js for Back end Development

### Build In Module Node.js

- **Console**

  Console merupakan module bawaan dari javascript yang ada di node.js. Console digunakan sebagai debug atau menampilkan kode secara interface.

- **Process**

  Process adalah module yang digunakan untuk menampilkan dan mengontrol prosess Node.js yang sedang dijalankan.

- **OS**

  OS module merupakan module yang digunakan untuk menyediakan informasi terkait sistem operasi komputer yang digunakan oleh user.

- **Util**

  Module Util merupakan alat bantu atau utilities untuk mendukung kebutuhan internal API di Node.js.

- **Events**

  Events merupakan

- **Errors**

  Errors merupakan module yang dapat digunakan untuk mendefinisikan error di Node.js sehingga lebih informatif. Kita juga dapat menghandle error menggunakan try catch.

- **Buffer**

  Buffer merupakan module yang digunakan untuk mengakses, mengelola, dan mengubah tipe data raw atau tipe data bytes.

- **FS**

  Fs (file system) merupakan module yang dapat membantu berinteraksi dengan file yang ada diluar kode. FS paling sering digunakan untuk membaca file dengan ekstensi .txt, .csv, dan .json.

- **Timers**

  Timers merupakan module yang digunakan untuk melakukan scheduling atau mengatur waktu pemanggilan fungsi yang dapat diatur di waktu tertentu.

### Membuat Web Server Dengan Node JS

- **Node.js Web Server**
- **Menambahkan HTTP Header**
- **Membaca Query String**
- **Split Query String**
- 
