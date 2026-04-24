+++
title= "Fix Error: Insufficient Permissions for Device With ADB"
date= 2018-03-29T01:36:25+07:00
subtitle= "Fix Eror Run APK pada Device"
categories= [
  "Android",
  "Linux"
]
tags= ["android","tips","linux","java"]
image= "/img/java/androidstudio.png"
+++
<!-- <img src="/img/java/androidstudio.png" width="50%"> -->

こんにちはみんな! (^o^)/
Halo semua, jadi ceritanya saya sedang belajar membuat aplikasi android. Aplikasi yang saya gunakan adalah Android Studio yang run pada Linux Mint. <!--more-->  

Sewaktu mau test aplikasi dengan run menggunakan device android terjadi error ```Insufficient Permissions for Device With ADB``` nah setelah googling saya menemukan solusinya agar aplikasi kita dapat ditest menggunakan device android pada OS Linux Mint. Berikut beberapa caranya yang saya dapatkan.

##### 1. Cek USB Debugging
 Cek perangkat android sudahkan pada mode developer. Jika belum silahkan aktifkan mode developer.

#### 2. Install adb
 Jika masih tidak bisa coba cek apakah adb-tools sudah terinstall. Jika belum install dengan mengetikan perintah berikut pada terminal.
 ```bash
 sudo apt install android-tools-adb
 ```
 Jika sudah maka lakukan hal berikut ini pada terminal linux
 ```bash
 adb kill-server
 ```
 Dan aktifkan ulang adb menggunakan root user
 ```bash
 sudo adb start-server
 ```
 Maka akan seperti ini

 ![Adb Start](/img/java/adbstart.png)

Nah akhirnya aplikasi bisa saya test menggunakan device android yang saya punya. :D

Semoga catatan belajar saya ini bermanfaat.   
<img src="/img/docker/cute.jpg" width="70%">
じゃ、また ヾ(＾-＾)ノ
