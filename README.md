# Praktikum 7
## Pertanyaan dan Tugas
Pertanyaan dan Tugas
Buatlah program PHP sederhana dengan menggunakan form input yang menampilkan
nama, tanggal lahir dan pekerjaan. Kemudian tampilkan outputnya dengan menghitung
umur berdasarkan inputan tanggal lahir. Dan pilihan pekerjaan dengan gaji yang
berbeda-beda sesuai pilihan pekerjaan.
## Jawaban 
### Source Code
![CodeTugas](/image/CodeTugas.png)

### Output
![Output](/image/Tugas.png)

## Langkah-Langkah Praktikum
- Install XAMPP <br>
Unduh XAMPP dari https://www.apachefriends.org/download.html dan pilih versi
portable untuk memudahkan proses installasi. Kemudian extract file tersebut, seusikan
direktorinya (misal: d:\xampp).
![xampp1](/image/xampp1.png)

- Menjalankan Web Server
Untuk menjalankan web server dari menu XAMPP Control.
![xampp2](/image/xampp2.png)

- Uji coba apakah server sudah berkerja dengan baik
http://127.0.0.1 atau http://localhost
Tampil halaman utama XAMPP jika server sudah berkerja dengan baik.

- Dokumen Website
Semua file website tempatkan di direktori: \xampp\htdocs\

- Database MySQL
Direktori: \xampp\mysql\
Manajemen database: http://localhost/phpmyadmin

- Memulai PHP
Buat folder lab7_php_dasar pada root directory web server (d:\xampp\htdocs)
![xampp3](/image/xampp3.png)

- Kemudian untuk mengakses direktory tersebut pada web server dengan mengakses URL:
http://localhost/lab7_php_dasar/
![xampp4](/image/xampp4.png)

- PHP Dasar<br>
Buat file baru dengan nama php_dasar.php pada directory tersebut. Kemudian buat
kode seperti berikut.
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello World";
    ?>
</body>
</html>
```
- Output
![ss2](/image/ss2.png)

- Variable PHP<br>
Menambahkan variable pada program.
```
<?php
$nim = "0411500400";
$nama = 'Abdullah';
echo "NIM : " . $nim . "<br>";
echo "Nama : $nama";
?>
```
- Output
![ss3](/image/ss3.png)

- Predefine Variable $_GET
```
<?php
echo 'Selamat Datang ' . $_GET['nama'];
?>
```
- Output

        Selamat datang Agung

- Membuat Form Input
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>PHP Dasar</title>
</head>
<body>
    <h2>Form Input</h2>
    <form method="post">
        <label>Nama: </label>
        <input type="text" name="nama">
        <input type="submit" value="Kirim">
    </form>
    <?php
    echo 'Selamat Datang ' . $_POST['nama'];
    ?>
</body>
</html>
```
- Output
![ss4](/image/ss4.png)

-  Contoh Operator pada PHP
```
<?php
$gaji = 1000000;
$pajak = 0.1;
$thp = $gaji - ($gaji*$pajak);
echo "Gaji sebelum pajak = Rp. $gaji <br>";
echo "Gaji yang dibawa pulang = Rp. $thp";
?>
```
- Ouuput
![ss5](/image/ss5.png)

- Contoh Kondisi IF Pada PHP
```
<?php
$nama_hari = date("l");
if ($nama_hari == "Sunday") {
    echo "Minggu";
} elseif ($nama_hari == "Monday") {
    echo "Senin";
} else {
    echo "Selasa";
}
?>
```
- Output 

        Selasa

-  Contoh Kondisi Switch Pada PHP
```
<?php
$nama_hari = date("l");
switch ($nama_hari) {
    case "Sunday":
        echo "Minggu";
        break;
    case "Monday":
        echo "Senin";
        break;
    case "Tuesday":
        echo "Selasa";
        break;
    default:
        echo "Sabtu";
?>
```
- Output

        Sabtu

- Contoh Perulangan For Pada PHP
```
<?php
    echo "Perulangan 1 sampai 10 <br />";
    for ($i=1; $i<=10; $i++) {
        echo "Perulangan ke: " . $i . '<br />';
    }
    echo "Perulangan Menurun dari 10 ke 1 <br />";
    for ($i=10; $i>=1; $i--) {
        echo "Perulangan ke: " . $i . '<br />';
    }
?>
```
- Output

![ss6](/image/ss6.png)

- Contoh Perulangan While Pada PHP 
```
<?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    while ($i<=10) {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
    }
?>
```
- Output

![ss7](/image/ss7.png)

- Contoh Perulangan Do While PHP
```
<?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    do {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
    } while ($i<=10);
?>
```
- Output

![ss8](/image/ss7.png)