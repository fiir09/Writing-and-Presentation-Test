# JavaScript Dasar

## JavaScript Function

### Definisi

Function adalah sebuah blok kode dalam sebuah grup untuk menyelesaikan 1 task atau 1 fitur. Function dapat dianalogikan seperti mesin cuci yang diberi inputan (berupa baju, detergen, air, dll) kemudian diatur atau diberi perintah (melalui tombol) untuk mengerjakan sesuatu yang diinginkan.

### Syntax Function

Function dapat dituliskan dengan beberapa cara seperti berikut ini:

- **Cara Pertama (Function Classic)**

  ```
  Function namaFungsi (kondisi){
    //statement
  }
  ```

- **Cara Kedua (Function Variable)**

  ```
  Let namaFungsi = function () {
    //statement
  }
  ```

- **Cara Ketiga (Arrow Function)**

  ```
  Let namaFungsi = () => {
    //statement
  }
  ```
  
 ### Pemanggilan Function
  
 Untuk memanggil function, cukup dengan menambahkan tanda kurung `()` setelah nama function tersebut. Contohnya adalah sebagai berikut:
  
 ```
 Function namaFungsi (kondisi){
   //statement
 }
  
 namaFungsi()
 console.log (namaFungsi())
 ```
  
 Pada kode di atas, console.log akan menampilkan informasi ke dalam tab console JavaScript.
 
 - **Contoh Function**
   
   ```
   function cariAngka(){
      for (let i = 1; i <= 20; i++){
        if (i == 18){
          console.log(i)
        }
      }
    }

   cariAngka()  //Output: 18
   ```
