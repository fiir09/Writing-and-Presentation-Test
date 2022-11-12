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

Setelah model tersedia, maka kita dapat menggunakan model tersebut untuk membuat CRUD.

### Get All Todo

Untuk membuat sebuah routing entuk get all todo, maka kita dapat menggunakan syntax berikut:

```
const TodoModel = require('./models').Todo;

app.get('/todos', async function (req, res) {
  try {
    const todos = await TodoModel.findAll();
    
    res.status(200).json(todos);
  } catch (error) {
      res.status(500).json({
        message: error.message || 'internal server error',
      });
    }
});
```

### Get Todo Detail By Id

Untuk membuat sebuah routing entuk get detail todo berdasarkan ID todo, maka kita dapat menggunakan syntax berikut:

```
const TodoModel = require('./models').Todo;

app.get('/todos/:todoId', async function (req, res) {
  try {
    const { todoId } = req.params;
    const todo = await TodoModel.findOne({ id: Number(todoId) });
    
    res.status(200).json(todo);
  } catch (error) {
    res.status(500).json({
      message: error.message || 'internal server error',
    });
    }
});
```

### Create New Todo

Untuk membuat sebuah routing entuk create new todo, kita dapat menggunakan syntax berikut:

```
const TodoModel = require('./models').Todo;

app.post('/todos', async function (req, res) {
  try {
    const { title, description, startTime } = req.body;
    
    const newTodoData = {
      title: title,
      description: description, 
      startTime: startTime,
      status: 'false',
    };
    
    const newTodo = await TodoModel.create(newTodoData);
    
    res.status(201).json({
      message: 'new todo created',
      todo: newTodo,
    });
  } catch (error) {
      res.status(500).json({
        message: error.message || 'internal server error',
      });
    }
});
```

### Update Todo By Id

Untuk membuat sebuah routing entuk update todo by ID, kita dapat menggunakan syntax berikut:

```
const TodoModel = require('./models').Todo;


```

### Delete Todo By Id

Untuk membuat sebuah routing entuk delete todo by Id, kita dapat menggunakan syntax berikut:



