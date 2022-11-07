# Database MySQL

## Database
Database dapat didefinisikan sebagai kumpulan data yang disimpan secara sistematis di dalam komputer yang dapat diolah dan dimanipulasi. Secara singkat, database dapat juga disebut sebagai gudang penyimpanan data untuk diolah lebih lanjut. 

Untuk membuat database diperlukan sebuah software yang dinamakan DBMS (Database Management System). DBMS adalah software yang dapat digunakan oleh user untuk berkomunikasi dengan data yang ada di dalam media penyimpanan.

![dbms](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2015%20-%20Database%20MySQL/dbms.png)

## Istilah Pada Database

- ### Table
  Table adalah kumpulan value yang dibangun oleh baris dan kolom yang di dalamnya berisi attribute dari sebuah data. Pada database, kolom didefinisikan sebagai struktur table, sedangkan baris adalah kontennya.

  Misal terdapat sebuah kasus dimana kita akan membuat database dari mahasiswa yang ingin mendaftarkan diri pada suatu kelas dan mengisi KRS. Berdasarkan kasus tersebut, kita dapat membuat beberapa table pada database, yaitu table mahasiswa, kelas, dosen, matakuliah, dan krs.

- ### Field
  Field didefinisikan sebagai kolom dari sebuah table dimana setiap field memiliki tipe datanya masing-masing. Dalam definisi yang lain, field merupakan kumpulan karakter yang terdapat dalam suatu attribute yang menunjukkan atau menampilkan suatu item.

  Misal pada kasus sebelumnya dimana kita akan membuat database dengan salah satu tablenya yaitu table mahasiswa. Field dari table mahasiswa adalah nim, nama, jurusan, dan angkatan.

   **MAHASISWA**
  | Column name | Data Type |
  | --- | --- |
  | NIM | int |
  | Nama_mahasiswa | varchar |
  | Jurusan | varchar |
  | Angkatan | int |

- ### Record
  Dalam database, record merupakan kumpulan elemen-elemen di dalam field yang saling berkaitan untuk memberikan informasi mengenai suatu entitas dengan lengkap. Secara singkat, record merupakan isi dari sebuah table.

  Contoh:

  **MAHASISWA**
  | NIM | Nama_mahasiswa | Jurusan | Angkatan |
  | --- | --- | --- | --- |
  | 1901 | Lala | sastra inggris | 2019 |
  | 1905 | Sari | hukum | 2019 |

  Pada table di atas, baris ke 2 dan 3 merupakan record.

- ### Query
  Query dapat didefinisikan sebagai kumpulan perintah yang digunakan untuk mengolah data dalam table maupun database.

## SQL
Secara struktur, Database dapat terbagi menjadi 2, yaitu SQL dan NoSQL. SQL (Structured Query Language) merupakan suatu bahasa yang digunakan untuk mengakses database. SQL adalah bahasa query yang digunakan untuk melakukan interaksi di RDMS (Relational Database Management System).

SQL memiliki tipe database relasional karena SQL mengatur data yang berada di dalam database secara terstruktur ke dalam baris dan kolom yang telah ditentukan dengan table yang saling terkait dalam satu database.

### Perintah SQL

Pada SQL, setidaknya terdapat 3 jenis perintah dasar. Perintah-perintah tersebut antara lain:

- **DDL (Data Definition Language)**

  DDL (Data Definition Language) adalah perintah yang digunakan untuk mendefinisikan data seperti membuat table database baru, mengubah dataset, dan menghapus data. Perintah dasar DDL dibagi menjadi beberapa jenis perintah, di antaranya adalah:
  
  - **Create**
  - **Alter**

    Alter digunakan untuk mengubah struktur dari table yang ada, seperti untuk menambahkan atau menghapus kolom atau field. Alter juga dapat digunakan untuk membuat atau menghapus primary key, mengubah jenis kolom atau field yang sudah ada, serta mengubah kolom atau nama table.
    
    Contoh:
    
    - **Menambah Primary Key**

      Misal kita memiliki table mahasiswa dengan field nya adalah nim, nama, jurusan, dan angkatan. Kemudian kita ingin menjadikan field `nim` sebagai primary key.
      
      ```
      ALTER TABLE mahasiswa ADD Primary key (nim)
      ```
      
      Pada contoh di atas, `mahasiswa` merupakan nama table dan `nim` merupakan nama field yang ingin kita jadikan sebagai primary key pada table mahasiswa.

    - **Menambah Kolom atau Field**

      Misal kita ingin menambahkan field `alamat` pada table mahasiswa.
      
      ```
      ALTER TABLE mahasiswa ADD alamat varchar (50)
      ```
      
      Pada contoh di atas, `mahasiswa` merupakan nama table, `alamat` merupakan field atau kolom yang ingin kita tambahkan pada table mahasiswa, dan `varchar (50)` merupakan tipe data dari field dengan panjangnya adalah 50.

    - **Mengubah Struktur Table**

      Misal kita ingin mengubah panjang dari field alamat yang sebelumnya 50 menjadi 40.
      
      ```
      ALTER TABLE mahasiswa ALTER COLUMN alamat varchar (40)
      ```
      
      Pada contoh di atas, `mahasiswa` adalah nama table, `alamat` adalah field yang panjangnya ingin kita ubah, dan `(40)` adalah panjang field yang kita inginkan.

  - **Rename**
  - **Drop**

    Drop digunakan untuk menghapus database, table, dan view atau index.
    
    Misal kita memiliki sebuah database dengan nama PBD2021 yang memiliki table mahasiswa, kelas, dosen, matakuliah, dan krs. Kemudian kita ingin menghapus database tersebut, maka kita dapat menggunakan perintah seperti berikut ini:
    
    ```
    DROP DATABASE PBD2021
    ```
    
    Pada contoh di atas, `PBD2021` merupakan nama database yang ingin kita hapus.


