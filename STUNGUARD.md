````markdown id="u5yl1k"
# STUNGUARD
## Aplikasi Kalkulator Antropometri Berbasis WHO LMS untuk Anak Usia 0–60 Bulan

---

# 1. Gambaran Umum Proyek

STUNGUARD merupakan aplikasi antropometri offline yang dirancang untuk menghitung status gizi dan pertumbuhan anak usia 0–60 bulan menggunakan standar WHO Child Growth Standards dan metode LMS (Lambda-Mu-Sigma).

Aplikasi ini berfokus pada:
- Berat Badan menurut Umur (BB/U)
- Panjang/Tinggi Badan menurut Umur (PB/U atau TB/U)
- Berat Badan menurut Panjang/Tinggi Badan (BB/PB atau BB/TB)
- BMI menurut Umur (BMI/U)

Aplikasi menghitung Z-score berdasarkan standar WHO dan mengklasifikasikan status gizi seperti:
- Normal
- Gizi Kurang
- Stunting
- Severely Stunted
- Overweight
- Obesitas

---

# 2. Tujuan Proyek

Tujuan utama STUNGUARD adalah:

1. Menyediakan aplikasi antropometri offline.
2. Membantu deteksi dini stunting dan malnutrisi.
3. Mengimplementasikan metode LMS WHO.
4. Mendukung skrining Posyandu dan Puskesmas.
5. Menyediakan perhitungan antropometri yang kompatibel dengan WHO Anthro.

---

# 3. Teknologi yang Digunakan

| Teknologi | Fungsi |
|---|---|
| Python | Bahasa Pemrograman Utama |
| PySide6 | Framework GUI |
| Pandas | Pemrosesan Dataset CSV |
| Math | Perhitungan LMS |
| Dataset WHO LMS | Standar Antropometri |

---

# 4. Indikator Antropometri

## 4.1 Berat Badan menurut Umur (BB/U)

Mengukur berat badan berdasarkan usia anak.

### Interpretasi

| Z-Score | Klasifikasi |
|---|---|
| < -3 SD | Berat Badan Sangat Kurang |
| -3 SD sampai < -2 SD | Berat Badan Kurang |
| -2 SD sampai +1 SD | Normal |
| > +1 SD | Risiko Berat Badan Lebih |

---

## 4.2 Panjang/Tinggi Badan menurut Umur (PB/U atau TB/U)

Mengukur panjang atau tinggi badan berdasarkan usia anak.

### Interpretasi

| Z-Score | Klasifikasi |
|---|---|
| < -3 SD | Sangat Pendek (Severely Stunted) |
| -3 SD sampai < -2 SD | Pendek (Stunted) |
| -2 SD sampai +3 SD | Normal |
| > +3 SD | Tinggi |

---

## 4.3 Berat Badan menurut Panjang/Tinggi Badan (BB/PB atau BB/TB)

Mengukur berat badan relatif terhadap panjang atau tinggi badan.

### Interpretasi

| Z-Score | Klasifikasi |
|---|---|
| < -3 SD | Gizi Buruk |
| -3 SD sampai < -2 SD | Gizi Kurang |
| -2 SD sampai +1 SD | Normal |
| +1 SD sampai +2 SD | Risiko Gizi Lebih |
| +2 SD sampai +3 SD | Gizi Lebih |
| > +3 SD | Obesitas |

---

## 4.4 BMI menurut Umur (BMI/U)

Mengukur Body Mass Index berdasarkan usia anak.

### Interpretasi

| Z-Score | Klasifikasi |
|---|---|
| < -3 SD | Gizi Buruk |
| -3 SD sampai < -2 SD | Gizi Kurang |
| -2 SD sampai +1 SD | Normal |
| +1 SD sampai +2 SD | Risiko Gizi Lebih |
| +2 SD sampai +3 SD | Gizi Lebih |
| > +3 SD | Obesitas |

---

# 5. Metode WHO LMS

Aplikasi menggunakan metode LMS WHO.

LMS terdiri dari:

| Parameter | Penjelasan |
|---|---|
| L | Lambda (Transformasi Box-Cox) |
| M | Median |
| S | Koefisien Variasi |

---

# 6. Rumus WHO LMS

Jika:

