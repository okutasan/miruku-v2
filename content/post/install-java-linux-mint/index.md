+++
title= "Install Java Linux Mint"
date= 2018-03-29T00:24:51+07:00
categories= [
  "Linux",
  "Java"
]
subtitle= "Install JDK Via PPA"
tags= ["linux","install","java"]
image="https://techaeris.com/wp-content/uploads/2016/01/Java-logo-png.png"
+++

<!-- <img src="https://techaeris.com/wp-content/uploads/2016/01/Java-logo-png.png" width="75%">    -->
こんにちはみんな! (^o^)/   
Selamat malam, Ini adalah catatan belajar ```Install Java Pada Linux Mint``` yang saya lakukan. Semoga bermanfaat..<!--more-->

Untuk instalasi java 8 atau 9 yang terbaru bisa menggunakan PPA [Webupd8 Team](https://launchpad.net/~webupd8team/+archive/ubuntu/java).

#### 1. Tambahkan PPA Webupd8 Team
 Buka terminal (ctrl+alt+t) kemudian copy paste atau ketikan pada terminal.
```bash
 sudo add-apt-repository ppa:webupd8team/java
```
Jika sudah akan muncul konfirmasi ```enter``` saja.
#### 2. Update Apt
 Update repositori agar dapat ter-list package javanya dengan menggunakan perintah.
 ```bash
 sudo apt update
 ```
#### 3. Install Java
Jika sudah selesai update install java 8/9 dengan cara ketikan perintah berikut ke terminal.
```bash
sudo apt install oracle-java8-installer
```
Tunggu sampai muncul aggrement license pilih ```ok``` kemudian ```yes```   

![JavaOK](/img/java/javaok.png)   
![Java Yes](/img/java/javayes.png)

Tunggu proses download JDK. Biasanya perlu waktu agak lama tergantung dari koneksi yang kita punya.

#### 4. Testing
 Jika sudah selesai instalasi silahkan test apakah java sudah terpasang pada Linux Mint dengan menggunakan perintah
 ```bash
 javac -version
 ```
 Maka akan tampil versi dari java yang kita install.

 ![Java](/img/java/javac.png).

Semoga catatan belajar saya ini bermanfaat.   
<img src="/img/docker/cute.jpg" width="70%">
じゃ、また ヾ(＾-＾)ノ
