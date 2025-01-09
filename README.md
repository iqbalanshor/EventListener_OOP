# Event Listener OOP

| NAMA  :| M IQBAL AL ANSHORI |
| --- | --- |
| NIM   :| 312310659 |
| KELAS :| TI.23.A.6 |
| DOSEN :| Agung Nugroho,S.Kom.,M.Kom |

# Latihan OOP
![latihan](https://github.com/user-attachments/assets/ff18c09d-87a7-40d8-866c-d1a2c61738d4)

# Struktur Proyek
**Proyek ini menggunakan arsitektur MVC (Model-View-Controller)**

![struktur](https://github.com/user-attachments/assets/ff82a0e0-6aef-4392-9736-1add26e9758f)

**Didalam struktur tersebut terdiri dari :**

**-Classes : Berisi atribut kolom dalam database**

**-Controller : Berisi Logika pengolahan data**

**-Model : Berisi struktur data dan operasi database**

**-View : Berisi tampilan GUI**

**-Main.java : File utama untuk menjalankan aplikasi**

# Database di MySql

**- #mysql -h127.0.0.1 -uroot**

```
CREATE DATABASE akademik;
```
```
USE akademik;
```
```
CREATE TABLE mahasiswa (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nim VARCHAR(20) NOT NULL UNIQUE,
    nama VARCHAR(100) NOT NULL,
    jurusan VARCHAR(50) NOT NULL,
    angkatan VARCHAR(100) NOT NULL
);
```
```
CREATE TABLE nilai (
    id INT PRIMARY KEY AUTO_INCREMENT,
    mahasiswa_id INT NOT NULL,
    mata_kuliah VARCHAR(100) NOT NULL,
    semester INT NOT NULL,
    nilai CHAR(2),
    FOREIGN KEY (mahasiswa_id) REFERENCES mahasiswa(id)
    ON DELETE CASCADE
);
```

# Penjelasan package dan file

### A. Package Classes:

#### BaseModel.java

### Output

- Form Mahasiswa

![outputmahasiswa](https://github.com/user-attachments/assets/f5561607-5c7b-4ceb-a782-36c447d552ab)

-Form Nilai

![outputnilai](https://github.com/user-attachments/assets/d2296951-ef7d-42ee-b900-76e6fdb7ac71)

