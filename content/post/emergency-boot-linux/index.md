+++
title= "Emergency Boot Linux"
date= 2018-04-17T17:43:30+07:00
draft= false
subtitle= "Yes, you can !"
categories = [
    "Linux",
    "Error"
]
tags= ["linux"]
image = "https://orig00.deviantart.net/92c1/f/2015/071/4/2/linuxmint_flat_wallpaper_by_x86basedhuman-d8lemzo.png"
+++

<!-- <img src="https://orig00.deviantart.net/92c1/f/2015/071/4/2/linuxmint_flat_wallpaper_by_x86basedhuman-d8lemzo.png" width="70%"> -->


こんにちはみんな! (^o^)/    
Halo semua, pernah mengalami emergency boot di linux ? . <!--more-->  


Pada kemarin sore saya mengalami hal ini. Entah apa yang saya lakukan sebelum shutdown linux mint tiba-tiba pas mau dinyalakan lagi malah muncul emergency boot. Emergency boot ini terjadi saat playmouth berjalan untuk tampilannya kurang lebih seperti ini.

<img src="https://i.stack.imgur.com/7Dhyo.jpg" width="70%">

Nah setelah googling saya menemukan solusinya dan dapat masuk ke linux mint kembali. Berikut saya share cara menangani Emergency boot pada linux.

#### 1. Masuk ke LiveUSB Linux   
 Silahkan buat Live Linux xubuntu atau yang lainnya. Bisa menggunakan media USB Flashdisk ataupun DVD. Setelah liveboot masuk ke terminal console dengan cara ```ctrl+t```.   
#### 2. Cek Lokasi Home Directory
 Masuk root user dengan cara
 ```bash
 sudo -i
 ```
 Kemudian cek Home directory teman-teman. Jika home tidak dipisah berarti cari directroy ```/``` jika dipisah maka cari directory home nya dengan cara ketik
 ```bash
 fdisk -l
 ```
 jika ketemu maka langkah selanjutnya
#### 3. Fix fsck
 Kita asumsikan disini partisi Home saya ada di /dev/sda1. nah untuk partisi teman-teman menyesuaikan ya tergantung hasil dari ```fdisk -l```. Kemudian ketikan perintah berikut.
 ```bash
 umount \dev\sda1\
 fsck -y
 ```
 nah jika sudah ```fsck``` tunggu prosesnya sampai selesai.
 Kemudian reboot.
 Dicoba boot pada linux teman-teman. Insyaallah berhasil hehe ^^.

 Semoga catatan belajar saya ini bermanfaat.   
<img src="/img/docker/cute.jpg" width="70%">
じゃ、また ヾ(＾-＾)ノ
