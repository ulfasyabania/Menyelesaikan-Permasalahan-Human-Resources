# Dokumentasi Proyek: **Menyelesaikan Permasalahan Human Resources** - ulfasyabania_dicoding

## Pendahuluan

### Deskripsi Proyek
Proyek ini merupakan bagian dari submission untuk kursus **Machine Learning Terapan**. Tujuan dari proyek ini adalah untuk **mengidentifikasi dan menyelesaikan permasalahan terkait Human Resources (HR)** dalam konteks perusahaan fiktif bernama **Jaya Jaya Maju** menggunakan pendekatan berbasis data dan machine learning.

Notebook ini memuat langkah-langkah untuk memproses data, melakukan analisis, hingga membangun model machine learning untuk mendukung pengambilan keputusan strategis dalam pengelolaan sumber daya manusia.

### Tujuan
1. Meningkatkan efisiensi pengelolaan sumber daya manusia.
2. Memprediksi potensi masalah dalam HR seperti tingkat turnover karyawan.
3. Memberikan rekomendasi actionable berdasarkan hasil analisis data.

---

## Detail Implementasi

### 1. Business Understanding
- **Tujuan Analisis**:
  - Mengidentifikasi tren turnover karyawan.
  - Menganalisis faktor-faktor yang memengaruhi tingkat kepuasan kerja.
- **Tools yang Digunakan**:
  - Visualisasi data menggunakan matplotlib dan seaborn.
  - Statistik deskriptif untuk memahami karakteristik data.

### 2. Data Understanding
- **Sumber Data**: Dataset internal perusahaan Jaya Jaya Maju.
  https://raw.githubusercontent.com/dicodingacademy/dicoding_dataset/refs/heads/main/employee/employee_data.csv

### 3. Data Preparation
- **Langkah-Langkah:**
  - Melakukan eksplorasi data untuk memahami distribusi dan pola.
  - Menangani nilai-nilai yang hilang (missing values).
  - Encoding data kategori menjadi format numerik.
  - Normalisasi dan standarisasi data untuk memastikan performa optimal model.
  - Exploratory Data Analysis (EDA)

### 3. Modeling Machine Learning
- **Model yang Dibangun**:
  - Model klasifikasi untuk memprediksi tingkat turnover karyawan.
  - Algoritma yang digunakan: Random Forest, Logistic Regression, dan XGBoost.
- **Evaluasi Model**:
  - Menggunakan metrik seperti akurasi, precision, recall, dan F1-score.
  - Memilih model terbaik berdasarkan performa di data validasi.

### 4. Deployment
- **Output**:
  - Dashboard Interaktif dengan Looker Studio.
    URL: https://lookerstudio.google.com/reporting/75f90d63-0782-44e5-b46c-22eded578b1a
  - Model siap digunakan untuk memprediksi masalah HR.
  - Rekomendasi tindakan untuk pemangku keputusan.

---

## 5. Kesimpulan dan Rekomendasi Strategis untuk HRD Jaya Jaya Maju
Berdasarkan hasil **analisis data dan model machine learning (XGBoost, Random Forest, Logistic Regression)**, ditemukan beberapa **pola signifikan** yang mempengaruhi **Attrition (tingkat keluar karyawan)** di Jaya Jaya Maju. Untuk membantu HR dalam **pengambilan keputusan strategis**, berikut **kesimpulan dan rekomendasi yang lebih mendalam**.

---

### **Kesimpulan: Faktor-Faktor yang Berkontribusi terhadap Tingginya Attrition**
Dari **analisis feature importance menggunakan XGBoost**, ditemukan bahwa **lima faktor utama** yang memengaruhi keputusan keluar karyawan adalah:

### **1. Age (Usia Karyawan)**
- **Usia menjadi faktor terkuat dalam prediksi attrition**. Karyawan yang lebih muda **(di bawah 35 tahun)** memiliki tingkat keluar lebih tinggi dibandingkan karyawan senior.
- Ini bisa disebabkan oleh **kurangnya kesempatan karier**, paket kompensasi yang tidak menarik bagi generasi muda, atau keinginan mereka untuk mengeksplorasi pekerjaan baru.

### **2. MonthlyIncome (Pendapatan Bulanan)**
- **Pendapatan memiliki dampak signifikan terhadap keputusan keluar**. Karyawan dengan pendapatan rendah lebih berisiko untuk meninggalkan perusahaan.
- Karyawan yang tetap bekerja memiliki pendapatan rata-rata lebih tinggi dibandingkan mereka yang keluar.

