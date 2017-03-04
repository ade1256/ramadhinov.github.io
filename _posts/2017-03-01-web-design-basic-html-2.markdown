---
layout: post
title:  "Web Design : HTML Basic 2"
date:   2017-03-01 06:32:02 +0700
categories: web design html basic
---

# HTML Basic 2 : Tag
## TOC
1. [Mengenal Tag](#mengenal-tag)
2. [Struktur HTML](#struktur-html)
	1. [Tag Head](#tag-head)
	2. [Tag Body](#tag-body)
3. [Struktur Tag](#struktur-tag)

## Mengenal Tag
_Tag_ adalah kode pada **HTML** yang kita tulis dengan diawali tanda kurang dari `<` diikuti nama _tag_ dan diakhiri dengan tanda lebih dari `>`.

Sebagian _tag_ memiliki pasangan, dan ada pula yang berdiri sendiri, biasanya _tag_ yang berpasangan memiliki _tag_ pembuka dan _tag_ penutup dengan ciri adanya tanda `/`seperti `<head> ... </head>`. Sedangkan untuk tag yang tidak memiliki pasangan biasanya berdiri sendiri, seperti _tag_ `<br>`.

## Struktur HTML
Dari materi sebelumnya, kita mengenal struktur dasar dari **HTML** (versi 5) adalah sebagai berikut:

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
Dengan komponen _tag_ utama adalah;
`<!DOCTYPE html>` sebagai [Document Type Declaration](http://www.htmlbasictutor.ca/doctype-declaration.htm) yang akan memberitahu _browser_ bagaimana me-_render_ sebuah halaman,
`<html> ... </html>` yang menjadi pembungkus seluruh _tag_ yang tersedia.
`<head> ... </head>` untuk menyisipkan beberapa elemen tambahan seperti _tag_ judul, CSS, atau _script_,
`<body> ... </body>` yang biasa diisi dengan _tag_ yang berhubungan dengan konten.

### Tag Head
Pada bagian ini ada beberapa _tag_ yang bisa kita simpan, diantaranya yang sering dimasukkan adalah:

- Judul Halaman
	`<title></title>`
- CSS
	`<style></style>`. Digunakan untuk memberikan dukungan grafis bagi **HTML**.
- Javascript
	`<script></script>`. Digunakan untuk menyimpan script **Javascript**.
- Metadata
	`<meta></meta>`. Meta data ini penting untuk mendeskripsikan _website_ kita.

```
	<head>
		<meta charset="UTF-8"> <!-- Encoding -->
		<meta name="description" content="Belajar HTML"> <!-- Deskripsi Web-->
		<meta name="keywords" content="HTML,CSS,Javascript"> <!-- Kata kunci-->
		<meta name="author" content="Ramadhan"> <!-- Pembuat -->
	</head>
```

### Tag Body
Karena **Body** akan berisikan konten, tentu saja didalamnya akan sangat banyak _tag_ yang bisa disimpan, beberapa contoh yang sering digunakan adalah:

- Teks
	**`<h1>, <h2>, <h3>, <h4>, <h5>, <h6>, <p>` dll. **
- **Pendukung Teks**
	`<br>, <hr>, <em>, <strong>` dll.
- Gambar
	`<img>`
- **Hyperlink**
	`<a>`
- **List**
	`<ul>, <ol>, <li>, <dl>, <dt>, <dd>`
- **Tabel**
	`<table>, <thead>, <tbody>`, dll.
- **Form**
	`<form>, <input>, <select>, <button>`, dll.
- **Script**
	`<script>`
- **Object**
	`<object>`
- **Grouping**
	`<div>, <span>`

Lalu ada juga _tag_ komentar yang bisa sangat membantu untuk memberikan deskripsi atau keterangan mengenai baris kode yang telah kita buat, sehingga nantinya akan mudah bila terjadi pengembangan ataupun pemanfaatan lainnya. Kata yang diapit oleh _Tag_ komentar tidak akan diproses oleh browser sehingga tidak akan tampil pada _browser_ dan hanya bisa dibaca melalui teks editor. Komentar tersebut ditulis di tengah tanda `<!--` dan `-->`, sehingga akan menjadi seperti berikut `<!-- Isi komentar -->`.

## Struktur Tag
Selain **HTML** keseluruhan, _tag_ pada dasarnya memiliki struktur. Struktur _tag_ tersebut adalah seperti berikut:
`<namatag atribut="nilai">`
`namatag` adalah bagian wajib dari sebuah tag.
`atribut` merupakan sebuah opsional dalam penggunaannya, hanya digunakan jika memang _tag_ tersebut perlu memiliki sebuah atribut.
`nilai` merupakan besaran dari `atribut`.
Contoh struktur _tag_ pada penggunaanya adalah:
`<body bgcolor="darkcyan"`
`body` merupakan nama _tag_.
`bgcolor` merupakan atribut yang akan memberikan tambahan warna background pada **Body**.
`darkcyan` merupakan _value_ atau nilai warna dari atribut `bgcolor`.

Sebuah tag boleh saja memiliki lebih dari satu atribut, contohnya:
`<body bgcolor="darkcyan" id="body" class="classroom"`.

Setiap _tag_ memiliki atribut yang _default_ atau _global_. Atribut tersebut seperti:

- Accesskey = Menentukan agar elemen bisa diakses dengan shortcut keyboard
- Class & Id = Memberikan tanda untuk sebuah elemen.
- dir = Menentukan _direction_ atau arah tulisan.
- lang = Menentukan bahasa.
- style = Menyisipkan _in-line_ **CSS**
- tabindex = Urutan tabulasi ketika ditekan.
- title = judul sebuah elemen.

Informasi lebih lengkap mengenai atribut global bisa diakses melalui [w3school](http://w3school.com/Tags).


