# Docker

## Definisi
Docker adalah software yang menjalankan suatu aplikasi dengan menggunakan container. Docker mensharing kernel dari host OS serta meng-container-kan suatu aplikasi agar dapat dijalankan dimana saja dan kapan saja. Aplikasi yang berjalan di dalam container docker terisolasi sehingga tidak akan terpengaruh oleh faktor luar. 

![docker](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2020%20-%20Docker/docker.png)

## Fungsi Docker
Docker berfungsi sebagai penyedia layanan virtual bagi aplikasi yang diinstall pada sebuah host. Docker akan menyediakan hal-hal yang diperlukan oleh aplikasi mulai dari akses file, koneksi internet, hingga port sehingga aplikasi dapat berjalan dengan lancar.

## Container vs Virtual Machine
Kenapa harus menggunakan container dibanding virtual machine (VM)?

Karena VM memakan lebih banyak resource dan waktu untuk booting karena melakukan virtualisasi pada host hardwarenya. Sedangkan container merupakan kebalikan dari VM dimana container melakukan virtualisasi pada host OS nya.

## Docker Fundamental

![docker fundamental](https://github.com/fiir09/Writing-and-Presentation-Test/blob/main/Module%2020%20-%20Docker/docker%20fundamental.png)

- **Docker File** merupakan blueprint untuk membuat image
- **Image** merupakan template untuk menjalankan container
- **Container** merupakan perwujudan dari image
- **Docker Registry** merupakan tempat untuk upload atau download image

## Perintah Dasar Docker

Berikut adalah beberapa perintah dasar yang digunakan dalam docker:

- `docker pull` digunakan untuk men-download image dari docker hub
- `docker images` digunakan untuk melihat kumpulan image yang telah terdownload
- `docker run` digunakan untuk menjalankan container
- `docker ps` digunakan untuk melihat container yang berjalan

## Docker File
Docker file merupakan sebuah blueprint untuk membuat image. Docker file juga dapat digunakan untuk membuat custom image. Untuk membuat custom image, caranya adalah sebagai berikut:

1. Buat file Dockerfile di dalam project yang dibuat
2. Tulis beberapa perintah ke dalam docker file
3. Jalankan docker file dengan menggunakan perintah berikut:

   `docker build -t NAMA_IMAGES:TAG`
   
   `docker build -t my-app:1.0`
 
## Docker Compose
Untuk menjalankan lebih dari 1 container secara bersamaan dan saling terhubung, kita dapat menggunakan `docker compose`. Caranya adalah sebagai berikut:

1. Buat file `NAMA_FILE.yaml` di dalam project yang dibuat
2. Tulis beberapa perintah di dalam file yang telah dibuat
3. Jalankan menggunakan perintah `docker-compose NAMA_FILE.yaml up`
