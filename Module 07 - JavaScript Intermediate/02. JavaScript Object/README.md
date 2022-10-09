# JavaScript Object

## Definisi

Pada programming, object merupakan sebuah tipe data pada variabel yang menyimpan property dan function (method). Property adalah data lengkap dari sebuah object. Method adalah action dari sebuah object. 

```
let namaObject = {
  property1: "value",
  property2: "value",
  property3: "value"
}
```

Sama seperti pada array, tipe data object juga dapat menyimpan property dengan tipe data apapun.

## Mengakses Object dan Property Object

- **Mengakses Object**

  Untuk mengakses object, kita dapat memanggil nama object seperti berikut ini:
  
  ```
  let siswa = {
          nama : "Ajeng",
          umur : 20,
          asal : "Bandung"
      }
      
  console.log(siswa);       //Output: {nama: 'Ajeng', umur: 20, asal: 'Bandung'}
  ```

- **Mengakses Property Object**

  Untuk mengakses suatu property pada object terdapat 2 cara yang dapat digunakan, yaitu:
  
    - **Dot Notation**

      Pada dot notation, kita dapat mengakses object dengan menambahkan tanda titik `.` di antara nama object dan property yang ingin diakses.
      
      Contoh:
      
      ```
      let siswa = {
          nama : "Ajeng",
          umur : 20,
          asal : "Bandung"
      }
      ```
      
      Misal terdapat sebuah object `siswa` seperti pada contoh di atas. Jika kita ingin mendapatkan value `Ajeng` dengan cara dot notation, maka kita dapat menambahkan kode seperti berikut ini:
      
      ```
      ...
      console.log(siswa.nama);        //Output: Ajeng
      ```
      
    - **Bracket**

      Selain dengan dot notation, kita juga dapat mengakses property object dengan menggunakan bracket. Caranya adalah dengan menuliskan nama object yang diikuti dengan nama property yang ingin diakses. Property yang ingin diakses tersebut harus diletakkan di dalam tanda kurung siku `[]`.
      
      Contoh:
      
      ```
       let siswa = {
          nama : "Ajeng",
          umur : 20,
          asal : "Bandung"
      }
      ```
      
      Misal kita ingin mengakses property umur, maka dapat menambahkan kode berikut:
      
      ```
      ...
      console.log(siswa["umur"]);       //Output: 20
      ```

## Menambahkan Property Baru

Kita dapat menambahkan property baru ke dalam object yang sudah ada. Untuk menambahkan property baru, caranya hampir mirip dengan saat kita ingin mengakses peroperty object. Namun, jika ingin menambahkan property baru, maka kita harus menuliskan value dari property tersebut.

Contoh:

```
let siswa = {
          nama : "Ajeng",
          umur : 20,
          asal : "Bandung"
      }
```

Misal kita ingin menambahkan property `hobi` dengan nilai `memancing` pada object `siswa`, maka kita dapat menambahkan kode seperti berikut:

```
siswa.hobi = "memancing"
console.log(siswa);         //Output: {nama: 'Ajeng', umur: 20, asal: 'Bandung', hobi: 'memancing'}
```

Selain dengan cara di atas, kita juga dapat menambahkan property pada object dengan menggunakan kurung siku `[]` seperti berikut:

```
siswa["hobi"] = "berenang"
console.log(siswa);           //Output: {nama: 'Ajeng', umur: 20, asal: 'Bandung', hobi: 'berenang'}
```

## Mengganti Value dari Property

Selain menambahkan property baru pada object, kita juga dapat mengganti value pada property yang ada pada object. Untuk mengganti value dari property, caranya sama dengan saat kita ingin menambahkan property baru. 

Contoh:

```
let siswa = {
          nama : "Ajeng",
          umur : 20,
          asal : "Bandung"
      }

console.log(siswa);           //Output: {nama: 'Ajeng', umur: 20, asal: 'Bandung'}
```

Misal kita ingin mengubah value pada property `asal` menjadi `Solo`, maka kita dapat menambahkan kode berikut ini:

```
...
siswa.asal = "Solo"
console.log(siswa);           //Output: {nama: 'Ajeng', umur: 20, asal: 'Solo'}
```

Selain kode di atas, kita juga dapat mengganti value pada property dengan kode berikut ini:

```
...
siswa["asal"] = "Jogja"
console.log(siswa);           //Output: {nama: 'Ajeng', umur: 20, asal: 'Jogja'}
```

## Delete Object Property

Selain menambahkan property, kita juga dapat menghapus property yang ada pada suatu object. Untuk menghapus property tersebut kita dapat menggunakan `delete` kemudian menuliskan nama object dan juga nama proeprty yang ingin dihapus.

Contoh:

```
let siswa = {
          nama : "Ajeng",
          umur : 20,
          asal : "Bandung"
      }

console.log(siswa);           //Output: {nama: 'Ajeng', umur: 20, asal: 'Bandung'}
```

Misal kita ingin menghapus property `umur`, maka kita dapat menuliskan kode berikut ini:

```
...
delete siswa.umur
console.log(siswa);           //Output: {nama: 'Ajeng', asal: 'Bandung'}
```

Selain menggunakan kode di atas, kita juga dapat menggunakan bracket untuk menghapus proeprty seperti berikut ini:

```
...
delete siswa["umur"]
console.log(siswa);           //Output: {nama: 'Ajeng', asal: 'Bandung'}
```

