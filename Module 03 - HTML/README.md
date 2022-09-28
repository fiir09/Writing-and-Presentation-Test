# HTML

## Definisi
HTML (Hypertext Markup Language) adalah sebuah bahasa komputer yang digunakan untuk membuat kerangka suatu website. HTML memiliki sifat statis sehingga HTML hanya dapat menampilkan konten yang diminta oleh developer.

## Tools HTML
Tools utama yang harus dipersiapkan sebelum membuat HTML adalah Browser dan Code Editor.
- **Browser**

  Browser adalah software yang digunakan untuk menerima dan menyajikan sumber informasi. Browser akan membaca dokumen HTML sesuai dengan tag-tag HTML yang terdapat       dalam dokumen tersebut.
  
  Contoh browser adalah Google Chrome dan Firefox.

- **Code Editor**

  Code editor adalah text editor yang dikhususkan untuk menulis kode-kode dari perangkat lunak yang dikembangkan. 
  
  Contoh dari code editor adalah Visual Studio Code, Notepad++, dan Atom.
  
## Tag HTML
Dokumen HTML terdiri dari komponen yang disebut dengan Tag HTML. Tag adalah penanda awalan dan akhiran dari sebuah elemen di HTML. Secara umum, tag HTML terdiri dari 2 tipe yaitu Opening Tag dan Closing Tag.

Pada Opening Tag (tag pembuka), tag dibuat dengan tanda kurung siku (<…>) dengan bagian tengah kurung berisi nama tag. Di bagian ini juga dapat ditambahkan dengan atribut.

Sedangkan pada Closing Tag (tag penutup), tag dibuat dengan menggunakan tanda kurung siku dimana setelah tanda kurung siku yang pertama sebelum nama tag, terdapat tanda garis miring (</…>).

Meskipun banyak tag HTML yang berpasangan (terdiri dari tag pembuka dan tag penutup), namun ada juga tag yang tidak memiliki tag penutup. Salah satu contoh tag HTML yang tidak disertai oleh tag penutup adalah tag <img> yang berfungsi untuk menampilkan gambar atau image.

**Contoh Tag HTML:**

- **Tag untuk membuat heading**

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

- **Tag untuk membuat paragraf**

  Di HTML, untuk membuat suatu paragraph dapat menggunakan tag `<p>`.

  Contoh:
  ```
  <p>Selamat Pagi</p>
  <p>Selamat siang</p>
  ```

  Tampilan di browser:

  ![tag paragraf](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2003%20-%20HTML/tag%20paragraf.jpg)

- **Tag untuk membuat teks tebal**

  Untuk membuat teks menjadi tebal, dapat menggunakan tag `<b>` atau `<strong>`.

  Contoh:
  ```
  <b>huruf tebal</b>
  <strong>ini juga tebal</strong>
  ```

  Tampilan di browser:
  
  ![teks tebal](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2003%20-%20HTML/teks%20tebal.jpg)

- **Tag untuk membuat teks miring**

  Jika ingin membuat teks menjadi miring, maka dapat menggunakan tag `<i>` atau `<em>`.

  Contoh:
  ```
  <i>huruf miring</i>
  <em>ini juga miring</em>
  ```
  
  Tampilan di browser:
  
  ![teks miring](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2003%20-%20HTML/teks%20miring.jpg)

- **Tag untuk membuat daftar/list**

  Terdapat 2 tipe list dalam HTML, yaitu:
  - Unordered List, menggunakan tag `<ul>`
  - Ordered List, menggunakan tag `<ol>`
  
  Kedua tag tersebut memiliki elemen `<li>` untuk mendefinisikan nilai-nilai dari list tersebut.
  
  Contoh Unordered List:
  ```
  <ul>
	  <li>Unordered List 1</li>
	  <li>Unorderes List 2</li>
	  <li>Unordered List 3</li>
  </ul>
  ```
  Tampilan di browser:
  
  ![Unordered List](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2003%20-%20HTML/Unordered%20List.jpg)
  
  Contoh Ordered List:
  ```
  <ol>
	  <li>Ordered List 1</li>
	  <li>Ordered List 2</li>
	  <li>Ordered List 3</li>
  </ol>
  ```
  Tampilan di browser:
  
  ![Ordered List](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2003%20-%20HTML/Ordered%20List.jpg)
  
- **Tag untuk membuat link**

  Untuk membuat link pada halaman web, maka dibutuhkan tag `<a>`. Tag `<a>` memiliki attribute `href` yang digunakan untuk menyimpan link website yang akan dituju.
  
  Contoh:
  ```
  <a href = “https://www.google.com/”>Google</a>
  ```
  
  Tampilan di browser:
  
  ![link](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2003%20-%20HTML/link.jpg)
  
  Saat “Google” diklik, maka akan menuju halaman awal Google.
  
- **Tag untuk menampilkan gambar**
  Untuk menampilkan gambar pada halaman website, maka dapat menggunakan tag `<img>`. Tag img memiliki attribute `src`.
  
  Selain `src`, kita juga dapat menambahkan attribute `alt` pada tag `<img>`. Atrribute `alt` berguna untuk memberikan informasi alternatif atas gambar jika user    tidak dapat melihat gambar tersebut baik dikarenakan koneksi yang buruk maupun alasan lainnya. 
  
  Contoh:
  ```
  <img src="https://img.freepik.com/free-vector/realistic-ice-cream-collection_52683-64217.jpg?w=996&t=st=1664316472~exp=1664317072~hmac=d96c75b628a13f9dcbfa00a487a0d9b3a64b7f4d0450c66e4575df32551959e8" alt="Ice Cream">
  ```
  
  Tampilan di browser:
  
  ![image](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2003%20-%20HTML/image.jpg)
  

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
	
Salah satu keuntungan menggunakan HTML sematic adalah dokumen HTML menjadi lebih mudah dibaca, baik oleh manusia maupun mesin. Perhatikan contoh berikut:

```
<div id = “header”></div>
<div class = “section”>
	<div class = “article”>
		<div class = “figure”>
			<img>
			<div class = “figcaption”></div>
		</div>
	</div>
</div>
<div id = “footer”>
```

Contoh di atas adalah layout yang dibuat dengan menggunakan tag `<div>`. Semakin banyak elemen `<div>` yang dimiliki, maka akan menimbulkan kebingungan dalam membacanya. Oleh karena itu, digunakan HTML sematic sehingga layout tersebut akan lebih mudah dibaca. Contoh dengan HTML Sematic:
	
```
<header></header>
<section>
	<article>
		<figure>
			<img>
			<figcaption></figcaption>
		</figure>
	</article>
</section>
<footer></footer>
```

## Deploy HTML
Deploy adalah sebuah proses untuk menyebarkan aplikasi yang telah dikerjakan agar dapat digunakan oleh banyak orang. Untuk file HTML, maka perlu mendeploy file tersebut ke server. Agar dapat melakukan proses deploy HTML, maka kita dapat menggunakan Netlify yang dapat diakses melalui netlify.com. 
