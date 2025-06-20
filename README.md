# 📊 Analisis Multivariat – Prediksi Status Pinjaman Nasabah
Dataset : https://www.kaggle.com/datasets/altruistdelhite04/loan-prediction-problem-dataset?select=train_u6lujuX_CVtuZ9i.csv
Repositori ini berisi implementasi tugas akhir mata kuliah **Analisis Multivariat** yang memanfaatkan teknik **Linear Discriminant Analysis (LDA)** dan **Regresi Logistik** untuk memprediksi status kelayakan pinjaman (Loan_Status) pada data pinjaman nasabah.

Proyek ini dilakukan menggunakan bahasa pemrograman **R** dan mencakup keseluruhan pipeline analisis: mulai dari pemahaman dataset, preprocessing lanjutan, eksplorasi data, pelatihan model, hingga evaluasi kinerja klasifikasi.

---

## 🎯 Tujuan

- Melakukan **pra-pemrosesan data** secara menyeluruh (imputasi, encoding, scaling, handling outlier, balancing)
- Membangun model **LDA** dan **Logistic Regression** untuk klasifikasi biner
- Melakukan **evaluasi model statistik** menggunakan metrik klasifikasi dan visualisasi ROC
- Menginterpretasikan hasil melalui **koefisien model**, **odds ratio**, dan **analisis signifikansi**

---

## 📁 Struktur Proyek

- `train_u6lujuX_CVtuZ9i.csv` – Dataset pelatihan
- `test_Y3wMUE5_7gLdaTN.csv` – Dataset pengujian
- `AnalisisMultivariat.Rmd` – File utama tugas akhir (RMarkdown)
- `README.md` – Deskripsi repositori

---

## 🛠 Teknologi & Package R

- `tidyverse`, `dplyr`, `readr` – manipulasi data
- `caret` – data partition, preprocessing, confusion matrix
- `fastDummies` – one-hot encoding
- `smotefamily` – balancing data menggunakan SMOTE
- `MASS` – Linear Discriminant Analysis (LDA)
- `pROC` – analisis ROC & AUC
- `biotools` – Box’s M test
- `ggplot2` – visualisasi data

---

## 🔍 Ringkasan Tahapan

### 📌 1. Pengenalan & Eksplorasi Data
- Melihat struktur dataset, mendeteksi missing values & duplikat
- Identifikasi tipe data numerik dan kategorikal

### 🧹 2. Preprocessing
- Imputasi nilai hilang (median & modus)
- Encoding variabel kategorikal (one-hot)
- Handling outlier (clipping IQR)
- SMOTE untuk penyeimbangan kelas target
- Scaling (standarisasi)

### 📊 3. EDA (Exploratory Data Analysis)
- Distribusi kelas target sebelum & sesudah preprocessing
- Boxplot outlier sebelum dan sesudah scaling
- Korelasi antar fitur numerik (heatmap)

### 📈 4. Linear Discriminant Analysis (LDA)
- Box’s M Test untuk homogenitas kovarians
- Uji signifikansi model
- Evaluasi: confusion matrix, accuracy, precision, recall, F1-score, ROC AUC
- Interpretasi: koefisien diskriminan, prior probability, mean per class

### 📉 5. Regresi Logistik
- Estimasi parameter dan uji signifikansi (parsial & simultan)
- Interpretasi Odds Ratio & Confidence Interval
- Evaluasi klasifikasi dan visualisasi: confusion matrix, ROC Curve

---

## 📌 Hasil Evaluasi (Contoh)

| Model              | Akurasi | Precision | Recall | AUC   |
|-------------------|---------|-----------|--------|-------|
| **LDA**           | 0.79    | 0.81      | 0.75   | 0.84  |
| **Logistic Reg.** | 0.80    | 0.83      | 0.76   | 0.86  |

> *Catatan: nilai-nilai di atas adalah contoh ilustratif. Silakan lihat output asli pada notebook.*

---

## 📊 Visualisasi

- Confusion Matrix (Heatmap)
- ROC Curve
- Boxplot outlier & distribusi fitur
- Barplot metrik klasifikasi

---



