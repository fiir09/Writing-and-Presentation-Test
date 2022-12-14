# CSS

## Definisi
CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mendesain halaman website. Seperti pada HTML, web browser akan membaca dokumen HTML. Jika pada dokumen HTML tersebut terdapat konten CSS, maka browser akan memproses CSS tersebut dan menampilkan design yang sesuai dengan apa yang telah ditentukan.

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

  Pada eksternal CSS, kode CSS disisipkan dengan membuat file CSS terpisah terlebih dahulu kemudian menggabungkan file CSS tersebut dengan file HTML dengan menggunakan elemen `<link>`. Elemen `<link>` tersebut diletakkan di dalam `<head>`.
  
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
   Syntax CSS digunakan untuk menunjuk atau memilih elemen HTML mana yang ingin diberi style. Syntax CSS terdiri dari selector, property, dan value seperti berikut:
  
   ```
   Selector{
    Property: value;
   }
   ```
  
   Contoh:
  
   ```
   h1{
    color: blueviolet;
   }
   ```
    
   Pada contoh di atas, `h1` adalah selector, `color` adalah property, dan `blueviolet` adalah value.
  
   Syntax CSS tersebut akan memberikan warna blueviolet untuk setiap konten yang ada di dalam tag `<h1>`.

## Styling CSS

  - **CSS - Tag Name**
 
    Untuk mendesain elemen HTML di CSS dapat menggunakan tag element HTML secara langsung pada CSS. Jika kita menggunakan tag element, maka desain tersebut akan bersifat global yang artinya akan mempengaruhi seluruh tag elemen HTML yang ada pada file tersebut.
    
    Contoh:
    ```
    Style.css
    h1{
      color: blueviolet;
    }
    ```
    
    ```
    Index.html
    <h1>Welcome</h1>
    <p>Selamat datang di IndoApril</p>
    <h1>Terima Kasih</h1>
    <p>Terima kasih telah berbelanja</p>
    ```
    
    Dengan menambahkan style CSS tersebut, maka seluruh konten pada HTML yang menggunakan tag `<h1>` akan memiliki warna blueviolet seperti berikut ini:
    
    ![CSS - Tag Name](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/CSS%20-%20Tag%20Name.png)
    
  - **CSS - Class Name**
    
    Attribute `class` dapat digunakan elemen HTML kemudian memanggil nama class tersebut pada CSS. HTML yang memiliki class yang sama akan mempunyai styling yang sama saat digunakan pada CSS.
    
    Contoh:
    ```
    Style.css
    .p{
      color: skyblue;
      font-size: 40px;
    }
    ```
    
    ```
    Index.html
    <div class="p">Selamat Pagi</div>
    <div class="p">Selamat Siang</div>
    ```
    
    Pada contoh di atas, seluruh elemen HTML yang memiliki `class="p"` akan diberi style yang sama, yaitu warna teks skyblue dan font size 40px seperti berikut ini:
   
    ![CSS - Class Name](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/CSS%20-%20Class%20Name.png)
    
  - **CSS - ID Name**
    
    Berbeda dengan Class Name, ID Name memiliki sifat unik yang berarti hanya ada 1 nama ID pada 1 elemen HTML. ID Class biasanya digunakan jika hanya ada 1 elemen pada 1 page, seperti `navigation`, `header`, dan `footer`.
    
  - **Chaining Selector**

    Chaining Selector dapat digunakan pada kasus seperti saat kita memiliki 3 tag elemen HTML pada CSS, namun kita ingin ada 1 elemen HTML yang memiliki styling berbeda.

  - **!important CSS**

    !important CSS berada pada level paling atas dari ID dan Class. Jika pada styling CSS digunakan !important CSS, maka styling sebelumnya akan dikesampingkan atau dibatalkan.

## Responsive Web Design
   - **Viewport**

      Viewport adalah daerah pada layar yang menampilkan suatu konten atau halaman website yang sedang diakses. Ukuran viewport tidak selalu sama dengan resolusi layar perangkat.
      
      Agar halaman website yang akan dibuat tetap terlihat rapi di perangkat dengan ukuran apapun, maka kita harus membuat halaman website tersebut menjadi responsive. Untuk membuat halaman website menjadi responsive, maka perlu menambahkan meta data di dalam elemen `<head>` yang ada di HTML. Meta data yang perlu ditambahkan adalah seperti berikut:
      
      ```
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      ```
      
      Meta data di atas akan memberikan instruksi kepada browser untuk mengatur bagaimana dimensi dan skala dari halaman website.
      
   - **Media Query**

     Setiap perangkat (mobile, laptop, dll) memiliki resolusi layar yang berbeda-beda. Agar tampilan website tetap terlihat bagus diresolusi apapun, maka dapat menggunakan media query. Dengan menggunakan media query, kita dapat mengatur lebar suatu elemen dan/atau memberikan style lain yang berbeda-beda sesuai dengan ukuran dari browser.
     
     Contoh:
     ```
     @media (max-width: 600px){
        .class{
          property: value;
         }
     }
     ```
     
     Pada contoh di atas, `@media (max-width: 600px)` merujuk pada jendela browser yang lebarnya maksimal 600px. Dengan kata lain, seluruh kode CSS yang ada di dalam `@media` akan diterapkan jika lebar layarnya 600px atau kurang.
     
     Berdasarkan contoh di atas, elemen dengan class `class` akan memiliki property dan value `property: value;` jika lebar layar kurang dari sama dengan 600px.

