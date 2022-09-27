# Git & GitHub

- ## Git
  <div align = "justify">Git adalah software yang berbasis Version Control System (VCS) yang bertugas untuk mencatat setiap perubahan pada file (termasuk code yang   dibuat) atau repository   suatu project.
  <div align = "justify">Untuk mengoperasikan Git, maka harus menginstall software terlebih dahulu. Software tersebut dapat didapatkan secara gratis melalui web       unduhan resminya di Git Downloading.
    
- ## GitHub
  <div align = "justify">GitHub adalah layanan berbasis cloud yang berguna untuk menyimpan dan mengelola sebuah project yang dinamakan repository.
  <div align = "justify">GitHub memungkinkan user untuk dapat berkomunikasi dengan user lain yang memiliki kesamaan karena pada GitHub, setiap user dapat melihat     project yang dikerjakan oleh user lain dan mencari tahu siapa saja yang terhubung dengan mereka.
    
- ## Perbedaan Git & GitHub
  
    Git | GitHub
    --- | ---
    Menginstall software di penyimpanan local | Host melalui layanan cloud
    Berfokus pada version control dan code sharing | Berfokus pada source code hosting terpusat
    Akses secara offline | Akses secara online
    Tidak menggunakan fitur user management | Menggunakan user management
    Menyediakan desktop interface “Git GUI” | Menggunakan nama desktop interface “GitHub Desktop”
    Open sourced licensed | Terdapat pilihan pengguna gratis dan berbayar
    
- ## Alur Kerja Git & GitHub
    (image)
    Cara kerja Git melibatkan beberapa file project yang tersimpan di directory project. File yang tersimpan tersebut akan diperbarui dan         dipindahkan ke         staging area. Setelah peninjauan, file kode dimuat ke Git Repository.
      
   File yang telah melewati pembaruan dan peninjauan tadi lantas melewati proses commit. Proses commit tersebut nantinya akan memberi           perintah pada Git      untuk merekam profil data atau kode hingga pembuatan kode.
      
    Jika ingin dapat terus memiliki akses suatu file meskipun dengan menggunakan perangkat yang berbeda, maka kita dapat menyimpan file           tersebut ke GitHub     dengan cara membuat commit tersebut masuk ke penyimpanan GitHub.
      
- ## Mengapa Harus Menggunakan Git & GitHub?
    Dengan menggunakan Git & GitHub, maka kolaborasi dalam mengerjakan suatu project dapat dilakukan tanpa harus repot copy paste folder aplikasi yang terupdate. Selain itu, setiap anggota tim juga tidak perlu menunggu rekan dalam satu tim menyelesaikan suatu program terlebih dahulu untuk berkolaborasi. Hal tersebut dikarenakan ketika menggunakan Git & GitHub, maka kita dapat membuat file dalam project yang sama atau membuat code di file yang sama kemudian menyatukannya saat sudah selesai.
    
- ## Command di dalam Git & GitHub

    - **Repository Git**
    
      Repository adalah directory project yang kita buat. Untuk membuat repository baru, maka dapat menggunakan command “git init”.
      
      ![git init](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2002%20-%20Git%20%26%20GitHub%20Dasar/git%20init.jpg)
      
      Pada contoh di atas, "coba_gitbash" adalah nama repository baru yang akan dibuat.
    
    - **Git Commit**
    
      Commit adalah kondisi dimana revisi telah disimpan pada version control. Untuk menyimpan perubahan pada version control, maka dapat          menggunakan command “git 
      commit”.
         
         ![git commit](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2002%20-%20Git%20%26%20GitHub%20Dasar/git%20commit.jpg)
         
       Pada contoh di atas, "Commit pertama" adalah pesan checkout.
    
    - **Git push origin**
    
      Untuk mengunggah atau mempublish ke remote repository atau GitHub, maka dapat menggunakan command “git push origin”.
    
    - **Git clone**
    
      Untuk membuat cloning dari GitHub dan menyimpannya ke local (computer), maka dapat menggunakan command “git clone”.
        
       ![git clone](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2002%20-%20Git%20%26%20GitHub%20Dasar/git%20clone.jpg)
