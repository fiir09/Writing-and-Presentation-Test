# Express JS Routing & Middleware

## Express.js

### Definisi
Express js atau express adalah framework back-end web application untuk node.js yang dirancang untuk membangun aplikasi web dan API. Back-end web application adalah aplikasi yang berjalan di server-side. Back-end application ini bekerja untuk memberikan informasi berupa data sesuai dengan request user atau browser atau front-end.

## Routing

### Definisi
Routes adalah sebuah end point yang dapat kita akses menggunakan URL di website. Di dalam routes, kita perlu menentukan method API, alamat, dan juga response apa saja yang akan dikeluarkan. Berikut adalah salah satu contoh dari routes:

```
app.get('/', (req, res) => {
  res.send ('Hello World!')
})
```

Keterangan:

- `get` merupakan method API

- `'/'` merupakan alamat

- `res.send ('Hello World!')` merupakan response

### Method
Selain method `get` kita juga dapat menggunakan method yang ada di dalam RESTFul API seperti `POST`, `PUT`, `PATCH`, dan `DELETE`.

### Response
Di dalam route kita juga dapat mengirim response menggunakan parameter dari route express.js yaitu `res.Send()` untuk mengirim plain text ketika kita mengakses route tersebut.

### Status Code
Pada pengaplikasian back-end application, kita perlu memberikan status code sebagai informasi apakah route yang kita akses berjalan sebagaimana mestinya dan tidak terjadi error.

### Query
Query adalah parameter yang digunakan untuk membantu dalam menentukan tindakan yang lebih spesifik dibanding hanya sekedar router biasa. Umumnya, query diletakkan pada bagian akhir route dengan memberikan informasi yang diawali dengan `?` kemudian terdapat key dan data yang dapat ditindak lanjuti.

Pada express.js, kita dapat membaca query dengan menggunakan `req.query`. Kemudian informasi yang kita dapatkan tersebut dapat diolah atau dikembalikan kembali.

### Nested Route
Nested route digunakan ketika terdapat banyak route yang memiliki nama yang sama atau saat kita ingin membuat route yang mendalam.

## Middleware

### Definisi
Middleware adalah sebuah function yang akan memiliki akses ke object request (req), object response (res), dan sebuah function next di dalam request-response cycle. Function next biasanya diberikan nama variabel next.

### Cara Kerja Middleware
Middleware mengabstraksi proses komunikasi mendasar antar komponen sehingga front-end application hanya perlu berkomunikasi dengan middleware dan tidak perlu mempelajari bahasa komponen back-end lainnya.

### Function Middleware

### Jenis Express Middleware

- **Berdasarkan Cara Penggunaan**

  Berdasarkan cara penggunaannya express middleware dikelompokkan menjadi 3, yaitu:
  
    - **Application Level Middleware**
    
      Application level middleware adalah sebuah function middleware yang melekat pada instance object apllication express. Untuk menggunakannya, kita dapat menggunakannya dengan cara memanggil method `app.use()`. Application level middleware ini akan dijalankan setiap kali express application menerima HTTP request.
      
      Contoh:
      
      ```
      
      ```
      
    - **Router Level Middleware**
      
      Router level middleware adalah sebuah function middleware yang cara kerjanya sama persis dengan application level middleware. Namun, berbeda dengan application level middleware yang melekat pada instance object apllication express, router level middleware melekat pada instance object router express. 
      
      Untuk menggunakan router level middleware ini, kita dapat memanggil method `express.Router()`. Router level middleware ini hanya akan dijalankan setiap kali sebuah express router yang menggunakan middleware menerima HTTP request.
      
    - **Error Handling Middleware**
    
      Error handling middleware mengacu pada bagaimana sebuah express application menangkap dan memroses error yang terjadi, baik berupa kesalahan synchronous meupun kesalahan asynchronous. Pada express application, telah tersedia error handling secara default sehingga kita tidak perlu lagi membuat functionnya sendiri.
      
      Error handling default yang disediakan oleh express application hanya kerangka function saja, sehingga kita tetap harus menuliskan di dalam function tersebut bagaimana error akan dihandle.
      
      Error handling middleware ini digunakan pada application level middleware.

- **Berdasarkan Source Middleware Function**
