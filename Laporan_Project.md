Pengujian aplikasi STUNGUARD, menggunakan:

```text
Jenis Kelamin (L/P)
Tanggal Lahir
Tanggal Pemeriksaan
Berat Badan (kg)
Tinggi Badan (cm)
```

Berikut **5 skenario pengujian lengkap berbasis tanggal**, digunakan untuk validasi program **STUNGUARD APPS**.

---

# PENGUJIAN 1 – STATUS GIZI NORMAL

## Input

```text
Jenis Kelamin      : L
Tanggal Lahir      : 10/01/2024
Tanggal Pemeriksaan: 10/07/2024

Berat Badan        : 7.0 kg
Panjang Badan      : 64.0 cm
```

## Perhitungan Umur

```text
10/01/2024 → 10/07/2024

= 0 Tahun
= 6 Bulan
= 0 Hari

Usia = 6 bulan
```

---

## BB/U

Referensi usia 6 bulan

```text
Median = 7.9
-1 SD  = 7.1

SD = 7.9 - 7.1
SD = 0.8

Z = (7.0 - 7.9) / 0.8
Z = -1.125
```

Status:

```text
Berat Badan Normal
```

---

## PB/U

```text
Median = 67.6
-1 SD  = 65.5

SD = 2.1

Z = (64.0 - 67.6) / 2.1
Z = -1.714
```

Status:

```text
Normal
```

---

## BB/PB

```text
Median = 7.0
+1 SD  = 7.6

SD = 0.6

Z = (7.0 - 7.0) / 0.6
Z = 0.000
```

Status:

```text
Gizi Baik (Normal)
```

---

## IMT/U

```text
IMT = 7 / (0.64²)

IMT = 17.090
```

```text
Median = 17.3
-1 SD  = 16.0

SD = 1.3

Z = (17.090 - 17.3) / 1.3
Z = -0.162
```

Status:

```text
Gizi Baik (Normal)
```

---

# PENGUJIAN 2 – BERAT BADAN SANGAT KURANG

## Input

```text
Jenis Kelamin      : L
Tanggal Lahir      : 15/01/2023
Tanggal Pemeriksaan: 15/07/2024

Berat Badan        : 7.5 kg
Panjang Badan      : 75 cm
```

## Umur

```text
1 Tahun 6 Bulan

= 18 bulan
```

---

## BB/U

```text
Median = 10.9
-1 SD  = 9.8

SD = 1.1

Z = (7.5 - 10.9) / 1.1

Z = -3.091
```

Status:

```text
Berat Badan Sangat Kurang
```

---

## PB/U

```text
Median = 82.3
-1 SD  = 79.6

SD = 2.7

Z = (75 - 82.3) / 2.7

Z = -2.704
```

Status:

```text
Pendek
```

---

## BB/PB

```text
Median = 9.5
-1 SD  = 8.8

SD = 0.7

Z = (7.5 - 9.5) / 0.7

Z = -2.857
```

Status:

```text
Gizi Kurang
```

---

## IMT/U

```text
IMT = 7.5 / (0.75²)

IMT = 13.333
```

```text
Median = 16.1
-1 SD  = 14.9

SD = 1.2

Z = (13.333 - 16.1) / 1.2

Z = -2.306
```

Status:

```text
Gizi Kurang
```

---

# PENGUJIAN 3 – STUNTING BERAT

## Input

```text
Jenis Kelamin      : L
Tanggal Lahir      : 10/01/2021
Tanggal Pemeriksaan: 10/01/2024

Berat Badan        : 14 kg
Tinggi Badan       : 85 cm
```

## Umur

```text
3 Tahun

= 36 bulan
```

---

## BB/U

```text
Median = 14.3
-1 SD  = 12.7

SD = 1.6

Z = (14 - 14.3) / 1.6

Z = -0.188
```

Status:

```text
Berat Badan Normal
```

---

## TB/U

```text
Median = 96.1
-1 SD  = 92.4

SD = 3.7

Z = (85 - 96.1) / 3.7

Z = -3.000
```

Status:

```text
Sangat Pendek
```

---

## BB/TB

```text
Median = 11.7
+1 SD  = 12.8

SD = 1.1

Z = (14 - 11.7) / 1.1

Z = 2.091
```

Status:

```text
Gizi Lebih
```

---

## IMT/U

```text
IMT = 14 / (0.85²)

IMT = 19.377
```

```text
Median = 15.6
+1 SD = 16.9

SD = 1.3

Z = (19.377 - 15.6) / 1.3

Z = 2.905
```

Status:

```text
Gizi Lebih
```

---

# PENGUJIAN 4 – RISIKO BERAT BADAN LEBIH

## Input

```text
Jenis Kelamin      : L
Tanggal Lahir      : 17/05/2024
Tanggal Pemeriksaan: 17/05/2026

Berat Badan        : 16 kg
Tinggi Badan       : 87 cm
```

## Umur

```text
2 Tahun

= 24 bulan
```

---

## BB/U

```text
Median = 12.2
+1 SD  = 13.6

SD = 1.4

Z = (16 - 12.2) / 1.4

Z = 2.714
```

Status:

```text
Risiko Berat Badan Lebih
```

---

## TB/U

```text
Median = 87.1
+1 SD  = 90.2

SD = 3.1

Z = (87 - 87.1) / 3.1

Z = -0.032
```

Status:

```text
Normal
```

---

## BB/TB

```text
Median = 12.2

+1 SD = 13.3

SD = 1.1

Z = (16 - 12.2) / 1.1

Z = 3.455
```

Status:

```text
Obesitas
```

---

## IMT/U

```text
IMT = 16 / (0.87²)

IMT = 21.142
```

```text
Median = 16.0

+1 SD = 17.3

SD = 1.3

Z = (21.142 - 16.0) / 1.3

Z = 3.955
```

Status:

```text
Obesitas
```

---

# PENGUJIAN 5 – OBESITAS

## Input

```text
Jenis Kelamin      : L
Tanggal Lahir      : 10/01/2019
Tanggal Pemeriksaan: 10/01/2024

Berat Badan        : 25 kg
Tinggi Badan       : 110 cm
```

## Umur

```text
5 Tahun

= 60 bulan
```

---

## BB/U

```text
Median = 18.3

+1 SD = 21.0

SD = 2.7

Z = (25 - 18.3) / 2.7

Z = 2.481
```

Status:

```text
Risiko Berat Badan Lebih
```

---

## TB/U

```text
Median = 110.0

+1 SD = 114.6

SD = 4.6

Z = (110 - 110) / 4.6

Z = 0.000
```

Status:

```text
Normal
```

---

## BB/TB

```text
Median = 18.5

+1 SD = 20.2

SD = 1.7

Z = (25 - 18.5) / 1.7

Z = 3.824
```

Status:

```text
Obesitas
```

---

## IMT/U

```text
IMT = 25 / (1.10²)

IMT = 20.661
```

```text
Median = 15.2

+1 SD = 16.6

SD = 1.4

Z = (20.661 - 15.2) / 1.4

Z = 3.901
```

Status:

```text
Obesitas
```

Kelima skenario ini dapat langsung digunakan sebagai **test case validasi aplikasi**, karena format inputnya sudah sama persis dengan yang dimasukkan pengguna ke program (`Jenis Kelamin`, `Tanggal Lahir`, `Tanggal Pemeriksaan`, `Berat Badan`, dan `Panjang/Tinggi Badan`).
