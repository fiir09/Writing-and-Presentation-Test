# JavaScript Data Type Built in Prototype & Method

## Dynamic and Weak Typing

JavaScript adalah bahasa yang dinamis dengan tipe yang dinamis. Variabel dalam JavaScript tidak secara langsung terkait dengan nilai tertentu dan variabel apa pun dapat diberi nilai atau pun ditetapkan kembali.

```
let foo = 41      //foo is now a number
foo = "bar"      //foo is now a string
foo = "true"    //foo is now a boolean
```

Selain dinamis, JavaScript juga merupakan weakly typed language sehingga memungkinkan konversi tipe implisit saat operasi melibatkan tipe yang tidak cocok alih-alih melemparkan kesalahan tipe.

```
const foo = 41              //foo is a number
const result = foo + "1"
console.log (result)       //Output: 411 (string)
```

Pada contoh di atas, JavaScript memaksa `foo` yang awalnya memiliki tipe data number untuk menjadi string agar dapat digabungkan dengan operan lainnya.

## Data Type

Tipe data adalah jenis data yang dapat disimpan, dimanipulasi, dan digunakan untuk memberitahu komputer bagaimana menafsirkan nilai atau datanya. Pada JavaScript, tipe data dikelompokkan menjadi 2, yaitu tipe data primitive dan non primitive.

### Tipe data Primitive

Tipe data primitive adalah tipe data yang hanya dapat menyimpan satu nilai pada satu waktu dan tidak dapat diubah menggunakan cara yang sama seperti tipe data non primitive. Tipe data primitive akan dianggap sama jika memiliki nilai yang sama.

Di JavaScript terdapat 7 tipe data dapat digunakan, yaitu:.

  - **String**
  - **Number**
  - **BigInt**
  - **Boolean**
  - **Undefined**
  - **Null**
  - **Symbol**

### Tipe Data Non Primitive

Tipe data non primitive merupakan tipe data yang dapat menyimpan lebih dari satu nilai pada satu waktu dan dapat diubah. Tipe data non primitive akan dianggap berbeda meskipun memiliki nilai yang sama dan dalam urutan yang sama.

Di JavaScript, terdapat banyak tipe data non primitive, di antaranya Array, Object, Map, Set, WeakMap, WeakSet, Date, dan lain sebagainya. Semua tipe data tersebut merupakan object.

## Standard Built-in Objects

Istilah "global object" atau "standard built-in object" berbeda dengan global object yang mengacu pada object dengan lingkup global. 

### String

- **Definisi**

  Object string digunakan untuk mewakili dan memanipulasi urutan karakter. String berguna untuk menyimpan data yang dapat direpresentasikan dalam bentuk text. 

- **Membuat String**

  String dapat dibuat sebagai primitive, dari literal string, maupun sebagai object dengan menggunakan `String()`. Contoh:
  
  ```
  const string1 = "A string primitive";
  const string2 = 'Also a string primitive';
  const string3 = `Yet another string primitive`;
  
  const string4 = new String("A String object");
  ```
  
  Primitive string dan object string memiliki banyak perilaku, tetapi memiliki perbedaan dan peringatan penting lainnya.
  
  Literal string dapat ditentukkan menggunakan tanda kutip tunggal `''`  atau tanda kutip ganda `""` yang diperlakukan secara identik atau menggunakan karakter backtick ` `` `.

- **Property String Length**

  Property `length` dari string berisi panjang string dalam unit kode UTF-16. Attribute property dari String length tidak dapat ditulis, dihitung, dan dikonfigurasikan. Property ini mengembalikan jumlah unit kode dalam string.
  
  ```
  const str = 'Life, the universe and everything. Answer:';

  console.log(`${str} ${str.length}`);
  
  //Output: "Life, the universe and everything. Answer: 42"
  ```

### Number

- **Definisi**

  Number adalah object pembungkus primitive yang digunakan untuk mewakili dan memanipulasi angka.

  Konstruktor `number` berisi konstanta dan metode untuk bekerja dengan angka. Nilai dengan tipe yang lain dapat dikonversikan ke number menggunakan function    `number()`. Saat digunakan sebagai function `number (value)` mengonversi string atau nilai lain ke tipe number. Jika nilai tidak dapat dikonversi, maka ia akan mengembalikan `NaN`.

  Contoh:

  ```
  Number ("123")            //return the number 123
  Number ("123") === 123    // true

  Number ("unicorn")        //NaN
  Number (undefined)        //NaN
  ```
  