- **DML (Data Manipulation Language)**

  DML (Data Manipulation Language) adalah perintah untuk memanipulasi data. Perintah DML terbagi menjadi beberapa jenis perintah, yaitu:
  
  - **Insert**

    Insert digunakan untuk memasukkan data ke kolom-kolom yang terdapat pada table.
    
    Contoh:
    
    ```
    INSERT INTO Nama_Table VALUES (value1, value2, ..., valueN)
    ```
    
    atau
    
    ```
    INSERT INTO Nama_Table (namaField1, namaField2, ..., namaFieldN) VALUES (value1, value2, ..., valueN)
    ```

  - **Select**

    Select digunakan untuk menyeleksi data berdasarkan syarat yang diberikan. Dengan menggunakan perintah select, record di dalam table tertentu dengan jumlah yang banyak dapat ditampilkan.
    
    ```
    SELECT * FROM NAMA_TABLE
    ```
    
    Perintah di atas digunakan jika kita ingin menampilkan seluruh data yang ada pada suatu table.
    
    ```
    SELECT Nama_column FROM Nama_Table
    ```
    
    Perintah di atas digunakan jika kita hanya ingin menampilkan kolom atau field tertentu yang ada pada suatu table.
    
    ```
    SELECT DISTINCT Nama_Column FROM Nama_Table
    ```
    
    Perintah di atas digunakan jika kita ingin menampilkan data yang ada pada kolom atau field tertentu yang ada pada suatu table. Perintah `DISTINCT` pada contoh di atas digunakan jika kita ingin menampilkan hasil duplikasi dari query.

  - **Update**

    Update digunakan untuk melakukan editing pada isi dari field yang dipilih. Hal tersebut dilakukan untuk memperbaiki data lama atau saat terjadi kesalahan.
    
    Contoh:
    
    ```
    UPDATE Nama_Table SET Nama_Kolom = "new data" WHERE key_column = 1;
    ```

  - **Delete**

    Delete digunakan untuk menghapus data dalam table yang menjadi target.
    
    Contoh:
    
    ```
    DELETE FROM Nama_Table WHERE Condition;
    ```


- **DCL (Data Control Language)**

  DCL (Data Control Language) adalah perintah yang digunakan khususnya untuk mengatur hak apa saja yang dimiliki oleh user. Baik hak terhadap database, table, maupun field yang ada. Dengan menggunakan perintah ini, admin database dapat menjaga kerahasiaan sebuah database. Perintah dasar DCL terbagi menjadi 2, yaitu:
  
  - **Grant**

    Grant digunakan untuk memberikan hak akses pada user.
    
    Contoh:
    
    ```
    GRANT INSERT, UPDATE, DELETE ON MAHASISWA TO PUBLIC
    ```

  - **Revoke**

    Revoke digunakan untuk mencabut hak akses yang telah diberikan kepada user.
    
    Contoh:
    
    ```
    REVOKE SELECT ON MAHASISWA TO PUBLIC
    ```

## Database MySQL

## Database Relationships
Database Relationships adalah relasi atau hubungan antar beberapa table dalam database. Relasi antar table tersebut dihubungkan oleh primary key dan foreign key.

- **Primary Key**

  Primary key adalah attribute yang mengidentifikasi secara unik suatu kejadian dan juga mewakili setiap kejadian suatu entitas. Setiap table dalam database wajib memiliki 1 primary key.
  
  Misal dalam sebuah database kita memiliki table mahasiswa dengan fieldnya yaitu nama, nim, jurusan, dan angkatan. Kita dapat menentukan primary key dalam table tersebut adalah `nim`. Hal tersebut dikarenakan `nim` berisi attribute yang unik dimana setiap mahasiswa akan memiliki nim yang berbeda dan setiap nim pasti akan merujuk pada satu nama mahasiswa.
  
  ```
  CREATE TABLE mahasiswa (
    nim int PRIMARY KEY,
    nama varchar (50),
    jurusan varchar (30),
    angkatan int
  );
  ```
  
  Pada contoh di atas, kita membuat sebuah table `mahasiswa` dengan `nim` sebagai primary key.

- **Foreign Key**

  Foreign key adalah attribute yang melengkapi relationship dan menunjukkan hubungan antar table induk dan table anak. Foreign key akan menjaga dari input data yang tidak valid pada kolom foreign key.
  
  Contoh:
  
  ```
  CREATE TABLE dosen (
    nip int PRIMARY KEY,
    nama varchar (50),
  );
  
  CREATE TABLE matakuliah (
    idMatakuliah int AUTO_INCREMENT PRIMARY KEY,
    SKS int,
    FOREIGN KEY (nip) REFERENCES dosen (nip)
  );
  ```

### Tipe Database Relationships

- **One To One Relationships**
- **One to Many and Many to One Relationships**
- **Many to Many Relationships**
- **Self Referencing Relationships**

## Tipe Data pada MySQL

## Manipulasi Query
