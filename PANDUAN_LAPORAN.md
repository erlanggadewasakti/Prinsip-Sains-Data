# 📝 PANDUAN MENULIS LAPORAN EDA

## Panduan Cepat untuk Menyusun Laporan dari Notebook EDA

---

## 🎯 STRUKTUR LAPORAN YANG DISARANKAN

### **BAB 1: PENDAHULUAN**
**Panjang:** 2-3 halaman

**Isi:**
- Latar belakang sentiment analysis
- Motivasi dan pentingnya analisis sentimen
- Tujuan penelitian/analisis
- Ruang lingkup
- Dataset yang digunakan

**Ambil dari Notebook:**
- Cell 1 (Dokumentasi) - Bagian "Tujuan Analisis"
- Cell 1 - Bagian "Informasi Proyek"

---

### **BAB 2: TINJAUAN PUSTAKA** (Optional)
**Panjang:** 2-3 halaman

**Isi:**
- Definisi sentiment analysis
- Metode-metode EDA
- Penelitian terkait

---

### **BAB 3: METODOLOGI**
**Panjang:** 3-4 halaman

**Isi:**
- Deskripsi dataset
- Tools dan library yang digunakan
- Metode analisis:
  - Statistik deskriptif
  - Analisis korelasi
  - Deteksi outlier (IQR)
  - Visualisasi eksploratif
- Preprocessing steps

**Ambil dari Notebook:**
- Cell 1 - Bagian "Metodologi Analisis"
- Cell 1 - Bagian "Library yang Digunakan"
- Cell 7 (Load dataset - code)
- Cell 15 (Preprocessing - code dan output)

**Contoh Paragraf:**
```
Dataset yang digunakan dalam penelitian ini terdiri dari 30,000 sampel
teks dengan 3 kategori sentimen: positive, negative, dan neutral.
Data diambil dari repository GitHub dan dimuat menggunakan library pandas.
Preprocessing dilakukan dengan ekstraksi label sentimen dari kolom output
dan pembersihan teks input menjadi lowercase.
```

---

### **BAB 4: HASIL DAN PEMBAHASAN**
**Panjang:** 10-15 halaman

#### **4.1 Deskripsi Dataset**

**Isi:**
- Struktur dataset (kolom, tipe data)
- Missing values
- Statistik dasar

**Ambil dari Notebook:**
- Cell 12 (df.info() dan df.isnull().sum())

**Tabel untuk Laporan:**
```
Tabel 4.1 Struktur Dataset
-----------------------------------
Kolom     | Tipe Data | Non-Null  |
----------|-----------|-----------|
output    | object    | 30000     |
input     | object    | 30000     |
task      | object    | 30000     |
split     | object    | 30000     |
options   | object    | 28000     |
```

#### **4.2 Distribusi Sentimen**

**Isi:**
- Jumlah dan proporsi per sentimen
- Visualisasi countplot
- Interpretasi keseimbangan data

**Ambil dari Notebook:**
- Cell 18 (Sentiment Distribution plot)
- Cell 53 (Proporsi sentimen - output)

**Gambar untuk Laporan:**
- Screenshot countplot dari Cell 18

**Contoh Paragraf:**
```
Gambar 4.1 menunjukkan distribusi sentimen dalam dataset.
Dari total 30,000 sampel, distribusi relatif seimbang dengan
masing-masing kategori memiliki proporsi sekitar 33.3%.
Keseimbangan ini mengindikasikan bahwa dataset tidak memerlukan
teknik resampling seperti oversampling atau undersampling.
```

#### **4.3 Analisis Statistik Teks**

**Isi:**
- Perhitungan char_length, word_count, avg_word_length
- Distribusi per sentimen
- Histogram dan boxplot
- Interpretasi perbedaan antar sentimen

**Ambil dari Notebook:**
- Cell 21 (Statistik teks - output table)
- Cell 23 (Histogram visualizations)
- Cell 25 (Boxplot visualizations)
- Cell 38 (Descriptive statistics detail)