## Flexbox
   Flexbox (flexible box) adalah cara untuk mengatur layout. Flexbox memudahkan untuk mengatur layout, posisi, dan ukuran dari setiap elemen di dalamnya.
  
   Terdapat 2 istilah penting pada flexbox, yaitu:
  
    - Container, merupakan elemen yang membungkus dan mengatur tampilan dari elemen di dalamnya
  
    - Item, merupakan elemen di dalam container yang diatur tampilannya
  
   Pada konsepnya, flexbox memiliki 1 kontainer dan pada container tersebut dapat memiliki beberapa (lebih dari 1) item.
  
  #### Properti Flex pada Container
  
  - **Display**
  
    Langkah pertama untuk membuat sebuah container menjadi flex adalah dengan menambahkan `flex` pada property `display`. Dengan menambahkan `flex`, maka container yang kita miliki akan dapat menggunakan property flex.

    ```
    .container{
      display: flex;
    }
    ```
  
  - **flex-direction**
  
    Property flex-direction digunakan untuk mengatur letak dan menentukkan arah dari item child. Pada flex-direction, terdapat 4 value yang dapat diberikan, yaitu:
  
    - row (default)
  
      Secara default, letak item child membentuk sebuah baris dari kiri ke kanan.
  
      Contoh:
  
      ```
      Style.css
       .container{
          border: 5px solid aliceblue;
          display: flex;
          flex-direction: row;
       }

        .item{
            border: 5px solid aliceblue;
            flex-basis: 100%;
            background: blueviolet;
            font-size: 60px;
            color: white;
            text-align: center;
        }
      ```
  
      ```
      Index.html
      ...
      <div class="container">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
      </div>
      ```
      
      Tampilan di browser:
  
      ![flex-direction-row](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/flex-direction-row.jpg)
      
    - row-reverse
  
      Dengan row-reverse, letak item child akan membentuk sebuah baris dari kanan ke kiri.
  
      ![flex-direction-row-reverse](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/flex-direction-row-reverse.jpg)
  
    - colomn
  
      Dengan colomn, letak item child membentuk sebuah baris dari atas ke bawah.
       
      ![flex-direction-colomn](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/flex-direction-colomn.jpg)
  
    - colomn-reverse
      Dengan colomn-reverse, letak item child membentuk sebuah garis dari bawah ke atas.
  
      ![flex-direction-colomn-reverse](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/flex-direction-colomn-reverse.jpg)
  
  - **flex-wrap**
  
    Secara default, flex akan membuat layout item child dalam 1 baris saja dengan menyesuaikan space yang ada. Namun, jika ingin membatasi jumlah item child dalam 1 baris lalu item child lain akan berpindah ke posisi baris yang baru, maka dapat menggunakan `flex-wrap`.
  
    Property yang dapat digunakan pada `flex-wrap`, yaitu:
  
    - wrap
  
      Dengan property `wrap`, flex item akan memiliki beberapa line dari atas ke bawah jika space dalam 1 line telah full width.
      
      Contoh:
      ```
      Style.css
       .container{
          border: 5px solid aliceblue;
          display: flex;
          flex-wrap: wrap;
       }

        .item{
            border: 5px solid aliceblue;
            width: 500px;
            background: blueviolet;
            font-size: 60px;
            color: white;
            text-align: center;
        }
      ```
  
      ```
      Index.html
      ...
      <div class="container">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
      </div>
      ```
  
      Tampilan di browser:
  
      ![flex-wrap-wrap](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/flex-wrap-wrap.jpg)
  
    - wrap-reverse
  
      Dengan property `wrap-reverse`, flex item akan memiliki beberapa line dari bawah ke atas jika space dalam 1 line telah full width.
  
      ![flex-wrap-wrap-reverse](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/flex-wrap-wrap-reverse.jpg)
  
    - nowrap (default)
  
      Secara default, flex tidak menggunakan flex-wrap.
      
      ![flex-wrap-nowrap](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/flex-wrap-nowrap.png)
  

  - **justify-content**
  
    Property justify-content digunakan untuk mengatur tata letak dan space antar item child secara horizontal atau main axis.
  
    Justify-content memiliki 6 value, yaitu:
  
    - flex-start
  
      Seluruh item akan ditempatkan di depan.
  
      Contoh:
      ```
      Style.css
      .container{
          border: 5px solid aliceblue;
          display: flex;
          justify-content: flex-start;
      }

      .item{
          border: 5px solid aliceblue;
          width: 200px;
          background: blueviolet;
          font-size: 60px;
          color: white;
          text-align: center;
      }
      ```
  
      ```
      Index.html
      <div class="container">
        <div class="item">1</div>
        <div class="item">2</div>
        <div class="item">3</div>
        <div class="item">4</div>
      </div>
      ```
  
      Tampilan di browser:
  
      ![justify-content-flex-start](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/justify-content-flex-start.png)
  
    - flex-end
  
      Seluruh item akan ditempatkan di belakang.
  
      ![justify-content-flex-end](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/justify-content-flex-end.png)
  
    - center
  
      Value ini akan memampatkan item ke bagian tengah.
  
      ![justify-content-center](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/justify-content-center.png)
  
    - space-between
  
      Value ini akan memberikan ruang pada setiap 2 item yang bersebelahan.
  
      ![justify-content-space-between](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/justify-content-space-between.png)
  
    - space-around
  
      Value ini akan memberikan ruang pada setiap item (tidak hanya di setiap 2 item yang bersebelahan saja).
  
      ![justify-content-space-around](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2004%20-%20CSS/justify-content-space-around.png)
  
  
      
  
