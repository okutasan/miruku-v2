+++
title= "Laradock"
date= 2018-11-19T04:15:43+07:00
draft= false
subtitle= "Setup laravel tanpa lara"
categories = [
    "Laravel"
]
tags= ["laravel","linux"]
image= "/img/laravel/laradock.jpg"
+++

<!-- ![git|20%](/img/laravel/laradock.jpg)    -->
こんにちはみんな! (^o^)/   
Halo, kali ini saya akan berbagi cara setup lingkungan kerja `laravel` menggunakan `docker` atau biasa disebut **`Laradock`**. Apa keuntungannya jika kita memakai laradock ? <!--more-->

Kalau untuk saya sendiri pada sisi kepraktisannya, dimana semua kebutuhan untuk lingkungan laravel sudah disediakan oleh laradock dan juga lingkungan kerja atau servernya memakai container didalam docker.

Jadi jika ada masalah tidak mempengaruhi sistem linux karena si server untuk laravel ada didalam container docker.

Keuntungan yang lain lingkungan kerja dalam conatiner laradock sudah terdapat tools seperti : PHP CLI - Composer - Git - Linuxbrew - Node - V8JS - Gulp - SQLite - xDebug - Envoy - Deployer - Vim - Yarn - SOAP - Drush. Sehingga kita tidak perlu menginstall satu" lagi.


Untuk fitur laradock bisa dilihat pada situs [**Laradock**](https://laradock.io/introduction/).

Jika masih bingung lebih baik dicoba saja, nanti pasti kamu akan mengerti enaknya lingkungan laradock ini hhe.

#### Install GIT
Pertama kamu install git dengan cara ketikan perintah berikut pada terminal
```shell
sudo apt install git
```
Tunggu sampai selesai, jika sudah cek instalasi git dengan ketik perintah berikut pada terminal
```shell
git --version
```
Maka akan tampil seperti berikut ![git](/img/gitver.png)

#### Install Docker
Untuk instalasi `Docker` pada `Ubuntu` silahkan cek post saya [**Instalasi Docker**](https://okutasan.github.io/post/docker-1/).

Jika kamu menggunakan selain Ubuntu 16.04 tinggal diedit saja pada bagian *`xenial`* dengan versi `Ubuntu` kamu
```bash
$ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(xenial) \
   stable"

```
Misal ubuntu 18.04 maka `bionic` dan seterusnya.   
Cek instalasi docker dengan perintah `docker` maka akan seperti ini ![docker](/img/docker/dockercek.png)

#### Install Docker Compose
1. Buka terminal console dan ketikan perintah
```bash
sudo curl -L https://github.com/docker/compose/releases/download/1.23.1/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose
```
2. Ubah `docker-compose` menjadi executable 
```shell
sudo chmod +x /usr/local/bin/docker-compose
```
3. Cek instalasi `docker-compose` dengan cara
```shell
docker-compose --version
```
Jika berhasil hasilnya seperti ini ![docker-compose](/img/docker/dockercompose.png)

#### Workspace Laravel
Nah jika kita sudah menyiapkan git, docker dan juga docker compose sekarang kita menyiapkan lingkungan kerja laravel kita.

Masih semangat kan ??? 😁

1. Buat folder untuk lingkungan kerja laradock dengan cara buka terminal dan ketik
```shell
mkdir laravel-projects
```
Masuk kedalam directory tersebut

```shell
cd laravel-projects
```
2. Clone laradock dengan ketik perintah berikut pada terminal
```shell
git clone https://github.com/Laradock/laradock.git
```
Tunggu proses cloning sampai selesai.
3. Masuk ke folder **laradock** yang sudah dicloning dengan cara
```shell
cd laradock
```
4. Copy file *env-example* dan simpan dengan nama *.env*
```shell
mv env-example .env
```
5. Aktifkan container ***laradock*** nya
```shell
docker-compose up -d nginx mysql phpmyadmin redis workspace
```
Biasanya ini memakan waktu agak lama tergantung koneksi internet. Tapi ini cuma dilakukan diawal, nantinya kita kamu tidak perlu mendownload lagi jika mengaktifkan `container` selanjutnya.

6. Buka file **.env** kemudian tambahkan script berikut

```shell
DB_HOST=mysql
REDIS_HOST=redis
QUEUE_HOST=beanstalkd
```
7. Masih dalam directory `laravel-projects/laradock`, jalankan perintah berikut untuk masuk ke container yang telah dibuat.
```shell
docker-compose exec --user=laradock workspace bash
```
Jika sudah masuk ke container workspace yang sudah kita buat seperti ini ![container-laradock](/img/containerlaradock.png)
Pastikan posisi sudah berada pada `/var/www/` didalam laradock container seperti diatas ya. Selanjutnya kita buat directory ***public*** dimana di dalam directory ini lah kita akan menginstall laravel kita. Buat directory ***public*** dan masuk ke dalam directorynya dengan cara
```shell
mkdir public
cd public
```

#### Instalasi Laravel
Untuk instalasi laravel membutuhkan composer tapi pada lingkungan laradock sudah tersedia semua jadi tinggal pakai saja 😁. Pastikan posisi sudah berada di container laradock dan sudah masuk directory ***/var/www/public***. 

1. Lalu ketikan perintah berikut untuk instalasi laravel installer
   
```shell
composer global require "laravel/installer"
```
Tunggu proses sampai selesai. Biasanya butuh waktu tergantung koneksi jaringan kita.

1. Setelah selesai, sekarang kita buat aplikasi laravelnya. Ketik perintah ini
```shell
laravel new blog
```
**blog** disini silahkan ganti dengan nama project/aplikasi kamu.

3. Jika sudah silahkan buka browser arahkan ke alamat [http://localhost/blog/public](http://localhost/blog/public). Jika berhasil maka tampilan akan seperti ini ![laravel](/img/laravel/Laravel.png)

 Semoga catatan belajar saya ini bermanfaat.   
<img src="/img/docker/cute.jpg" width="70%">
じゃ、また ヾ(＾-＾)ノ
