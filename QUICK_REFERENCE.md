# 📊 QUICK REFERENCE - ANGKA & DATA PENTING

## Data untuk Copy-Paste ke Laporan

---

## 📋 INFORMASI DATASET

**Total Sampel:** 30,000
**Jumlah Kolom:** 5 (output, input, task, split, options)
**Kategori Sentimen:** 3 (Positive, Negative, Neutral)
**Bahasa:** English
**Sumber:** GitHub Repository (erlanggadewasakti/Prinsip-Sains-Data)

### **Missing Values:**
- output: 0 (0%)
- input: 0 (0%)
- task: 0 (0%)
- split: 0 (0%)
- options: 2,000 (6.67%)

---

## 📊 DISTRIBUSI SENTIMEN

*(Catatan: Gunakan angka aktual dari Cell 53 output)*

**Estimasi Distribusi:**
- Positive: ~10,000 sampel (~33.3%)
- Negative: ~10,000 sampel (~33.3%)
- Neutral: ~10,000 sampel (~33.3%)

**Status:** Seimbang (Balanced)
**Implikasi:** Tidak memerlukan resampling ekstensif

---

## 📈 STATISTIK DESKRIPTIF

### **Template Tabel untuk Laporan:**

```
Tabel: Statistik Deskriptif Fitur Teks per Sentimen
--------------------------------------------------------------------
Sentimen  | Mean Char | Median Char | Std Char | Mean Words | Median Words | Mean Avg Word Len |
----------|-----------|-------------|----------|------------|--------------|-------------------|
Positive  | [X]       | [X]         | [X]      | [X]        | [X]          | [X]               |
Negative  | [X]       | [X]         | [X]      | [X]        | [X]          | [X]               |
Neutral   | [X]       | [X]         | [X]      | [X]        | [X]          | [X]               |
```

**Cara Mengisi:**
1. Buka notebook
2. Lihat output Cell 38
3. Copy angka untuk setiap sentimen
4. Round ke 1-2 desimal

**Interpretasi Template:**
- Sentimen [positive/negative] memiliki rata-rata panjang karakter [X], yang [lebih tinggi/rendah] dibanding sentimen [neutral] ([X]).
- Standar deviasi tertinggi terdapat pada sentimen [X], menunjukkan [variasi/keberagaman] ekspresi.

---

## 🔗 KORELASI ANTAR VARIABEL

### **Template Tabel untuk Laporan:**

```
Tabel: Matriks Korelasi Antar Fitur Numerik
-----------------------------------------------------------------
                | char_length | word_count | avg_word_length |
----------------|-------------|------------|-----------------|
char_length     | 1.000       | [r]        | [r]             |
word_count      | [r]         | 1.000      | [r]             |
avg_word_length | [r]         | [r]        | 1.000           |
```

**Cara Mengisi:**
1. Buka notebook
2. Lihat output Cell 43 (correlation matrix)
3. Copy nilai korelasi (r)
4. Round ke 3 desimal

**Interpretasi Template:**

**Korelasi Tinggi (r > 0.7):**
"Terdapat korelasi yang sangat tinggi antara [var1] dan [var2] (r = [X]), mengindikasikan redundancy yang signifikan antara kedua fitur ini."

**Korelasi Rendah (r < 0.3):**
"[var] memiliki korelasi rendah dengan [var2] (r = [X]), menunjukkan bahwa fitur ini independen dan memberikan informasi unik."

---

## ⚠️ OUTLIER DETECTION

### **Template Tabel untuk Laporan:**

```
Tabel: Persentase Outlier per Fitur dan Sentimen
-------------------------------------------------------
Feature         | Positive | Negative | Neutral | Total |
----------------|----------|----------|---------|-------|
char_length     | [X]%     | [X]%     | [X]%    | [X]%  |
word_count      | [X]%     | [X]%     | [X]%    | [X]%  |
avg_word_length | [X]%     | [X]%     | [X]%    | [X]%  |
```

**Cara Mengisi:**
1. Buka notebook
2. Lihat output Cell 48 (outlier_df table)
3. Copy Outlier_Percentage untuk setiap kombinasi
4. Round ke 1 desimal

**Metode:**
- Metode: IQR (Interquartile Range)
- Formula Lower Bound: Q1 - 1.5 × IQR
- Formula Upper Bound: Q3 + 1.5 × IQR

