# Praktik Algoritma dan Logika

Repository ini berisi materi praktik Algoritma dan Logika dalam Python. Materi ini mencakup konsep-konsep fundamental dalam pemrograman Object-Oriented Programming (OOP) dari pertemuan 1 hingga pertemuan 4.

---

## 📚 Daftar Isi

1. [Pertemuan 1: Pengenalan OOP](#pertemuan-1-pengenalan-oop)
2. [Pertemuan 2: Pengembangan Class dan Object](#pertemuan-2-pengembangan-class-dan-object)
3. [Pertemuan 3: Abstraction (Abstraksi)](#pertemuan-3-abstraction-abstraksi)
4. [Pertemuan 4: Inheritance dan Polymorphism](#pertemuan-4-inheritance-dan-polymorphism)

---

## Pertemuan 1: Pengenalan OOP

### Deskripsi
Pertemuan pertama memperkenalkan konsep dasar Object-Oriented Programming (OOP) dalam Python. Materi fokus pada pemahaman class, object, constructor (__init__), dan method serta bagaimana menggunakannya dalam program praktis.

### Topik Utama
1. **Class dan Object** - Memahami struktur dasar class dan cara membuat object
2. **Constructor (__init__)** - Inisialisasi atribut object
3. **Method** - Fungsi yang terikat pada class
4. **Atribut Instance** - Variabel yang melekat pada object

### Kode-kode yang Dipelajari

#### 1. Kode String - Class Mahasiswa
```python
class Mahasiswa:
    def __init__(self, nama, npm, jurusan, semester, asal):
        # Inisialisasi atribut dengan parameter yang diterima
        self.nama = nama
        self.npm = npm
        self.jurusan = jurusan
        self.semester = semester
        self.asal = asal

    def info_mahasiswa(self):
        # Method untuk menampilkan informasi mahasiswa
        print(f"Nama: {self.nama}")
        print(f"NPM: {self.npm}")
        print(f"Jurusan: {self.jurusan}")
        print(f"Semester: {self.semester}")
        print(f"Asal: {self.asal}")

mahasiswa1 = Mahasiswa("Kimi Thora", "184250012", "Sains Data", "2", "Kota Padang")
mahasiswa1.info_mahasiswa()
```

**Penjelasan:**
- Membuat class `Mahasiswa` untuk menyimpan data mahasiswa
- Method `info_mahasiswa()` menampilkan semua atribut dalam format string yang terformat
- Object `mahasiswa1` dibuat dengan data spesifik

#### 2. Operasi Matematika - Class Trapesium
```python
class trapesium:
    def __init__(self, sisi_a, sisi_b, tinggi):
        self.sisi_a = sisi_a
        self.sisi_b = sisi_b
        self.tinggi = tinggi

    def luas_trapesium(self):
        # Menghitung luas trapesium: 0.5 * (a + b) * t
        luas = 0.5 * (self.sisi_a + self.sisi_b) * self.tinggi
        print(f"Luas trapesium {luas} cm^2")

trapesium1 = trapesium(10, 15, 5)
trapesium1.luas_trapesium()
```

**Penjelasan:**
- Class untuk menghitung luas trapesium dengan formula geometri
- Menggunakan operasi matematika dalam method
- Mendemonstrasikan penggunaan atribut dalam perhitungan

#### 3. Percabangan - Class Gaji
```python
class Gaji:
    def __init__(self, gaji):
        self.gaji = gaji

    def hitung_pajak(self):
        # Percabangan: pajak hanya jika gaji > 5000000
        if self.gaji > 5000000:
            pajak = self.gaji * 0.1
            print(f"Pajak yang harus dibayar: {pajak}")
        else:
            print("Tidak dikenakan pajak")

gaji1 = Gaji(6000000)
gaji2 = Gaji(4000000)

# Loop untuk menghitung pajak beberapa object
for g in [gaji1, gaji2]:
    g.hitung_pajak()
```

**Penjelasan:**
- Menggunakan kondisional (if-else) dalam method
- Menunjukkan logika pengambilan keputusan
- Menggunakan loop untuk memproses multiple objects

---

## Pertemuan 2: Pengembangan Class dan Object

### Deskripsi
Pertemuan kedua merupakan lanjutan dari konsep OOP dengan fokus pada pengembangan class yang lebih kompleks dan praktis. Materi melibatkan class dengan operasi bisnis/komersial.

### Topik Utama
1. **Class dengan Konteks Bisnis**
2. **Multiple Objects dan Looping**
3. **Manipulasi Data Atribut**
4. **Method untuk Perhitungan Transaksi**

### Kode-kode yang Dipelajari

#### 1. Class Tambang - Domain Pertambangan
```python
class tambang:
    def __init__(self, nama_tambang, simbol, berat):
        self.nama_tambang = nama_tambang
        self.simbol = simbol
        self.berat = berat

    def tambang_mineral(self):
        print(f"{self.nama_tambang} dengan simbol {self.simbol} dan berat {self.berat}")

tambang1 = tambang("Tambang Emas", "Au", 100)
tambang2 = tambang("Tambang Perak", "Ag", 200)

tambang1.tambang_mineral()
tambang2.tambang_mineral()
```

**Penjelasan:**
- Membuat class yang merepresentasikan data mineral
- Mendemonstrasikan pembuatan multiple objects dengan data berbeda
- Method menampilkan informasi lengkap mineral

#### 2. Class Jualan - Keranjang Belanja
```python
class jualan:
    def __init__(self, nama_produk, harga, jumlah):
        self.nama_produk = nama_produk
        self.harga = harga
        self.jumlah = jumlah

    def belanjaa(self):
        # Menghitung total harga untuk pembelian
        total_harga = self.harga * self.jumlah
        print(f"produk {self.nama_produk} berjumlah {self.jumlah} dengan total harga adalah {total_harga}")

keranjang1 = jualan("saos ABC", 2500, 4)
keranjang2 = jualan("mie instan", 3500, 2)
keranjang3 = jualan("minyak goreng", 27000, 1)

# Loop untuk menampilkan semua item belanja
for keranjang in [keranjang1, keranjang2, keranjang3]:
    keranjang.belanjaa()
```

**Penjelasan:**
- Class yang merepresentasikan item dalam keranjang belanja
- Method menghitung total harga untuk setiap item (harga × jumlah)
- Menunjukkan cara mengelola multiple items dengan loop

---

## Pertemuan 3: Abstraction (Abstraksi)

### Deskripsi
Pertemuan ketiga memperkenalkan konsep Abstraction dalam OOP. Abstraksi memungkinkan kita mendefinisikan interface/blueprint yang harus diimplementasikan oleh class turunan tanpa mendetail cara implementasinya.

### Topik Utama
1. **Abstract Base Class (ABC)**
2. **Abstract Method**
3. **Interface/Blueprint**
4. **Polymorphic Behavior**

### Kode-kode yang Dipelajari

#### 1. Abstraction - Class Kendaraan
```python
from abc import ABC, abstractmethod

class Kendaraan(ABC):
    @abstractmethod
    def jalan(self):
        pass
    
    @abstractmethod
    def bahan_bakar(self):
        pass

class Mobil(Kendaraan):
    def jalan(self):
        return "Mobil berjalan dengan roda empat"
    
    def bahan_bakar(self):
        return "Mobil menggunakan bensin"

class SepedaMotor(Kendaraan):
    def jalan(self):
        return "Motor berjalan dengan dua roda"
    
    def bahan_bakar(self):
        return "Motor menggunakan bensin"

# Implementasi
kendaraan1 = Mobil()
kendaraan2 = SepedaMotor()

print(kendaraan1.jalan())
print(kendaraan2.bahan_bakar())
```

**Penjelasan:**
- `Kendaraan` adalah abstract class yang mendefinisikan interface
- `@abstractmethod` menandai method yang HARUS diimplementasikan di subclass
- Class `Mobil` dan `SepedaMotor` mengimplementasikan abstract method dengan cara mereka sendiri
- Tidak bisa membuat object langsung dari `Kendaraan`, harus melalui subclass

#### 2. Abstraction - Class AkunBank
```python
from abc import ABC, abstractmethod

class AkunBank(ABC):    
    def __init__(self, nama, saldo):
        self.nama = nama
        self.saldo = saldo
    
    @abstractmethod
    def hitung_bunga(self):
        pass
    
    @abstractmethod
    def info_akun(self):
        pass

class Tabungan(AkunBank):
    def hitung_bunga(self):
        return self.saldo * 0.02  # Bunga 2%
    
    def info_akun(self):
        return f"Akun Tabungan - {self.nama}, Saldo: {self.saldo}"

class Deposito(AkunBank):
    def hitung_bunga(self):
        return self.saldo * 0.05  # Bunga 5%
    
    def info_akun(self):
        return f"Akun Deposito - {self.nama}, Saldo: {self.saldo}"

akun1 = Tabungan("Kimi", 1000000)
akun2 = Deposito("Kimi", 1000000)

print(akun1.info_akun())
print("Bunga:", akun1.hitung_bunga())

print(akun2.info_akun())
print("Bunga:", akun2.hitung_bunga())
```

**Penjelasan:**
- `AkunBank` abstract class mendefinisikan blueprint untuk semua tipe akun
- Class `Tabungan` dan `Deposito` mengimplementasikan perhitungan bunga berbeda
- Menunjukkan bagaimana abstraksi memungkinkan fleksibilitas dalam implementasi
- Constructor dapat didefinisikan di abstract class dan diwariskan ke subclass

---

## Pertemuan 4: Inheritance dan Polymorphism

### Deskripsi
Pertemuan keempat membahas dua pilar penting OOP: Inheritance (Pewarisan) dan Polymorphism (Polimorfisme). Inheritance memungkinkan class mewarisi atribut dan method dari class lain, sedangkan Polymorphism memungkinkan object dengan tipe berbeda merespons method yang sama dengan cara berbeda.

### Topik Utama
1. **Single Inheritance** - Class mewarisi dari satu parent class
2. **Method Overriding** - Menimpa method dari parent class
3. **Multiple Inheritance** - Class mewarisi dari multiple parent classes
4. **Polymorphism** - Object berbeda merespons method yang sama dengan cara berbeda

### Kode-kode yang Dipelajari

#### 1. Single Inheritance - Dasar
```python
class parent:
    def hai(self):
        print("This is the parent class")

class child(parent):
    pass  # Child mewarisi semua method dari parent

obj = child()
obj.hai()  # Dapat mengakses method dari parent
```

**Penjelasan:**
- Class `child` mewarisi dari class `parent`
- Method `hai()` tidak perlu didefinisikan ulang di child, bisa langsung digunakan
- Konsep inheritance dasar - code reusability

#### 2. Method Overriding
```python
class parent:
    def greet(self):
        print("Good morning")

class child(parent):
    def greet(self):  # Override method dari parent
        print("Good afternoon")

c = child()
c.greet()  # Output: "Good afternoon"
```

**Penjelasan:**
- Method dengan nama sama di child menimpa (override) method parent
- Berguna ketika behavior harus berbeda untuk class yang berbeda
- Child class memiliki kontrol penuh atas implementasi method

#### 3. Multiple Inheritance
```python
class A:
    def methode_a(self):
        print("methode a")

class B:
    def methode_b(self):
        print("methode b")

class C(A, B):  # Mewarisi dari A dan B
    pass

obj = C()
obj.methode_a()  # Dari class A
obj.methode_b()  # Dari class B
```

**Penjelasan:**
- Class `C` mewarisi method dari dua parent class (A dan B)
- Dapat mengakses method dari kedua parent
- Memungkinkan kombinasi fungsionalitas dari multiple sources

#### 4. Polymorphism dengan Override
```python
class employe:
    def __init__(self, name):
        self.name = name

    def work(self):
        print(f"{self.name} sedang bekerja")

class dataanalyst(employe):
    def work(self):  # Override dengan behavior spesifik
        print(f"{self.name} lagi ngitung")

class manager(employe):
    def work(self):  # Override dengan behavior berbeda
        print(f"{self.name} lagi tidur")

A = dataanalyst("kimi")
B = manager("thora")

A.work()  # Output: "kimi lagi ngitung"
B.work()  # Output: "thora lagi tidur"
```

**Penjelasan:**
- `dataanalyst` dan `manager` mewarisi dari `employe`
- Kedua class meng-override method `work()` dengan implementasi berbeda
- Polymorphism: method yang sama, behavior berbeda tergantung tipe object

#### 5. Polymorphism - Perhitungan Gaji dengan Bonus
```python
class Employe:
    def __init__(self, salary):
        self.salary = salary

    def calc(self):
        return self.salary

class DataAnalyst(Employe):
    def calc(self):
        bonus = self.salary * 0.15  # Bonus 15%
        return self.salary + bonus

class Manager(Employe):
    def calc(self):
        bonus = self.salary * 0.25  # Bonus 25%
        return self.salary + bonus
```

**Penjelasan:**
- Base class `Employe` mendefinisikan method `calc()`
- Subclass `DataAnalyst` dan `Manager` menghitung gaji dengan bonus berbeda
- Polymorphism memungkinkan perhitungan berbeda dengan interface yang sama
- Fleksibilitas dalam menangani berbagai tipe employee dengan code yang konsisten

---

## 🎯 Konsep-Konsep Kunci OOP

### 1. **Class dan Object**
- **Class**: Template/blueprint untuk membuat object
- **Object**: Instance dari class dengan atribut dan method

### 2. **Inheritance**
- Memungkinkan class mewarisi atribut dan method dari parent class
- Tujuan: code reusability dan hierarchy

### 3. **Abstraction**
- Menyembunyikan detail implementasi
- Mendefinisikan interface yang harus diikuti
- Menggunakan ABC dan @abstractmethod

### 4. **Polymorphism**
- "Banyak bentuk" - method yang sama, behavior berbeda
- Dapat di-achieve melalui method overriding
- Memungkinkan flexibility dalam design

---

## 💡 Cara Menjalankan File

Setiap file notebook dapat dijalankan dengan Jupyter Notebook atau JupyterLab:

```bash
jupyter notebook "pertemuan 1.ipynb"
```

Atau gunakan VS Code dengan Python extension yang mendukung Jupyter Notebook.

---

## 📝 Ringkasan Pembelajaran

| Pertemuan | Topik Utama | Konsep Kunci |
|-----------|-----------|-----------|
| 1 | Pengenalan OOP | Class, Object, Constructor, Method, Atribut |
| 2 | Pengembangan Class | Multiple Objects, Looping, Data Manipulation |
| 3 | Abstraction | Abstract Class, Abstract Method, Interface |
| 4 | Inheritance & Polymorphism | Single/Multiple Inheritance, Method Overriding |

---

## 📚 Referensi

- Python Official Documentation: https://docs.python.org/3/
- OOP Concepts: https://en.wikipedia.org/wiki/Object-oriented_programming
- Python ABC Module: https://docs.python.org/3/library/abc.html
