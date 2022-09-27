# HTML

## Definisi
HTML (Hypertext Markup Language) adalah sebuah bahasa komputer yang digunakan untuk membuat kerangka suatu website. HTML memiliki sifat statis sehingga HTML hanya dapat menampilkan konten yang diminta oleh developer.

## Tools HTML
Tools utama yang harus dipersiapkan sebelum membuat HTML adalah Browser dan Code Editor.
- Browser

  Browser adalah software yang digunakan untuk menerima dan menyajikan sumber informasi. Browser akan membaca dokumen HTML sesuai dengan tag-tag HTML yang terdapat       dalam dokumen tersebut.
  
  Contoh browser adalah Google Chrome dan Firefox.

- Code Editor

  Code editor adalah text editor yang dikhususkan untuk menulis kode-kode dari perangkat lunak yang dikembangkan. 
  
  Contoh dari code editor adalah Visual Studio Code, Notepad++, dan Atom.
  
## Tag HTML
Dokumen HTML terdiri dari komponen yang disebut dengan Tag HTML. Tag adalah penanda awalan dan akhiran dari sebuah elemen di HTML. Secara umum, tag HTML terdiri dari 2 tipe yaitu Opening Tag dan Closing Tag.

Pada Opening Tag (tag pembuka), tag dibuat dengan tanda kurung siku (<…>) dengan bagian tengah kurung berisi nama tag. Di bagian ini juga dapat ditambahkan dengan atribut.

Sedangkan pada Closing Tag (tag penutup), tag dibuat dengan menggunakan tanda kurung siku dimana setelah tanda kurung siku yang pertama sebelum nama tag, terdapat tanda garis miring (</…>).

Meskipun banyak tag HTML yang berpasangan (terdiri dari tag pembuka dan tag penutup), namun ada juga tag yang tidak memiliki tag penutup. Salah satu contoh tag HTML yang tidak disertai oleh tag penutup adalah tag <img> yang berfungsi untuk menampilkan gambar atau image.

**Contoh Tag HTML:**

- Tag untuk membuat heading

  Heading adalah judul yang biasanya diberikan di sebuah halaman. Di HTML, terdapat 6 tag heading sesuai dengan tingkatannya. Tag `<h1>` untuk heading yang paling     besar dan `<h6>` untuk heading yang paling kecil.

  Contoh:
  ```
  <h1>Hello World</h1>
  <h2>Hello World</h2>
  <h3>Hello World</h3>
  <h4>Hello World</h4>
  <h5>Hello World</h5>
  <h6>Hello World</h6>
  ```

  Tampilan di browser:

  ![tag heading](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2003%20-%20HTML/tag%20heading.jpg)

- Tag untuk membuat paragraf

  Di HTML, untuk membuat suatu paragraph dapat menggunakan tag `<p>`.

  Contoh:
  ```
  <p>Selamat Pagi</p>
  <p>Selamat siang</p>
  ```

  Tampilan di browser:

  ![tag paragraf](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2003%20-%20HTML/tag%20paragraf.jpg)

- Tag untuk membuat teks tebal

  Untuk membuat teks menjadi tebal, dapat menggunakan tag `<b>` atau `<strong>`.

  Contoh:
  ```
  <b>huruf tebal</b>
  <strong>ini juga tebal</strong>
  ```

  Tampilan di browser:
  **image**

- Tag untuk membuat teks miring

  Jika ingin membuat teks menjadi miring, maka dapat menggunakan tag `<i>` atau `<em>`.

  Contoh:
  ```
  <i>huruf miring</i>
  <em>ini juga miring</em>
  ```

- Tag untuk membuat daftar/lis
- Tag untuk membuat link
- Tag untuk menampilkan gambar
- Tag untuk menampilkan video
- Tag untuk menampilkan audio

## Struktur HTML
Dokumen HTML memiliki 3 tag utama, yaitu `<html>`, `<head>’, dan `<body>`. Ketiga tag tersebut kemudian akan membentuk struktur HTML seperti pada gambar berikut:

![struktur HTML](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2003%20-%20HTML/struktur%20HTML.jpg)

Penjelasan:

-	`<!DOCTYPE>`, merupakan syntax yang mendefinisikan versi dari HTML yang digunakan dan harus dideklarasikan sebelum tag `<html>`
- `<html>`, adalah root elemen dari halaman HTML. Seluruh HTML tag lainnya harus dibungkus oleh tag ini
-	`<head>`, tag ini pada umumnya berisi tag `<meta>`, `<title>`, konten CSS/JavaScript internal maupun link yang menghubungkan dengan CSS/JavaScript eksternal
-	`<body>`, tag ini berisi konten website yang ingin ditampilkan pada browser 

## HTML Sematic
HTML Sematic adalah elemen-elemen HTML yang menyatakan makna atau tujuan dari elemen itu sendiri. HTML sematic digunakan agar kode HTML dapat lebih mudah dibaca dan dipahami.

Contoh elemen-elemen HTML sematic adalah:
`<article>`, `<footer>`, `<header>`, `<nav>`


## Deploy HTML
Deploy adalah sebuah proses untuk menyebarkan aplikasi yang telah dikerjakan agar dapat digunakan oleh banyak orang. Untuk file HTML, maka perlu mendeploy file tersebut ke server. Agar dapat melakukan proses deploy HTML, maka kita dapat menggunakan Netlify yang dapat diakses melalui netlify.com. 
