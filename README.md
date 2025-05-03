---

# Dokumentasi Proyek: Analisis Attrition Perusahaan Jaya Jaya Maju

## 1. Deskripsi Proyek
Proyek ini bertujuan untuk menganalisis faktor-faktor yang memengaruhi tingkat keluar karyawan (*attrition*) di perusahaan **Jaya Jaya Maju**. Perusahaan ini menghadapi masalah tingkat keluar karyawan yang tinggi (lebih dari 10%) dari total lebih dari 1.000 karyawan.

### Tujuan Proyek
- Mengidentifikasi faktor-faktor yang memengaruhi attrition.
- Menyusun insight untuk mendukung pengambilan keputusan oleh tim HR.
- Membangun dashboard interaktif untuk memonitor metrik kunci.

---

## 2. Tahapan Proyek

### **A. Business Understanding**
Pada tahap ini, permasalahan bisnis didefinisikan:
- **Masalah**: Tingkat attrition yang tinggi (>10%).
- **Tujuan**: Menyusun strategi untuk mengurangi tingkat keluar karyawan.

---

### **B. Data Understanding**
Dataset yang digunakan diambil dari sumber eksternal melalui `pd.read_csv()` dan dilakukan eksplorasi awal:
- **Dataset**: Berisi 35 kolom seperti *Age*, *Attrition*, *MonthlyIncome*, *YearsAtCompany*, dan lainnya.
- **Eksplorasi Awal**:
  - Terdapat *missing values* di kolom `Attrition` yang perlu ditangani.
  - Fitur-fitur seperti `Age`, `MonthlyIncome`, dan `YearsAtCompany` mungkin berpengaruh terhadap tingkat attrition.

---

### **C. Data Preparation**
1. **Penghapusan Missing Values**: Baris dengan nilai kosong pada kolom `Attrition` dihapus.
2. **Transformasi Data**: 
   - Kolom `Attrition` dipastikan bertipe numerik (`1` untuk keluar, `0` untuk tetap bekerja).
   - Fitur-fitur numerik yang relevan dipilih untuk pemodelan.
3. **Pemisahan Dataset**:
   - Data dibagi menjadi data latih dan data uji (80:20) dengan stratifikasi.

---

### **D. Exploratory Data Analysis (EDA)**
1. **Analisis Korelasi**:
   - Matriks korelasi dihitung untuk fitur numerik.
   - Heatmap digunakan untuk visualisasi.
   - Insight: Fitur dengan korelasi tinggi terhadap `Attrition` menjadi kandidat utama untuk pemodelan.
2. **Visualisasi Pairwise**:
   - Pairplot dibuat untuk melihat hubungan antar fitur numerik dengan `Attrition`.

---

## 3. Action Items dan Rencana Lanjutan

### **A. Action Items**
1. **Data Cleaning**:
   - Tangani *missing values* di kolom lain jika ditemukan.
   - Konversi tipe data untuk fitur kategorik sebelum pemodelan.
2. **Feature Engineering**:
   - Ciptakan fitur baru jika ada pola menarik dari EDA.
   - Hapus fitur dengan korelasi sangat tinggi untuk menghindari *multicollinearity*.
3. **Modeling**:
   - Gunakan model seperti Logistic Regression dan Random Forest.
   - Evaluasi model dengan metrik seperti *accuracy*, *confusion matrix*, dan lainnya.
4. **Dashboard Interaktif**:
   - Gunakan alat seperti Tableau atau Dash untuk membangun dashboard.

### **B. Rencana Lanjutan**
1. **Optimisasi Model**:
   - Lakukan *hyperparameter tuning* untuk meningkatkan performa model.
2. **Integrasi Dashboard**:
   - Integrasikan hasil analisis ke dalam dashboard untuk pemantauan real-time.
3. **Sosialisasi Hasil**:
   - Presentasikan hasil analisis dan rekomendasi kepada manajemen HR.

---

## 4. Insight Utama
- **Tingkat Keluar Karyawan**: Fitur seperti `Age`, `MonthlyIncome`, dan `YearsAtCompany` memiliki potensi sebagai prediktor utama.
- **Multikolinearitas**: Beberapa fitur memiliki korelasi tinggi; perlu dipertimbangkan untuk penghapusan atau kombinasi fitur.
- **Proporsi Data**: Stratifikasi memastikan distribusi `Attrition` antara data latih dan data uji tetap terjaga.

---

## 6. Referensi
- Dataset: [Dicoding Employee Data](https://raw.githubusercontent.com/dicodingacademy/dicoding_dataset/refs/heads/main/employee/employee_data.csv)
- Library: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

---
