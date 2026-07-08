# Penjelasan Data Tabulasi untuk Pengujian SPSS

Dokumen ini menjelaskan struktur data tabulasi yang telah disiapkan untuk kebutuhan pengujian menggunakan **SPSS**. Data ini berasal dari jawaban kuesioner yang telah dirapikan menjadi format tabular, sehingga setiap responden berada pada satu baris dan setiap pertanyaan atau variabel berada pada satu kolom.

---

## 1. Tujuan Pembuatan Data Tabulasi

Data tabulasi dibuat agar data kuesioner lebih mudah digunakan untuk proses analisis statistik di SPSS, seperti:

- Uji validitas
- Uji reliabilitas
- Statistik deskriptif
- Uji korelasi
- Uji regresi
- Analisis rata-rata setiap variabel

Format ini memudahkan proses impor data ke SPSS karena setiap item pertanyaan sudah diberi kode variabel yang ringkas dan konsisten.

---

## 2. Struktur Umum Data

Setiap baris pada data menunjukkan **satu responden**.

Setiap kolom menunjukkan **identitas responden, item pertanyaan, atau hasil perhitungan rata-rata variabel**.

Secara umum, struktur data adalah sebagai berikut:

| Bagian Data | Keterangan |
|---|---|
| Identitas responden | Berisi nomor, tanggal, nama, dan NIM responden |
| Item pertanyaan | Berisi jawaban responden untuk setiap butir pertanyaan |
| Mean variabel | Berisi nilai rata-rata dari setiap kelompok variabel |
| Total mean | Berisi nilai rata-rata keseluruhan jawaban responden |

---

## 3. Penjelasan Kolom Identitas

Kolom identitas digunakan untuk mengenali responden. Kolom ini tidak digunakan sebagai variabel utama dalam pengujian statistik, tetapi berguna untuk administrasi data.

| Kolom | Keterangan |
|---|---|
| **NO** | Nomor urut responden |
| **TANGGAL** | Tanggal responden mengisi kuesioner |
| **NAMA** | Nama responden |
| **NIM** | Nomor Induk Mahasiswa responden |

---

## 4. Penjelasan Kolom Item Pertanyaan

Kolom seperti **KMS1**, **KMS2**, **KPP1**, **MS1**, dan seterusnya merupakan kode dari item pertanyaan kuesioner.

Kode tersebut dibuat agar nama variabel lebih singkat dan mudah dibaca oleh SPSS.

| Kode Variabel | Keterangan |
|---|---|
| **KMS1–KMS4** | Item pertanyaan ke-1 sampai ke-4 pada variabel KMS |
| **KPP1–KPP4** | Item pertanyaan ke-1 sampai ke-4 pada variabel KPP |
| **MS1–MS4** | Item pertanyaan ke-1 sampai ke-4 pada variabel MS |
| **EP1–EP4** | Item pertanyaan ke-1 sampai ke-4 pada variabel EP |
| **PP1–PP4** | Item pertanyaan ke-1 sampai ke-4 pada variabel PP |
| **KT1–KT4** | Item pertanyaan ke-1 sampai ke-4 pada variabel KT |
| **PK1–PK4** | Item pertanyaan ke-1 sampai ke-4 pada variabel PK |
| **SA1–SA4** | Item pertanyaan ke-1 sampai ke-4 pada variabel SA |

Contoh:

| Kode | Arti |
|---|---|
| **KMS1** | Pertanyaan pertama pada variabel KMS |
| **KMS2** | Pertanyaan kedua pada variabel KMS |
| **KMS3** | Pertanyaan ketiga pada variabel KMS |
| **KMS4** | Pertanyaan keempat pada variabel KMS |

---

## 5. Skala Jawaban

Data menggunakan skala Likert. Skala ini umum digunakan dalam penelitian kuantitatif untuk mengukur tingkat persetujuan responden terhadap suatu pernyataan.

Contoh skala Likert yang digunakan:

| Skor | Keterangan |
|---|---|
| **1** | Sangat Tidak Setuju |
| **2** | Tidak Setuju |
| **3** | Netral |
| **4** | Setuju |
| **5** | Sangat Setuju |

Dengan demikian, apabila pada kolom **KMS1** terdapat nilai **4**, maka responden tersebut menjawab **Setuju** terhadap pertanyaan KMS1.

Semakin tinggi skor yang diberikan, semakin tinggi tingkat persetujuan responden terhadap pernyataan tersebut.

---

## 6. Penjelasan Kolom Mean Variabel

Kolom mean digunakan untuk menghitung nilai rata-rata dari setiap kelompok item pertanyaan.

Contohnya, variabel **KMS** memiliki empat item pertanyaan, yaitu:

- KMS1
- KMS2
- KMS3
- KMS4

Maka kolom **KMS_MEAN** merupakan rata-rata dari keempat item tersebut.

Rumusnya:

```text
KMS_MEAN = (KMS1 + KMS2 + KMS3 + KMS4) / 4
```

Contoh perhitungan:

| KMS1 | KMS2 | KMS3 | KMS4 | KMS_MEAN |
|---|---|---|---|---|
| 4 | 5 | 4 | 4 | 4.25 |

Perhitungannya:

```text
KMS_MEAN = (4 + 5 + 4 + 4) / 4
KMS_MEAN = 17 / 4
KMS_MEAN = 4.25
```