```math
L ≠ 0
````

Maka:

```math id="0f9d53"
Z = \frac{\left(\frac{X}{M}\right)^L - 1}{L \times S}
```

Keterangan:

| Simbol | Penjelasan       |
| ------ | ---------------- |
| X      | Nilai Pengukuran |
| L      | Lambda           |
| M      | Median           |
| S      | Simpangan Baku   |

---

# 7. Rumus Ketika L = 0

Jika:

```math id="w7f05v"
L = 0
```

Maka:

```math id="91b84r"
Z = \frac{\ln(X/M)}{S}
```

---

# 8. Rumus BMI

BMI dihitung menggunakan rumus:

```math id="xjzlm7"
BMI = \frac{Berat\ Badan\ (kg)}{Tinggi\ Badan\ (m)^2}
```

---

# 9. Contoh Perhitungan Manual

## Studi Kasus

| Parameter           | Nilai      |
| ------------------- | ---------- |
| Jenis Kelamin       | Perempuan  |
| Tanggal Lahir       | 17/05/2024 |
| Tanggal Pemeriksaan | 17/05/2026 |
| Berat Badan         | 12 kg      |
| Tinggi Badan        | 75 cm      |

---

# 10. Langkah 1 — Menghitung Umur

Usia anak:

```text id="19bh3n"
24 bulan
```

---

# 11. Langkah 2 — Menghitung BMI

Rumus:

```math id="o0h6zk"
BMI = \frac{12}{0.75^2}
```

Hasil:

```math id="l8rll0"
BMI = 21.33
```

---

# 12. Langkah 3 — Referensi LMS WHO

Contoh Dataset WHO BMI/U:

| Umur | L       | M      | S       |
| ---- | ------- | ------ | ------- |
| 24   | -0.3833 | 16.423 | 0.08592 |

---

# 13. Langkah 4 — Perhitungan LMS

Rumus:

```math id="f8x0v9"
Z = \frac{\left(\frac{X}{M}\right)^L - 1}{L \times S}
```

Substitusi:

```math id="ed7exm"
Z = \frac{\left(\frac{21.33}{16.423}\right)^{-0.3833} - 1}{-0.3833 \times 0.08592}
```

Hasil:

```text id="qaqgvi"
Z ≈ 3.52
```

---

# 14. Hasil Akhir Antropometri

| Indikator | Z-Score | Klasifikasi   |
| --------- | ------- | ------------- |
| BB/PB     | 2.86    | Gizi Lebih    |
| BB/U      | 0.36    | Normal        |
| PB/U      | -3.53   | Sangat Pendek |
| BMI/U     | 3.52    | Obesitas      |

---

# 15. Pentingnya WHO LMS

Metode LMS WHO memberikan:

* distribusi pertumbuhan non-linear,
* deteksi obesitas lebih akurat,
* deteksi stunting lebih akurat,
* kompatibilitas dengan WHO Anthro.

Interpolasi SD sederhana sering menghasilkan kesalahan pada kasus ekstrem.

---

# 16. Struktur Dataset

```text id="c73mh8"
dataset/
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
```

---

# 17. Contoh Dataset

## girls/bmifa.csv

```csv id="2wbk33"
age,L,M,S
24,-0.3833,16.423,0.08592
25,-0.3833,16.353,0.08584
```

---

# 18. Instalasi

Install library yang dibutuhkan:

```bash id="3hzn2m"
pip install PySide6 pandas
```

---

# 19. Menjalankan Program

```bash id="ybf29m"
python main.py
```

---

# 20. Fitur Aplikasi

## Fitur Saat Ini

* Perhitungan WHO LMS
* Offline Mode
* GUI Interface
* Perhitungan BMI
* BB/U
* PB/U atau TB/U
* BB/PB atau BB/TB
* BMI/U
* Klasifikasi WHO Z-score

---

# 21. Pengembangan Selanjutnya

Rencana pengembangan berikutnya:

* Export PDF
* Grafik Pertumbuhan
* Database SQLite
* Versi Android
* Integrasi Posyandu
* Multi-language Support
* Visualisasi Grafik WHO

---

# 22. Kesimpulan

STUNGUARD berhasil mengimplementasikan standar antropometri WHO LMS untuk anak usia 0–60 bulan.

Aplikasi menyediakan:

* perhitungan Z-score kompatibel WHO,
* klasifikasi status gizi,
* skrining stunting,
* skrining obesitas,
* pemeriksaan antropometri offline.

Metode LMS menghasilkan perhitungan lebih akurat dibandingkan interpolasi SD sederhana karena standar pertumbuhan WHO bersifat non-linear.

---

# 23. Referensi

1. World Health Organization (WHO). WHO Child Growth Standards.
2. WHO Anthro Software Manual.
3. Kementerian Kesehatan Republik Indonesia.
4. PMK No. 2 Tahun 2020 tentang Standar Antropometri Anak.
5. WHO Training Course on Child Growth Assessment.

```
```
