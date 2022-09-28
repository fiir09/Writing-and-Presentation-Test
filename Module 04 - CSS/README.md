# CSS

## Definisi
CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mendesain halaman website. Seperti pada HTML, web browser akan membaca dokumen HTML. Jika pada dokumen HTML tersebut terdapat konten CSS, maka browser akan memproses CSS tersebut dan menampilkan design yang sesuai denga napa yang telah ditentukan.

Pada suatu website, CSS berfungsi sebagai baju yang memberi style seperti warna dan layout sehingga halaman website menjadi lebih indah dan rapi.

## Menyisipkan CSS ke HTML
Agar CSS dapat terbaca oleh browser, maka CSS harus disisipkan ke dalam dokumen HTML terlebih dahulu. Untuk menyisipkan konten CSS ke dalam dokumen HTML, terdapat 3 cara yang dapat digunakan, yaitu:

- Inline CSS

  Pada inline CSS, digunakan attribute `style` untuk menyisipkan kode CSS langsung di dalam elemen HTML. 
  
  Contoh:
  ```
  <h1 style="color: skyblue;">Welcome</h1>
  ```
  
  Tampilan di browser:
  
  ![inline CSS](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/inline%20CSS.jpg)
  
- Internal CSS

  Pada internal CSS, digunakan elemen `<style>` untuk menyisipkan kode CSS. Elemen `<style>` tersebut diletakkan di dalam `<head>`.
  
  Contoh:
  ```
  <head>
     …
    <style>
      body{
        background-color: beige;
       }
       h1 {
        color: rebeccapurple;
       }
    </style>
  </head>
  <body>
    <h1>Hello World</h1>
  </body>
  ```

  Tampilan di browser:
  
  ![internal CSS](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/internal%20CSS.jpg)
  
- Eksternal CSS

  Pada eksternal CSS, kode CSS disisipkan dengan membuat file CSS terpisah terlebih dahulu kemudian menggabungkan file CSS tersebut dengan file HTML dengan menggunakan elemen `<link>’. Elemen `<link>` tersebut diletakkan di dalam `<head>`.
  
  Contoh:
  
  ```
  Index.html
  <head>
    …
    <link rel="stylesheet" href="style.css">	
  </head>
  <body>
    <h1>Hello World</h1>
  </body>
  ```

  ```
  Style.css
  body{
      background-color: aliceblue;
  }

  h1{
      color: blueviolet;
  }
  ```

  Tampilan di browser:
  
  ![eksternal CSS](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/eksternal%20CSS.jpg)
## Syntax Dasar CSS

## Styling CSS

## Responsive Web Design

## Flexbox