Artinya, responden tersebut memiliki nilai rata-rata **4.25** pada variabel KMS.

---

## 7. Daftar Kolom Mean

Berikut adalah daftar kolom mean yang terdapat dalam data:

| Kolom Mean | Keterangan |
|---|---|
| **KMS_MEAN** | Rata-rata item KMS1 sampai KMS4 |
| **KPP_MEAN** | Rata-rata item KPP1 sampai KPP4 |
| **MS_MEAN** | Rata-rata item MS1 sampai MS4 |
| **EP_MEAN** | Rata-rata item EP1 sampai EP4 |
| **PP_MEAN** | Rata-rata item PP1 sampai PP4 |
| **KT_MEAN** | Rata-rata item KT1 sampai KT4 |
| **PK_MEAN** | Rata-rata item PK1 sampai PK4 |
| **SA_MEAN** | Rata-rata item SA1 sampai SA4 |

Kolom mean ini biasanya digunakan untuk analisis lanjutan, seperti korelasi dan regresi.

---

## 8. Penjelasan Kolom TOTAL_MEAN

Kolom **TOTAL_MEAN** merupakan rata-rata keseluruhan dari semua variabel atau semua item yang digunakan dalam kuesioner.

Rumus sederhananya:

```text
TOTAL_MEAN = (KMS_MEAN + KPP_MEAN + MS_MEAN + EP_MEAN + PP_MEAN + KT_MEAN + PK_MEAN + SA_MEAN) / 8
```

Kolom ini digunakan untuk melihat kecenderungan umum jawaban responden terhadap seluruh pertanyaan dalam kuesioner.

Semakin tinggi nilai **TOTAL_MEAN**, semakin tinggi tingkat persetujuan responden secara keseluruhan.

---

## 9. Fungsi Data dalam Pengujian SPSS

Data ini dapat digunakan untuk beberapa jenis pengujian statistik di SPSS.

| Jenis Pengujian | Data yang Digunakan | Tujuan |
|---|---|---|
| **Uji validitas** | Item pertanyaan, misalnya KMS1–KMS4 | Mengetahui apakah setiap item pertanyaan valid |
| **Uji reliabilitas** | Item dalam setiap variabel | Mengetahui konsistensi item pertanyaan |
| **Statistik deskriptif** | Item dan mean variabel | Mengetahui nilai minimum, maksimum, mean, dan standar deviasi |
| **Uji korelasi** | Kolom mean variabel | Mengetahui hubungan antarvariabel |
| **Uji regresi** | Kolom mean variabel | Mengetahui pengaruh variabel bebas terhadap variabel terikat |
| **Uji normalitas** | Kolom mean atau residual regresi | Mengetahui apakah data berdistribusi normal |

---

## 10. Perbedaan Item Pertanyaan dan Mean Variabel

Item pertanyaan dan mean variabel memiliki fungsi yang berbeda.

| Jenis Kolom | Contoh | Fungsi |
|---|---|---|
| **Item pertanyaan** | KMS1, KMS2, KMS3, KMS4 | Digunakan untuk uji validitas dan reliabilitas |
| **Mean variabel** | KMS_MEAN | Digunakan untuk analisis korelasi, regresi, dan deskriptif |
| **Total mean** | TOTAL_MEAN | Digunakan untuk melihat rata-rata keseluruhan jawaban responden |

Item pertanyaan menunjukkan jawaban responden pada setiap butir pertanyaan, sedangkan mean variabel menunjukkan nilai rata-rata dari beberapa item dalam satu variabel.

---

## 11. Cara Membaca Data

Contoh data seorang responden:

| KMS1 | KMS2 | KMS3 | KMS4 | KMS_MEAN |
|---|---|---|---|---|
| 5 | 4 | 4 | 5 | 4.50 |

Interpretasi:

Responden tersebut memberikan jawaban yang tinggi terhadap variabel KMS. Nilai rata-rata **4.50** menunjukkan bahwa responden cenderung **setuju hingga sangat setuju** terhadap pernyataan-pernyataan pada variabel KMS.

Contoh lain:

| KPP1 | KPP2 | KPP3 | KPP4 | KPP_MEAN |
|---|---|---|---|---|
| 3 | 3 | 4 | 3 | 3.25 |

Interpretasi:

Nilai rata-rata **3.25** menunjukkan bahwa responden cenderung berada pada kategori **netral menuju setuju** terhadap variabel KPP.

---

## 12. Kesimpulan

Data tabulasi ini merupakan data kuesioner yang telah disusun dalam format yang rapi dan siap digunakan untuk pengujian SPSS.

Kolom **NO**, **TANGGAL**, **NAMA**, dan **NIM** digunakan sebagai identitas responden. Kolom **KMS1 sampai SA4** merupakan item pertanyaan kuesioner. Kolom **KMS_MEAN sampai SA_MEAN** merupakan rata-rata dari setiap variabel. Sementara itu, kolom **TOTAL_MEAN** menunjukkan nilai rata-rata keseluruhan jawaban responden.

Dengan format ini, data dapat digunakan untuk uji validitas, uji reliabilitas, statistik deskriptif, korelasi, regresi, dan analisis statistik lainnya sesuai kebutuhan penelitian.
