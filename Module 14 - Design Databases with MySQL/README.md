# Design Databases with MySQL

## Menentukan Entity
Entity atau entitas adalah suatu object atau hal lainnya yang merepresentasikan sebuah data. Entity dapat diidentifikasikan berdasarkan requirement yang ada dalam database.

## Menentukan Attribute dari Entity
Setiap entity memiliki suatu attribute. Setelah kita selesai menentukan entity, maka selanjutnya adalah menentukan attribute yang ada dalam setiap entity. Attribute yang diperlukan di dalam entity kemungkinan sudah ada di dalam requirement document atau mungkin juga memerlukan penafsiran sendiri.

## Menentukan Relasi Antar Entity
Di dalam requirement terkadang telah dijelaskan relasi dari beberapa entity. Namun, terkadang relasi tersebut tidak dijelaskan di dalam requirement sehingga database developer perlu menafsirkan relasi antar entity terlebih dahulu. 

Terdapat 3 macam relasi yang mungkin terjadi antar entity, yaitu: one to one, one to many, dan many to many.

### One to One

### One to Many

### Many to Many

## Membuat SQL Table dari Entity
Setelah kita menentukan entity, menentukan attribute untuk setiap entity, dan juga menentukan relasi antar entity, maka kita telah memiliki ERD (Entity Relationship Diagram). Setelah kita memiliki ERD, maka selanjutnya adalah create table berdasarkan dengan data yang telah kita miliki. Untuk melakukan create table, kita dapat menggunakan query SQL.
