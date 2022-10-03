# JavaScript HTML DOM

## Definisi
DOM (Document Object Model) yang berarti dokumen (HTML) yang dimodelkan dalam sebuah object. Object dari dokumen ini menyediakan sekumpulan function dan attribute/data yang dapat dimanfaatkan dalam membuat program JavaScript. Inilah yang disebut dengan API (Application Programming Interface). Dengan adanya DOM, JavaScript diberi akses untuk membuat HTML menjadi dinamis.

Perlu diingat bahwa DOM bukan merupakan bagian dari JavaScript, melainkan bagian dari browser (web API).

## Struktur HTML DOM

![HTML DOM](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2006%20-%20JavaScript%20Dasar/HTML%20DOM.png)

## DOM Property dan DOM Method

Di HTML DOM, semua element HTML dari sebuah website akan dianggap sebagai object. Sama seperti object JavaScript pada umumnya, object element HTML di HTML DOM juga mempunyai properti dan method atau yang lebih dikenal dengan istilah DOM Property dan DOM Method. DOM Property dapat digunakan untuk mengubah nilai property dari element HTML. Sedangkan DOM Method dapat digunakan untuk memanggil function dari suatu element HTML.

## Memanipulasi Element HTML

### Mengakses Element HTML

Jika ingin mengakses elemen yang spesifik, maka dapat menggunakan beberapa function berikut ini:

- **getElementById()**

  Function tersebut digunakan untuk memilih element berdasarkan attribute `id`.

- **getElementByName()**

  Function tersebut digunakan untuk memilih element berdasarkan attribute `name`.
  
- **getElementByClassName()**

  Function tersebut digunakan untuk memilih element berdasarkan attribute `class`.

- **getElementByTagName()**

  Function tersebut digunakan untuk memilih element berdasarkan nama tag.

- **querySelector()**

  Function tersebut digunakan untuk memilih element berdasarkan query.
 
 
**Contoh Penggunaan**

```
Index.html

<body>
  <div id = "header">
    ...
  </div>
  
  <div class = "container"></div>
</body>
```

```
document.getElementById ("header")
document.getElementByClassName ("container")
```

### Mengubah Konten Element

- **Element.textContent**

  `Element.textContent` dapat digunakan untuk mengubah teks di dalam sebuah element.
  
  Contoh Penulisan:
  
  ```
  ...
  document.getElementById ("heading").textContent = "perubahan text"
  ...
  ```

- **Element.innerHTML**

  `Element.innerHTML` dapat digunakan untuk mengubah konten HTML di dalam sebuah element.
  
  Contoh Penulisan:
  
  ```
  ...
  document.getElementById ("heading").innerHTML = "perubahan konten HTML"
  ...
  ```

### Membuat Element HTML

Untuk membuat sebuah element HTML, dapat menggunakan:

- **.createElement()**

  `.createElement()` digunakan untuk membuat sebuah element HTML.

- **.textContent**

  `.textContent` digunakan untuk mengubah kontennya.

- **appendChild()**

  `appendChild()` digunakan untuk menambahkan elemen ke DOM

**Contoh: **

```
<div id = "header"></div>

//membuat element heading
const heading = document.createElement("h1")
heading.textContent = "Ini Heading"

document.getElementById ("header").appendChild (heading)
```

Hasil akhir dari kode di atas akan terlihat seperti berikut ini:

```
<div id = "header">
  <h1>Ini Heading</h1>
</div>
```
### Interaksi User (Events)

Interaksi user bersifat 2 arah. Selain menampilkan elemen HTML, halaman web juga harus dapat menangkap interaksi user. Untuk menangkap interaksi user, maka dapat menggunakan:

- **Element.addEventListener(“event”)**

  

- **Element.onevent**