- **Property Number**
  
  Number memiliki beberapa property, di antaranya adalah:
  
    - **Number.EPSILON**
    
      Property `Number.EPSILON` mewakili perbedaan antara 1 angka floating point terkecil yang lebih besar dari 1. 
      
      ```
      const result = Math.abs(0.2 - 0.3 + 0.1);

      console.log(result);      //Output: 2.7755575615628914e-17

      console.log(result < Number.EPSILON);    //Output: true
      ```
      
    - **Number.MAX_VALUE**
    
      Property `Number.MAX_VALUE` mewakili nilai numerik maksimum yang dapat diwakili dalam JavaScript.
      
      ```
      function multiply(x, y) {
        if (x * y > Number.MAX_VALUE) {
          return ('Process as Infinity');
        }
        return (x * y);
      }

      console.log(multiply(1.7976931348623157e+308, 1));      //Output: 1.7976931348623157e+308

      console.log(multiply(1.7976931348623157e+308, 2));      //Output: "Process as Infinity"
      ```
      
    - **Number.MIN_VALUE**
    
      Property `Number.MIN_VALUE` mewakili nilai numerik positif terkecil yang dapat diwakili dalam JavaScript.
      
      ```
      function divide(x, y) {
        if (x / y < Number.MIN_VALUE) {
          return 'Process as 0';
        }
        return (x / y);
      }

      console.log(divide(5e-324, 1));      //Output: 5e-324

      console.log(divide(5e-324, 2));     //Output: Process as 0
      ```
      
    - **Number.NaN**
    
      Property `Number.NaN` mewakili Not-A-Number yang setara dengan `NaN`.
      
      ```
      function clean(x) {
        if (x === Number.NaN) {
          return null;
        }
        if (isNaN(x)) {
          return 0;
        }
      }

      console.log(clean(Number.NaN));     //Output: 0
      ```
 - **Method Number**
 
   Number memiliki beberapa method, di antaranya adalah:
   
    - **Number.isFinite()**
    
      Method `Number.isFinite()` menentukan apakah nilai yang diteruskan adalah bilangan berhingga. Property ini memeriksa apakah nilai yang diberikan adalah bilangan dan bilangan itu bukan bilangan positif infinity, negatif infinity, atau NaN.
      
      **Syntax Penulisan**
      
      Syntax dari method `Number.isFinite()` adalah sebagai berikut:
      
      ```
      Number.isFinite(value)
      ```
      
      `value` di atas adalah nilai yang akan diuji untuk fititeness
      
      **Contoh:**
      
      ```
      Number.isFinite(Infinity); // Output: false
      Number.isFinite(NaN); // Output: false
      Number.isFinite(-Infinity); // Output: false

      Number.isFinite(0); // Output: true
      Number.isFinite(2e64); // Output: true
      ```
      
    - **Number.isInteger()**
    
      Method `Number.isInteger()` menentukan apakah nilai yang diteruskan adalah bilangan bulat atau tidak.
      
      **Syntax Penulisan**
      
      ```
      Number.isInteger(value)
      ```
      
      `value` di atas adalah nilai yang akan diuji untuk menentukan apakah nilai tersebut merupakan bilangan bulat atau tidak.
      
      **Contoh**
      
      ```
      Number.isInteger(1);          //Output: true
      Number.isInteger(-100000);    //Output: true
      Number.isInteger(0.1);        //Output: false
      Number.isInteger("10");       //Output: false
      ```
      
    - **Number.isNaN()**
    
      Method `Number.isNaN()` menentukan apakah nilai yang diteruskan adalah `NaN` dan tipenya adalah number atau bukan.
      
      **Syntax Penulisan**
      
      ```
      Number.isNaN(value)
      ```
      
      `value` pada kode di atas adalah nilai yang akan diuji `NaN`.
      
      **Contoh**
      
      ```
      Number.isNaN(NaN);          //Output: true
      Number.isNaN(Number.NaN);   //Output: true
      Number.isNaN(0 / 0);        //Output: true
      Number.isNaN(37);           //Output: false
      ```

### Math

- **Definisi**

  `Math` adalah built-in object yang memiliki property dan method untuk konstanta dan fungsi matematika. `Math` bekerja dengan `Number` tetapi tidak bekerja dengan `BigInt`.
  
  `Math` bukan konstruktor seperti kebanyakan object global lainnya. Semua property dan method `Math` memiliki sifat statis.

