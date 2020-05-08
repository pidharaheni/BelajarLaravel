# BelajarLaravel
## 1. Install Laravel
Sebelum install laravel, pastikan di komputer sudah terpasang PHP dan composer.
Disini saya akan mencoba install laravel dengan lembar kerja "blog"
```sh
$ composer create-project --prefer-dist laravel/laravel blog
```
kemudian buka editor, disini saya menggunakan visual studio code.
didalam editor ada beberapa menu, yaitu:

```sh
.
├── app
├── artisan
├── bootstrap
├── composer.json
├── composer.lock
├── config
├── database
├── package.json
├── phpunit.xml
├── public
├── readme.md
├── resources
├── routes
├── server.php
├── storage
├── tests
├── vendor
└── webpack.mix.js

10 directories, 8 files
```
  
## 2. Contoh
### Membuat Tabel
klik resources --> views --> buat file, misal nama file nya **tabel.blade.php** --> kemudian ketikan seperti di bawah ini
```html
<body>
   <table>
    <tr>
        <th>No</th>
        <th>Nama Karakter</th>
        <th>Foto</th>
    </tr>
    <tr>
        <td>1</td>
        <td class="teks-kiri">Najwa</td>
        <td><img src="https://cdn2.tstatic.net/makassar/foto/bank/images/najwa-shihab-tema-mata-najwa-malam-ini-link-live-streaming-trans-7.jpg"></td>
    </tr>
    </table>
</body>
</html>
```
Perintah diatas adalah  untuk membuat table dengan tiga kolom, dengan kolom pertama "No",kolom ke-2 "Nama", dan yang ke-3 "Foto"
Untuk melihat hasil dari html diatas 
- aktifkan serve nya terlebih dulu
  ```sh
  php artisan serve
  ```
- buat route baru di file **routes/web.php** untuk memanggil file **resources/views/tabel.blade.php** 
  ```php
  Route::get ('/tabel',function(){
    return view ('tabel');
    });
  ```
- kemudian buka browser, ketikan url 
  http://localhost:8000/tabel

Dari di atas bisa dilihat bahwa tabel yang dibuat masih berantakan,untuk merapikan tabel di atas maka bisa ditambahkan **css** di file **tabel.blade.php**
```css
   table {
        width: 100%;
        /* ini digunakan untuk menampilkan tabel dengan lebar sesuai halaman browser */
    } 
    table,th, td {
        border: 1px solid brown;
    /* perintah ini digunakan untuk memberikan border 1 pixel pada garis kolom dan baris, dengan jenis garis solid dan warna coklat */
        border-collapse: collapse;
    /*perintah ini digunakan untuk menyaatukan border  */
    }
    th, td {
        padding: 5px;
    /*perintah ini untuk memberikan ruang antara content dengan border  */
    }
    th, td {
        text-align: center;
    /* perintah ini digunakan untuk mengatur text di tengah */
    }
    .teks-kiri {
        text-align: left;
    /*perintah ini digunakan untuk mengatur teks di  sebelah kiri  */
    /* bedanya dengan perintah di atas adalah, perintah ini hanya untuk mengatur teks di kolom kedua  */
    }
```
