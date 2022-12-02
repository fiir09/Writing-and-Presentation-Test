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

![komponen mongoDB]()

Database mongoDB terdiri dari  komponen, yaitu database, collection, dan document.

- ### Database

Database adalah wadah atau tempat untuk menyimpan berbagai macam collection.

- ### Collection

Collection adalah tempat kumpulan dari berbagai macam document. Collection sering disamakan dengan table pada SQL.

- ### Document

Document merupakan unit terkecil yang berada pada mongoDB.