- **Property Math**

  Math memiliki beberapa property, di antaranya adalah:
  
  - **Math.E**
  
    Properti `Math.E` mewakili bilangan Euler, basis logaritma natural yaitu e (kira-kira 2,718).
    
    Contoh:
    
    ```
    function getNapier() {
      return Math.E;
    }

    getNapier();    //Output: 2.718281828459045
    ```
  
  - **Math.LN10**
  
    Properti `Math.LN10` mewakili logaritma natural dari 10 (sekitar 2,302).
    
    Contoh:
    
    ```
    function getNatLog10() {
      return Math.LN10;
    }

    getNatLog10(); //Output: 2.302585092994046
    ```
  
  - **Math.LOG10E**
  
    Properti `Math.LOG10E` mewakili logaritma basis 10 dari e (sekitar 0,434).
    
    Contoh:
    
    ```
    function getLog10e() {
      return Math.LOG10E;
    }

    getLog10e(); //Output: 0.4342944819032518
    ```
  
  - **Math.PI**
  
    Properti `Math.PI` mewakili rasio keliling lingkaran dengan diameternya, sekitar 3,14159.
    
    Contoh:
    
    ```
    function calculateCircumference(radius) {
      return Math.PI * (radius + radius);
    }

    calculateCircumference(1); //Output: 6.283185307179586
    ```
  
  - **Math.SQRT2**
  
    Properti `Math.SQRT2`mewakili akar kuadrat dari 2, sekitar 1,414.
    
    Contoh:
    
    ```
    function getRoot2() {
      return Math.SQRT2;
    }

    getRoot2(); //Output: 1.4142135623730951
    ```

- **Method Math**

Math memiliki beberapa method, di antaranya adalah:

  - **Math.abs()**
  
    `Math.abs()` digunakan mengembalikan nilai mutlak suatu bilangan.
    
    Contoh:
    
    ```
    Math.abs(-8); //Output: 8
    Math.abs(-0); //Output: 0
    ```

  - **Math.ceil()**
  
    `Math.ceil()` selalu membulatkan dan mengembalikan bilangan bulat yang lebih kecil, lebih besar dari, atau sama dengan angka yang diberikan.
    
    Contoh:
    
    ```
    Math.ceil(-7.004); //Output: -7
    Math.ceil(-4); //Output: -4
    Math.ceil(-0.95); //Output: -0
    ```
  
  - **Math.floor()**
  
    `Math.floor()` digunakan untuk membulatkan ke bawah dan mengembalikan bilangan bulat terbesar yang kurang dari atau sama dengan angka tertentu.
    
    Contoh:
    
    ```
    Math.floor(45.05); //Output: 45
    Math.floor(45.95); //Output: 45
    ```
  
  - **Math.max()**
  
    `Math.max()` akan mengembalikan angka terbesar yang diberikan sebagai parameter input.
    
    Contoh:
    
    ```
    Math.max(10, 20); //Output: 20
    Math.max(-10, -20); //Output: -10
    Math.max(-10, 20); //Output: 20
    ```
  
  - **Math.min()**
  
     `Math.min()` akan mengembalikan angka terkecil yang diberikan sebagai parameter input.
     
     Contoh:
     
     ```
     Math.min(10, 20); //Output: 10
     Math.min(-10, -20); //Output: -20
     Math.min(-10, 20); //Output: -10
     ```
  
  - **Math.round()**
  
    `Math.round()` digunakan untuk mengembalikan nilai angka yang dibulatkan ke bilangan bulat terdekat.
    
    Contoh:
    
    ```
    Math.round(-20.5);    //Output: -20
    Math.round(-0.1);     //Output: -0
    Math.round(20.49);    //Output: 20
    Math.round(20.5);     //Output: 21
    ```
  
  - **Math.sqrt()**
  
    `Math.sqrt()` digunakan untuk mengembalikan akar kuadrat dari suatu bilangan.
    
    Contoh:
    
    ```
    Math.sqrt(-1); //Output: NaN
    Math.sqrt(0); //Output: 0
    Math.sqrt(1); //Output: 1
    Math.sqrt(2); //Output: 1.414213562373095
    Math.sqrt(9); //Output: 3
    ```
