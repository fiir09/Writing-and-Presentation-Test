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

  Relasi One to One adalah relasi dimana setiap satu baris data pada table pertama hanya berhubungan dengan satu baris data pada table kedua.
  
  ![1-1](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2015%20-%20Database%20MySQL/1-1.png)

- **One to Many and Many to One Relationships**

  Relasi One to Many adalah relasi dimana setiap satu baris data pada table pertama berhubungan dengan lebih dari satu baris data pada table kedua. Sedangkan relasi Many to One adalah kebalikan dari relasi One to Many, yaitu ketika lebih dari satu baris data pada table pertama berhubungan dengan satu baris data pada table kedua.
  
  Berikut adalah visualisasi dari relasi One to Many.
  
  ![1-Many](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2015%20-%20Database%20MySQL/1-many.png)

- **Many to Many Relationships**

  Relasi Many to Many adalah relasi dimana lebih dari satu baris data pada table pertama berhubungan dengan lebih dari satu baris data pada table kedua.
  
  ![Many-Many](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2015%20-%20Database%20MySQL/many-many.png)

## SQL Table Join
Join adalah penggabungan table yang dilakukan melalui kolom atau key tertentu yang memiliki nilai terkait untuk mendapatkan satu set data dengan informasi yang lengkap. Join dapat dibagi menjadi 4 jenis, yaitu inner join, full join, left join, dan right join.

- ### Inner Join
  
  Inner Join digunakan untuk menampilkan data hanya yang sesuai di kedua table.
  
  ![inner join](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2015%20-%20Database%20MySQL/inner%20join.png)

- ### Full Join

  Full join digunakan untuk menampilkan seluruh data yang ada pada kedua table.
  
  ![full join](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2015%20-%20Database%20MySQL/full%20join.png)

- ### Left Join

  Left join digunakan untuk menampilkan semua data sebelah kiri dari table yang dijoinkan dan menampilkan data sebelah kanan yang cocok dengan kondisi join. Jika pada data sebelah kanan tidak ditemukan kecocokan dengan kondisi join, maka akan diset NULL secara otomatis.
  
  ![left join](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2015%20-%20Database%20MySQL/left%20join.png)

- ### Right Join

  Right join digunakan untuk menampilkan semua data sebelah kanan dari tabel yang dijoinkan dan menampilkan data sebelah kiri yang cocok dengan kondisi join. Jika pada data sebelah kiri tidak ditemukan kecocokan dengan kondisi join, maka akan diset NULL secara otomatis. Singkatnya, right join adalah kebalikan dari left join.
  
  ![right join](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2015%20-%20Database%20MySQL/right%20join.png)

## Database Normalization

### Definisi
Database normalization merupakan teknik analisis data yang mengorganisasikan attribute-attribute data dengan cara mengelompokkan data tersebut sehingga terbentuk suatu entitas yang non-redundant, stabil, dan fleksibel.

Database normalization ini memiliki beberapa bertujuan, diantaranta adalah untuk:

- Menghilankan redundant data pada database
- Memudahkan jika terdapat perubahan struktur table database
- Memperkecil pengaruh jika terdapat perubahan dari struktur table database

### Efek Jika Tidak Melakukan Normalization
Jika suatu database tidak dilakukan normalization, maka akan menimbulkan efek. Efek-efek yang dapat ditimbulkan diantaranya adalah:

- **INSERT Anomali**

  INSERT Anomali adalah situasi dimana tidak memungkinkan untuk memasukkan beberapa jenis data secara langsung di database.

- **DELETE Anomali**

  DELETE Anomali adalah penghapusan data yang tidak sesuai dengan yang diharapkan sehingga data yang seharusnya tidak terhapus memiliki kemungkinan untuk ikut terhapus juga.

- **UPDATE Anomali**

  UPDATE Anomali adalah situasi dimana nilai yang diubah menyebabkan inkonsistensi database sehingga data yang diubah tidak sesuai dengan yang diperintahkan atau yang diinginkan.

### Bentuk Database Normalization

- **Unnormalized Form (UNF)**

  UNF adalah bentuk data tidak normal dimana pada data tersebut terdapat pengulangan grup sehingga menimbulkan masalah saat melakukan manipulasi data.

- **First Normal Form (1NF)**

  Suatu table dikatakan 1NF ketika:
  
  - Setiap kolom bernilai tunggal (single value)
  - Setiap kolom memiliki nama yang unik
  - Urutan penyimpanan data tidak menjadi masalah

