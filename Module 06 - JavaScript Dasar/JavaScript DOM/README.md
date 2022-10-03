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

### Membuat dan Menyematkan Element HTML

- **Membuat ELement HTML**

  Agar halaman web menjadi lebih dinamis, maka terkadang kita perlu membuat element baru. Untuk membuat element baru, kita dapat memanfaatkan method `.createElement()`. Method ini digunakan untuk membuat element baru dengan menyertakan nama tag spesifik yang dituju sebagai parameter.
  
- **Menyematkan Element HTML**

  Setelah element baru dibuat dengan menggunakan `.createElement()`, kita dapat menggunakan method `append()` dan `appendChild()` agar konten element tersebut tidak kosong.

    - **append()**
    
      Method ini digunakan untuk menerima argument yang memiliki tipe node atau string.
      
    - **appendChild()**
    
      Method ini digunakan untuk menyematkan element lain sebagai child dari element tersebut.

  **Contoh:**

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

### Memanipulasi Attribute Element

Element yang terdaftar dalam DOM terkadang masih perlu mendapatkan perubahan agar tampilan menjadi lebih dinamis. Untuk melakukan hal tersebut, maka diperlukan method `setAttribut()` dari object bertipe Element. Method tersebut menerima 2 parameter, yaitu nama attribute dan value dari attribute itu sendiri.

**Contoh Penggunaan `setAttribut()`**

Misal kita akan melakukan manipulasi pada attribute element `<img>`.

```
...
const image = document.getElementsByTagName('img')[0];
    image.setAttribute('src', 'link image');
...
```

### Menambahkan Event Pada Element

- **Definisi**

  Event merupakan hal yang tidak dapat dipisahkan ketika kita ingin membuat halaman web yang interaktif. Event merupakan kemampuan JavaScript untuk menerima keadaan atau kejadian dari suatu element. Event dapat dipicu oleh aksi yang dilakukan user seperti mengeklik tombol mouse, menekan tombol keyboard, dan sebagainya. Selain itu, event juga dapat dipicu secara terprogram.
  
  Untuk menerapkan event handler pada element, maka dapat menggunakan interface EventTarget. Salah satu method dari EventTarget adalah `addEventListener()`. Method tersebut dapat menyiapkan function yang akan dipanggil kapan pun event tersebut dipicu pada element target.
  
- **Contoh:**

  ```
  ...
  const btn = document.querySelector('button');
 
    function random(number) {
      return Math.floor(Math.random() * (number+1));
    }
 
    btn.addEventListener('click', () => {
      const rndCol = `rgb(${random(255)}, ${random(255)}, ${random(255)})`;
      document.body.style.backgroundColor = rndCol;
    });
    ...
  ```
