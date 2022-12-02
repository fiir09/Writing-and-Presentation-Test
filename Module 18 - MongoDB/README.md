# MongoDB

## Definisi
MongoDB adalah salah satu database open source noSQL yang menggunakan dokumen dengan format JSON untuk menyimpan data. MongoDB sering digunakan untuk aplikasi berbasis Cloud, Big Data, maupun Grid Computing.  

## NoSQL
Pada noSQL atau Not Only SQL, kita dapat mengolah database secara fleksibel dan tidak membutuhkan query sehingga kita memiliki skalabilitas yang tinggi sesuai dengan perkembangan data.

## Kelebihan dan Kekurangan MongoDB

### Kelebihan
Berikut adalah beberapa kelebihan yang dimiliki oleh mongoDB:

- Sistem yang tidak memerlukan table
- Tidak perlu menggunakan table yang terstruktur
- By Default sudah menggunakan JSON sehingga memudahkan integrasi dengan JavaScript
- Memiliki performa yang lebih cepat dengan kemampuan menampung banyak data yang bervariasi

### Kekurangan
Selain memiliki kelebihan, mongoDB juga memiliki kekurangan. Berikut adalah beberapa kekurangan yang dimiliki oleh mongoDB:

- Tidak mendukung transaksi
- Memiliki masalah terhadap konsistensi data
- Menggunakan lebih banyak memory
- Hanya dapat menampung maksimal 16MB di setiap document

## Komponen dari Database MongoDB
Berikut adalah gambaran anatomi komponen dari database mongoDB

![komponen mongoDB](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2018%20-%20MongoDB/komponen%20mongodb.png)

Database mongoDB terdiri dari  komponen, yaitu database, collection, dan document.

- ### Database

  Database adalah wadah atau tempat untuk menyimpan berbagai macam collection.

- ### Collection

  Collection adalah tempat kumpulan dari berbagai macam document. Collection sering disamakan dengan table pada SQL.

- ### Document

  Document merupakan unit terkecil yang berada pada mongoDB.

## Operasi CRUD MongoDB

## Mendesain Schema MongoDB
Dalam mendesain mongoDB, terdapat 2 pendekatan yang dapat digunakan, yaitu Embedding dan Referencing.

### Embedding

Dengan menggunakan pendekatan Embedding, kita memasukkan semua data yang terkait dalam satu document. Misal kita mendapatkan detail user dengan 2 document yang berbeda, yaitu personal_details dan contact seperti yang terlihat pada gambar berikut:

![embedding](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2018%20-%20MongoDB/embedded.png)

### Referencing

Dengan pendekatan Referencing, kita tidak memasukkan keseluruhan data, tetapi hanya sebagian saja. Misal kita ingin mendapatkan riwayat_lagu, maka kita hanya perlu memberikan ObjectID nya saja seperti yang terlihat pada contoh di bawah ini.

![referencing](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2018%20-%20MongoDB/referencing.png)

