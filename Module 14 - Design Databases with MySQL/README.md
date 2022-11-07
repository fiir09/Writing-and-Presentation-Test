# Design Databases with MySQL

## Menentukan Entity
Entity atau entitas adalah suatu object atau hal lainnya yang merepresentasikan sebuah data. Entity dapat diidentifikasikan berdasarkan requirement yang ada dalam database.

## Menentukan Attribute dari Entity
Setiap entity memiliki suatu attribute. Setelah kita selesai menentukan entity, maka selanjutnya adalah menentukan attribute yang ada dalam setiap entity. Attribute yang diperlukan di dalam entity kemungkinan sudah ada di dalam requirement document atau mungkin juga memerlukan penafsiran sendiri.

Di setiap entity diperlukan key attribute. Key attribute adalah attribute yang mewakili setiap data yang ditampung dan memiliki nilai yang unik.

## Menentukan Relasi Antar Entity
Di dalam requirement terkadang telah dijelaskan relasi dari beberapa entity. Namun, terkadang relasi tersebut tidak dijelaskan di dalam requirement sehingga database developer perlu menafsirkan relasi antar entity terlebih dahulu. 

Terdapat 4 macam relasi yang mungkin terjadi antar entity, yaitu: one to one, one to many, dan many to many.

### One to One
Relasi one to one adalah relasi dimana sebuah data pada sebuah entity hanya memiliki relasi ke sebuah data pada entity yang lain.

### One to Many
Relasi one to many adalah relasi dimana sebuah data pada sebuah entity memiliki relasi ke beberapa data pada entity yang lain.

### Many to One
Relasi many to one adalah relasi dimana banyak data pada sebuah entity memiliki relasi ke satu data pada entity lain. Relasi many to one merupakan kebalikan dari relasi one to many.

### Many to Many
Relasi many to many adalah relasi dimana banyak data pada sebuah entity memiliki relasi ke banyak data juga pada pada entity yang lain.

## Membuat SQL Table dari Entity
Setelah kita menentukan entity, menentukan attribute untuk setiap entity, dan juga menentukan relasi antar entity, maka kita telah memiliki ERD (Entity Relationship Diagram). Setelah kita memiliki ERD, maka selanjutnya adalah create table berdasarkan dengan data yang telah kita miliki. Untuk melakukan create table, kita dapat menggunakan query SQL.
