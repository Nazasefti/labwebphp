# Nama : Naza Sefti Pranita 

# NIM : 312210306

# Kelas : TI.22.A3

# Mata Kuliah : Pemrograman Web 2

# Praktikum 1 | Kerangka PHP (Codeigniter)

# Langkah langkah praktikum

# Persiapan

Sebelum memulai menggunakan Framework Codeigniter, perlu dilakukan konfigurasi pada server web. Beberapa ekstensi PHP perlu diaktifkan untuk kebutuhan pengembangan Codeigniter 4. Berikut beberapa ekstensi yang perlu diaktifkan:

- ekstensi php-json untuk bekerja dengan JSON;

- driver asli php-mysqlnd untuk MySQL;

- ekstensi php-xml untuk bekerja dengan XML;

- php-intl ekstensi untuk membuat aplikasi multibahasa;

- libcurl (opsional), jika ingin menggunakan Curl.

Untuk mengaktifkan ekstentsi tersebut, lewati XAMPP Control Panel, pada bagian Apache klikConfig -> PHP.ini

![Screenshot (25)](https://github.com/Nazasefti/labwebphp/assets/115772516/92619161-d289-4ad5-831d-b36567d0c77a)

Pada bagian extension, hilangkan tanda ; (titik koma) pada ekstensi yang akan diaktifkan. Kemudian simpan kembali filenya dan restart server web Apache.

![Screenshot (26)](https://github.com/Nazasefti/labwebphp/assets/115772516/c1b69d6d-be25-40c1-83a5-1d7a382355ea)

# Instalasi CodeIgniter 4

Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara manual.

- Unduh Codeigniter dari situs web https://codeigniter.com/download
  
- Ekstrak file zip Codeigniter ke direktori htdocs/lab11_ci.
  
- Ubah nama direktori framework-4.x.xx menjadi ci4.
  
- Buka browser dengan alamat http://localhost/lab11_ci/ci4/public/

# Penjaga CLI (Antarmuka Baris Perintah)

Codeigniter 4 menyediakan CLI untuk mempermudah proses pengembangan. Untuk mengakses CLI buka terminal/command prompt. Arahkan lokasi direktori sesuai dengan direktori kerja proyek yang dibuat (xampp/htdocs/lab11_ci/ci4/).

Perintah yang dapat dijalankan untuk memanggil CLI Codeigniter adalah :

    php spark

# Mengaktifkan Mode Debugging

- Ketik php spark serve pada CLI untuk menjalankan.

- Menampilkan pesan error, untuk coba ubah kode file app/Controllers/home.php, hapus ;nya.
  
- Ketik http://localhost:8080pada browser. Berikut tampilan errornya.
  
- Kemudian, ubah nama file envmenjadi .env. Masuk ke dalam filenya, hapus tanda #padaCI_ENVIRONMENT =
  
- Refresh url sebelumnya, Berikut tampilan errornya.

# Perutean dan Pengontrol

Router terletak pada fileapp/config/Routes.php

# Membuat Rute Baru

Tambahkan kode berikut di dalamRoutes.php

    $routes->get('/about', 'Page::about');
    $routes->get('/contact', 'Page::contact');
    $routes->get('/faqs', 'Page::faqs');
