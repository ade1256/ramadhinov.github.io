---
layout: post
title:  "Integrasi FunctionKey pada i3wm"
date:   2016-10-05 06:32:02 +0700
categories: configuration i3
---

Beberapa hari lalu saya meng-_install_ laptop yang baru saja diperbaiki dengan **GNU/Linux** serta memasang _windows manager_ **i3wm**. Salah satu yang harus ditanggung ketika menggunakan _windows manager_ yang tidak familiar adalah terbatasnya beberapa kemampuan bawaan dari komputer/laptop tersebut. Contoh kecilnya adalah fungsi dari _function key_, _functon key_ merupakan tombol paling atas pada _keyboard_ yang memiliki awalah nama huruf 'f' yang diikuti dengan angka yang menjadi urutan tombol tersebut (mis:F1, F2, F3, Fn)  _just in case_ anda belum mengetahui _function key_.

Pada laptop, tombol tersebut memiliki kemampuan lain yang bisa digunakan ketika digabungkan dengan menekan tombol 'fn' pada _keyboard_, misalkan adalah `fn+F12` yang bisa berfungsi untuk menghidupkan atau mematikan fungsi dari _wireless ethernet_ (kemampuan ini bergantung pada vendor keyboard). Ketika kita menginstall OS dengan WM atau DE tertentu, kadang kita tidak bisa menggunakan fungsi dari tombol kombinasi tersebut, termasuk ketika saya menggunakan **I3WM**. Lalu bagaimana mengaktifkan fungsi yang hilang dari _keyboard_ tersebut?

Pada kasus ini, fungsi yang hilang dari _function key_ saya adalah fungsi audio, diantaranya yaitu:

1. Previous (XF86AudioPrevious).
1. Play/Pause (XF86AudioPlay).
1. Next (XF86AudioNext).
1. Lower Volume (XF86AudioLowerVolume).
1. Raise Volume (XF86AudioRaiseVolume).
1. Mute Volume (XF86AudioMute).

Untuk memperbaiki kekurangan tersebut, hal yang perlu dilakukan adalah menambahkan _configuration script_ pada file _config_ i3wm. Lokasi file tersebut berada di `$HOME/.config/i3/config` (lokasi tentatif). Lalu, kita tambahkan _script_ dibawah ini:

<script src="https://gist.github.com/ramadhinov/072412c44c47f69eeeb0621fc923ce7e.js"></script>

Keterangan:
Untuk tombol _lower_, _raise_, dan _mute_ adalah tombol global yang memiliki fungsi sama, yakni mengurangi, menambah, serta mematikan fungsi volume laptop/komputer.

Sedangkan tombol _previous_, _play_, dan _next_ merupakan tombol yang dapat anda sesuaikan. Pada kasus ini, saya integrasikan dengan aplikasi _Spotify_.