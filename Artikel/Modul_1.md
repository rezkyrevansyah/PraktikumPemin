# Modul 1 Instalasi Lumen, MongoDB dan Konfigurasi APP Key

## Dasar Teori
## Lumen
<p align="justify">Lumen adalah solusi sempurna untuk membangun microservice berbasis Laravel dan API yang sangat cepat. Lumen merupakan salah satu kerangka kerja mikro tercepat yang tersedia. Pada lumen tidak perlu banyak melibatkan frontend framework JS, namun lebih difokuskan ke backend pakai php dan API. Pada penggunaan API bisa juga menggunakan laravel tapi sangat disarankan untuk tidak memakai Laravel kalau hanya untuk kebutuhan API saja karena Laravel mempunyai banyak fitur, yang nantinya fitur-fitur ini tidak terpakai karena hanya memanfaatkan API nya saja.</p>

## MongoDB
<p align="justify">MongoDB adalah database NoSQL berorientasi dokumen (document-oriented) yang menyimpan datanya dalam bentuk collection dan document Cara kerja MongoDB tidak seperti database relasional (SQL) yang bergantung pada tabel dan kolom. Hal ini memungkinkan setiap data pada MongoDB memiliki skema yang berbeda-beda.</p>

## Langkah Percobaan
1. Percobaan instalasi Composer <br>
   a. Buka halaman https://getcomposer.org/download/ <br>
   b. Download dan jalankan Composer-Setup.exe

2. Percobaan instalasi MongoDB <br>
   a. Buka halaman https://www.mongodb.com/try/download/community dan klik Download <br>
   ![](../Screenshot_1/1.png) <br>
   b. Jalankan mongodb-windows-x86_64-6.0.1-signed.msi <br>
   c. Pada welcome screen klik Next <br>
   d. Pada bagian End-User License Agreement centang “I accept the terms in the License Agreement” dan klik Next <br>
   e. Pada bagian Choose Setup Type klik Complete <br>
   f. Pada bagian Service Configuration tanpa mengubah apapun klik Next <br>
   g. Pastikan “Install MongoDB Compass” tercentang <br>
   h. Pada langkah terakhir klik Install <br>
   i. Tunggu hingga tahap instalasi selesai <br>
   j. MongoDB Compass akan terbuka secara otomatis <br>
   ![](../Screenshot_1/3.png) <br>
   k. Klik Finish untuk menutup dialog instalasi
   ![](../Screenshot_1/2.png) <br>

3. Percobaan instalasi Lumen <br>
   a. Buka folder yang diinginkan pada file explorer <br>
   b. Copy path dari folder yang diinginkan <br>
   c. Buka cmd <br>
   d. Buka path pada cmd <br>
   ![](../Screenshot_1/4.png) <br>
Untuk membuka path pada cmd kita dapat menjalankan command berikut pada cmd,
```
G: # Pindah storage jika folder yang dituju berada pada storage yang berbeda dengan pada saat CMD dibuka
```
```
cd G:\My Drive\College\5th Semester\Pemrograman Integratif # menggunakan command cd untuk mengganti directory kita sekarang
```
```
pwd # jalankan command pwd untuk mengecek apakah kita sudah berada di folder yang kita tuju /g/My Drive/College/5th Semester/Pemrograman Integratif
```
<br><br>
   e. Jalankan command untuk menginstall lumen pada folder tersebutSebelum menjalankan projek lumen kita, kita perlu membuka folder projek kita pada cmd dengan menggunakan command cd lumenapi <br>
   ![](../Screenshot_1/5.png) <br>
   ```
   composer create-project --prefer-dist laravel/lumen lumenapi
   ```
   <br><br>
   f. Buka folder projek lumen kita dan jalankan projek kita <br>
   ![](../Screenshot_1/6.png) <br>

#Konfigurasi APP_KEY
a. Buka file web.php pada folder routes, kemudian buat endpoint yang akan mengembalikan random string dengan panjang 32 <br>
![](../Screenshot_1/9.png) <br>
```
$router->get('/key', function () {
return Str::random(32);
});
```
b. Melakukan generate dari website https://pinetools.com/random-string-generator<br>
![](../Screenshot_1/10.png) <br>

Setelah mendapat random string kita akan memasukkan random string tersebut ke file .env kita pada bagian APP_KEY <br>
![](../Screenshot_1/8.png) <br>
```
APP_KEY=<<random_string>>
```
