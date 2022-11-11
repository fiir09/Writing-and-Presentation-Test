# Authentication & Authorization

## Authentication

### Definisi
Authentication adalah suatu proses dimana seorang user (melalui berbagai macam akses fisik berupa komputer, melalui jaringan, atau melalui remote access) mendapatkan hak akses terhadap suatu entity. Seorang user melakukan login ke dalam suatu infrastruktur jaringan dan sistem mengenali user ID ini dan menerimanya untuk kemudian diberikan akses terhadap resources jaringan sesuai dengan authorization yang diterima.

### Metode Authentication

- **Single-Factor Authentication**

  Single-Factor Authentication (SFA) adalah bentuk paling sederhana dari metode authentication. Dengan SFA, seseorang mencocokkan 1 kredensial untuk memverifikasi dirinya sendiri secara online. Contoh paling populer dari SFA adalah kata sandi (kredensial) untuk nama pengguna. Sebagian besar verifikasi saat ini menggunakan metode authentication jenis ini.

- **Two-Factor Authentication**

  Two-Factor Authentication (2FA) adalah authentication yang menggunakan kombinasi kata sandi atau nama pengguna yang sama tetapi dengan tambahan diminta untuk memverifikasi dengan menggunakan sesuatu yang hanya dimiliki oleh orang tersebut, seperti mobile device. Dengan kata lain, 2FA menggunakan 2 faktor untuk mengkonfirmasi identitas.

- **Multi-Factor Authentication**

  Multi-Factor Authentication (MFA) menggunakan kombinasi dari beberapa faktor, yaitu:
  
    - Something you know, seperti username dan password
    - Something you have, seperti security card dan mobile device
    - Something you are, umumnya mengacu pada data biometrik seperti retina dan sidik jari
  
  2FA juga merupakan bagian dari MFA.

## Authorization

Authorization adalah proses penentuan apakah seorang user diizinkan atau ditolak untuk melakukan satu atau beberapa action akses terhadap resources tertentu dalam sistem. User login terhadap system dengan menggunakan user ID dan password, kemudian system mengenalinya dan user mendapatkan akses atau ditolak terhadap suatu resources system tertentu.

Authorization sangat penting bagi keamanan web. Authorization juga bertanggung jawab atas segala hal mulai dari mencegah pengguna memodifikasi akun satu sama lain, melindungi aset back-end dari penyerang, hingga memberikan akses terbatas ke layanan eksternal.

## Hubungan Authentication dan Authorization

Sebelum client dapat menikmati layanan server, client tersebut harus melalui proses authentication terlebih dahulu. Setelah proses authentication berhasil, maka akan terjalin hubungan trust antara client dan server sehingga client cukup melakukan proses authentication sekali saja sampai client tersebut logout atau keluar. Selanjutnya, setiap ada permintaan layanan, server akan menghubungi system authorization untuk menentukan apakah client tersebut berhak atas layanan yang dimintanya atau tidak. Hubungan di atas, dapat dilihat dari gambar berikut ini:

![hub auth](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2016%20-%20Authentication%20%26%20Authorization/hub%20auth.png)

## Encryption

Encryption adalah proses untuk membuat suatu susunan acak dari text yang dapat dibaca manusia (human-readable plaintext) menjadi text yang tidak dapat dibaca manusia dan hanya dimengerti oleh system saja. Text hasil proses encryption disebut dengan ciphertext.

Encryption sering digunakan untuk mengamankan data yang berupa informasi atau pesan, hal tersebut bertujuan untuk menjaga keamanan dan mencegah pihak tidak bertanggung jawab mengetahui isi dari pesan yang dikirimkan. Saat pihak ketiga yang tidak bertanggung jawab berusaha untuk membaca pesan tersebut, maka yang terbaca hanyalah teks acak yang tidak dapat dimengerti.

Meskipun proses encryption akan mengubah pesan yang dikirimkan menjadi text acak, namun pesan tersebut tetap dapat dibaca oleh penerima pesan yang dimaksudkan. Hal tersebut dikarenakan sebelum pesan tersampaikan kepada penerima pesan, ciphertext akan melewati proses decrypt terlebih dahulu. Proses decrypt merupakan proses yang mengubah text acak atau ciphertext menjadi text biasa atau plain text. Proses decrypt tersebut hanya akan terjadi jika seseorang memiliki akses atau diberi akses untuk melihat data yang dienskripsi.

### Jenis-jenis Encryption 

- **Symmetric Encryption**
- **Asymmetric Encryption**
