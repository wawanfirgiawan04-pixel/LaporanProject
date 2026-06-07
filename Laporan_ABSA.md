# Pengujian Pertama

## Konfigurasi Eksperimen

### Dataset

* Dataset Eksplorasi: **3054 data**
* Jumlah aspek: **4**

### Parameter

```bash
--aspects 4
--no-stopword
--no-negasi
```

### Pra-pemrosesan Teks

| Tahap            | Status |
| ---------------- | ------ |
| Case Folding     | ✓      |
| Cleansing        | ✓      |
| Normalisasi      | ✓      |
| Tokenizing       | ✓      |
| Convert Negasi   | ✗      |
| Stopword Removal | ✗      |
| Stemming         | ✓      |
| TF-IDF           | ✓      |

---

## Hasil Evaluasi

### Gameplay & Storyline

| Balancing   | Accuracy | Precision | Recall |     F1-Score |
| ----------- | -------: | --------: | -----: | -----------: |
| None        |   86.70% |    86.18% | 86.70% | **86.42%** ⭐ |
| SMOTE       |   81.12% |    87.28% | 81.12% |       83.19% |
| Tomek-Link  |   86.27% |    86.27% | 86.27% |       86.27% |
| SMOTE-Tomek |   81.12% |    87.28% | 81.12% |       83.19% |

### Aksesibilitas

| Balancing   | Accuracy | Precision | Recall |     F1-Score |
| ----------- | -------: | --------: | -----: | -----------: |
| None        |   73.12% |    72.89% | 73.12% |       73.00% |
| SMOTE       |   75.27% |    75.49% | 75.27% | **75.37%** ⭐ |
| Tomek-Link  |   75.27% |    75.49% | 75.27% | **75.37%** ⭐ |
| SMOTE-Tomek |   75.27% |    75.49% | 75.27% | **75.37%** ⭐ |

### Grafis & Performa

| Balancing   | Accuracy | Precision | Recall |     F1-Score |
| ----------- | -------: | --------: | -----: | -----------: |
| None        |   77.22% |    75.43% | 77.22% |       75.03% |
| SMOTE       |   75.95% |    76.31% | 75.95% |       76.12% |
| Tomek-Link  |   77.85% |    76.28% | 77.85% | **76.19%** ⭐ |
| SMOTE-Tomek |   75.95% |    76.31% | 75.95% |       76.12% |

### Fitur

| Balancing   | Accuracy | Precision | Recall |     F1-Score |
| ----------- | -------: | --------: | -----: | -----------: |
| None        |   77.22% |    74.96% | 77.22% |       75.09% |
| SMOTE       |   73.42% |    72.98% | 73.42% |       73.19% |
| Tomek-Link  |   78.48% |    76.68% | 78.48% | **76.80%** ⭐ |
| SMOTE-Tomek |   73.42% |    72.98% | 73.42% |       73.19% |

---

## Ringkasan Pengujian Pertama

| Aspek                | Metode Terbaik              | F1-Score |
| -------------------- | --------------------------- | -------: |
| Gameplay & Storyline | None                        |   86.42% |
| Aksesibilitas        | SMOTE / Tomek / SMOTE-Tomek |   75.37% |
| Grafis & Performa    | Tomek-Link                  |   76.19% |
| Fitur                | Tomek-Link                  |   76.80% |

---

# Pengujian Kedua

## Konfigurasi Eksperimen

### Dataset

* Dataset Eksplorasi: **3054 data**
* Jumlah aspek: **4**

### Parameter

```bash
--aspects 4
--no-stopword
--no-negasi
```

### Pra-pemrosesan Teks

| Tahap            | Status |
| ---------------- | ------ |
| Case Folding     | ✓      |
| Cleansing        | ✓      |
| Normalisasi      | ✓      |
| Tokenizing       | ✓      |
| Convert Negasi   | ✗      |
| Stopword Removal | ✗      |
| Stemming         | ✓      |
| TF-IDF           | ✓      |

---

## Hasil Evaluasi

### Gameplay & Storyline

| Balancing   | Accuracy | Precision | Recall |     F1-Score |
| ----------- | -------: | --------: | -----: | -----------: |
| None        |   85.16% |    84.30% | 85.16% |       83.73% |
| SMOTE       |   79.69% |    80.23% | 79.69% |       79.94% |
| Tomek-Link  |   85.16% |    84.21% | 85.16% | **84.05%** ⭐ |
| SMOTE-Tomek |   79.69% |    80.23% | 79.69% |       79.94% |

### Aksesibilitas

| Balancing   | Accuracy | Precision | Recall |     F1-Score |
| ----------- | -------: | --------: | -----: | -----------: |
| None        |   82.09% |    81.69% | 82.09% |       81.05% |
| SMOTE       |   83.58% |    83.24% | 83.58% | **82.82%** ⭐ |
| Tomek-Link  |   82.09% |    81.69% | 82.09% |       81.05% |
| SMOTE-Tomek |   83.58% |    83.24% | 83.58% | **82.82%** ⭐ |

### Grafis & Performa

| Balancing   | Accuracy | Precision | Recall |     F1-Score |
| ----------- | -------: | --------: | -----: | -----------: |
| None        |   76.74% |    76.62% | 76.74% |       76.64% |
| SMOTE       |   76.74% |    76.62% | 76.74% |       76.64% |
| Tomek-Link  |   77.91% |    77.84% | 77.91% | **77.86%** ⭐ |
| SMOTE-Tomek |   76.74% |    76.62% | 76.74% |       76.64% |

### Fitur

| Balancing   | Accuracy | Precision | Recall |     F1-Score |
| ----------- | -------: | --------: | -----: | -----------: |
| None        |   83.33% |    85.10% | 83.33% | **82.22%** ⭐ |
| SMOTE       |   81.82% |    82.01% | 81.82% |       81.13% |
| Tomek-Link  |   81.82% |    82.73% | 81.82% |       80.79% |
| SMOTE-Tomek |   81.82% |    82.01% | 81.82% |       81.13% |

---

## Ringkasan Pengujian Kedua

| Aspek                | Metode Terbaik      | F1-Score |
| -------------------- | ------------------- | -------: |
| Gameplay & Storyline | Tomek-Link          |   84.05% |
| Aksesibilitas        | SMOTE / SMOTE-Tomek |   82.82% |
| Grafis & Performa    | Tomek-Link          |   77.86% |
| Fitur                | None                |   82.22% |
|                      |                     |          |
