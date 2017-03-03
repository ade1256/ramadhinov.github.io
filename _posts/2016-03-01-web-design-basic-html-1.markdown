#HTML Basic 1
## TOC
1. [Overview](#overview)
2. [Getting Started](#getting-started)
	1. [File HTML](#file-html)
	2. [Teks Editor](#teks-editor)
3. [Hello World](#hello-world)
4. [Discussion](#discussion)
5. [HTML Structure](#html-structure)
	1. [Head Tag](#head-tag)
	2. [Body Tag](#body-tag)

## Overview
HTML merupakan kependekan dari _hypertext markup language_.

Merupakan bahasa _markup_ dan bukan bahasa pemrograman karena tidak memiliki variabel, function, struktur kontrol, pengkondisian, dsb.

__*Markup*__ bisa juga disebut _*tag*_ yang berfungsi untuk memberitahu _browser_, bagaimana sebuah teks akan ditampilkan. Sebagai contoh, kita bisa membuat teks untuk dijadikan sebagai _heading_, _title_, _paragraph_, dsb.

Penulisan *tag* diawali dengan `<` dan diakiri dengan `>`, kebanyakan _tag_ terdiri dari satu pasang, yakni _tag_ pembuka dan _tag_ penutup, namun ada juga _tag_ yang tidak memiliki pasangan.

HTML Pertamakali diciptakan oleh **Tim Berners-Lee**.

**Tim Berners-Lee** juga penggagas beberapa teknologi, diantaranya:

- HTTP
- HTML
- WWW
- Web Browser
- Web Server
- Web Page

## Getting Started
### File HTML

**HTML** bisa berjalan di komputer klien dengan bantuan *browser* seperti; chrome, firefox, safari, opera, dll. Maka pastikan komputer telah terpasang salah satu aplikasi _browser_ tersebut.

**HTML** memiliki ekstensi `*.html`, karakter `*` mewakili nama **HTML** yang diberikan oleh pembuat.

Dalam penamaan **HTML** tidak disarankan untuk menggunakan _space_ atau spasi seperti pada contoh nama-nama _file_ html berikut:

- `halaman utama.html`
- `tampilan beranda.html`
- `halaman saya .html`

Pemberian nama seperti atas memang berlaku dan bisa digunakan, namun akan bermasalah ketika dijalankan di-_browser_, karena _browser_ akan mengganti spasi tersebut dengan karakter lain. Adapun contoh penulisan nama _file_ **HTML** yang disarankan adalah:

- `HalamanDepan.html`
- `Tampilan_Awal.html`
- `tampakAtas.html`
- `bab1.html`

Memperhatikan huruf kecil/besar serta tanda lainnya sangat disarankan untuk meminimalisir kesalahan yang ditimbulkan ketika sudah dikembangkan secara jauh.

### Teks Editor

Teks editor merupakan aplikasi yang digunakan oleh _programmer_ untuk menuliskan kode-kode atau _syntax_-nya. Ada banyak teks editor yang sering digunakan, beberapa diantaranya adalah:

- [Vim](http://www.vim.org)
- [Sublime](https://sublimetext.com)
- [Atom](https://atom.io)
- [Brackets](http://brackets.io)
- [Notepad++](https://notepad-plus-plus.org)

Untuk memulai belajar **HTML**, pastikan komputer telah ter-_install_ salah satu aplikasi teks editor, sangat disarankan untuk memasang aplikasi yang berlabel _freeware_ atau gratis bila tidak ingin membeli lisensi aplikasi berbayar.

Setiap teks editor memiliki kelebihan dan kekurangannya masing-masing, oleh karena itu sangat penting memilih teks editor mana yang cocok untuk belajar.

Saya menyarankan menggunakan _Brackets_ sebagai teks editor karena memiliki dua kelebihan penting, yakni memiliki plugin yang bisa mengefektifkan pengetikan, serta memiliki kemampuan _live preview_ untuk melakukan pengecekan langsung terhadap _browser_ tanpa harus menekan _refresh_. Informasi lebih lengkap, silakan kunjungi situs resmi [mereka](https://brackets.io)

## Hello World

_Hello world_ dapat diartikan sebagai proses pertama dalam mencicipi sebuah bahasa. Singkatnya, dengan _hello world_ kita mengetahui hasil akhir dari bahasa tersebut.

Dalam membuat halaman **HTML** pertama saya menggunakan teks editor _brackets_ dan _browser_-nya _google chrome_.

1. Langkah pertama adalah dengan membuat sebuah _file_ baru berekstensi `*.html` menggunakan teks editor yang disimpan pada sebuah folder. Penamaan _file_ tersebut bisa menyesuaikan dengan kebutuhan, contoh `latihan1.html`.

2. Lalu ketikan kata yang akan kita tampilkan. Kata apapun yang kita ketikan tanpa menggunakan _tag_ akan langsung muncul apa adanya. Setelah diketik, lalu simpan kembali.

3. Buka direktori tempat dimana _file_ disimpan, file html tersebut nantinya akan mempunyai _icon_ _browser_ _default_ kita, dan ketika dibuka (_double click_) akan terbuka browser kita, berisikan isi _file_ **HTML**.
![Hello world -fullwidth]({{site.baseurl}}/asset/images/html1.png)

## Discussion

Ketika kita membuka _file_ dengan nama `latihan1.html` dengan menggunakan _browser_, kita berarti tengah membuka _file_ **HTML** pertama kita.
_File_ yang kita buat tersebut masih berbentuk `plain text`/teks biasa, artinya _browser_ menampilkan apapun yang dituliskan tanpa mengetahui tulisan tersebut seharusnya berada pada bagian apa. Ini terjadi karena kita tidak memberikan _tag_ pada _file_ **HTML** kita, sehingga browser tidak membacanya sebagai _file_ **HTML**. Maka untuk memjadikan _file_ tersebut terbaca sebagai **HTML** kita harus menambahkan struktur **HTML** pada _file_ tersebut.

## HTML Structure

Struktur umum dari **HTML5** adalah sebagai berikut:

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	
</body>
</html>
```

Seperti pada pembahasan sebelumnya, _tag_ pada **HTML** yakni sebuah _syntax_ yang diawali dengan tanda `<` dan diakhiri dengan tanda `>`. Maka bila kita mengambil satu contoh _tag_ dari struktur diatas, tag-tag tersebut seperti `<head>`, `<body>`, `</title>`, dll. Dari contoh diatas pula, kita dapat mengetahui bahwa _tag_ kebanyakan berpasangan, ada _tag_ pembuka dan _tag_ penutup. _Tag_ pembuka yakni, _tag_ yang tidak memiliki garis miring/_slash_ `/`, sedangkan tag penutup memiliki garis miring setelah `<`.

Pada struktur `<html> ... </html>` diatas pula kita dapat mengetahui bahwa _tag_ **HTML** membungkus seluruh **HTML** yang didalamnya dapat dibagi menjadi dua _tag_ utama, yakni _tag_ **head** `<head> ... </head>` dengan _tag_ **body** `<body> ... </body>`. Maka apapun yang kita tuliskan nantinya haruslah berada didalam _tag_ **head** ataupun _tag_  **body**.

Untuk mencoba penggunakan struktur **HTML** tersebut, kita dapat coba memasukkan `hello world` pertama kita kedalam struktur tersebut, menjadi seperti berikut:

```
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	Hello World
</body>
</html>
```

Bila kita benar menuliskan _syntax_ diatas, maka kita akan mendapatkan hasil yang sama seperti pada tahap pertama, yakni hanya tulisan `Hello World`. Ini karena kita belum membuat penempatan spesifik terhadap kata atau tulisan tersebut, perincian tersebut misalnya adalah menjadi `Hello World` sebagai judul, atau sebagai paragraf, atau sebagai _heading_, dll.

## Head Tag
**Head** _tag_ merupakan bagian dimana kita bisa menyimpan beberapa pengaturan **HTML** didalamnya, penjelasan lebih lanjut akan dibahas pada tulisan berikutnya.

Didalam **Head** _tag_ tersebut terdapat _tag_ dengan nama **title** yang berarti judul. **Title** _tag_ ini bisa kita isi dengan judul dari _file_ **HTML** kita. Judul tersebut nantinya akan muncul pada _title bar_. Contohnya adalah sebagai berikut:
![Title Tag -fullwidth]({{site.baseurl}}/asset/images/html2.png)

## Body Tag
Pada bagian ini biasanya kita menuliskan isi dari _website_ kita.

Bila kita langsung mengetikkan tulisan didalam **Body** _tag_, maka tulisan tersebut masih bersifat _plain text_. Bagaimana mengetahui jika tulisan kita tersebut masih dalam bentuk `plain text` atau tidak?

Caranya cukup mudah, kita tinggal coba memberikan kalimat baru, namun kita tambahkan setelah enter. Jadi, kita memiliki dua baris kalimat seperti:

```
Hello world,
today was a good day.
```
Kalimat tersebut tentu saja dimasukkan kedalam struktur html, melanjutkan dari kata sebelumnya yang telah ada. Setelah kita simpan, kita akan melihat hasilnya yang berbeda, yakni tulisan yang kita buat ternyata tidak menjadi dua baris seperti yang kita tulis, melainkan tetap menjadi satu.

![Plain text -fullwidth]({{site.baseurl}}/asset/images/html3.png)

Lalu bagaimana jika kita ingin membuat tulisan kita tersebut sesuai keinginan awal, yakni menjadi dua baris?

Maka, kita harus melakukan perincian terhadap kata tersebut, memasukkannya kedalam _tag_ yang benar sehingga tidak menjadi _plain text_ lagi.

Kita bisa menjadikannya sebuah paragraf dengan bantuan _tag_ `<p> ... </p>`, maka mengasilkan _output_ seperti berikut:

![Paragraf -fullwidth]({{site.baseurl}}/asset/images/html4.png)

Tanpa memperhatikan kata tersebut mempunyai arti apa, maka ketika kita menetapkannya sebagai paragraf, browser akan secara otomatis menjadikan kata tersebut sebagai paragraf dan memposisikan kata tersebut sebagaimana seharusnya sebuah paragraf.