# Build Web Service and RESTFul API with Express.js and Sequalize

## Sequelize

Sequelize adalah ORM (Object Relational Mapping) Node JS yang berbasis promise. Sequelize mendukung sebagian besar relational Database seperti MySQL, PostgresQL, MariaDB, SQLite dan Miscrosoft SQL Server. Dengan menggunakan fitu yang ada di Sequelize, kita dapat mengelola dan mengatur data di database dengan cepat dan efisien.

ORM atau Object Relational Mapping adalah suatu teknik atau metode pemrograman yang digunakan untuk mengkonversi data dari lingkungan bahasa pemrograman berorientasi object (OOP) dengan lingkungan database relational.

## Installation Sequelize

### Install Sequelize-cli

Agar dapat menjalankan generator menggunakan terminal, maka kita perlu menginstall sequelize cli terlebih dahulu. Untuk menginstall sequlize cli dapat dilakukan dengan menggunakan perintah berikut:

```
npm install -g sequelize-cli
```

![sequlize-cli](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2017%20-%20Sequelize/sequelize-cli.png)

### Install Sequelize

Ketika kita melakukan inisiasi project, pertama kita perlu menginstall sequelize menggunakan npm install sequelize. Selain itu, kita juga perlu menginstall driver sql yang dibutuhkan. 

Untuk menginstall npm, kita dapat menggunakan perintah berikut ini:

```
npm install --save sequelize
```

![sequelize](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2017%20-%20Sequelize/sequelize.png)

Untuk menginstall driver database, kita dapat menggunakan perintah berikut ini:

```
npm install --save mysql
```

![sequelize mysql](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2017%20-%20Sequelize/sequelize%20mysql.png)


## Generate Sequelize

### Sequelize init

Sebelum melakukan generate code, pertama kita perlu melakukan inisialisasi di project kita terlebih dahulu. Untuk melakukan inisialisasi, kita dapat menggunakan perintah berikut:

```
npx sequelize-cli init
```

![sequelize init](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2017%20-%20Sequelize/sequelize%20init.png)

### Setting database

### Generate Model

Pada tahap ini, kita dapat membuat table todo dengan field seperti berikut:

```
npx sequelize-cli model:generate --name Todo --attributes title:string,description:string,startTime:date,status:string 
```

![generate model1](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2017%20-%20Sequelize/generate%20model1.png)

Kemudian kita dapat mengecek ke database sehingga dapat kita gunakan untuk penimpanan DB

```
npx sequelize-cli db:migrate
```

Jika terdapat kesalahan, kita dapat mengembalikan (undo) dengan menggunakan perintah berikut:

```
npx sequelize-cli db:migrate:undo
```

### Generate Seed

Seed adalah data awal yang dapat digunakan untuk mengisi data di database untuk keperluan awal project menggunakan sequelize. Untuk melakukannya, kita dapat menggunakan perintah berikut ini:

```
npx sequelize-cli seed:generate --name demo-todo
```

![generate seed1](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2017%20-%20Sequelize/generate%20seed1.png)

Kemudian kita dapat menjalankan generate seed menggunakan sequelize dengan perintah berikut:

```
npx sequelize-cli db:seed:all
```

Jika terdapat kesalahan, maka kita dapat mengembalikan (undo) dengan menggunakan perintah ini:

```
npx sequelize-cli db:seed:undo
```

## Membuat CRUD Dengan Express dan Sequelize

### Get All Todo

### Get Todo Detail By Id

### Create New Todo

### Update Todo By Id

### Delete Todo By Id



