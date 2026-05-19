# STUNGUARD
## Aplikasi Kalkulator Antropometri Anak Berbasis WHO dan Kemenkes RI

STUNGUARD merupakan aplikasi antropometri offline yang digunakan untuk menghitung status gizi dan pertumbuhan anak usia 0–60 bulan berdasarkan standar WHO Child Growth Standards dan Kementerian Kesehatan Republik Indonesia (PMK No. 2 Tahun 2020).

Aplikasi ini mendukung pemeriksaan:

- Berat Badan menurut Umur (BB/U)
- Panjang/Tinggi Badan menurut Umur (PB/U atau TB/U)
- Berat Badan menurut Panjang/Tinggi Badan (BB/PB atau BB/TB)
- BMI menurut Umur (BMI/U)

TUJUAN APLIKASI
======================================================================

1. Membantu deteksi dini stunting.
2. Membantu skrining status gizi anak.
3. Mendukung Posyandu dan Puskesmas.
4. Menyediakan aplikasi antropometri offline.
5. Mengimplementasikan perhitungan Z-score WHO.

TEKNOLOGI YANG DIGUNAKAN
======================================================================

| Teknologi | Fungsi |
|---|---|
| Python | Bahasa Pemrograman |
| PySide6 | GUI Desktop |
| Pandas | Membaca Dataset CSV |
| CSV Dataset | Standar Antropometri WHO |
| Math | Perhitungan Z-score |

STANDAR KEMENTERIAN KESEHATAN REPUBLIK INDONESIA
======================================================================

Penilaian status gizi anak menggunakan acuan:

Peraturan Menteri Kesehatan Republik Indonesia (PMK)
Nomor 2 Tahun 2020
Tentang:
Standar Antropometri Anak

Standar ini mengadopsi WHO Child Growth Standards untuk anak usia 0–60 bulan.

RUMUS Z-SCORE
======================================================================

Rumus utama yang digunakan:

Z-score = (Nilai Pengukuran - Median Referensi) / Simpangan Baku Referensi

Keterangan:

| Komponen | Penjelasan |
|---|---|
| Nilai Pengukuran | Hasil pengukuran anak |
| Median Referensi | Nilai median WHO |
| Simpangan Baku Referensi | Standar deviasi WHO |

RUMUS BMI
======================================================================

BMI = Berat Badan / (Tinggi Badan)^2

Contoh:

BMI = 12 / (0.75)^2

BMI = 21.33

KATEGORI DAN AMBANG BATAS STATUS GIZI ANAK
(BERDASARKAN PMK NO. 2 TAHUN 2020)
======================================================================

1. BERAT BADAN MENURUT UMUR (BB/U)
----------------------------------------------------------------------

| Z-Score | Status Gizi |
|---|---|
| < -3 SD | Berat Badan Sangat Kurang |
| -3 SD sampai < -2 SD | Berat Badan Kurang |
| -2 SD sampai +1 SD | Normal |
| > +1 SD | Risiko Berat Badan Lebih |

----------------------------------------------------------------------

2. PANJANG/TINGGI BADAN MENURUT UMUR (PB/U atau TB/U)
----------------------------------------------------------------------

| Z-Score | Status Gizi |
|---|---|
| < -3 SD | Sangat Pendek (Severely Stunted) |
| -3 SD sampai < -2 SD | Pendek (Stunted) |
| -2 SD sampai +3 SD | Normal |
| > +3 SD | Tinggi |

----------------------------------------------------------------------

3. BERAT BADAN MENURUT PANJANG/TINGGI BADAN (BB/PB atau BB/TB)
----------------------------------------------------------------------

| Z-Score | Status Gizi |
|---|---|
| < -3 SD | Gizi Buruk |
| -3 SD sampai < -2 SD | Gizi Kurang |
| -2 SD sampai +1 SD | Normal |
| +1 SD sampai +2 SD | Risiko Gizi Lebih |
| +2 SD sampai +3 SD | Gizi Lebih |
| > +3 SD | Obesitas |

----------------------------------------------------------------------

4. BMI MENURUT UMUR (BMI/U)
----------------------------------------------------------------------

| Z-Score | Status Gizi |
|---|---|
| < -3 SD | Gizi Buruk |
| -3 SD sampai < -2 SD | Gizi Kurang |
| -2 SD sampai +1 SD | Normal |
| +1 SD sampai +2 SD | Risiko Gizi Lebih |
| +2 SD sampai +3 SD | Gizi Lebih |
| > +3 SD | Obesitas |

CONTOH DATA STANDAR ANTROPOMETRI KEMENKES
======================================================================

1. BERAT BADAN MENURUT UMUR (BB/U)
ANAK LAKI-LAKI USIA 24 BULAN
----------------------------------------------------------------------

| Parameter | Nilai |
|---|---|
| -3 SD | 8.6 kg |
| -2 SD | 9.7 kg |
| -1 SD | 10.8 kg |
| Median | 12.2 kg |
| +1 SD | 13.6 kg |
| +2 SD | 15.3 kg |
| +3 SD | 17.1 kg |

