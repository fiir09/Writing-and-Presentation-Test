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
