# Tutorial Menghubungkan Project Flutter 16.cruid ke MySQL dengan API

## Pendahuluan
Repository ini adalah penghubung antara project Flutter dan MySQL (dengan XAMPP sebagai server lokal), yang biasa disebut sebagai API. Ikuti langkah-langkah berikut untuk mengatur dan menjalankan aplikasi Anda.

---

## Langkah 1: Clone Repository Project Flutter
Clone terlebih dahulu repository project Flutter yang akan digunakan:

<div align="center">
  <a href="https://github.com/TEUNGKU-ZULKIFLI/16.crud"><button style="font-size: 18px; padding: 10px 20px; background-color: #28a745; color: white; border: none; border-radius: 5px; cursor: pointer;">REPO 16.CRUID</button></a>
</div>

---

## Langkah 2: Clone Repository API
Pastikan repository API ini di-clone ke dalam folder `htdocs` di direktori XAMPP Anda. Contoh lokasi:

```
C:\xampp\htdocs\
```

---

## Langkah 3: Membuat Database dan Tabel
Jalankan kode SQL berikut untuk membuat database dan tabel-tabel yang diperlukan:
```codingan
-- Membuat database
CREATE DATABASE IF NOT EXISTS my_store;

-- Menggunakan database yang baru dibuat
USE my_store;

-- Membuat tabel tb_item
CREATE TABLE tb_item (
  id INT(11) NOT NULL,
  item_code TEXT NOT NULL,
  item_name TEXT NOT NULL,
  price INT(11) NOT NULL,
  stock INT(11) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1 COLLATE=latin1_swedish_ci;

-- Menambahkan primary key pada tabel tb_item
ALTER TABLE tb_item
  ADD PRIMARY KEY (id);

-- Menambahkan AUTO_INCREMENT untuk kolom id
ALTER TABLE tb_item
  MODIFY id INT(11) NOT NULL AUTO_INCREMENT;

-- Selesai
COMMIT;
```
---

## Langkah 4: Menguji API
Gunakan browser kesayangan anda untuk menguji endpoint API. Pastikan endpoint seperti `http://localhost/my_store/` berfungsi dengan baik.
pastikan anda melihat list foder yang sama seperti repo ini juga.
---

## Penutup
Dengan mengikuti tutorial ini, Anda telah berhasil menghubungkan project Flutter dengan MySQL menggunakan API. Semoga berhasil dan selamat mencoba!
