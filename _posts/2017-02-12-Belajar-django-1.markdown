##Overview

**Django** merupakan Free dan Open Source _web_ Framework yang dibangun menggunakan bahasa pemrograman _Python_. Sebuah _web framework_ yang didalamnya sudah terdapat komponen untuk lebih mempercepat dan memudahkan _web development_. Arsitektur yang digunakan oleh **Django** adalah **_model_**-**_template_**-**_view(MTV)_**.

###Mengenal MVT

1. **_Model_** adalah lapisan akses data. Pada lapisan ini terdapat tentang apa saja sebuah data itu: bagaimana cara akses, bagaimana cara validasi dan lain-lain.

1. **_Template_** adalah lapisan representasi. Pada lapisan ini terdapat presentasi tentang bagaimana seharusnya _web_ tersebut ditampilan.

1. **_View_** adalah lapisan yang berurusan dengan logika. Pada lapisan ini terdapat logika yang dapat mengakses _model_ dan juga _template_. Bisa juga disebut sebagai jembatan antara _model_ dan _template_.

###Beberapa Kelebihan

2. ***Rapidly*** : **Django** telah dirancang untuk membantu _developer_ membuat aplikasi dari konsep sampai selesai secepat mungkin. _"from concept to completion as quickly as possible"_

2. ***Flexible*** : **Django** cocok untuk digunakan dalam skala _project_ kecil hingga skala _project_ besar.

2. ***Fully Loaded*** : **Django** menyediakan banyak komponen yang dibutuhkan untuk _development_ aplikasi _web_ atau pun _mobile_. **Django** itu sendiri lebih lengkap dibandingkan dengan framework _Python_ lain nya.

2. ***Cross-Plaftorm*** : Karena **Django** ini menggunakan _Python_, dan kita tahu bahwa _Python_ ini bisa berjalan pada _platform_ apapun yang sudah terpasang _Python_.

2. ***Good Documentation*** : **Django** memiliki _web_ dengan dokumentasi yang sangat lengkap dan terstruktur. Sangat cocok untuk yang sedang belajar untuk tahap awal. Juga disediakan _code examples_ sebagai bahan belajar


