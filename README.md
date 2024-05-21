## tugas.pert.11
## profil

| Variable       |    DATA DIRI         |
| ---------------| ----------------     |
| Nama           | Lutpiah Ainus Shiddik|                                     
| NIM            | 312310474            |
| Kelas          | TI.23.A.5            |
| Mata Kuliah    |Basis data            |

## Soal Latihan Praktikum (pegawai)

![gambar tabel pegawai](https://github.com/lutpi9/tugas.pert.11/assets/147919251/fd70f724-951a-44a9-b83f-1d039b27cf9e)


## perintah SQL :

```

CREATE TABLE pegawai (
    idpegawai VARCHAR(5) PRIMARY KEY,
    nama_depan VARCHAR(10) NOT NULL,
    nama_belakang VARCHAR(15) NOT NULL,
    email VARCHAR(25) UNIQUE KEY,
    telepon VARCHAR(15),
    tgl_kontrak DATA,
    id_job VARCHAR(5),
    gaji INT,
    tunjangan INT
    );

INSERT INTO pegawai VALUES
    ('E001', 'Ferry', 'Gustiawan', 'ferry@yahoo.com', '07117059004', '2005-09-01', 'L0001', 2000000, 500000),
	('E002', 'Aris', 'Ganiardi', 'aris@yahoo.com', '081312345678', '2006-09-01', 'L0002', 2000000, 200000),
	('E003', 'Faiz', 'Ahnad', 'faiz@gmail.com', '081367384322', '2006-10-01', 'L0003', 1500000, NULL),
	('E004', 'Emna', 'Bunton', 'emna@gmail.com', '081363484342', '2006-10-01', 'L0004', 1500000, 9),
	('E005', 'Mike', 'Scoff', 'mike@plasa.com', '08163454555', '2007-09-01', 'L0005', 1250000, 9),
	('E006', 'Lincoln', 'Burrows', 'linc@yahoo.com', '08527388432', '2008-09-01', 'L0006', 1750000, NULL);

```
## *outputnya*:
![output tabel pegawai](https://github.com/lutpi9/tugas.pert.11/assets/147919251/e9beb0a0-5754-43c5-bd86-884ea3572252)

## TUGAS PRAKTIKUM
 
 ## *1. Tampilkan pegawai yang gajinya bukan 2.000.000 dan 1.250.000 !*
 ```
 SELECT*FROM pegawai WHERE gaji NOT IN (2000000, 1250000);
 ```


 ## OUTPUTNYA :
![output 1 pegawai](https://github.com/lutpi9/tugas.pert.11/assets/147919251/c285f26c-aebb-46b4-a0be-807bf938df2c)


 ## *2. Tampilkan pegawai yang tunjangannya NULL!*
 ```
 SELECT*FROM pegawai WHERE tunjangan IS NULL;
 ```

 ## OUTPUTNYA :
![output 2 pegawai](https://github.com/lutpi9/tugas.pert.11/assets/147919251/6b169a64-8522-4d4c-89c2-c2eb86ccaf7e)

 ## *3. Tampilkan pegawai yang tunjangannya tidak NULL!*
 ```
 SELECT*FROM pegawai WHERE tunjangan IS NOT NULL;
 ```

 ## OUTPUTNYA :
 ![output 3 pegawai](https://github.com/lutpi9/tugas.pert.11/assets/147919251/6f791181-dc3f-4dd3-98bd-280692f13a33)


 ## *4. Tampilkan/hitung jumlah baris/record tabel pegawai!*
 ```
 SELECT COUNT(*) AS jmlh_pegawai FROM pegawai;
 ```

 ## OUTPUTNYA :
 ![output 4 pegawai](https://github.com/lutpi9/tugas.pert.11/assets/147919251/1db7daeb-0691-465a-beff-7e84dcdca876)


 ## *5. Tampilkan/hitung jumlah total gaji di tabel pegawai!*
 ```
 SELECT SUM(gaji) AS ttl_gaji FROM pegawai;
 ```

 ## OUTPUTNYA :
![output 5 pegawai](https://github.com/lutpi9/tugas.pert.11/assets/147919251/699d3d6a-66f0-4b8f-8e5d-f2d10eb607e8)

 ## *6. Tampilkan/hitung rata-rata gaji pegawai!*
 ```
 SELECT AVG(gaji) AS mean_gaji FROM pegawai;
 ```

 ## OUTPUTNYA :
![output 6 pegawai](https://github.com/lutpi9/tugas.pert.11/assets/147919251/635dbc77-e416-463a-b679-07b7fd5cb271)

 ## *7. Tampilkan gaji terkecil!*
 ```
 SELECT MIN(gaji) AS terkecil FROM pegawai;
 ```

 ## OUTPUTNYA :
![output 7 pegawai](https://github.com/lutpi9/tugas.pert.11/assets/147919251/2759599f-b8c3-4a71-ac5a-a13e123491e8)


 ## *8. Tampilkan gaji terbesar!*
 ```
 SELECT MAX(gaji) AS terbesar FROM pegawai;
 ```

 ## OUTPUTNYA :
 ![output 8 pegawai](https://github.com/lutpi9/tugas.pert.11/assets/147919251/af9189ea-70da-4fe6-9399-1c6d3f05c3c0)


## Soal Latihan Praktikum (hewan)
![tabel hewan](https://github.com/lutpi9/tugas.pert.11/assets/147919251/60fe6428-6f4f-4e76-968d-c692759880a8)


## perintah SQL :
```
CREATE TABLE hewan (
    id VARCHAR (5) PRIMARY KEY,
    name VARCHAR (10) NOT NULL,
    owner VARCHAR (10),
    species VARCHAR (10),
    sex enum('M', 'F')
    );

INSERT INTO hewan VALUES
    ('p1', 'Puffball', 'Diane', 'Hamster', 'F'),
    ('p2', 'Claws', 'Gwen', 'Cat', 'M'),
    ('p3', 'Fluffy', 'Haro 1d', 'Cat', 'F'),
    ('p4', 'Buffy', 'Haro 1d', 'Dog', 'F'),
    ('p5', 'Fang', 'Benny', 'Dog', 'M'),
    ('p6', 'Bowser', 'Diane', 'Dog', 'M'),
    ('p7', 'Chirpy', 'Gwen', 'Bird', 'F'),
    ('p8', 'Whistler', 'Gwen', 'Bird', NULL),
    ('p9', 'Slim', 'Benny', 'Snake', 'M');
```

## *OUTPUTNYA :*
![output tabel hewan](https://github.com/lutpi9/tugas.pert.11/assets/147919251/a401d381-a759-402d-9e8a-d0608e676888)


## TUGAS PRAKTIKUM

## *1. Tampilkan jumlah hewan yang dimiliki setiap owner.*
```
SELECT owner, COUNT(*) AS jmlh_hewan FROM hewan GROUP BY owner;
```

## OUTPUTNYA :
![output 1 hewan](https://github.com/lutpi9/tugas.pert.11/assets/147919251/45a2233c-b9b2-4de2-a357-1d47d31d5a62)


## *2. Tampilkan jumlah hewan berdasarkan spesies*
```
SELECT species, COUNT(*) AS jmlh_hewan FROM hewan GROUP BY species;
```

## OUTPUTNYA :
![output 2 hewan](https://github.com/lutpi9/tugas.pert.11/assets/147919251/2dc46549-1dca-4832-ab6a-052c519f78a2)

## *3. Tampilkan jumlah hewan berdasarkan jenis kelamin*
```
SELECT sex, COUNT(*) AS jmlh_hewan FROM hewan GROUP BY sex;
```

## OUTPUTNYA :
![output 3 hewan](https://github.com/lutpi9/tugas.pert.11/assets/147919251/576f6296-fd9c-4564-b6ae-eae4438503cd)


## *4. Tampilkan jumlah hewan berdasarkan spesies dan jenis kelamin*
```
SELECT species, sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species, sex;
```

## OUTPUTNYA :
![output 4 hewan](https://github.com/lutpi9/tugas.pert.11/assets/147919251/be5502d6-2cf4-47e3-b3d9-20b9d143022b)


## *5. Tampilkan jumlah hewan berdasarkan spesis (cat dan dog saja) dan jenis kelamin*
```
SELECT species, sex, COUNT(*) AS jumlah_hewan FROM hewan WHERE
species IN ('Cat', 'Dog')
GROUP BY species, sex;
```

## OUTPUTNYA :
![output 5 hewan](https://github.com/lutpi9/tugas.pert.11/assets/147919251/aa0e7810-a5fc-4f86-af3d-7efd73e0a234)


## *6. Tampilkan jumlah hewan berdasarkan jenis kelamin yang diketahui saja*
```
SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan WHERE sex IS NOT NULL GROUP BY sex;
```

## OUTPUTNYA :
![output 6 hewan](https://github.com/lutpi9/tugas.pert.11/assets/147919251/715c27f3-7d2f-475d-ab1f-86873275e9d9)


## Evaluasi dan Pertanyaan
## *• Tulis semua perintah-perintah SQL percobaan di atas beserta outputnya!*
```
CREATE DATABASE praktikum4;
USE praktikum4;
CREATE TABLE pegawai (
    idpegawai VARCHAR (5) PRIMARY KEY,
    nama_depan VARCHAR (10) NOT NULL,
    nama_belakang VARCHAR (15) NOT NULL,
    email VARCHAR (25) UNIQUE KEY,
    telepon VARCHAR (15),
    tgl_kontrak DATE,
    id_job VARCHAR (5),
    gaji INT,
    tunjangan INT
    );

INSERT INTO pegawai VALUES
    ('E001', 'Ferry', 'Gustiawan', 'ferry@yahoo.com', '07117059004', '2005-09-01', 'L0001', 2000000, 500000),
	('E002', 'Aris', 'Ganiardi', 'aris@yahoo.com', '081312345678', '2006-09-01', 'L0002', 2000000, 200000),
	('E003', 'Faiz', 'Ahnad', 'faiz@gmail.com', '081367384322', '2006-10-01', 'L0003', 1500000, NULL),
	('E004', 'Emna', 'Bunton', 'emna@gmail.com', '081363484342', '2006-10-01', 'L0004', 1500000, 9),
	('E005', 'Mike', 'Scoff', 'mike@plasa.com', '08163454555', '2007-09-01', 'L0005', 1250000, 9),
	('E006', 'Lincoln', 'Burrows', 'linc@yahoo.com', '08527388432', '2008-09-01', 'L0006', 1750000, NULL);

SELECT * FROM pegawai;

SELECT * FROM pegawai WHERE gaji NOT IN (2000000, 1250000);

SELECT * FROM pegawai WHERE tunjangan IS NULL;

SELECT * FROM pegawai WHERE tunjangan IS NOT NULL;

SELECT COUNT(*) AS jumlah_pegawai FROM pegawai;

SELECT SUM(gaji) AS total_gaji FROM pegawai;

SELECT AVG(gaji) AS rata_rata_gaji FROM pegawai;

SELECT MIN(gaji) AS gaji_terkecil FROM pegawai;

SELECT MAX(gaji) AS gaji_terbesar FROM pegawai;

CREATE TABLE hewan (
    id VARCHAR (5) PRIMARY KEY,
    name VARCHAR (10) NOT NULL,
    owner VARCHAR (10),
    species VARCHAR (10),
    sex enum('M', 'F')
    );

INSERT INTO hewan (id, name, owner, species, sex)
VALUES ('p1', 'Puffball', 'Diane', 'Hamster', 'F'),
       ('p2', 'Claws', 'Gwen', 'Cat', 'M'),
       ('p3', 'Fluffy', 'Haro 1d', 'Cat', 'F'),
       ('p4', 'Buffy', 'Haro 1d', 'Dog', 'F'),
       ('p5', 'Fang', 'Benny', 'Dog', 'M'),
       ('p6', 'Bowser', 'Diane', 'Dog', 'M'),
       ('p7', 'Chirpy', 'Gwen', 'Bird', 'F'),
       ('p8', 'Whistler', 'Gwen', 'Bird', NULL),
       ('p9', 'Slim', 'Benny', 'Snake', 'M');

SELECT * from hewan;

SELECT owner, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY owner;

SELECT species, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species;

SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY sex;

SELECT species, sex, COUNT(*) AS jumlah_hewan FROM hewan GROUP BY species, sex;

SELECT species, sex, COUNT(*) AS jumlah_hewan FROM hewan WHERE species IN ('Cat', 'Dog') GROUP BY species, sex;

SELECT sex, COUNT(*) AS jumlah_hewan FROM hewan WHERE sex IS NOT NULL GROUP BY sex;
```
## *• Beri kesimpulan Anda!*
Terdapat beberapa Query Filter yang ditemukan pada tugas praktikum 4 :

`IN`: Operator yang digunakan untuk membandingkan nilai kolom dengan daftar nilai.

Operator `NOT IN` adalah kebalikan dari operator IN, yang digunakan untuk memfilter data dan memilih baris data yang tidak cocok dengan nilai-nilai dalam daftar yang ditentukan.

Operator `IS NULL` adalah salah satu operator penting dalam bahasa query, terutama dalam SQL, yang digunakan untuk memeriksa nilai null pada kolom dalam tabel.

Operator `IS NOT NULL` adalah kebalikan dari operator `IS NULL`, yang digunakan untuk memfilter data dan memilih baris data yang memiliki nilai tidak null pada kolom tertentu.

Perintah `COUNT` adalah salah satu fungsi agregat fundamental dalam bahasa query, terutama dalam SQL, yang digunakan untuk menghitung jumlah baris data dalam suatu tabel atau hasil query.

Perintah `SUM` adalah salah satu fungsi agregat fundamental dalam bahasa query, terutama dalam SQL, yang digunakan untuk menjumlahkan nilai numerik dalam satu atau beberapa kolom pada tabel.


Perintah `AVG` adalah salah satu fungsi agregat fundamental dalam bahasa query, terutama dalam SQL, yang digunakan untuk menghitung nilai rata-rata (mean) dari kolom numerik dalam tabel.

`MIN` adalah perintah yang digunakan untuk mencari nilai minimum (terkecil) dari kolom numerik dalam tabel. 

`MAX` adalah perintah yang digunakan untuk menampilkan nilai terbesar dari suatu kolom pada tabel.

Klausa `GROUP BY` berfungsi untuk meringkas dan menganalisis data berdasarkan kategori atau kelompok yang berbeda.

## *FINISH*



