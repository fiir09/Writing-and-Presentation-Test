# Database MySQL

## Database
Database dapat didefinisikan sebagai kumpulan data yang disimpan secara sistematis di dalam komputer yang dapat diolah dan dimanipulasi. Secara singkat, database dapat juga disebut sebagai gudang penyimpanan data untuk diolah lebih lanjut. 

Untuk membuat database diperlukan sebuah software yang dinamakan DBMS (Database Management System). DBMS adalah software yang dapat digunakan oleh user untuk berkomunikasi dengan data yang ada di dalam media penyimpanan.

![dbms](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2015%20-%20Database%20MySQL/dbms.png)

## Istilah Pada Database

### Table
Table adalah kumpulan value yang dibangun oleh baris dan kolom yang di dalamnya berisi attribute dari sebuah data. Pada database, kolom didefinisikan sebagai struktur table, sedangkan baris adalah kontennya.

Misal terdapat sebuah kasus dimana kita akan membuat database dari mahasiswa yang ingin mendaftarkan diri pada suatu kelas dan mengisi KRS. Berdasarkan kasus tersebut, kita dapat membuat beberapa table pada database, yaitu table mahasiswa, kelas, dosen, matakuliah, dan krs.

### Field
Field didefinisikan sebagai kolom dari sebuah table dimana setiap field memiliki tipe datanya masing-masing. Dalam definisi yang lain, field merupakan kumpulan karakter yang terdapat dalam suatu attribute yang menunjukkan atau menampilkan suatu item.

Misal pada kasus sebelumnya dimana kita akan membuat database dengan salah satu tablenya yaitu table mahasiswa. Field dari table mahasiswa adalah nim, nama, jurusan, dan angkatan.

 **MAHASISWA**
| Column name | Data Type |
| --- | --- |
| NIM | int |
| Nama_mahasiswa | varchar |
| Jurusan | varchar |
| Angkatan | int |

### Record
Dalam database, record merupakan kumpulan elemen-elemen di dalam field yang saling berkaitan untuk memberikan informasi mengenai suatu entitas dengan lengkap. Secara singkat, record merupakan isi dari sebuah table.

Contoh:

**MAHASISWA**
| NIM | Nama_mahasiswa | Jurusan | Angkatan |
| --- | --- | --- | --- |
| 1901 | Lala | sastra inggris | 2019 |
| 1905 | Sari | hukum | 2019 |

Pada table di atas, baris ke 2 dan 3 merupakan record.

### Query
Query dapat didefinisikan sebagai kumpulan perintah yang digunakan untuk mengolah data dalam table maupun database.

## SQL
Secara struktur, Database dapat terbagi menjadi 2, yaitu SQL dan NoSQL. SQL (Structured Query Language) merupakan suatu bahasa yang digunakan untuk mengakses database. SQL adalah bahasa query yang digunakan untuk melakukan interaksi di RDMS (Relational Database Management System).

SQL memiliki tipe database relasional karena SQL mengatur data yang berada di dalam database secara terstruktur ke dalam baris dan kolom yang telah ditentukan dengan table yang saling terkait dalam satu database.

### Perintah SQL

Pada SQL, setidaknya terdapat 3 jenis perintah dasar. Perintah-perintah tersebut antara lain:

- **DDL (Data Definition Language)**

  DDL (Data Definition Language) adalah perintah yang digunakan untuk mendefinisikan data seperti membuat table database baru, mengubah dataset, dan menghapus data. Perintah dasar DDL dibagi menjadi setidaknya 5 jenis perintah, yaitu:
  
  - **Create**
  - **Alter**
  - **Rename**
  - **Drop**
  - **Show**

- **DML (Data Manipulation Language)**

  DML (Data Manipulation Language) adalah perintah untuk memanipulasi data. Perintah DML terbagi menjadi 4 jenis, yaitu:
  
  - **Insert**
  - **Select**
  - **Update**
  - **Delete**

- **DCL (Data Control Language)**

  DCL (Data Control Language) adalah perintah yang digunakan khususnya untuk mengatur hak apa saja yang dimiliki oleh user. Baik hak terhadap database, table, maupun field yang ada. Dengan menggunakan perintah ini, admin database dapat menjaga kerahasiaan sebuah database. Perintah dasar DCL terbagi menjadi 2, yaitu:
  
  - **Grant**
  - **Revoke**

## Database MySQL

## Database Relationships
Database Relationships adalah relasi atau hubungan antar beberapa table dalam database. Relasi antar table tersebut dihubungkan oleh primary key dan foreign key.

Primary key adalah attribute yang mengidentifikasi secara unik suatu kejadian dan juga mewakili setiap kejadian suatu entitas. Setiap table dalam database wajib memiliki 1 primary key. Sedangkan foreign key adalah attribute yang melengkapi relationship dan menunjukkan hubungan antar table induk dan table anak. 

### Tipe Database Relationships

- **One To One Relationships**
- **One to Many and Many to One Relationships**
- **Many to Many Relationships**
- **Self Referencing Relationships**

## Tipe Data pada MySQL

## Manipulasi Query
