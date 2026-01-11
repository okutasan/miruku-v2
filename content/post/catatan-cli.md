+++
title = "Catatan Cli"
date = 2019-02-10T16:19:19+07:00
#draft: false
subtitle = "Yo mung kanggo awakmu"
categories = [
    "Linux",
    "Shell"
]
tags = ["linux","cli"]
image = "/img/cli-thumbnail.png"
+++

こんにちはみんな! (^o^)/   
Selamat malam, Ini adalah catatan belajar ```Command Line Interface``` yang saya lakukan. Semoga bermanfaat..<!--more-->

#### mkdir
perintah ini digunakan untuk membuat directory, cara penggunaannya **```mkdir nama_folder```**
```bash
╭─tuturu@tuturu ~  
╰─$ mkdir latihan
```
#### cd
perintah ini digunakan untuk masuk/pindah directory atau folder, cara penggunaannya ```cd lokasi_directory```
```bash
╭─tuturu@tuturu ~  
╰─$ cd latihan
```
#### touch
perintah ini digunakan untuk membuat file entah apa, cara penggunaannya ``` touch nama-file.extensi```
```bash
╭─tuturu@tuturu ~/latihan  
╰─$ touch cli-asyique.md
```
#### ls
perintah ini digunakan untuk ngelist atau mencetak daftar file/directory pada layar, cara penggunaannya ```ls```
```bash
╭─tuturu@tuturu ~/latihan  
╰─$ ls
cli-asyique.md  dildo
```
***ls -a*** : digunakan untuk cetak semua daftar file/dir termasuk yang ter-hidden.   
***ls -l*** : digunakan untuk cetak daftar file/dir beserta tanggal,permision,dan ukurannya.   
dll.
#### mv
perintah ini digunakan untuk mengganti atau memindah folder/file, cara penggunaannya ```mv [folderlama] [folderbaru]``` ```mv [dir/lama] [dir/target]```   
```bash
╭─tuturu@tuturu ~/latihan  
╰─$ mv dildo tronjaltronjol
╭─tuturu@tuturu ~/latihan  
╰─$ ls
cli-asyique.md  tronjaltronjol
```
#### echo
perintah ini berhubungan dengan string, bisa digunakan untuk input string ke dalam file, cara penggunaaannya ```echo "string" > target```
```bash
╭─tuturu@tuturu ~/latihan  
╰─$ echo "koalisi tronjal tronjol" > cli-asyique.md
```
#### cat
perintah ini untuk menampilkan isi file, penggunaan ```cat [nama-file]```
```bash
╭─tuturu@tuturu ~/latihan  
╰─$ cat cli-asyique.md
koalisi tronjal tronjol
```
#### pwd
perintah ini digunakan mengetahui lokasi dir aktif, cara penggunaan ```pwd```
```bash
╭─tuturu@tuturu ~/latihan  
╰─$ pwd
/home/tuturu/latihan
```
#### rm
perintah ini digunakan untuk menghapus dir atau folder , cara penggunaan ```rm [option] [dir/file]```
```bash
╭─tuturu@tuturu ~/latihan  
╰─$ rm cli-asyique.md
╭─tuturu@tuturu ~/latihan  
╰─$ ls
tronjaltronjol
```
***rm -rf*** : digunakan kala directory mempunyai child dan ada banyak file sehingga akan menghapus secara recursive dan force(paksa)

Semoga catatan belajar CLI saya ini bermanfaat.   
![runserver](/img/docker/cute.jpg)
じゃ、また ヾ(＾-＾)ノ
