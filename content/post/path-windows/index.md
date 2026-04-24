+++
title= "Setting Path Windows"
date= 2018-02-19T00:09:16+07:00
categories= [
  "Windows",
  "Tips"
]
tags= ["tips","windows"]
image="/img/path/cover.png"
+++
<!-- ![cover](/img/path/cover.png) -->

こんにちはみんな! (^o^)/   
Kali ini saya akan memberikan tips tentang penggunaan **$PATH** pada Windows.<!--more-->

Untuk penjelasan tentang apa itu **$PATH** bisa dibaca sendiri di [Wikipedia](https://en.wikipedia.org/wiki/PATH_(variable)).  
Oke sekarang kita mulai untuk mengatur **$PATH** di windows.

#### 1. Buka System   
Dengan cara ```klik kanan my computer/this pc (win10) > pilih properties``` atau dengan kombinadi tombol ```"windows+break"```
#### 2. Masuk Ke Environment Variables
Untuk masuk ke Environment Variable pilih menu ```Advancanced System Settings``` lalu pilih ```Environment Variables```

![system](/img/path/system.PNG)   
![system](/img/path/env.PNG)
#### 3. Add Path
Pada Environment Variable pilih ```Path > pilih edit``` lalu klik ```New > Browse``` masukan lokasi aplikasi ataupun Path yang akan dieksekusi. Dalam hal ini saya memilih path untuk aplikasi composer yang berada pada

> ```C:\Users\okuta\AppData\Roaming\Composer\vendor\bin```

![path](/img/path/path.PNG)   
![path](/img/path/newpath.PNG)
#### 4. Jalankan Path
Untuk mencoba menjalankannya menggunaakn CommandPrompt/terminal console yang ada kemudian ketikan perintah/aplikasi yang akan dieksekusi dalam hal ini kita coba ```composer```.   

> pastikan lokasi path benar agar perintah $path dapat dijalankan.   

![composer](/img/laravel/composercmd.png)

> Setting $path pada windows ini sangat berguna ketika digunakan dalam pekerjaan , dengan menggunakan path ini kita tidak perlu membuang-buang waktu untuk mencari aplikasi yang akan dijalankan terutama bila aplikasi berupa CLI. Sehingga lebih menghemat waktu dalam develops ataupun project.

Semoga tips penggunaan $Path ini bermanfaat.   

じゃ、また ヾ(＾-＾)ノ
