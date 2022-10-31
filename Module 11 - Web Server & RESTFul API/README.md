# Web Server & RESTFul API

## Web Server

### Definisi
Web server adalah tempat untuk meletakkan codingan atau untuk request HTTP. Web server terdiri dari 2 bagian, yaitu hardware dan software.

Dalam sisi hardware, web server adalah komputer yang menyimpan web server software dan komponen file website (misal dokumen HTML, CSS, JavaScript, dan image). Web server terhubung dengan internet dan mendukung pertukaran data fisik dengan perangkat lain yang terhubung dengan web.

Dalam sisi software, web server mencakup beberapa bagian yang mengontrol bagaimana user mengakses hosted files, setidaknya file HTTP. Server HTTP merupakan software yang dapat memahami URL (alamat web) dan HTTP (protokol yang digunakan browser untuk melihat website). File HTTP dapat diakses melalui nama domain dari situs web yang disimpan dan kemudian mengirimkan konten website yang dihosting ke user device.

### Static Web Server VS Dynamic Web Server

- **Static Web Server**

  Static web server, atau stack, terdiri dari komputer (hardware) dan server HTTP (software). Pada static web server, server akan mengirimkan hosted files atau file yang dihosting apa adanya ke browser.

- **Dynamic Web Server**

  Dynamic web server terdiri dari static web server ditambah dengan extra software. Extra software tersebut biasanya adalah server aplikasi dan database. Pada dynamic web server, server aplikasi akan memperbarui hosted files atau file yang dihosting sebelum mengirim konten ke browser melalui server HTTP.

### Server Side Programming

- **Definisi**

  Server side programming atau pemrograman sisi server adalah suatu program yang berjalan di server yang menangani pembuatan konten halaman website. Pada dasarnya server side programming memiliki arti yang sama dengan backend scripting. Server side programming akan memproses user input, berinteraksi dengan database, dan mengontrol konten apa yang akan ditampilkan sebagai respond dari permintaan user.
  
- **Static Sites**

  Static sites adalah situs yang mengembalikan konten hard-coded yang sama dari server setiap kali particular resource diminta. Saat user ingin menavigasi ke halaman, browser akan mengirimkan HTTP `GET` request yang menentukan URL nya.
  
  ![static sites](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2011%20-%20Web%20Server%20%26%20RESTFul%20API/static%20sites.png)

- **Dynamic Sites**

  Dynamic sites dimana beberapa response content dihasilkan secara dinamis, hanya jika diperlukan. Di situs web dinamis, halaman HTML biasanya dibuat dengan memasukkan data dari database ke dalam placeholder di template HTML. Dynamic sites juga merupakan cara yang lebih efisien untuk menyimpan konten dalam jumlah besar jika dibandingkan dengan static sites.
  
  Dynamic sites dapat mengembalikan data yang berbeda untuk URL berdasarkan informasi yang diberikan oleh user atau preferensi yang disimpan. Selain itu, dynamic sites juga dapat melakukan operasi lain sebagai bagian dari pengembalian response.
  
  Sebagian besar kode yang digunakan untuk mendukung dynamic website harus dijalankan di sisi server. Oleh karena itu, membuat kode tersebut juga dapat dinamakan dengan server side programming atau back-end scripting.
  
  ![dynamic sites](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2011%20-%20Web%20Server%20%26%20RESTFul%20API/dynamic%20sites.png)


## RESTFul API

### REST

REST (REpresentational State Transfer) merupakan gaya arsitektur untuk menyediakan standart antara sistem komputer di web sehingga memudahkan sistem untuk berkomunikasi satu sama lain. Sistem yang sesuai dengan REST sering disebut dengan sistem RESTFul yang dicirikan oleh sifatnya yang stateless dan dapat memisahkan masalah antara client dan server.



### Communication between Client and Server

### Headers and Accept Parameters

### Paths

### Sending Responses

### Request & Response