- **Second Normal Form (2NF)**

  Pada 2NF, tidak diperkenankan terdapat partial functional dependency kepada primary key dalam sebuah table. Functional dependency adalah setiap attribute yang bukan merupakan kunci bergantung secara fungsional terhadap primary key. Secara ringkas, pada tahap 2NF table harus dipecah berdasarkan primary key.

- **Third Normal Form (3NF)**

  Pada 3NF tidak diperkenankan adanya partial transitive dependency dalam sebuah table. Transitive dependency biasanya terjadi pada table hasil relasi atau kondisi dimana terdapat attribute A, B, dan C sedemikian hingga A => B dan B=> C maka C dikatakan sebagai transitive dependency terhadap A melalui B.
  
  Secara ringkas, pada 3NF ini jika terdapat attribute yang tidak bergantung pada primary key tetapi bergantung pada field yang lain, maka attribute-attribute tersebut perlu dipisah ke table yang baru.

## Aggregate Functions
Aggregate Functions adalah function yang menerima koleksi nilai dan mengembalikan nilai tunggal sebagai hasilnya. Beberapa aggregate function adalah sebagai berikut:

- ### MAX
  `MAX` adalah aggregate function yang digunakan untuk mengembalikan nilai terbesar dari kolom yang dipilih.
  
  ```
  SELECT MAX (Nama_Column)
  FROM Nama_Table
  WHERE Condition;
  ```

- ### MIN
  `MIN` adalah aggregate function yang digunakan untuk mengembalikan nilai terkecil dari kolom yang dipilih.
  
   ```
   SELECT MIN (Nama_Column)
   FROM Nama_Table
   WHERE Condition;
   ```

- ### SUM
  `SUM` adalah aggregate function yang mengembalikan jumlah total kolom numerik.
  
  ```
  SELECT SUM (Nama_Column)
  FROM Nama_Table
  WHERE Condition;
  ```

- ### COUNT
  `COUNT` adalah aggregate function yang mengembalikan jumlah baris yang cocok dengan kriteria yang telah ditentukan.
  
  ```
  SELECT COUNT (Nama_Column)
  FROM Nama_Table
  WHERE Condition;
  ```

- ### AVG
  `AVG` adalah aggregate function yang mengembalikan nilai rata-rata dari kolom numerik.
  
  ```
  SELECT AVG (Nama_Column)
  FROM Nama_Table
  WHERE Condition;
  ```

## UNION
`UNION` digunakan untuk menggabungkan kumpulan hasil dari dua atau lebih pernyataan `SELECT`. Setiap pernyataan `SELECT` dalam `UNION` harus memiliki jumlah kolom yang sama dengan urutan yang sama dan setiap kolom tersebut juga harus memiliki tipe data yang serupa.

```
SELECT Nama_Column(s) FROM Table1
UNION
SELECT Nama_Column(s) FROM Table2;
```

## GROUP BY
`GROUP BY` digunakan untuk mengelompokkan baris yang memiliki nilai yang sama ke dalam baris ringkasan. `GROUP BY` juga sering digunakan dengan aggregate function untuk mengelompokkan kumpulan hasil dengan satu atau lebih kolom.

```
SELECT Nama_Column(s)
FROM Nama_Table
WHERE Condition
GROUP BY Nama_Column(s);
```

## HAVING
`HAVING` ditambahkan ke SQL karena kata kunci WHERE tidak dapat digunakan dengan aggregate function.

```
SELECT Nama_Column(s)
FROM Nama_Table
WHERE Condition
GROUP BY Nama_Column(s)
HAVING Condition
ORDER BY Nama_Column(s);
```

## LIKE & Wildcards

### LIKE
Operator `LIKE` digunakan dalam klausa `WHERE` untuk mencari pola tertentu dalam suatu kolom. 

```
SELECT Column1, Column2, ...
FROM Nama_Table
WHERE ColumnN LIKE Pattern;
```

### Wildcards
Karakter Wildcards digunakan untuk menggantikan satu atau lebih karakter dalam sebuah string.

- **Wildcard Characters di SQL**

  - **%**

    Karakter `%` mewakili nol atau lebih karakter. 
    
    Contoh:
    
    - `%a` akan cocok dengan `banana`, `iguana`, dan 'anoa'
    
    - `k%` akan cocok dengan `kadal`, `kecambah`, dan `kecamatan`

    - `r%a` akan cocok dengan `rusa`, `rasa`, dan `raksasa`
    
  - **_**

    Karakter `_` mewakili satu karakter.
    
    Contoh:
    
    - `_api` akan cocok dengan `sapi` dan `tapi`

    - `kak_` akan cocok dengan `kaki` dan `kaku`

    - `_arun_` akan cocok dengan `karung` dan `warung`
