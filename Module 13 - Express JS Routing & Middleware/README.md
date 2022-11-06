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
Middleware adalah 

### Cara Kerja Middleware

### Function Middleware

### Jenis Express Middleware

- **Berdasarkan Cara Penggunaan**

- **Berdasarkan Source Middleware Function**