### **3. YearsAtCompany dan TotalWorkingYears**
- Masa kerja juga berpengaruh: **semakin lama seseorang bekerja di perusahaan, semakin kecil kemungkinan mereka keluar**.
- Namun, jika masa kerja panjang **tanpa pertumbuhan karier**, ini bisa meningkatkan risiko attrition.

### **4. YearsSinceLastPromotion**
- **Karyawan yang sudah lama bekerja tetapi belum mendapatkan promosi lebih cenderung keluar**.
- Ini menandakan bahwa kurangnya kesempatan untuk naik jabatan menjadi faktor utama penyebab resign.

### **5. Job Role dan Departemen**
- **Sales dan Customer Service memiliki tingkat keluar yang lebih tinggi**, dibandingkan departemen seperti **Engineering dan Research & Development**.
- Kemungkinan penyebabnya adalah **tingkat tekanan pekerjaan yang lebih tinggi**, target penjualan yang sulit, atau kurangnya kepuasan kerja.

---

## **Rekomendasi Strategis untuk HRD Jaya Jaya Maju**
Berdasarkan analisis ini, tim HR **perlu menerapkan strategi berbasis data** untuk meningkatkan retensi karyawan dan mengurangi tingkat keluar.

### **1. Program Retensi Karyawan Muda**  
🔹 **Pelatihan dan mentorship intensif untuk karyawan baru** agar mereka merasa lebih terikat dengan perusahaan.  
🔹 **Meningkatkan keseimbangan kerja-kehidupan (work-life balance)** melalui fleksibilitas kerja dan tunjangan tambahan.  
🔹 **Memberikan kesempatan pengembangan karier lebih cepat** untuk karyawan di bawah 35 tahun.  

### **2. Kebijakan Kenaikan Gaji dan Insentif Berbasis Masa Kerja**  
🔹 **Menyesuaikan struktur gaji untuk mempertahankan karyawan dengan pendapatan lebih rendah**.  
🔹 **Menawarkan bonus berbasis loyalitas** bagi mereka yang tetap bekerja lebih dari 3 tahun.  
🔹 **Membangun sistem reward untuk karyawan dengan performa tinggi** guna meningkatkan motivasi kerja.  

### **3. Optimalisasi Sistem Promosi dan Pengembangan Karier**  
🔹 **Mengurangi masa tunggu untuk promosi bagi karyawan berprestasi**.  
🔹 **Menerapkan program job rotation** untuk menghindari stagnasi dalam peran yang sama.  
🔹 **Memastikan karyawan yang telah lama bekerja mendapatkan pengakuan dan peningkatan karier**.  

### **4. Strategi HR Berdasarkan Model Prediksi (XGBoost & Dashboard Data)**  
🔹 **Menggunakan machine learning untuk mengidentifikasi karyawan yang berisiko keluar** lebih dini.  
🔹 **Mengembangkan dashboard interaktif** untuk memantau pola attrition secara real-time.  
🔹 **Mengintegrasikan analisis data dalam pengambilan keputusan HR**, bukan hanya berdasarkan intuisi.  

---

### **Kesimpulan Akhir**
- **Pendekatan berbasis data dan AI menunjukkan bahwa usia, gaji, dan jenjang karier adalah faktor utama dalam keputusan keluar karyawan.**  
- **HR dapat mengurangi attrition dengan strategi yang lebih terarah**, termasuk retensi karyawan muda, peningkatan kompensasi, dan promosi yang lebih cepat.  
- **Menggunakan model prediksi seperti XGBoost memungkinkan perusahaan untuk melakukan intervensi lebih awal terhadap karyawan yang berisiko keluar.**  

Jika strategi ini diterapkan, Jaya Jaya Maju dapat **meningkatkan loyalitas karyawan, mengurangi angka resign, dan menciptakan lingkungan kerja yang lebih stabil dan produktif**.


---

## Cara Menjalankan Proyek
1. Install dependencies yang diperlukan:
   ```bash
   pip install -r requirements.txt
   ```
3. Buka file notebook `Jaya_Jaya_Maju.ipynb` di Jupyter Notebook atau Jupyter Lab.
4. Jalankan setiap sel secara berurutan untuk mereproduksi hasil.

---
