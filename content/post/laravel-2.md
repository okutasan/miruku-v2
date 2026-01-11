+++
title= "Belajar Laravel 1.1"
date= 2018-10-12T22:39:05+07:00

subtitle= "MO DAIJOBU, NAZETTE... WATASHIGA KITA!"
categories = [
    "Linux",
    "Shell"
]
tags= ["laravel","linux"]
image = "/img/midoriya.png"
+++

<!-- <p><img src="/img/midoriya.png" alt="midoriya" width="80%"></p>    -->
こんにちはみんな! (^o^)/  

Halo semua, yatta setelah mencoba beberapa kali dan gagal akhirnya saya bisa memasang laravel pada mesin linux Xubuntu 18.04 saya. Nah ini adalah beberapa langkah yang saya lakukan.<!--more-->

**1. Install Web Server dan PHP**   

Oke sebelum menginstall laravel kita harus menyiapkan web server apache dan juga php. Pada linux bisa menggunakan LAMP ataupun bisa langsung kita menginstall kebutuhan tersebut secara manual.     
Kali ini saya menginstallnya secara manual menggunakan apt. Ketikan perintah berikut pada terminal.

```bash   
$ sudo add-apt-repository ppa:ondrej/php
$ sudo apt-get update
```

Kemudian install php, direkomendasikan versi php 7.0 keatas ya. Kali ini saya pakainya yang php 7.2.

```bash
$ sudo apt-get install apache2 libapache2-mod-php7.2 php7.2 php7.2-xml php7.2-gd php7.2-opcache php7.2-mbstring php7.2-zip
```

Cek versi phpnya dengan cara berikut.

```bash
$ php --version
```
dan pastikan versinya benar.
![PHP Version](/img/laravel/phpversion.png)


**2. Install Composer**   

Nah kalau sudah install yang dibutuhkan sekarang install composernya.

```bash
$ sudo apt-get install curl
$ curl –sS https://getcomposer.org/installer | php
$ sudo mv composer.phar /usr/local/bin/composer
```
Kemudian cek dengan mengetik perintah ```composer``` pada terminal maka akan muncul tampilan kayak gini berarti sudah siap digunakan si composernya.
![Composer](/img/laravel/composerconsole.png)


**3. Install Laravel**
Nah ini saatnya install laravel, caranya ketikan perintah berikut pada terminal console kesayangan.
```bash
$ composer global require "laravel/installer"
```   
Perintah ini akan menginstall laravel secara global pada mesin linux kita.   

Setting path laravel pada shell kesayangan anda. Kalau saya pakai shell zsh maka tinggal buka file ```.zshrc```.   
Jika kalian pakai bash buka saja file ```.bashrc```.
Kemudian pastekan lokasi laravelnya.    
Kalau di punyaku laravelnya ada di ```$HOME/.config/composer/vendor/bin```.   
```bash
export PATH="$HOME/.config/composer/vendor/bin:$PATH"
```
Cek dengan ketik perintah ```laravel``` maka akan keluar seperti ini.
![Yey](/img/laravel/laravelyey.png)

**4. Buat Projectnya**
Kalau sudah sukses install laravelnya saatnya buat projectnya. Ketikan perintah berikut.
```bash
$ laravel new blog
```
Ganti ```blog``` dengan nama project kamu ya. Proses ini biasanya makan waktu tergantung koneksi internetmu.   
Jika sudah selesai masuk ke dalam directory projectnya.
Kalau sudah sukses install laravelnya saatnya buat projectnya. Ketikan perintah berikut.
```bash
$ cd blog
```

Untuk menjalankan laravel bisa menggunakan Built-In Web Server atau setting pada apache. Untuk saat ini saya menggunakan yang pertama. nah ketikan perintah dibawah
```bash
$ php artisan serve
```
lalu buka browser dan ketikan url ```http://localhost:8000``` atau ```http://127.0.0.1:8000```   
Maka tampil kayak gini di browsernya
![xampp](/img/laravel/laravel.PNG)


 Semoga catatan belajar saya ini bermanfaat.   
<img src="/img/docker/cute.jpg" width="70%">
じゃ、また ヾ(＾-＾)ノ
