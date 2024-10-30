# Dwi Okta Ramadhani
# _TI.24.A.1_

# Program 1 Harga Tiket
Program ini adalah program harga tiket yang menghitung total biaya tiket
berdasarkan dua faktor utama: tipe tiket (Reguler atau VIP) dan status keanggotaan (apakah pengguna memiliki kartu member atau tidak)

# Deskripsi Program
Program ini dibuat menggunakan bahasa python dengan fitur:
1. Input dan Output: input(): Untuk menerima masukan dari pengguna. print(): Untuk menampilkan output ke konsol.
2. Tipe Data: String: Menyimpan tipe tiket dan status member sebagai teks. Integer: Menggunakan harga tiket sebagai angka.
3. Pengkondisian: if, elif, dan else: Untuk menentukan harga tiket berdasarkan input pengguna dan memberikan diskon jika pengguna adalah anggota.
4. Operasi Aritmetika: Menghitung total harga dengan mengalikan harga tiket dan mengurangi 20% jika pengguna memiliki kartu member.
5. Fungsi lower(): Untuk mengubah input menjadi huruf kecil, sehingga memudahkan validasi.
6. Penggunaan List: Menggunakan in untuk memeriksa validitas tipe tiket dalam list yang berisi "reguler" dan "vip".

# Flowchart Program
![Flowchart](https://github.com/Dwiokta10/lab2py./blob/main/flowchart1diskon20%25..png?raw=true)

# Kode Program Tiket
``` python
# Harga tiket
harga_reguler = 50000
harga_vip = 100000

# Input tipe tiket
tipe_tiket = input("Masukkan tipe tiket (reguler/vip): ").lower()

# Input status member
status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ").lower()

# Menentukan harga tiket berdasarkan tipe tiket dan member
if tipe_tiket == "reguler":
    harga_tiket = harga_reguler
elif tipe_tiket == "vip":
    harga_tiket = harga_vip
else:
    print("Tipe tiket tidak valid.")
    exit()

# Menghitung harga dengan diskon jika pengguna adalah member
if status_member == "ya":
    total_harga = harga_tiket * 0.8  # Diskon 20%
else:
    total_harga = harga_tiket

# Output total harga yang harus dibayar
print("Total harga yang harus dibayar: Rp", int(total_harga))
```

# Output Program Tiket
```
PS C:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 3> python -u "c:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 3\lab2.py"
Masukkan tipe tiket (reguler/vip): reguler
Apakah Anda memiliki kartu member? (ya/tidak): ya
Total harga yang harus dibayar: Rp 40000
PS C:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 3> python -u "c:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 3\lab2.py"
Masukkan tipe tiket (reguler/vip): VIP
Apakah Anda memiliki kartu member? (ya/tidak): tidak
Total harga yang harus dibayar: Rp 100000
PS C:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 3>
```

# Cara Kerja Program Tiket
1. *Mulai (Start)*: Proses dimulai.
2. *Input tipe tiket*: Pengguna memasukkan jenis tiket yang diinginkan, yang dapat berupa tiket reguler (Reg) atau VIP.
3. *Input status member*: Pengguna memasukkan status keanggotaannya, apakah ia adalah seorang anggota (member) atau bukan.
4. *Pengecekan tipe tiket*:
   - Jika tiket adalah *Reguler (Reg)*, lanjut ke langkah berikutnya.
   - Jika tiket adalah *VIP*, juga lanjut ke langkah berikutnya.
5. *Pengecekan status member*:
   - Jika pengguna adalah *member* (YA), maka akan diberikan diskon sebesar 20%.
   - Jika pengguna *bukan member* (TIDAK), maka tidak ada diskon yang diberikan.
6. *Akhir (End)*: Proses selesai.

Flowchart ini menunjukkan bahwa hanya pengguna dengan status member yang mendapatkan diskon 20%, baik untuk tiket reguler maupun VIP.

# Program 2 Kalkulator
Program ini merupakan kalkulator sederhana yang membantu pengguna melakukan operasi matematika dasar antara dua angka, yaitu penjumlahan, pengurangan, perkalian, dan pembagian. 

# Deskripsi Program
Program ini dibuat menggunakan bahasa python dengan fitur:
1. Input Angka
2. Memilih Operator pilihan operasi (+, -, *, /)
3. Proses Operasi Aritmatika if, elif, dan else

# Flowchart Program
![Flowchart](https://github.com/Dwiokta10/lab2py./blob/main/flowchart2kalkulator..png)

# Kode Program Kalkulator
``` python
# Program Kalkulator Sederhana
# Meminta pengguna memasukkan dua angka
angka1 = float(input("Masukkan angka pertama: "))
angka2 = float(input("Masukkan angka kedua: "))

# Meminta pengguna memilih operator
print("Pilih operasi aritmatika:")
print("1. Penjumlahan (+)")
print("2. Pengurangan (-)")
print("3. Perkalian (*)")
print("4. Pembagian (/)")
operator = input("Masukkan pilihan operasi (+, -, *, /): ")

# Menggunakan if, elif, else untuk menentukan operasi yang sesuai
if operator == '+':
    hasil = angka1 + angka2
    print("Hasil dari penjumlahan:", hasil)
elif operator == '-':
    hasil = angka1 - angka2
    print("Hasil dari pengurangan:", hasil)
elif operator == '*':
    hasil = angka1 * angka2
    print("Hasil dari perkalian:", hasil)
elif operator == '/':
    if angka2 != 0:
        hasil = angka1 / angka2
        print("Hasil dari pembagian:", hasil)
    else:
        print("Error: Pembagian dengan nol tidak diperbolehkan.")
else:
    print("Operator tidak valid. Silakan pilih (+, -, *, /).")
```
# Output Program Kalkulator
```
PS C:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 3> python -u "c:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 3\lab2kalkulator.py"
Masukkan angka pertama: 75
Masukkan angka kedua: 30
Pilih operasi aritmatika:
1. Penjumlahan (+)
2. Pengurangan (-)
3. Perkalian (*)
4. Pembagian (/)
Masukkan pilihan operasi (+, -, *, /): -
Hasil dari pengurangan: 45.0
PS C:\Users\acer\Documents\KULIAH\PEMROGRAMAN\Pratikum 3>
````
# Cara Kerja Program 
*Meminta Input Angka Pertama dan Kedua*:
   - Program dimulai dengan meminta pengguna memasukkan dua angka. Keduanya diambil sebagai input dari pengguna dan dikonversi menjadi tipe float agar bisa menangani angka desimal.
*Meminta Pengguna Memilih Operator Aritmatika*:
   - Program kemudian menampilkan pilihan operator aritmatika yang tersedia, yaitu penjumlahan (+), pengurangan (-), perkalian (*), dan pembagian (/).Pengguna diminta memilih salah satu dari operator tersebut dan memasukkannya sebagai input, misalnya, dengan mengetik + untuk penjumlahan.
*Mengidentifikasi Operator yang Dipilih*:
   - Program menggunakan conditional statement (if, elif, dan else) untuk memeriksa operator yang dipilih pengguna:
*Hasil operasi dan langsung ditampilkan*.