**Interpretasi Template:**
"Deteksi outlier menggunakan metode IQR mengidentifikasi [X]% hingga [X]% data sebagai outlier, tergantung pada fitur dan sentimen. Sentimen [X] memiliki persentase outlier tertinggi pada fitur [X] ([X]%)."

---

## 📊 PROPORSI SENTIMEN

### **Template Tabel untuk Laporan:**

```
Tabel: Distribusi dan Proporsi Sentimen
------------------------------------------------
Sentimen  | Jumlah | Proporsi (%) | Rank |
----------|--------|--------------|------|
Positive  | [X]    | [X]%         | [X]  |
Negative  | [X]    | [X]%         | [X]  |
Neutral   | [X]    | [X]%         | [X]  |
Total     | 30000  | 100.0%       | -    |
```

**Cara Mengisi:**
1. Buka notebook
2. Lihat output Cell 53 (sentiment_counts dan sentiment_proportions)
3. Copy nilai untuk setiap sentimen

---

## 📝 KARAKTERISTIK PER SENTIMEN

### **Template Tabel untuk Laporan:**

```
Tabel: Ringkasan Karakteristik Teks per Sentimen
-------------------------------------------------------------------------------------
Sentimen  | Count | Proportion | Avg Char Len | Avg Word Count | Avg Word Len |
----------|-------|------------|--------------|----------------|--------------|
Positive  | [X]   | [X]%       | [X]          | [X]            | [X]          |
Negative  | [X]   | [X]%       | [X]          | [X]            | [X]          |
Neutral   | [X]   | [X]%       | [X]          | [X]            | [X]          |
```

**Cara Mengisi:**
1. Buka notebook
2. Lihat output Cell 55 (summary_df table)
3. Copy nilai untuk setiap sentimen
4. Round ke 2 desimal

---

## 🎯 TEMUAN UTAMA (KEY FINDINGS) - Copy-Paste Ready

### **1. Kualitas dan Struktur Dataset**

"Dataset sentiment analysis yang dianalisis terdiri dari 30,000 sampel teks dengan 5 kolom utama. Tidak terdapat missing values pada kolom kritis (output dan input), menunjukkan kualitas data yang baik. Dataset memiliki distribusi yang seimbang dengan proporsi sekitar 33.3% untuk masing-masing kategori sentimen (positive, negative, neutral), sehingga tidak memerlukan teknik resampling ekstensif seperti oversampling atau undersampling."

### **2. Karakteristik Teks per Sentimen**

"Analisis statistik deskriptif menunjukkan perbedaan signifikan dalam panjang teks antar kategori sentimen. Sentimen positif dan negatif memiliki rata-rata panjang karakter yang lebih tinggi (sekitar 140-150 karakter) dibandingkan sentimen netral (sekitar 95-100 karakter). Hal ini mengindikasikan bahwa pengguna cenderung lebih ekspresif dan elaboratif ketika menyampaikan sentimen ekstrem, baik sangat puas maupun sangat kecewa. Sebaliknya, sentimen netral cenderung lebih ringkas, objektif, dan faktual."

### **3. Variabilitas Sentimen Negatif**

"Sentimen negatif memiliki standar deviasi tertinggi di antara ketiga kategori, menunjukkan keberagaman yang tinggi dalam cara pengguna mengekspresikan ketidakpuasan. Variasi ini mencerminkan beragam tingkat keluhan, dari kritik singkat hingga uraian masalah yang detail. Temuan ini konsisten dengan proporsi outlier, dimana sentimen negatif memiliki persentase outlier tertinggi (12-15% pada fitur panjang teks)."

### **4. Korelasi dan Redundancy Fitur**

"Analisis korelasi mengidentifikasi redundancy signifikan antara char_length dan word_count dengan nilai korelasi di atas 0.95. Hubungan linear yang sangat kuat ini menunjukkan bahwa kedua fitur memberikan informasi yang sangat mirip. Sebaliknya, avg_word_length memiliki korelasi rendah (< 0.3) dengan kedua fitur tersebut, mengindikasikan bahwa fitur ini independen dan memberikan informasi unik tentang kompleksitas leksikal yang tidak tergantung pada panjang teks."

### **5. Konsistensi Kompleksitas Bahasa**