----------------------------------------------------------------------

2. TINGGI BADAN MENURUT UMUR (TB/U)
ANAK PEREMPUAN USIA 24 BULAN
----------------------------------------------------------------------

| Parameter | Nilai |
|---|---|
| -3 SD | 76.0 cm |
| -2 SD | 80.0 cm |
| -1 SD | 82.5 cm |
| Median | 85.1 cm |
| +1 SD | 87.7 cm |
| +2 SD | 90.3 cm |
| +3 SD | 93.0 cm |

----------------------------------------------------------------------

3. BERAT BADAN MENURUT TINGGI BADAN (BB/TB)
ANAK PEREMPUAN TINGGI 75 CM
----------------------------------------------------------------------

| Parameter | Nilai |
|---|---|
| -3 SD | 6.9 kg |
| -2 SD | 7.7 kg |
| -1 SD | 8.5 kg |
| Median | 9.4 kg |
| +1 SD | 10.4 kg |
| +2 SD | 11.5 kg |
| +3 SD | 12.8 kg |

----------------------------------------------------------------------

4. BMI MENURUT UMUR (BMI/U)
ANAK PEREMPUAN USIA 24 BULAN
----------------------------------------------------------------------

| Parameter | Nilai |
|---|---|
| -3 SD | 12.5 |
| -2 SD | 13.8 |
| -1 SD | 15.0 |
| Median | 16.0 |
| +1 SD | 19.1 |
| +2 SD | 21.9 |
| +3 SD | 24.8 |


CONTOH PERHITUNGAN MANUAL
======================================================================

KASUS:
----------------------------------------------------------------------

| Parameter | Nilai |
|---|---|
| Jenis Kelamin | Perempuan |
| Umur | 24 bulan |
| Berat Badan | 12 kg |
| Tinggi Badan | 75 cm |

#### BERAT BADAN MENURUT UMUR (BB/U)

Data Referensi:
- Median = 11.5 kg
- SD = 1.4 kg

Rumus:

Z-score = (12 - 11.5) / 1.4

Perhitungan:

Z-score = 0.5 / 1.4

Hasil:

Z-score = 0.36

Interpretasi:
- Status = Normal

#### TINGGI BADAN MENURUT UMUR (TB/U)

Data Referensi:
- Median = 85.1 cm
- SD = 2.8 cm

Rumus:

Z-score = (75 - 85.1) / 2.8

Perhitungan:

Z-score = -10.1 / 2.8

Hasil:

Z-score = -3.61

Interpretasi:
- Status = Sangat Pendek (Severely Stunted)

#### BERAT BADAN MENURUT TINGGI BADAN (BB/TB)

Data Referensi:
- Median = 9.4 kg
- SD = 0.9 kg

Rumus:

Z-score = (12 - 9.4) / 0.9

Perhitungan:

Z-score = 2.6 / 0.9

Hasil:

Z-score = 2.89

Interpretasi:
- Status = Gizi Lebih

#### BMI MENURUT UMUR (BMI/U)

Langkah 1 — Menghitung BMI

Rumus BMI:

BMI = Berat Badan / (Tinggi Badan)^2

Perhitungan:

BMI = 12 / (0.75)^2

BMI = 12 / 0.5625

Hasil:

BMI = 21.33

----------------------------------------------------------------------

Data Referensi:
- Median BMI = 16.0
- SD BMI = 1.5

----------------------------------------------------------------------

Menghitung Z-score BMI/U

Rumus:

Z-score = (21.33 - 16.0) / 1.5

Perhitungan:

Z-score = 5.33 / 1.5

Hasil:

Z-score = 3.55

Interpretasi:
- Status = Obesitas

KESIMPULAN AKHIR STATUS GIZI
======================================================================

| Indikator | Z-Score | Status |
|---|---|---|
| BB/U | 0.36 | Normal |
| TB/U | -3.61 | Sangat Pendek |
| BB/TB | 2.89 | Gizi Lebih |
| BMI/U | 3.55 | Obesitas |

Kesimpulan:
- Anak mengalami stunting berat berdasarkan TB/U.
- Berat badan relatif berlebih terhadap tinggi badan.
- BMI menunjukkan obesitas.
- Kondisi ini dapat dikategorikan sebagai stunted obesity, yaitu anak pendek tetapi mengalami berat badan berlebih.

STRUKTUR DATASET
======================================================================

dataset/
│
├── boys/
│   ├── wfa.csv
│   ├── lfa.csv
│   ├── wfl.csv
│   └── bmifa.csv
│
├── girls/
│   ├── wfa.csv
│   ├── lfa.csv
│   ├── wfl.csv
│   └── bmifa.csv


1. World Health Organization (WHO). WHO Child Growth Standards.
2. WHO Anthro Software Manual.
3. PMK No. 2 Tahun 2020 tentang Standar Antropometri Anak.
4. Kementerian Kesehatan Republik Indonesia.
5. WHO Training Course on Child Growth Assessment.
