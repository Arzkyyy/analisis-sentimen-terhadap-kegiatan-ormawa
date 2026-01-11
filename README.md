# 📘 Analisis Sentimen Mahasiswa terhadap Kegiatan ORMAWA Menggunakan Deep Learning

## 👤 Tim
- Rafi Sidiqamrullah – 2230511132  
- M. Arizki – 2230511076  
- m.jaki sidik - 2230511123

Program Studi Teknik Informatika  
Fakultas Sains dan Teknologi  
Universitas Muhammadiyah Sukabumi  
2026  

---

## 1. Latar Belakang

Perkembangan Artificial Intelligence (AI) atau kecerdasan buatan saat ini mengalami kemajuan pesat dan telah dimanfaatkan dalam berbagai bidang, termasuk pendidikan. AI didefinisikan sebagai kemampuan sistem komputer untuk meniru kecerdasan manusia seperti memahami bahasa, belajar dari data, serta mengambil keputusan secara otomatis (Russell & Norvig, 2021).

Salah satu penerapan AI yang berkembang pesat adalah **sentiment analysis**, yaitu proses untuk mengidentifikasi dan mengklasifikasikan opini atau emosi dalam data teks (Pang & Lee, 2008). Seiring meningkatnya penggunaan media sosial, mahasiswa sering menyampaikan pendapat, kritik, maupun apresiasi terhadap berbagai kegiatan kampus, khususnya kegiatan Organisasi Mahasiswa (ORMAWA) seperti BEM, HIMA, dan UKM.

Namun, opini tersebut umumnya hanya menjadi arsip digital tanpa dianalisis secara sistematis. Padahal, informasi tersebut sangat berharga sebagai bahan evaluasi bagi pihak kampus. Oleh karena itu, proyek ini bertujuan untuk **menganalisis sentimen mahasiswa terhadap kegiatan ORMAWA menggunakan metode deep learning** sehingga dapat memberikan gambaran objektif terhadap persepsi mahasiswa dan membantu peningkatan kualitas kegiatan kemahasiswaan.

---

## 2. Pemrosesan Data

### 2.1 Pengumpulan Data
- Scraping mandiri dari:
  - Instagram
  - TikTok
- Kata kunci:
  - ORMAWA
  - BEM
  - HIMA
  - UKM Kampus
  - Kegiatan Mahasiswa
- Target data: **≥ 3.000 komentar**

### 2.2 Data Cleaning
- Hapus URL  
- Hapus angka & simbol  
- Hapus emoji  
- Lowercase  
- Hapus spasi berlebih  

### 2.3 Preprocessing
- Tokenisasi  
- Stopword removal  
- Normalisasi kata  
- Stemming (opsional)  

---

## 3. Skema Pelabelan Sentimen

| Label | Kategori | Deskripsi |
|--------|------------|--------------|
| 0 | Negatif | Kritik, keluhan |
| 1 | Netral | Informasi |
| 2 | Positif | Pujian |

**Metode:**
- Manual (sampling)
- Otomatis (rule-based)

---

## 4. Feature Engineering

- Tokenisasi
- Padding
- Embedding layer
- Konversi teks → numerik

---

## 5. Model dan Skema Pelatihan

### Arsitektur
**LSTM**
- Embedding
- LSTM
- Dropout
- Dense

**BiLSTM**
- Embedding
- BiLSTM
- Dropout
- Dense

### Skema Eksperimen

| Skema | Model | Split | Epoch | Optimizer |
|--------|--------|---------|----------|--------------|
| 1 | LSTM | 80:20 | 10 | Adam |
| 2 | BiLSTM | 80:20 | 15 | Adam |
| 3 | BiLSTM | 70:30 | 20 | RMSprop |

---

## 6. Hasil Evaluasi Model

**Metrik:**
- Accuracy
- Precision
- Recall
- F1-score

| Model | Akurasi |
|--------|-----------|
| LSTM | 87% |
| BiLSTM | 91% |

---

## 7. Inference / Prediksi

**Input:**
> "Kegiatan BEM kemarin sangat bermanfaat"

**Output:**
> Sentimen: Positif

---

## 8. Sitasi

1. Russell & Norvig (2021)  
2. Pang & Lee (2008)  
3. Kominfo RI  
4. Dataset scraping Instagram & TikTok  