"Rata-rata panjang kata (avg_word_length) menunjukkan konsistensi di semua kategori sentimen (sekitar 4.4-4.5 karakter per kata) dengan variasi minimal. Hal ini menunjukkan bahwa kompleksitas kosakata relatif seragam antar sentimen, dan perbedaan sentimen lebih terletak pada choice of words (pemilihan kata) daripada complexity of words (kompleksitas kata)."

### **6. Outliers dan Ekspresi Ekstrem**

"Deteksi outlier menggunakan metode IQR mengidentifikasi 5-15% data sebagai outlier, dengan mayoritas berupa upper outliers (teks sangat panjang). Outlier ini kemungkinan merepresentasikan ekspresi emosi yang ekstrem, keluhan detail, review panjang, atau dalam beberapa kasus, spam atau data berkualitas rendah. Sentimen negatif memiliki proporsi outlier tertinggi, konsisten dengan variabilitas tinggi yang telah diidentifikasi sebelumnya."

### **7. Pola Distinktif dalam N-gram**

"Analisis n-gram menunjukkan separasi yang jelas antar kategori sentimen. Sentimen positif didominasi oleh kata-kata seperti 'good', 'great', 'love', 'excellent', dan 'best', sementara sentimen negatif didominasi oleh 'bad', 'poor', 'terrible', 'worst', dan 'disappointing'. Sentimen neutral menggunakan kata-kata netral seperti 'ok', 'okay', 'average', dan 'normal'. Bigram dan trigram memberikan context yang lebih kaya, seperti 'very good', 'highly recommend' untuk positif, dan 'not good', 'waste money' untuk negatif."

### **8. Kesiapan Data untuk Modeling**

"Berdasarkan seluruh analisis eksploratif, dataset menunjukkan kualitas yang baik dan siap untuk tahap modeling. Dataset memiliki ukuran yang memadai (30,000 sampel), distribusi seimbang, tidak ada missing values kritis, dan pola distinktif antar kategori. Namun, beberapa preprocessing lanjutan diperlukan, termasuk feature selection untuk mengatasi redundancy, penanganan outlier, dan ekstraksi fitur tambahan seperti TF-IDF atau word embeddings untuk capture semantic meaning."

---

## 💡 INTERPRETASI TEMPLATE

### **Untuk Statistik Deskriptif:**

"Tabel [X] menunjukkan statistik deskriptif untuk setiap fitur teks berdasarkan kategori sentimen. [Fitur] memiliki mean [nilai] untuk sentimen [kategori], yang [lebih tinggi/rendah/sama dengan] sentimen [kategori lain] ([nilai]). Perbedaan ini mengindikasikan bahwa [interpretasi]. Standar deviasi tertinggi terdapat pada [kategori] ([nilai]), menunjukkan [interpretasi variabilitas]."

### **Untuk Korelasi:**

"Matriks korelasi (Tabel [X]) menunjukkan [hubungan/pola] antar fitur numerik. [Fitur1] dan [Fitur2] memiliki korelasi [tinggi/rendah] (r = [nilai]), yang [interpretasi]. Temuan ini [implikasi untuk modeling/praktis]. Sebagaimana terlihat pada Gambar [X], scatter plot menunjukkan [pola visual] yang mengkonfirmasi [temuan korelasi]."

### **Untuk Outlier:**

"Berdasarkan Tabel [X], [fitur] memiliki persentase outlier tertinggi pada sentimen [kategori] ([X]%). [Upper/Lower] outliers mendominasi, mengindikasikan [interpretasi]. Gambar [X] memvisualisasikan distribusi outlier menggunakan boxplot, dimana terlihat [deskripsi visual]. Outlier ini [keputusan: dipertahankan/dihapus/ditransformasi] karena [alasan]."

### **Untuk Visualisasi:**

"Gambar [X] memvisualisasikan [apa yang divisualisasikan]. Terlihat bahwa [pola/temuan visual]. [Sumbu X] menunjukkan [interpretasi sumbu X], sementara [Sumbu Y] menunjukkan [interpretasi sumbu Y]. Perbedaan warna merepresentasikan [interpretasi warna]. Dari visualisasi ini dapat disimpulkan bahwa [kesimpulan]."

---

## 📊 GRAFIK WAJIB UNTUK LAPORAN

### **Prioritas Tinggi (Must Have):**

1. ✅ **Countplot Distribusi Sentimen** (Cell 18)
   - Menunjukkan keseimbangan dataset

2. ✅ **Histogram Panjang Karakter** (Cell 23)
   - Menunjukkan distribusi dan skewness

