# Tugas3_PCD
# CPD_Tugas3

---

## NOTE 1

- **Poin 1 (Grayscale):** Proses ini mengubah citra berwarna menjadi keabuan dengan mengambil rata-rata dari nilai Red, Green, dan Blue menggunakan formula `xg = (r + g + b) / 3` pada setiap piksel.

- **Poin 2 (Biner):** Proses thresholding yang mengubah citra grayscale menjadi hanya memiliki dua nilai warna, yaitu 0 (hitam) dan 1 atau nilai maksimum (putih).

- **Poin 3 (m-Bit / Kuantisasi):** Proses mengurangi jumlah variasi warna keabuan menjadi tingkat yang lebih sedikit, misalnya membatasi rentang nilai warna hanya menjadi `2^m` tingkat.

- **Poin 4 (Brightness):** Proses penambahan intensitas cahaya, dilakukan dengan menambahkan nilai derajat keabuan `x` dengan suatu nilai konstanta perubahan brightness pada setiap piksel.

- **Poin 5 (Contrast):** Proses penajaman rentang warna, dilakukan dengan mengalikan nilai derajat keabuan `x` dengan suatu nilai konstanta perubahan contrast.

- **Poin 6 (Histogram):** Menampilkan grafik yang menyatakan distribusi dari derajat keabuan (terang/gelap) pada suatu citra.

- **Poin 7 (Histogram Equalization):** Proses untuk meratakan distribusi histogram agar derajat keabuan dari 0 hingga 255 memiliki kemunculan yang rata.

---

## NOTE 2

**Apakah teori di kelas dengan kode di Python/Colab prosesnya sama atau tidak?**

Secara konsep hasil akhir adalah sama, namun secara proses eksekusi komputasi berbeda:

1. **Teori di Kelas (Pemrosesan Manual):**  
   Pengolahan citra dilakukan dengan pendekatan memproses piksel satu per satu menggunakan perulangan bersarang (*nested loop*), lalu menerapkan operasi matematika secara manual.

2. **Kode Python (OpenCV):**  
   Menggunakan library seperti `cv2.cvtColor()` atau `cv2.equalizeHist()` yang memproses seluruh citra secara langsung (*vectorized operation*).

3. **Penanganan Batas Nilai (Overflow):**  
   OpenCV memiliki mekanisme otomatis untuk menjaga nilai piksel tetap dalam rentang 0–255.

---
