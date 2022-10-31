# Responsive Web Design

## Definisi
Responsive web design bertujuan agar website yang telah dibuat dapat diakses dengan device apapun dengan ukuran berapapun dengan tampilan website yang masih tertata dengan baik dan indah. Jika suatu website tidak memiliki design yang responsive, maka sangat mungkin website tersebut menjadi kurang tertata dan tidak terlihat baik saat diakses dengan device yang memiliki ukuran berbeda.

## Viewport

### Definisi
Viewport adalah area web yang terlihat dari perangkat. Setiap perangkat memiliki ukuran viewport yang bervariasi. Ukuran viewport pada ponsel memiliki ukuran yang lebih kecil jikan dibandingkan dengan ukuran viewport pada komputer.

### Mengatur Viewport
Untuk mengatur viewport, kita dapat menggunakan tag `<meta>` seperti berikut ini:

```
<meta name = "viewport" content = "width=device-width, initial-scale=1.0">
```

Kode di atas akan memberikan instruksi kepada browser tentang cara mengontrol dimensi dan penskalaan pada halaman web.

`width=device-width` digunakan untuk men-setting lebar halaman agar mengikuti lebar layar perangkat.

`initial-scale = 1.0` digunakan untuk men-setting tingkat zoom awal saat halaman pertama kali dimuat oleh browser.

## Media Query

### Definisi
Media query merupakan modul CSS yang berguna untuk membuat layout menjadi responsive dengan menyesuaikan tampilan berdasarkan ukuran layar perangkat.

### Cara Kerja Media Query
Media query juga dapat disebut dengan breakpoint karena cara kerjanya dengan melakukan pengecekan pada ukuran viewport apakah telah sesuai dengan kondisi yang dideklarasikan atau belum. Jika kondisi telah sesuai, maka kode dalam kondisi tersebut akan dieksekusi.

### Jenis Media Query
Media query pada responsive web design umumnya hanya menggunakan 2 jenis media query, yaitu:

- **min-width**

  Contoh penggunaan:
  
  ```
  @media (max-width: 960px) {
    //kode CSS
  }
  ```
  
  Pada contoh di atas, semua kode CSS yang berada di dalam blok tersebut akan diterapkan saat lebar layar perangkat memiliki ukuran di bawah atau sama dengan 960px.

- **max-width**

   Contoh penggunaan:
  
    ```
    @media (min-width: 800px) {
      //kode CSS
    }
    ```

    Pada contoh di atas, semua kode CSS yang berada di dalam blok tersebut akan diterapkan saat lebar layar perangkat memiliki ukuran di atas atau sama dengan 800px.

