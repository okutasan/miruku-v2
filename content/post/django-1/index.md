+++
title= "Belajar Django 1"
subtitle= "Persiapan dan Instalasi"
date= 2018-02-20T16:24:44+07:00
categories= [
  "Django",
  "Python"
]
tags= ["django","python"]
image= "/img/django.jpg"
+++
<!-- <img src="https://i0.wp.com/samueleresca.net/wp-content/uploads/2015/12/python-django-logo.jpg?ssl=1" width="75%"> -->

こんにちはみんな! (^o^)/   
Selamat malam, Ini adalah catatan belajar ```Django``` yang saya lakukan. Semoga bermanfaat..<!--more-->

Django adalah web framework Python yang didesain untuk membuat aplikasi web yang dinamis, kaya fitur dan aman. Django yang dikembangkan oleh Django Software Foundation terus mendapatkan perbaikan sehingga membuat web framework yang satu ini menjadi pilihan utama bagi banyak pengembang aplikasi web. ([Codepolitan](https://www.codepolitan.com/situs-situs-populer-yang-dibuat-dengan-djangos))

Sebelum menginstall Django ada beberapa hal yang perlu dipersiapkan yaitu :

#### 1. Python    
Django sendiri adalah framework yang menggunakan Python Language maka yang pertama dilakukan adalah menginstall ```Python```. Untuk Python dapat diunduh di[SINI](https://www.python.org/downloads/).   
Pilih Python 3 keatas karena pada Django ini menggunakan Python versi 3 keatas.

>Untuk pengguna Windows setelah instalasi Python setting $PATH Python agar dapat digunakan pada cmd.   
Untuk cara settingnya bisa lihat post saya yang [Setting Path](https://okutasan.github.io/post/path-windows/).

Cek dengan mengetikan perintah ```python``` pada cmd, jika berhasil akan tampil seperti ini
![python](/img/django/python.png)

>Untuk pengguna Linux Python sudah langsung terinstall pada system jadi tidak perlu menginstall lagi.   
Tapi jika versi python masih 2.xx maka harus diupgrade ke versi 3.xxx keatas.

#### 2. Install GIT
`Git` adalah sistem kontrol versi terdistribusi yang bersifat bebas dan open source untuk menghandle suatu projek dari sekala kecil maupun dalam sekala besar dengan cepat dan efisien.   
Untuk sofware dapat didownload di [GIT](https://git-scm.com/)   

Untuk cara instalasi dan penggunaan dapat dibaca pada post teman saya [Tutorial_GIT](https://abas.github.io/2017/12/09/How-to-Install-Git/).   
Untuk mengecek git sudah terinstall dengan cara ketik perintah `git --version`, jika sudah akan muncul versi git ![git](/img/django/git.png)

#### 3. Clone Django
Untuk instalasi Django kita clone dahulu github django dengan cara ketik perintah berikut pada git   
```git clone https://github.com/django/django.git```   

jika sudah masuk ke folder django yang sudah kita clone tadi lalu ketikan perintah berikut   
```C:\ python setup.py install```   

> **Catatan : saat eksekusi perintah diatas pastikan cmd/console sudah dalam posisi root/admin permission**

Jika sudah selesai menginstall cek versi django dengan cara ketikan perintah berikut
Windows = ```c:\>python -c "import django; print(django.get_version())"```   
Linux   = ```$ django-admin.py --version```

#### 4. Create Project
Nah untuk persiapan sudah selesai saatnya kita buat project menggunakan ```Django```.    

Pertama masuk ke folder yang kamu inginkan melalui cmd/terminal terserah sih folder apa saja asalkan jangan system yang krusial kemudian ketik perintah berikut   

```c:\> django-admin startproject blog```   

dalam hal ini kita membuat project dengan `django-admin startproject` dan dengan nama folder `blog`. Nah langsung masuk ke folder blog yang telah kita buat.

Disini kita sudah masuk ke project yang sudah kita buat memiliki struktur sebagai berikut
```
blog/
   manage.py
   blog/
      __init__.py
      settings.py
      urls.py
      wsgi.py
```
Untuk penjelasannya akan saya bahas lain kali karena untuk saat ini saya sendiri juga belum mengerti ごめん (⋟﹏⋞)

nah kemudian untuk menjalankan project yang sudah kita buat menggunakan perintah

`c:\blog> python manage.py runserver`

Maka akan seperti ini hasilnya
![runserver](/img/django/runserver.PNG)

Sekarang buka broswer dan ketikkan alamat yang sudah ada dari runserver diatas yaitu `http://127.0.0.1:8000/` maka akan terlihat roket yang akan bersiap meluncur yang menandakan projek sudah siap akan diluncurkan tinggal kita mau mengisi dan tujuan roket kemana (⁎˃ᆺ˂)

![runserver](/img/django/rocket.PNG)

Semoga catatan belajar Django saya ini bermanfaat.   

じゃ、また ヾ(＾-＾)ノ