**Tabel untuk Laporan:**
```
Tabel 4.2 Statistik Deskriptif Fitur Teks per Sentimen
-----------------------------------------------------------------
Sentimen  | Avg Char | Avg Words | Avg Word Length | Std Char |
----------|----------|-----------|-----------------|----------|
Positive  | 150.2    | 25.3      | 4.5            | 75.8     |
Negative  | 145.7    | 24.1      | 4.5            | 82.3     |
Neutral   | 98.5     | 16.8      | 4.4            | 55.2     |
```

**Gambar untuk Laporan:**
- Screenshot histogram (Cell 23)
- Screenshot boxplot (Cell 25)
- Screenshot violin plot (Cell 40)

**Contoh Paragraf:**
```
Tabel 4.2 menunjukkan statistik deskriptif untuk setiap fitur teks
berdasarkan kategori sentimen. Sentimen positif dan negatif memiliki
rata-rata panjang karakter yang lebih tinggi (150.2 dan 145.7)
dibandingkan sentimen netral (98.5). Hal ini mengindikasikan bahwa
pengguna cenderung lebih ekspresif ketika menyampaikan sentimen ekstrem.

Gambar 4.2 memvisualisasikan distribusi panjang karakter menggunakan
histogram yang distacking berdasarkan sentimen. Terlihat bahwa distribusi
menunjukkan pola right-skewed dengan ekor panjang ke kanan,
mengindikasikan adanya beberapa teks yang sangat panjang (outliers).
```

#### **4.4 Analisis N-gram dan Word Cloud**

**Isi:**
- Top unigram, bigram, trigram per sentimen
- Word cloud visualization
- Keywords distinktif per sentimen

**Ambil dari Notebook:**
- Cell 30 (N-gram analysis - bar charts)
- Cell 33 (Word clouds)
- Cell 57 Section F (N-gram insights)

**Gambar untuk Laporan:**
- Screenshot bar chart n-grams (pilih beberapa yang representatif)
- Screenshot word clouds (all + per sentiment)

#### **4.5 Analisis Korelasi**

**Isi:**
- Matriks korelasi antar fitur
- Heatmap visualization
- Interpretasi hubungan antar variabel
- Implikasi untuk feature selection

**Ambil dari Notebook:**
- Cell 43 (Correlation matrix - output dan heatmap)
- Cell 45 (Scatter plots)
- Cell 57 Section C (Correlation insights)

**Tabel untuk Laporan:**
```
Tabel 4.3 Matriks Korelasi Antar Fitur Numerik
---------------------------------------------------------
              | char_length | word_count | avg_word_length |
--------------|-------------|------------|-----------------|
char_length   | 1.000       | 0.976      | 0.245           |
word_count    | 0.976       | 1.000      | 0.189           |
avg_word_len  | 0.245       | 0.189      | 1.000           |
```

**Gambar untuk Laporan:**
- Screenshot heatmap (Cell 43)
- Screenshot scatter plots (Cell 45)

**Contoh Paragraf:**
```
Tabel 4.3 menunjukkan matriks korelasi antar fitur numerik.
Terdapat korelasi yang sangat tinggi antara char_length dan word_count
(r = 0.976), mengindikasikan redundancy yang signifikan.
Sebaliknya, avg_word_length memiliki korelasi rendah dengan kedua
fitur tersebut (r < 0.3), menunjukkan bahwa fitur ini independen
dan memberikan informasi unik.

Gambar 4.X memvisualisasikan hubungan ini melalui scatter plot.
Terlihat pola linear yang jelas antara char_length dan word_count,
sementara avg_word_length tersebar tanpa pola yang jelas.
Temuan ini penting untuk feature engineering, dimana kita dapat
memilih salah satu dari char_length atau word_count untuk menghindari
multicollinearity dalam modeling.
```

#### **4.6 Identifikasi Outlier**

**Isi:**
- Metode IQR
- Persentase outlier per fitur dan sentimen
- Visualisasi boxplot dengan outliers
- Interpretasi dan implikasi outlier

**Ambil dari Notebook:**
- Cell 48 (Outlier detection - output table)
- Cell 50 (Outlier visualization)
- Cell 57 Section D (Outlier insights)

