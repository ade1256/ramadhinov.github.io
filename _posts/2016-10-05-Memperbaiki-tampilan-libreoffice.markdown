---
layout: post
title:  "Memperbaiki Tampilan Libreoffice"
date:   2016-10-05 06:32:02 +0700
categories: office libreoffice
---

**Libreoffice** merupakan salah satu perangkat lunak yang dikategorikan sebagai aplikasi kantor. Libreoffice sendiri merupakan pengembangan dari _Open Office_ yang telah lebih dulu dikenal. Bagi penggunakan **GNU/Linux**, libreoffice merupakan pilihan utama yang digunakan sebagai pengganti _MS Office_ keluaran _Microsoft_ yang berjalan pada sistem operasi _windows_ (dan program **wine** pada **GNU/Linux**).

Secara tampilan, **LibreOffice** mirip dengan pendahulunya yang memiliki tampilan simple dan tidak terlalu banyak menu tersedia di _toolbar_, jika pernah menggunakan _MS Office 2003_, maka tampilannya akan sangat akrab. Secara default, **LibreOffice** menggunakan _GTK-3_ sebagai pendukung tampilan _defaultnya_, bagi saya sendiri, tampilan tersebut terasa kurang menarik ketika kita menggunakan tema yang tidak support. Seperti tampilan **LibreOffice** berikut ini:

![Tampilan awal libreoffice -fullwidth]({{site.baseurl}}/asset/images/libreoffice1.png)

Untuk mengubah tampilannya menjadi lebih menarik, kita akan mengganti GTK-3 menjadi GTK-2, cukup gunakan perintah berikut

```
sudo sed -i s/Exec=/Exec=env\ SAL_USE_VCLPLUGIN=gtk\ /g /usr/share/applications/libreoffice-*
```

Lalu logout komputer/laptop, dan buka kembali aplikasi **LibreOffice**. Maka tampilan defaultnya akan menjadi seperti berikut:

![Tampilan akhir libreoffice -fullwidth]({{site.baseurl}}/asset/images/libreoffice2.png)

> Perintah diatas perlu dijalankan kembali ketika kita melakukan _update_ terhadap aplikasi.