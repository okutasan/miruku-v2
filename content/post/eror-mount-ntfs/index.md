+++
title= "Eror Mount Ntfs Di Ubuntu"
date= 2018-03-18T01:54:33+07:00
draft= false
categories= [
  "Linux",
  "Error"
]
tags= ['tips','linux']
image="/img/ntfseror.png"
+++

<img src="/img/ntfseror.png" width="90%">   
こんにちはみんな! (^o^)/
Selamat pagi, Ini adalah catatan tips ```Eror mount NTFS di Ubuntu``` Semoga bermanfaat..<!--more-->

Jadi saya mengalami eror saat membuka file system ```ntfs``` pada ubuntu. Dimana partisi ntfs ini adalah milik windows yang saya dual boot dengan ubuntu.   

Biasanya eror ini terjadi karena kita tidak menshutdown windows sehingga pengaturan system ntfs terlock ke windows dan tidak dapat dibuka pada sistem operasi linux.

Oke jadi cara mengatasinya adalah :

### 1. Buka terminal
 Jadi buka terminal console dengan menekan ```ctrl+t```.
### 2. Cek SDA
 Cek partisi kita tadi pada sda berapa dengan melihat erornya seperti di bawah ini

<img src="/img/ntfseror.png" width="65%">

### 3. Ntfsfix
 Ketikan command dibawah ini agar dapat membuka ntfs partisi.   
```bash
$ sudo ntfsfix /dev/sda*   
```
 nah pada ```/dev/sda*``` itu diisi sda partisi yang akan kita buka.   
 Pada kasus saya adalah ```/dev/sda6```.   
 Daaaaan partisi saya sudah bisa dibuka.

Semoga catatan belajar saya ini bermanfaat.   
<img src="/img/docker/cute.jpg" width="70%">
じゃ、また ヾ(＾-＾)ノ
