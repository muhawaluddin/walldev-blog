---
draft: false
date: 2021-12-21T00:30:20+08:00
title: "Cara Install Hugo di Linux"
slug: first-artikel

tags:
    - Hugo

categories:
    - Pemrograman


image: https://res.cloudinary.com/walldev/image/upload/c_scale,h_339,w_509/hugo-logo_beyk0d.png
thumbnail: https://res.cloudinary.com/walldev/image/upload/v1640149500/hugo-logo_beyk0d.png
---

![](/img/hugo-logo.png)

# Tutorial Install [Hugo](https://gohugo.io/) (Linux)

## Step 1. Install [Hugo](https://gohugo.io/)

Install Hugo menggunakan [brew](https://brew.sh/index_id).

```php
brew install hugo
# or
port install hugo 
```

Verifikasi Hugo version.

```php
hugo version
```

## Step 2. Create a New Site

Membuat new site dengan menggunakan perintah berikut :

```php
hugo new site dir-name-site
```

## Step 3. Add a Theme

Menambahkan tema default [Ananke.](https://github.com/theNewDynamic/gohugo-theme-ananke.git)

```php
cd dir-name-site
git init
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke
```

Kemudian, tambahkan tema pada `config.toml`

```php
theme = \"ananke\"
```

## Step 4. Add some Content

Anda bisa menambahkan konten secara manual dengan cara menambahkan file dengan ekstensi `.md` atau **markdown** ( contoh : `content/<Folder>/<File.md>` ) atau menggunakan cara berikut dengan perintah `new`

```php
hugo new blog/blog-pertama.md
```

buka file `blog-pertama.md` , akan tampil format berikut. Silahkan menambahkan tulisan pertama Anda.

```php
title: "My First Blog"
date: 2019-03-26T08:47:11+01:00
draft: true
```

* * *

`draft : true` halaman masih sebagai draft
`draft : false` halaman siap untuk dipublish

## Step 5. Start a Hugo Server

Sekarang, jalankan Hugo Server untuk melihat tampilan website Anda.
```php
hugo server
```
---
```php
▶ hugo server

                   | EN
+------------------+----+
  Pages            | 10
  Paginator pages  |  0
  Non-page files   |  0
  Static files     |  3
  Processed images |  0
  Aliases          |  1
  Sitemaps         |  1
  Cleaned          |  0

Total in 11 ms
Watching for changes in /Users/bep/quickstart/{content,data,layouts,static,themes}
Watching for config changes in /Users/bep/quickstart/config.toml
Environment: "development"
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```
Jalankan pada browser Anda `http://localhost:1313/`

Untuk melakukan configurasi pada website Hugo anda, silahkan untuk mengeksplor file `config.toml`

---
```php
baseURL = "https://example.org/"
languageCode = "en-us"
title = "My New Hugo Site"
theme = "ananke"
```