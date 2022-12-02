# Mongoose

## Definisi
Mongoose adalah library yang dapat dikatakan juga sebagai Object Modelling MongoDB untuk NodeJS. Mongoose dapat digunakan untuk mengelola hubungan antara data dan menyediakan validasi. Selain itu, mongoose juga digunakan untuk menerjemahkan antara object dalam kode dan merepresentasi object tersebut di mongoDB.

## Create Connection
Untuk membuat connection ke database dapat dilakukan dengan perintah berikut:

```
import mongoose from "mongoose";

const connectDB = async() => {
    try {
        const conn = await mongoose.connect(process.env.MONGO_URI, {
            useUnifiedTopology: true,
            useNewUrlParser: true,
        })
        console.log(`MongoDB is connected : ${conn.connection.host}`.cyan.underline)
    } catch (error) {
        console.log(`MongoDB Error : ${error.message}`.red.underline)
        process.exit(1)
    }
}

export default connectDB
```

Kemudian untuk membuat koneksi ke MongoDB database dapat dilakukan dengan meletakkan `MONGO_URL` ke dalam file `.env`. Kita perlu membiasakan untuk menggunakan file `.env` untuk menyimpan URL atau data rahasia yang tidak perlu dilihat oleh public.

## Define Schema
Misal kita mendefine schema seperti contoh berikut:

```
import mongoose from "mongoose";
import bcrypt from 'bcryptjs';

const userSchema = mongoose.Schema({
    nama: {
        type: String,
        required: true
    },
    email: {
        type: String, 
        required: true
    },
    password: {
        type: String,
        required: true
    }
},
{
    timestamp: true
}
);

const User = mongoose.model('users', userSchema);

export default User
```

Pada contoh di atas, dapat dilihat bahwa kita mendefine schema dan juga tipe data untuk setiap field yang akan digunakan. Disini kita juga dapat memberikan validasi data. Misalnya untuk field yang wajib diisi, kita dapat menambahkan `required: true`.

Kemudian kita akan menggunakan model user dari schema yang telah dibuat di atas untuk melakukan pengolahan data atau operasi CRUD.

## Simple CRUD

### Create
Untuk membuat sebuah data baru, kita dapat menggunakan function `create()`. Misal kita akan membuat sebuah task, maka kita dapat menggunakan perintah berikut:

```
//Create Task Todo
const createTask = asyncHandler(async (req, res) => {
    const {task, active} = req.body
    const todo = await Todo.create({task, active});

    if(todo) {
        res.status(201).json({
            success: true,
            data: todo,
            message: 'Task is created successfully'
        })
    } else {
        res.status(400).json({
            success: false,
            message: 'Something went wrong'
        })
    }
})
```

Untuk membuat task atau menjalankan perintah di atas, kita dapat menggunakan method `POST` pada route. 

### Read
Untuk menampilkan keseluruhan data, kita dapat menggunakan function `find()`. Sedangkan untuk menampilkan data by id, dapat menggunakan function `findById()` atau function `findOne(id)`. Contohnya adalah sebagai berikut:

```
//Get Task By Id
const getTaskById = asyncHandler(async (req, res) => {
    const existTask = await Todo.findOne({ _id : req.params.id})
    if(existTask){
        res.status(200).json({
            success: true,
            data: existTask,
            message: 'Task is fetched successfully'
        })
    }else{
        res.status(401).json({
            success: false,
            data: null,
            message: 'Task is Not Found'
        })
    }
})


//Get All Task
const getAllTasks = asyncHandler(async (req, res) => {
    const allTasks = await Todo.find({})
    if(allTasks){
        res.status(200).json({
            success: true,
            data: allTasks,
            message: 'All Tasks are fetched successfully'
        })
    }else{
        res.status(401).json({
            success: false,
            data: null,
            message: 'Tasks are Not Found'
        })
    }
})
```

Untuk mendapatkan data di atas, kita dapat menggunakan method `GET` pada route.

### Update
Untuk melakukan update pada data yang telah ada, kita dapat menggunakan syntax berikut:

```
//Update Todo
const updateTask = asyncHandler(async (req, res) => {
    const {task, active} = req.body
    const existTask = await Todo.findOne({ _id: req.params.id})

    if(existTask){
        existTask.task = task;
        existTask.active = active
        const updateTask = await existTask.save();
        res.status(200).json({
            success: true,
            data: updateTask,
            message: 'Task is updated successfully'
        })
    }else{
        res.status(401).json({
            success: false,
            data: null,
            message: 'Task is Not Found'
        })
    }
})
```

Sebelum melakukan update, kita harus menemukan data yang akan diupdate terlebih dahulu dengan cara mengirimkan id data. Untuk melakukannya, kita menggunakan perintah `.findOne({ _id: req.params.id})` pada contoh di atas. Untuk menjalankan update, dapat menggunakan method `UPDATE` dan `PATCH` pada route.

### Delete
Untuk menghapus data, kita dapat menggunakan `.remove()` untuk menghapus seluruh data yang ada. Jika hanya ingin menghapus satu data berdasarkan id, maka kita harus mendapatkan data yang akan dihapus terlebih dahulu dengan menggunakan `findOne()`. Berikut adalah contoh kodenya:

```
//Delete Task By Id
const deleteTaskById = asyncHandler(async (req, res) => {
    const existTask = await Todo.findOne({ _id : req.params.id})
    if(existTask){
        await existTask.remove();
        res.status(200).json({
            success: true,
            message: 'Task is deleted successfully'
        })
    }else{
        res.status(401).json({
            success: false,
            data: null,
            message: 'Task is Not Found'
        })
    }
})


//Delete All Task
const deleteAllTasks = asyncHandler(async (req, res) => {
    const allTasks = await Todo.remove({})
    if(allTasks){
        res.status(200).json({
            success: true,
            message: 'All Tasks are deleted successfully'
        })
    }else{
        res.status(401).json({
            success: false,
            data: null,
            message: 'Task is Not Found'
        })
    }
})
```

Untuk menjalankannya, kita dapat menggunakan method `DELETE` pada route.

## Populate
Populate memiliki kaitan dengan relasi database. Populate merupakan proses penggabungan 2 collection atau lebih menjadi 1 object JSON. 