**Tabel untuk Laporan:**
```
Tabel 4.4 Persentase Outlier per Fitur dan Sentimen
---------------------------------------------------
Feature         | Positive | Negative | Neutral |
----------------|----------|----------|---------|
char_length     | 8.2%     | 12.5%    | 6.3%    |
word_count      | 8.5%     | 12.1%    | 6.7%    |
avg_word_length | 5.1%     | 6.8%     | 4.2%    |
```

**Gambar untuk Laporan:**
- Screenshot bar chart persentase outlier (Cell 50)
- Screenshot boxplot dengan outliers (Cell 50)

**Contoh Paragraf:**
```
Deteksi outlier menggunakan metode IQR mengidentifikasi 5-15% data
sebagai outlier, tergantung pada fitur dan sentimen. Tabel 4.4 menunjukkan
bahwa sentimen negatif memiliki persentase outlier tertinggi,
terutama pada fitur char_length (12.5%) dan word_count (12.1%).
Hal ini mengindikasikan bahwa sentimen negatif memiliki variasi
yang lebih besar dalam panjang teks.

Mayoritas outlier berupa upper outliers (teks sangat panjang),
yang kemungkinan merepresentasikan keluhan detail atau ekspresi
emosi ekstrem. Outlier pada avg_word_length menunjukkan penggunaan
kata-kata yang tidak biasa, baik sangat pendek maupun sangat panjang.
```

#### **4.7 Analisis Proporsi dan Karakteristik Sentimen**

**Isi:**
- Proporsi detail per sentimen
- Perbandingan karakteristik teks
- Pola distinktif per kategori

**Ambil dari Notebook:**
- Cell 53 (Pie chart dan bar chart)
- Cell 55 (Comparison characteristics)
- Cell 57 Section E (Proportion insights)

**Gambar untuk Laporan:**
- Screenshot pie chart (Cell 53)
- Screenshot grouped bar chart (Cell 55)

---

### **BAB 5: KESIMPULAN DAN REKOMENDASI**
**Panjang:** 2-3 halaman

#### **5.1 Kesimpulan**

**Isi:**
- Rangkuman temuan utama
- Jawaban atas tujuan analisis
- Konfirmasi hipotesis (jika ada)

**Ambil dari Notebook:**
- Cell 57 Section H (Kesimpulan Utama)

**Poin-poin Kesimpulan:**

1. **Kualitas Dataset**
   - Dataset berkualitas dengan 30,000 sampel
   - Tidak ada missing values pada kolom kritis
   - Distribusi seimbang antar kelas sentimen

2. **Karakteristik Sentimen**
   - Sentimen positif dan negatif lebih ekspresif (teks lebih panjang)
   - Sentimen netral lebih ringkas dan objektif
   - Sentimen negatif memiliki variasi tertinggi

3. **Hubungan Antar Fitur**
   - char_length dan word_count sangat berkorelasi (r > 0.95)
   - avg_word_length merupakan fitur independen
   - Korelasi konsisten antar semua sentimen

4. **Outliers**
   - 5-15% data teridentifikasi sebagai outlier
   - Sentimen negatif memiliki outlier terbanyak
   - Upper outliers (teks panjang) lebih dominan

5. **Kesiapan Modeling**
   - Dataset siap untuk tahap modeling
   - Perlu feature selection (char_length vs word_count)
   - Preprocessing lanjutan diperlukan

#### **5.2 Rekomendasi**

**Isi:**
- Feature engineering
- Preprocessing lanjutan
- Model selection
- Handling outliers

**Ambil dari Notebook:**
- Cell 57 Section I (Rekomendasi untuk Modeling)

**Rekomendasi Utama:**

1. **Feature Engineering**
   - Pilih word_count (drop char_length)
   - Pertahankan avg_word_length
   - Tambahkan TF-IDF atau word embeddings
   - Ekstrak sentiment-specific keywords

2. **Preprocessing**
   - Tokenization dan lemmatization
   - Remove punctuation dan special characters
   - Consider bigram/trigram untuk context

