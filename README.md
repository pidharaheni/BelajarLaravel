# BelajarLaravel
## 1. Install Laravel
Sebelum intall laravel, pastikan di komputer sudah terpasang PHP dan composer.
Disini saya akan mencoba install laravel dengan lembar kerja "blog"
```sh
$ composer create-project --prefer-dist laravel/laravel blog
```
kemudian buka editor, disini saya menggunakan visual studio code.
didalam editor ada beberapa menu, yaitu:
  - app
  - bootsrap
  - config
  - database
  - public
  - resources, dll
  
## 2. Contoh
### Membuat Tabel
klik resources --> views --> 
```sh
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
perintah diatas adalah  untuk membuat table dengan tiga kolom, dengan kolom pertama "No",
