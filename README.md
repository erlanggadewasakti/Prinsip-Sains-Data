# Prinsip Sains Data / Data Science Principles

[![GitHub](https://img.shields.io/badge/GitHub-Repository-blue?logo=github)](https://github.com/erlanggadewasakti/Prinsip-Sains-Data)

## 📚 Tentang / About

**[Bahasa Indonesia]**

Repository ini berisi materi pembelajaran tentang Prinsip-Prinsip Sains Data. Materi dirancang untuk memberikan pemahaman mendasar tentang konsep, teknik, dan praktik terbaik dalam bidang sains data.

**[English]**

This repository contains learning materials about Data Science Principles. The materials are designed to provide a fundamental understanding of concepts, techniques, and best practices in the field of data science.

## 🎯 Tujuan Pembelajaran / Learning Objectives

**[Bahasa Indonesia]**

Setelah menyelesaikan kursus ini, peserta diharapkan dapat:
- Memahami konsep dasar sains data dan perannya dalam pengambilan keputusan
- Menguasai proses dan metodologi dalam proyek sains data
- Menganalisis dan memvisualisasikan data dengan efektif
- Menerapkan teknik machine learning untuk memecahkan masalah dunia nyata
- Memahami aspek etika dan tanggung jawab dalam sains data

**[English]**

After completing this course, participants are expected to be able to:
- Understand basic data science concepts and their role in decision-making
- Master the processes and methodologies in data science projects
- Analyze and visualize data effectively
- Apply machine learning techniques to solve real-world problems
- Understand ethical aspects and responsibilities in data science

## 📖 Topik Pembelajaran / Course Topics

### 1. Pengenalan Sains Data / Introduction to Data Science
- Definisi dan ruang lingkup sains data
- Peran data scientist
- Siklus hidup proyek sains data
- Tools dan teknologi yang digunakan

### 2. Statistika dan Probabilitas / Statistics and Probability
- Statistika deskriptif
- Distribusi probabilitas
- Inferensi statistik
- Uji hipotesis

### 3. Pengumpulan dan Pembersihan Data / Data Collection and Cleaning
- Sumber data (databases, APIs, web scraping)
- Data wrangling
- Menangani missing values
- Deteksi dan penanganan outliers

### 4. Eksplorasi dan Visualisasi Data / Data Exploration and Visualization
- Exploratory Data Analysis (EDA)
- Teknik visualisasi data
- Dashboard dan reporting
- Storytelling dengan data

### 5. Machine Learning Dasar / Basic Machine Learning
- Supervised learning (klasifikasi dan regresi)
- Unsupervised learning (clustering)
- Feature engineering
- Model evaluation dan validation

### 6. Machine Learning Lanjutan / Advanced Machine Learning
- Ensemble methods
- Deep learning fundamentals
- Natural Language Processing (NLP)
- Time series analysis

### 7. Big Data dan Cloud Computing / Big Data and Cloud Computing
- Pengenalan big data
- Distributed computing
- Cloud platforms untuk data science
- Scalability considerations

### 8. Etika dan Praktik Terbaik / Ethics and Best Practices
- Privacy dan keamanan data
- Bias dalam data dan model
- Interpretability dan explainability
- Responsible AI

## 🔧 Prasyarat / Prerequisites

**[Bahasa Indonesia]**
- Pemahaman dasar pemrograman (Python direkomendasikan)
- Matematika dasar (aljabar, kalkulus)
- Statistika dasar (akan lebih baik)

**[English]**
- Basic programming knowledge (Python recommended)
- Basic mathematics (algebra, calculus)
- Basic statistics (preferred)

## 🚀 Instalasi dan Setup / Installation and Setup

### Requirements

```bash
# Python 3.8 atau lebih baru / Python 3.8 or newer
python --version

# Package manager
pip install --upgrade pip
```

### Recommended Libraries

```bash
# Data manipulation
pip install pandas numpy

# Visualization
pip install matplotlib seaborn plotly

# Machine learning
pip install scikit-learn

# Jupyter notebooks
pip install jupyter notebook

# Optional: Deep learning
pip install tensorflow pytorch
```

### Menggunakan Virtual Environment / Using Virtual Environment

**[Bahasa Indonesia]**
```bash
# Buat virtual environment
python -m venv venv

# Aktivasi (Windows)
venv\Scripts\activate

# Aktivasi (Linux/Mac)
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

**[English]**
```bash
# Create virtual environment
python -m venv venv

# Activate (Windows)
venv\Scripts\activate

# Activate (Linux/Mac)
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

## 📁 Struktur Repository / Repository Structure

```
Prinsip-Sains-Data/
│
├── README.md                 # File ini / This file
├── requirements.txt          # Dependencies Python
│
├── 01-introduction/          # Materi pengenalan
├── 02-statistics/            # Materi statistika
├── 03-data-wrangling/        # Pengolahan data
├── 04-visualization/         # Visualisasi data
├── 05-machine-learning/      # Machine learning dasar
├── 06-advanced-ml/           # Machine learning lanjutan
├── 07-big-data/              # Big data & cloud
├── 08-ethics/                # Etika & praktik terbaik
│
├── datasets/                 # Dataset untuk praktik
├── projects/                 # Project assignments
└── resources/                # Sumber belajar tambahan
```

## 💻 Cara Menggunakan / How to Use

**[Bahasa Indonesia]**

1. Clone repository ini:
   ```bash
   git clone https://github.com/erlanggadewasakti/Prinsip-Sains-Data.git
   ```

2. Masuk ke direktori:
   ```bash
   cd Prinsip-Sains-Data
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Mulai dengan modul pertama di folder `01-introduction/`

5. Ikuti materi secara berurutan atau sesuai kebutuhan

**[English]**

1. Clone this repository:
   ```bash
   git clone https://github.com/erlanggadewasakti/Prinsip-Sains-Data.git
   ```

2. Navigate to directory:
   ```bash
   cd Prinsip-Sains-Data
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Start with the first module in `01-introduction/` folder

5. Follow materials sequentially or as needed

## 📚 Sumber Belajar / Learning Resources

### Buku / Books
- "Python for Data Analysis" by Wes McKinney
- "Introduction to Statistical Learning" by James, Witten, Hastie, Tibshirani
- "Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow" by Aurélien Géron

### Online Courses
- [Coursera: Data Science Specialization](https://www.coursera.org/specializations/jhu-data-science)
- [edX: Data Science MicroMasters](https://www.edx.org/micromasters/data-science)
- [Kaggle Learn](https://www.kaggle.com/learn)

### Websites
- [Towards Data Science](https://towardsdatascience.com/)
- [Analytics Vidhya](https://www.analyticsvidhya.com/)
- [KDnuggets](https://www.kdnuggets.com/)

## 🤝 Kontribusi / Contributing

**[Bahasa Indonesia]**

Kontribusi sangat diterima! Jika Anda ingin berkontribusi:

1. Fork repository ini
2. Buat branch baru (`git checkout -b feature/AmazingFeature`)
3. Commit perubahan Anda (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5. Buat Pull Request

**[English]**

Contributions are welcome! If you want to contribute:

1. Fork this repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Create a Pull Request

## 📧 Kontak / Contact

Erlangga Dewasa Sakti - [@erlanggadewasakti](https://github.com/erlanggadewasakti)

Project Link: [https://github.com/erlanggadewasakti/Prinsip-Sains-Data](https://github.com/erlanggadewasakti/Prinsip-Sains-Data)

## 📝 Lisensi / License

Materi dalam repository ini tersedia untuk tujuan pembelajaran. Silakan merujuk ke file LICENSE untuk informasi lebih lanjut.

Materials in this repository are available for educational purposes. Please refer to the LICENSE file for more information.

## ⭐ Dukungan / Support

Jika repository ini bermanfaat, silakan berikan ⭐️!

If you find this repository helpful, please give it a ⭐️!

---

**Happy Learning! / Selamat Belajar!** 🎓📊🤖