3. **Model Selection**
   - Baseline: Naive Bayes
   - Classical ML: Logistic Regression, SVM
   - Ensemble: Random Forest, XGBoost
   - Deep Learning: LSTM, BERT (untuk advanced)

4. **Outlier Handling**
   - Keep untuk robust model
   - Remove untuk optimal performance
   - Transform (log, normalize) sebagai alternatif

---

### **BAB 6: DAFTAR PUSTAKA**

**Contoh:**

[1] Bird, S., Klein, E., & Loper, E. (2009). Natural Language Processing with Python. O'Reilly Media.

[2] Liu, B. (2012). Sentiment Analysis and Opinion Mining. Morgan & Claypool Publishers.

[3] Pang, B., & Lee, L. (2008). Opinion Mining and Sentiment Analysis. Foundations and Trends in Information Retrieval, 2(1-2), 1-135.

---

## 📊 TEMPLATE TABEL DAN GAMBAR

### **Daftar Tabel yang Disarankan:**

1. Tabel 4.1: Struktur Dataset
2. Tabel 4.2: Statistik Deskriptif Fitur Teks per Sentimen
3. Tabel 4.3: Matriks Korelasi Antar Fitur Numerik
4. Tabel 4.4: Persentase Outlier per Fitur dan Sentimen
5. Tabel 4.5: Proporsi Sentimen dalam Dataset

### **Daftar Gambar yang Disarankan:**

1. Gambar 4.1: Distribusi Sentimen (Countplot)
2. Gambar 4.2: Histogram Panjang Karakter per Sentimen
3. Gambar 4.3: Boxplot Word Count per Sentimen
4. Gambar 4.4: Violin Plot Distribusi Fitur Teks
5. Gambar 4.5: Perbandingan Mean dan Median
6. Gambar 4.6: Top 20 Unigram per Sentimen (pilih salah satu)
7. Gambar 4.7: Word Cloud Keseluruhan
8. Gambar 4.8: Word Cloud per Sentimen
9. Gambar 4.9: Heatmap Korelasi
10. Gambar 4.10: Scatter Plot Matrix
11. Gambar 4.11: Persentase Outlier per Fitur
12. Gambar 4.12: Boxplot dengan Outliers
13. Gambar 4.13: Pie Chart Proporsi Sentimen
14. Gambar 4.14: Perbandingan Karakteristik Antar Sentimen

---

## ✍️ TIPS MENULIS LAPORAN

### **1. Bahasa dan Style**

✅ **DO:**
- Gunakan bahasa formal dan objektif
- Gunakan kalimat aktif: "Analisis menunjukkan..." bukan "Ditunjukkan oleh analisis..."
- Konsisten dalam istilah (char_length vs panjang karakter - pilih salah satu)
- Selalu interpretasikan angka, jangan hanya menyebutkan

❌ **DON'T:**
- Jangan gunakan bahasa casual
- Jangan copy-paste langsung dari notebook tanpa formatting
- Jangan gunakan cell ID atau technical terms tanpa penjelasan

### **2. Visualisasi**

✅ **DO:**
- Screenshot dengan resolusi tinggi
- Tambahkan caption yang jelas
- Referensikan dalam teks: "Gambar 4.1 menunjukkan..."
- Interpretasikan setiap visualisasi

❌ **DON'T:**
- Jangan sisipkan gambar tanpa penjelasan
- Jangan gunakan gambar blur atau terpotong

### **3. Angka dan Data**

✅ **DO:**
- Gunakan angka dari output notebook
- Round ke 2-3 desimal untuk readability
- Konsisten dalam format (%, absolut, etc.)
- Cantumkan sumber data

❌ **DON'T:**
- Jangan mengarang angka
- Jangan inkonsisten dalam pembulatan

### **4. Interpretasi**

✅ **DO:**
- Selalu berikan "so what?" → apa implikasinya?
- Hubungkan dengan tujuan analisis
- Gunakan contoh konkret
- Jelaskan dalam konteks bisnis/praktis

**Contoh Interpretasi:**

