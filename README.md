# Dwi Okta Ramadhani
# TI.24.A.1

# Program Harga Tiket
Program ini adalah program harga tiket yang menghitung total biaya tiket
berdasarkan dua faktor utama: tipe tiket (Reguler atau VIP) dan status keanggotaan (apakah pengguna memiliki kartu member atau tidak)

# Program ini dibuat menggunakan bahasa python dengan fitur:
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
