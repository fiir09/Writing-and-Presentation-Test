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

Stateless berarti server tidak perlu mengetahui apapun tentang status client begitu pula sebaliknya. Sehingga baik server maupun client dapat memahami pesan apapun yang diterima, bahkan tanpa melihat pesan sebelumnya. Dengan kata lain, dalam gaya arsitektur REST, implementasi client dan implementasi server dapat dilakukan secara independen tanpa saling mengetahui satu sama lain. Karena implementasi tersebut dapat dilakukan secara independen, maka kode pada sisi client dapat diubah setiap saat tanpa mempengaruhi operasi server dan kode di sisi server dapat diubah tanpa mempengaruhi operasi client.

### Communication between Client and Server

**Making Request**

  REST mengharuskan client untuk membuat request ke server untuk mengambil atau mengubah data yang ada pada server. Pada umumnya, request terdiri dari:
  
    - HTTP verb yang mendefinisikan jenis operasi apa yang harus dilakukan 
    
    - header, yang memungkinkan client untuk menyampaikan informasi mengenai request
    
    - path yang menuju ke resource
    
    - optional message body yang berisikan data

- **HTTP VERBS**

  Terdapat 4 HTTP Verb dasar yang digunakan dalam request untuk berinteraksi dengan resource di dalam sistem REST, yaitu:
  
    - `GET`, digunakan untuk mengambil resource tertentu (berdasarkan id) atau kumpulan resources
    
    - `POST`, digunakan untuk membuat resource baru
    
    - `PUT`, digunakan untuk memperbarui resource tertentu (berdasarkan id)

    - `DELETE`, digunakan untuk menghapus resource tertentu dengan id

### Headers and Accept Parameters

Di dalam header request, client mengirimkan jenis konten yang dapat diterimanya dari server. Itu disebut dengan accept field, yang memastikan server tidak mengirim data yang tidak dapat dipahami atau diproses oleh client. Opsi untuk tipe konten adalah MIME Types (Multipurpose Internet Mail Extensions).

Tipe dan subtipe lain yang umum digunakan juga adalah:

  - **Image**

    Contohnya adalah image/png, image/jpeg, dan image/gif
    
  - **Audio**

    Contohnya adalah audio/wav dan audio/mpeg
    
  - **Video**

    Contohnya adalah video/mp4 dan video/ogg
    
  - **Application**

    Contohnya adalah application/json, application/pdf, application/xml, dan application/octet-stream

### Paths

Request harus diberi path atau jalur ke resource tempat operasi harus dilakukan. Dalam RESTful API, path harus dirancang untuk membantu client mengetahui apa yang sedang terjadi. Misal terdapat path berikut ini:

```
skilvulstore.com/customers/223/orders/12
```

Path tersebut memiliki sifat hierarkis dan deskriptif sehingga kita dapat mengerti apa yang ditunjukkan path tersebut meski belum pernah melihatnya sebelumnya. Path pada contoh di atas menunjukkan bahwa kita mengakses orders dengan id 12 untuk costumers yang memiliki id 223.

### Sending Responses

**Respond Code**

Respond dari server berisi status codes untuk memperingatkan client tentang informasi mengenai keberhasilan operasi. 

Ada 5 kategori yang berbeda status code HTTP yang diklasifikasikan berdasarkan jenis response yang dikomunikasikan server kepada client, yaitu:

  - **`1xx` - Informational code**
  
     Kode tersebut menunjukkan bahwa request telah diterima dan dipahami. Kode ini dikeluarkan sementara pemrosesan request berlanjut.
     
  - **`2xx` - Success code**

    Kode tersebut menunjukkan bahwa request yang diminta diterima, dipahami, dan disetujui. Dengan kata lain, server menyelesaikan apa yang diminta dengan lengkap dan sukses.
    
  - **`3xx` - Redirection code**

    Kode tersebut menunjukkan bahwa client dapat mengambil tindakan tambahan untuk menyelesaikan request. Biasanya tindakan tambahan itu adalah mengarahkan pengguna ke URL lain. Banyak kode status dalam kategori ini digunakan dalam pengalihan URL.
    
  - **`4xx` - Client error code**

    Kode tersebut menunjukkan bahwa request tidak dapat dipenuhi karena ada kesalahan yang datang dari client.
    
  - **`5xx` - Server error code**

    Kode tersebut menunjukkan bahwa server mengalami kesalahan atau tidak mampu melakukan permintaan yang valid.
