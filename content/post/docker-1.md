+++
title= "Belajar Docker"
subtitle= "Instalasi Docker Ubuntu Server"
date= 2018-03-15T05:15:01+07:00
categories=[
  "Docker",
  "Devops"
]
tags= ["docker"]
image="/img/docker/dockerhero.jpg"
+++

<!-- <img src="/img/docker/dockerhero.jpg" width="60%"> -->

こんにちはみんな! (^o^)/
Selamat pagi, Ini adalah catatan belajar ```Docker Portainer``` yang saya lakukan. Semoga bermanfaat..<!--more-->

<br>
### Persiapan
Pada kali ini saya mengguanakan **Ubuntu Server 16.04** sebagai OS nya. Untuk instalasi Ubuntu Server sementara belum saya tulis catatannya.   

### Instalasi Docker
 Untuk instalasi Docker ada 2 cara yaitu : 1. Dari Repositori, 2 Dari package. Untuk kali ini saya akan install docker melalui repository.   

**1. Update Repositori**   
 Silahkan update Ubuntu Server menggunanak repositori kesayangan kamu.   
 ```bash
 $ sudo apt update
 ```
**2. Instalasi paket pendukung.**    
 Install paket-paket pendukung untuk docker dengan cara ketik di terminal.  
```bash
 $ sudo apt-get install \
       apt-transport-https \
       ca-certificates \
       curl \
       software-properties-common
```
**3. Add gpg docker.**  
Perintah ini untuk menambahkan gpg key docker.
 ```bash
 $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
 ```
**4. Add fingerprint**  
Verifikasi fingerprint dengan menambahkan 8 karakter terakhir dari ```9DC8 5822 9FC7 DD38 854A E2D8 8D81 803C 0EBF CD88```. Jika benar akan muncul fingerprintnya.   
 ```bash
 $ sudo apt-key fingerprint 0EBFCD88

 pub   4096R/0EBFCD88 2017-02-22
      Key fingerprint = 9DC8 5822 9FC7 DD38 854A  E2D8 8D81 803C 0EBF CD88
 uid                  Docker Release (CE deb) <docker@docker.com>
 sub   4096R/F273FCD8 2017-02-22
 ```
**5. Atur stable Repositori**   
 Atur repositori docker yang stable.
 ```shell
 $ sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(xenial) \
   stable"
 ```
**6. Install Docker**   
 Update dahulu repository pada terminal.
 ```bash
 $ sudo apt update
 ```
 Kemudian install docker
 ```bash
 $ sudo apt-get install docker-ce
 ```
**7. Cek Docker**   
 Untuk cek docker sudah terinstall atau belum tuliskan perintah berikut
 ```bash
 $ docker version
 ```
 Jika sudah terinstall maka versi docker akan muncul. Setelah itu cek docker untuk menjalankan hello-world images dengan cara
```bash
$ sudo docker run hello-world
```
 Perintah tersebut adalah untuk mengunduh images hello-world dan menjalankannya pada docker. Jika berhasil maka akan muncul ```hello-world```.   

Semoga catatan belajar Docker saya ini bermanfaat.   
<img src="/img/docker/cute.jpg" width="70%">
じゃ、また ヾ(＾-＾)ノ
