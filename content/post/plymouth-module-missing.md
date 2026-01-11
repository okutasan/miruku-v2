+++
title= "Plymouth Module Missing"
date= 2018-10-07T20:13:06+07:00

subtitle= "Sudahlah Aku Pasrah"
categories = [
    "Linux",
    "Desktop"
]
tags= ["linux","tips"]
image = "/img/miku.gif"
+++

<!-- <img src="https://cn.pling.com/img/f/7/b/4/3d11483df3d7c1a3664974198fb6d964c499.gif" width="30%"> -->


こんにちはみんな! (^o^)/
Halo semua, jadi saat saya ingin merubah plymouth terjadi eror seperti ini<!--more-->

 ```bash
 update-initramfs: Generating /boot/initrd.img-4.4.0-87-generic
 W: plymouth module (/usr/lib/x86_64-linux-gnu/plymouth//two-step.so) missing, skipping that theme
 ```
Sebelumnya yang belum tau pylmouth itu apa , jadi plymouth adalah animasi saat kita boot linux.
Nah salah satu yang saya coba pakai adalah plymouth Ene Kagerou Project  di [sini](https://www.gnome-look.org/p/1187464/).

### Cara Mengatasinya

Oke cara mengatasinya adalah buka terminal dan ketikan perintah berikut.
```
$ sudo apt-get install plymouth-themes
```

Nah silahkan di update initramfsnya maka tidak akan eror lagi ^^.

Semoga catatan belajar saya ini bermanfaat.
![runserver](/img/docker/cute.jpg)
じゃ、また ヾ(＾-＾)ノ
