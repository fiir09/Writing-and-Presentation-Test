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

Di JavaScript terdapat 7 tipe data dapat digunakan, yaitu String, Number, BigInt, Boolean, Undefined, Null, dan Symbol.

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

- **Object**
- **Array**

## Standard Built-in Objects

Istilah "global object" atau "standard built-in object" berbeda dengan global object yang mengacu pada object dengan lingkup global. 

### String



### Number

### Math
