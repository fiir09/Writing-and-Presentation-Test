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