2. ***Secure*** : Sebenarnya _Secure_ ini relatif dan tidak mutlak karena tidak ada sistem yang aman. Namun, **Django** sudah _include_ pengamanan untuk serangan umum seperti : _SQL Injection, XSS, CSRF_ dan _clickjacking_. **Django** pun membuka _bug bounty_ program di [hackerone.com/django](http://hackerone.com/django).

2. Dukungan database yang lebih _flexible_, ___NoSQL___ _No Worry!_

2. _Make it As Soon As Posible_ (cocok untuk prototipe _project_ besar).

2. Rest API why no?

###Pengguna

Siapa yang menggunakan **Django** sebagai _web framework_ nya? beberapa _web_ terkenal ini menggunakan **Django** sebagai frameworknya:

- Disqus.
- Bitbucket. 
- Instagram.
- Mozilla Firefox.
- Pinterest.
- NASA. 
- Onion. 
- Mahalo.

Referensi: [Linkedin](https://www.linkedin.com/pulse/top-10-sites-built-Django-framework-vladimir-bogdano)


##Getting Started

###Memasang PIP

__PIP__ adalah package manager untuk **Python**, jadi kita bisa gunakan pip untuk menginstall django. Untuk pengguna **Archlinux**, kita bisa gunakan paket `python-pip` atau `python2-pip` untuk menginstall `pip`, dan untuk distro lain bisa menyesuaikan.

###Memasang Django

_Install_ **Django** itu mudah, tinggal lakukan perintah berikut dengan _superuser_ _a.k.a_ _root_.

```
# pip install Django (paket Python-pip)
```

###Membuat Project Baru

Buat _project_ baru dengan nama _djangotutorial_, sesuaikan dengan _project_ yang dibuat.
`django-admin startproject djangotutorial`

`django-admin` merupakan aplikasi dari __Django__.
`startproject` digunakan untuk memulai `project`.
`djangotutorial` nama _folder_ untuk `project` baru.

Sehingga nanti akan terbuat direktori bernama _djangotutorial_ seperti berikut:

```
djangotutorial/
|-- djangotutorial
|   |-- __init__.py
|   |-- settings.py
|   |-- urls.py
|   `-- wsgi.py
`-- manage.py
```

`Djangotutorial/` adalah direktori inti yang memuat sebuah _project_. Perlu diketahui bahwa nama tersebut tidak berpengaruh sama sekali dengan **Django**, jadi bisa ubah sesuka hati.

`manage.py` sebuah utilitas yang digunakan untuk melakukan interaksi terhadap _project_ **Django** dengan berbagai cara. Untuk lebih lengkapnya silahkan membaca [DOC](https://docs.djangoproject.com/en/1.10/ref/django-admin/).

`djangotutorial/` kedua adalah _Python package_ untuk _project_ yang kita buat. Nama tersebut yang akan digunakan ketika melakukan `import package` (cont: djangotutorial.urls)

`djangotutorial/__init__.py` adalah sebuah berkas kosong yang memberitahukan bahwa direktori tersebut merupakan _Python package_.

`djangotutorial/settings.py` merupakan pengaturan atau konfigurasi untuk _project_ **Django** itu sendiri. Lebih lengkap nya silahkan baca [disini](https://docs.djangoproject.com/en/1.10/topics/settings/).

`djangotutorial/urls.py` merupakan deklarasi **URL*** untuk _project_ **Django**; Berisi konfigurasi URL pada _project_ yang kita buat. Akan kita bahas pada kesempatan selanjutnya untuk _URL Dispatcher_ dan **URLConf**. Berikut isi berkas urls.py :

```
djangotutorial URL Configuration

The urlpatterns list routes URLs to views. For more information please see:
    https://docs.djangoproject.com/en/1.10/topics/http/urls/
Examples:
Function views
    1. Add an import:  from my_app import views
    2. Add a URL to urlpatterns:  url(r'^$', views.home, name='home')
Class-based views
    1. Add an import:  from other_app.views import Home
    2. Add a URL to urlpatterns:  url(r'^$', Home.as_view(), name='home')
Including another URLconf
    1. Import the include() function: from django.conf.urls import url, include
    2. Add a URL to urlpatterns:  url(r'^blog/', include('blog.urls'))
"""
from django.conf.urls import include,url
from django.contrib import admin

urlpatterns = [
    url(r'^admin/', admin.site.urls),
```

`djangotutorial/wsgi.py` merupakan dukungan kompatibilitas WSGI dengan _web server_ untuk menjalankan _project_ **Django**. Nantinya bisa diintegrasikan dengan menggunakan _web_ server pada umumnya seperti apache, nginx dan lain-lain.

**Django** itu sendiri sudah menyediakan _web server_ yang dibuat dengan **Python** untuk melakukan testing dalam masa _development_. Jadi memudahkan kita untuk _development_ sebelum memasukan _server production_. Perlu diingat bahwa _web server_ yang disediakan tidak dianjurkan untuk digunakan pada masa produksi. Pada kesempatan selanjutnya akan membahas tentang integrasi antara **WSGI** dan _web server_.


###Running Test

Menjalankan server django pada terminal dengan perintah `python manage.py runserver`.

Maka akan menampilkan pesan seperti berikut:
```
Performing system checks...

System check identified no issues (0 silenced).

You have 13 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.

November 30, 2016 - 01:06:48
django version 1.10.3, using settings 'djangotutorial.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C
```

Perlu diingat bahwa `runserver` secara _default_ akan menjalankan _web server_ dengan internal IP pada port 8000. Kita bisa mengubah nya dengan menggunakan:

`python manage.py runserver 8989` # untuk ubah port
`python manage.py runserver 0.0.0.0:8989` # untuk ubah ip dan port
`python manage.py runserver &` # akan menjalankan server tanpa log. Untuk menghentikan _service_ gunakan `px aux | grep pyton`, lalu matikan _service_.

Oh iya, _web server_ yang sudah berjalan ini sudah otomatis reload ketika kita melakukan perubahan terhadap _project_. Jadi tidak usah restart _web server_ ketika melakukan perubahan kecuali melakukan penambahan berkas. Lebih lengkap bisa baca [disini](https://docs.djangoproject.com/en/1.10/ref/django-admin/#django-admin-runserver).

###Membuat _First Page_

Buat file views.py pada direktori inti sebuah _project_ yang sudah dijelaskan sebelumnya. Untuk _case_ sederhana kita hanya akan menampilkan pesan `It's Django`. Caranya, pada folder `/Belajardjango/djangotutorial/djangotutorial/` buat _file_ `views.py`, lalu isikan dengan:

```
from django.http import HttpResponse

def hello(request):
  return HttpResponse("It's Django")
```

Pertama kita melakukan **import class HttpResponse** yang berada pada modul **django.http**, kita perlu melakukan **import class** tersebut karena kita akan menggunakan fungsi yang ada didalamnya.

Kedua, kita melakukan pendefinisian terhadap fungsi yang bernama `hello` dengan parameter berupa `request`. Setiap _views_ dibutuhkan setidaknya 1 parameter. Nah kita disini menggunakan _request_ sebagai parameter karena _request_ merupakan sebuah _object_ yang menyimpan informasi tentang _web request_. Pada kasus ini kita tidak akan melakukan apapun terhadap request karena kita masih belum membutuhkan.

Ketiga, kita mengembalikan nilai berupa HttpResponse yang berisi `It's Django`.

Agar views yang kita buat dapat berjalan, kita perlu melakukan konfigurasi pada **URLConf**. Bila kita menjalankan perintah `python manage.py runserver` maka yang akan tampil masihlah tampilan dari 'Welcome django'.

Seperti yang sudah dijelaskan sebelumnya bahwa *URLConf* adalah konfigurasi _URL_ untuk **Django**, mungkin padanannya adalah _route_ pada **CodeIgniter**. Untuk memanggil fungsi view `hello` yang berada pada `views.py` kita harus melakukan perubahan pada **URLConf** dalam bekas `urls.py` menjadi seperti berikut:

```
from django.conf.urls import include,url
from django.contrib import admin
from djangotutorial.views import hello

urlpatterns = [
    url(r'^admin/', admin.site.urls),
    url(r'^page/$', hello),
]
```

- Kita melakukan _import_ untuk `hello` _views_ yang ada pada _modul_ `djangotutorial/views.py`
- Kita menambahkan `url(r'^page/$', hello)` ke `urlpatterns`, fungsi ini ditujukan untuk memberitahu **Django** tentang **URL** yang sudah dikonfigurasikan. Argumen pertama merupakan _pattern-matching_ berupa **RegExp** yang dimulai dengan tanda `'^'` dan diakhiri dengan `'$'`, dan yang kedua merupakan fungsi _view_ yang kita panggil dari berkas `views.py`.
- Satu lagi yang penting adalah `'r'`, karakter tersebut memberitahukan bahwa _string_ merupakan _'raw string'_. Sila baca [disini](https://docs.python.org/2.0/ref/strings.html) . Untuk **RegExp** sila baca [disini](https://docs.python.org/3.4/library/re.html)

###Running Tes 2
Kita jalankan kembali `python manage.py runserver`, lalu akses `http://127.0.0.1:8000/page`. Maka akan tampil seperti berikut :

![Hello Django -fullwidth]({{site.baseurl}}/asset/images/django1.png)

##Footnote
**representasi** /_re·pre·sen·ta·si_/ /_répréséntasi_/ **(n)** 1 perbuatan mewakili; 2 keadaan diwakili; 3 apa yang mewakili; perwakilan.

**prototipe** /_pro·to·ti·pe_/ **(n)** model yang mula-mula (model asli) yang menjadi contoh; contoh baku; contoh khas.

**integrasi** /_in·teg·ra·si_/ **(n)** pembauran hingga menjadi kesatuan yang utuh atau bulat.

**parameter** /_pa·ra·me·ter_/ /_paraméter_/ **(n)** ukuran seluruh populasi dalam penelitian yang harus diperkirakan dari yang terdapat di dalam percontoh.

**_Bug bounty_** _"pada dasarnya merupakan suatu program yang diperuntukkan bagi para praktisi keamanan untuk mencari celah-celah yang rentan dieksploitasi dari suatu produk layanan yang berbasis TI"_ -[CISO](http://www.ciso.co.id/efektivitas-bug-bounty-program/)

