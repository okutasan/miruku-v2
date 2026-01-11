+++
title= "Belajar Laravel 1"
date= 2018-02-17T02:12:34+07:00
subtitle= "Persiapan dan Instalasi"
#draft: true
tags= ["laravel"]
image= "/img/laravel/laravelogo.png"
+++
<!-- <img src="/img/laravel/laravelogo.png" width="75%"> -->
Selamat malam, Ini adalah catatan belajar laravel yang saya lakukan. Semoga bermanfaat.

<!--more-->

Oke sebelum menggunakan Laravel Framework ada beberapa hal yang perlu dipersiapkan yaitu :

1. Web Server
2. Composer
3. Koneksi Internet

Pada setiap platfrom cara persiapannya berbeda-beda tergantung platfrom OS yang digunakan. Berikut beberapa persiapan yang dibutuhkan sesuai OS nya.

### Windows

1. Install XAMPP
 - Download XMPP/WAMP/ sejenisnya untuk server pada windows. Pilih yang menggunakan PHP 5. Untuk XAMPP download di [XAMPP](https://www.apachefriends.org/download.html). Setelah itu install XAMPP pada windows.  

2. Install Composer
 - Composer sendiri manajemen dependency pada PHP seperti npm (Node.js) dan Bundler (Ruby). Composer memungkinkan untuk membuat library pada project anda dan composer sendiri akan menginstall atau mengupdate secara otomatis tanpa anda harus menginstall manual -[idcloudhost](https://idcloudhost.com/pengertian-dan-manfaat-composer-bagi-developer/).

 - Download Composer [DISINI](https://getcomposer.org/Composer-Setup.exe).

 - Kemudian install Composer, tapi pastikan sudah menginstall XAMPP server dulu.

 - Cek apakah composer sudah terinstall dengan cara buka CommandPrompt. CTRL+R ketik CMD kemudian ketikan composer. Jika sudah terinstall maka akan seperti berikut : ![Composer](/img/laravel/composercmd.png)

 - Jika belum masukan/edit PATH composer sesuai lokasi install Composer. Atau bisa baca postingan [Setting *PATH* Pada Windows](https://okutasan.github.io/post/path-windows/).

3. Install Laravel Framework

Setelah composer terinstall sekarang saatnya kita menginstall Laravel Frameworknya.

 - Pertama kita buka Commandprompt windows, kemudian kita arahkan ke directory htdocs XAMPP yang telah kita install. ![Composer](/img/laravel/htdocs.png)
 - Setelah itu ketik perintah composer berikut untuk mengunduh laravel   
 `composer create-project --prefer-dist laravel/laravel blog`

> Penjelasan :  
        **composer** : perintah menjalankan composer  
        **create-project** :  pilihan untuk membuat project baru   
        **laravel/laravel** : pilihan mengunduh laravel library  
        **blog** : nama directory yang akan dibuat untuk library laravel

 - Jika sudah selesai kemudian masuk ke directory yang sudah dibuat menggunakan perintah ```cd```.
![Selesai](/img/laravel/selesai.png)  
 - Cek apakah laravel sudah terdownload dengan benar dengan perintah ```php artisan -V```. Jika benar maka versi laravel akan muncul.
![PHPArtisan](/img/laravel/phpartisan.png)
 - Buka XAMPP Control Panel dan aktifkan servernya.
![xampp](/img/laravel/xampp.PNG)
 - cek di browser dengan mengetikan di url browser ```http://localhost/fulan/public/```. Jika tampilan seperti berikut berarti laravel siap untuk dioprek dan digunakan. ![xampp](/img/laravel/laravel.PNG)

Untuk setup pada Linux bisa dibaca pada post yang telah saya buat. [Setup Laravel Linux](https://okutasan.github.io/post/laravel-2/)
Oke terimakasih semoga bermanfaat.
<img src="/img/docker/cute.jpg" width="70%">
じゃ、また ヾ(＾-＾)ノ