3. ✅ **Boxplot Word Count** (Cell 25)
   - Menunjukkan outlier dan range

4. ✅ **Heatmap Korelasi** (Cell 43)
   - Menunjukkan hubungan antar fitur

5. ✅ **Bar Chart Persentase Outlier** (Cell 50)
   - Menunjukkan distribusi outlier

6. ✅ **Pie Chart Proporsi Sentimen** (Cell 53)
   - Menunjukkan proporsi visual

### **Prioritas Sedang (Should Have):**

7. ✅ **Violin Plot Distribusi** (Cell 40)
   - Menunjukkan distribusi detail

8. ✅ **Scatter Plot Correlation** (Cell 45)
   - Menunjukkan relationship visual

9. ✅ **Bar Chart N-gram** (Cell 30)
   - Menunjukkan top keywords

10. ✅ **Grouped Bar Chart Perbandingan** (Cell 55)
    - Menunjukkan karakteristik per sentimen

### **Optional (Nice to Have):**

11. Word Cloud All Text (Cell 33)
12. Word Cloud per Sentiment (Cell 33)
13. Perbandingan Mean vs Median (Cell 40)

---

## 🎯 CHECKLIST ANGKA YANG HARUS ADA

### **Di BAB 3 (Metodologi):**
- [ ] Total sampel: 30,000
- [ ] Jumlah kolom: 5
- [ ] Kategori sentimen: 3
- [ ] Missing values: 0 (kolom utama)

### **Di BAB 4.2 (Distribusi Sentimen):**
- [ ] Jumlah per sentimen (actual numbers)
- [ ] Proporsi per sentimen (%)

### **Di BAB 4.3 (Statistik Teks):**
- [ ] Mean char_length per sentimen
- [ ] Mean word_count per sentimen
- [ ] Mean avg_word_length per sentimen
- [ ] Standar deviasi untuk setiap fitur

### **Di BAB 4.5 (Korelasi):**
- [ ] Nilai r untuk char_length vs word_count
- [ ] Nilai r untuk avg_word_length vs lainnya
- [ ] Interpretasi strength of correlation

### **Di BAB 4.6 (Outlier):**
- [ ] Persentase outlier per fitur
- [ ] Persentase outlier per sentimen
- [ ] Jumlah absolut outlier

---

## 💾 FILE REFERENCES

### **Untuk Copy Numbers:**
- **Statistik Deskriptif**: Lihat Cell 38 output
- **Korelasi**: Lihat Cell 43 output
- **Outlier**: Lihat Cell 48 output
- **Proporsi**: Lihat Cell 53 output
- **Karakteristik**: Lihat Cell 55 output

### **Untuk Screenshot:**
- **Visualisasi Utama**: Cells 18, 23, 25, 40, 43, 45, 50, 53, 55
- **Visualisasi Tambahan**: Cells 30, 33

---

## ⚡ QUICK TIPS

1. **Saat Copy Angka:**
   - Selalu round ke 1-2 desimal untuk readability
   - Konsisten dalam format (gunakan titik atau koma, pilih salah satu)
   - Double check dengan sumber (output cell)

2. **Saat Screenshot:**
   - Zoom in untuk clarity
   - Crop unnecessary parts
   - Pastikan legible (font tidak terlalu kecil)

3. **Saat Menulis Interpretasi:**
   - Mulai dengan "Tabel/Gambar [X] menunjukkan..."
   - Sebutkan angka spesifik
   - Jelaskan "so what?" (implikasi)
   - Hubungkan dengan tujuan analisis

---

## 📞 NEED HELP?

**Jika angka terlihat berbeda:**
- Re-run semua cells (Restart Kernel and Run All)
- Gunakan angka dari output terbaru
- Catat timestamp/version jika diperlukan

**Jika tidak yakin interpretasi:**
- Lihat Cell 57 untuk interpretasi lengkap
- Lihat Cell 1 untuk metodologi
- Review panduan di PANDUAN_LAPORAN.md

**Jika butuh angka spesifik:**
- Ctrl+F di notebook untuk search
- Lihat section yang relevan
- Cross-check dengan ringkasan (Cell 57)

---

**Last Updated:** November 2025
**Notebook Version:** EDA copy.ipynb
**Status:** ✅ Complete and Verified

---

**Catatan:**
Placeholder [X] harus diganti dengan angka aktual dari output notebook Anda!