❌ **Buruk:**
"Sentimen positif memiliki mean char_length 150.2."

✅ **Baik:**
"Sentimen positif memiliki rata-rata panjang karakter 150.2, yang secara signifikan lebih tinggi dibandingkan sentimen netral (98.5). Hal ini mengindikasikan bahwa pengguna yang puas cenderung lebih detail dan ekspresif dalam menyampaikan pengalaman positif mereka, berbeda dengan sentimen netral yang lebih ringkas dan faktual."

---

## 📋 CHECKLIST SEBELUM SUBMIT

### **Konten:**

- [ ] Semua BAB lengkap (1-6)
- [ ] Setiap tabel memiliki caption dan nomor
- [ ] Setiap gambar memiliki caption dan nomor
- [ ] Semua gambar direferensikan dalam teks
- [ ] Interpretasi ada di setiap hasil
- [ ] Kesimpulan menjawab tujuan
- [ ] Rekomendasi actionable dan spesifik

### **Format:**

- [ ] Numbering konsisten (BAB, subbab, tabel, gambar)
- [ ] Font konsisten (heading vs body)
- [ ] Spacing konsisten
- [ ] Margin sesuai (biasanya 3-3-3-4 cm)
- [ ] Page numbering
- [ ] Header/footer (jika diperlukan)

### **Bahasa:**

- [ ] Tidak ada typo
- [ ] Tidak ada kalimat ambigu
- [ ] Istilah konsisten
- [ ] Grammar benar
- [ ] Ejaan sesuai PUEBI

### **Teknis:**

- [ ] Semua angka akurat (dari notebook)
- [ ] Formula matematika benar (jika ada)
- [ ] Referensi lengkap
- [ ] Lampiran (jika diperlukan)

---

## 🎯 TARGET PANJANG LAPORAN

**Minimum:** 20 halaman
**Ideal:** 25-30 halaman
**Maximum:** 35 halaman

**Komposisi:**
- BAB 1: 2-3 halaman
- BAB 2: 2-3 halaman (optional)
- BAB 3: 3-4 halaman
- BAB 4: 12-15 halaman (inti laporan)
- BAB 5: 2-3 halaman
- BAB 6: 1 halaman
- Lampiran: seperlunya

---

## 📞 QUICK ANSWERS

**Q: Berapa banyak tabel yang harus ada?**
A: Minimal 5-7 tabel. Pastikan setiap tabel informatif dan direferensikan dalam teks.

**Q: Berapa banyak gambar yang harus ada?**
A: Minimal 10-12 gambar. Pilih visualisasi yang paling representatif.

**Q: Apakah harus mencantumkan code?**
A: Tidak di bab utama. Jika perlu, masukkan ke lampiran dengan penjelasan.

**Q: Bagaimana format referensi tabel/gambar?**
A: "Tabel 4.1 menunjukkan..." atau "Sebagaimana terlihat pada Gambar 4.2..."

**Q: Apakah interpretasi harus panjang?**
A: Tidak harus, yang penting substantif. 2-4 kalimat per hasil sudah cukup.

**Q: Bagaimana jika angka di notebook berbeda sedikit karena re-run?**
A: Gunakan angka terakhir dari output yang ter-execute. Catat timestamp jika perlu.

---

## ✨ BONUS TIPS

### **Untuk Presentasi (Jika Ada):**

1. Buat slide ringkas (10-15 slides)
2. Fokus pada visualisasi (gunakan gambar dari notebook)
3. Highlight key findings
4. Siapkan backup slides untuk Q&A
5. Praktik presentasi dengan timer

### **Untuk Nilai Maksimal:**

1. ✅ Tambahkan insight yang deep (tidak cuma deskriptif)
2. ✅ Hubungkan dengan real-world application
3. ✅ Berikan rekomendasi yang actionable
4. ✅ Tunjukkan critical thinking
5. ✅ Format professional dan clean

---

**Semoga sukses dengan laporannya! 🎓✨**

Jika ada pertanyaan, review kembali notebook di bagian dokumentasi (Cell 1) dan ringkasan lengkap (Cell 57).
