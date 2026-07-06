# UAS-KecerdasanBuatan-Kelompok-17
kelompok 17

# 🎯 Proyek UAS Kecerdasan Buatan: Prediksi Keputusan Pembelian Klasifikasi Social Media Ads

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Focus-Machine%20Learning-orange.svg?style=for-the-badge)

Repositori ini disusun sebagai pemenuhan tugas **Ujian Akhir Semester (UAS) Mata Kuliah Kecerdasan Buatan / Artificial Intelligence**. Proyek ini mendemonstrasikan end-to-end proses implementasi *Machine Learning* untuk menyelesaikan permasalahan klasifikasi biner pada ranah pemasaran digital, yaitu memprediksi probabilitas seorang pengguna untuk membeli produk (*purchased*) setelah terpapar iklan media sosial berdasarkan atribut demografisnya.

---

## 📑 Daftar Isi
1. [Identitas Pengembang](#-identitas-pengembang)
2. [Alat dan Teknologi](#️-alat-dan-teknologi-tech-stack)
3. [Latar Belakang & Pemahaman Bisnis](#-latar-belakang--pemahaman-bisnis-business-understanding)
4. [Pemahaman Data](#-pemahaman-data-data-understanding)
5. [Metodologi Proyek](#-metodologi-proyek)
6. [Hasil dan Insight Utama](#-hasil-dan-insight-utama)
7. [Struktur Repositori](#-struktur-repositori)
8. [Panduan Eksekusi Program](#-panduan-eksekusi-program)
9. [Rencana Pengembangan](#-rencana-pengembangan-future-work)
10. [Referensi Ilmiah](#-referensi-ilmiah)

---

## 📌 Identitas Pengembang
* **Nama Lengkap:** [Masukkan Nama Anda]
* **NIM:** [Masukkan NIM Anda]
* **Kelas:** [Masukkan Kelas Anda]
* **Program Studi:** [Masukkan Prodi Anda, misal: Teknik Informatika]
* **Dosen Pengampu:** [Masukkan Nama Dosen Anda]

---

## 🛠️ Alat dan Teknologi (Tech Stack)
Proyek ini dibangun menggunakan bahasa pemrograman **Python** dengan pustaka (*libraries*) pengolahan data standar industri:
* **Pengolahan Data:** `Pandas`, `NumPy`
* **Visualisasi Data:** `Matplotlib`, `Seaborn`
* **Machine Learning:** `Scikit-Learn` (Model, Preprocessing, dan Evaluasi)
* **Environment:** `Jupyter Notebook` / `Google Colab`

---

## 💼 Latar Belakang & Pemahaman Bisnis (*Business Understanding*)
Dalam *digital marketing*, membuang-buang anggaran untuk menargetkan iklan kepada audiens yang tidak relevan (*ad-spend waste*) adalah masalah besar. Proyek ini memberikan solusi berupa sistem **Predictive Analytics**. Dengan memprediksi potensi pembelian pelanggan sebelum kampanye iklan dieksekusi, tim pemasar dapat menyaring audiens non-potensial, memfokuskan anggaran pada pengguna dengan probabilitas konversi tinggi, dan pada akhirnya meningkatkan *Return on Ad Spend* (ROAS).

---

## 📊 Pemahaman Data (*Data Understanding*)
Dataset yang digunakan adalah data publik anonim dari pengguna media sosial.
* **Sumber Data Asli:** [Kaggle - Social Network Ads Dataset](https://www.kaggle.com/datasets/d4rklucif3r/social-network-ads)
* **Format & Dimensi:** `.csv` | 400 Baris | 5 Kolom.
* **Deskripsi Fitur:**
  * `User ID`: Identitas unik (Dihapus saat pemrosesan).
  * `Gender`: Jenis kelamin pengguna (Kategorikal).
  * `Age`: Usia pengguna dalam tahun (Numerik).
  * `EstimatedSalary`: Estimasi gaji tahunan dalam USD (Numerik).
  * `Purchased` **[TARGET]**: Keputusan akhir (Biner: `0` = Tidak Membeli, `1` = Membeli).

---

## ⚙️ Metodologi Proyek

1. **Eksplorasi Data (EDA):** Menganalisis distribusi data, mendeteksi *outlier*, dan melihat korelasi antar fitur menggunakan visualisasi plot.
2. **Pra-Pemrosesan Data (*Data Preparation*):** * *Encoding* variabel `Gender` menjadi numerik.
   * *Feature Scaling* menggunakan `StandardScaler` agar algoritma tidak bias terhadap nilai gaji yang jauh lebih besar dari usia.
   * Pemisahan data menjadi **75% Training Data** dan **25% Testing Data**.
3. **Pemodelan AI (*Modeling*):**
   * **K-Nearest Neighbors (KNN):** Dioptimalkan untuk menemukan pola kemiripan antar pengguna secara spasial.
   * **Decision Tree Classifier:** Digunakan untuk mendapatkan aturan klasifikasi yang *explainable* dan mudah dibaca oleh tim bisnis.
4. **Evaluasi Model:** Model diukur menggunakan *Confusion Matrix* (Akurasi, Presisi, Recall, dan F1-Score) untuk memastikan tidak terjadi ketimpangan prediksi (*overfitting*).

---

## 💡 Hasil dan Insight Utama
Meskipun hasil komprehensif tertulis pada laporan lengkap, temuan utama dari proyek ini menunjukkan bahwa:
1. **Fitur Paling Berpengaruh:** `Age` (Usia) dan `EstimatedSalary` (Gaji) memiliki korelasi positif yang sangat kuat terhadap konversi pembelian. 
2. **Karakteristik Pembeli Utama:** Pengguna dengan usia di atas 40 tahun atau memiliki gaji di atas $70.000 mendominasi kelas "Membeli".
3. **Performa Model:** Implementasi algoritma terbukti mampu memprediksi target dengan tingkat akurasi yang memadai (di atas 85%), menjadikannya sangat layak untuk diintegrasikan sebagai filter otomatis pada sistem *Ad-Manager*.
