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

### Definisi
Authorization adalah proses penentuan apakah seorang user diizinkan atau ditolak untuk melakukan satu atau beberapa action akses terhadap resources tertentu dalam sistem. User login terhadap system dengan menggunakan user ID dan password, kemudian system mengenalinya dan user mendapatkan akses atau ditolak terhadap suatu resources system tertentu.

## Encryption
