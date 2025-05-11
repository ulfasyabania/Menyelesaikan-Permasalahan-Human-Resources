# **Menyelesaikan Permasalahan Human Resources Menggunakan Pendekatan Data Science** - ulfasyabania_dicoding

---

**Latar Belakang**

Di era digital yang semakin kompetitif, pengelolaan sumber daya manusia (SDM) telah mengalami transformasi signifikan melalui adopsi teknologi dan analisis data. Perusahaan tidak hanya dituntut untuk merekrut dan mempertahankan talenta terbaik, tetapi juga harus memahami secara mendalam faktor-faktor yang mendorong karyawan untuk meninggalkan perusahaan. Turnover atau attrition karyawan bukan hanya sekadar angka statistik, ia menjadi cerminan dari dinamika kepuasan, beban kerja, dan keseimbangan kehidupan kerja yang mendasari kesejahteraan organisasi.

Dalam konteks ini, penerapan Data Science di bidang Human Resources membuka peluang untuk menggali wawasan tersembunyi dari data operasional yang selama ini tidak tereksplorasi secara maksimal. Dengan mengintegrasikan berbagai atribut seperti profil demografis, kompensasi, dan metrik kepuasan kerja, penelitian ini berfokus pada identifikasi penyebab utama attrition karyawan dan bagaimana kekuatan faktor-faktor tersebut saling berinteraksi. Melalui pendekatan analisis statistik dan pemodelan prediktif, misalnya dengan Logistic Regression yang dikembangkan dan ditingkatkan melalui hyperparameter tuning, kita dapat mengurai kontribusi masing-masing variabel terhadap risiko turnover. Hasil analisis ini tidak hanya memberikan gambaran mendalam tentang profil karyawan yang berisiko keluar, tetapi juga menyajikan dasar bagi rekomendasi strategis untuk meningkatkan retensi dan menciptakan lingkungan kerja yang lebih seimbang dan kondusif.

Dataset yang digunakan, dengan 35 atribut mencakup aspek keuangan, demografi, dan pengalaman kerja, menyediakan gambaran komprehensif mengenai faktor-faktor yang mungkin mempengaruhi keputusan karyawan untuk bertahan atau meninggalkan perusahaan. Tantangan dalam pengolahan data, seperti penanganan missing value pada variabel kunci dan konversi fitur kategorikal, mencerminkan kompleksitas dunia nyata. Namun, melalui proses eksplorasi, pembersihan, dan pemodelan yang cermat, analisis ini mampu mengungkap insight kritis yang sebelumnya tersimpan dalam data. Inilah esensi dari pendekatan data-driven dalam HR Analytics, dirancang untuk mengubah tantangan turnover menjadi peluang strategis dalam pertumbuhan dan inovasi perusahaan.

---

**Business Understanding**

Dalam era persaingan global yang semakin ketat, manusia adalah aset yang paling berharga bagi perusahaan. Perusahaan modern tidak lagi hanya berfokus pada pertumbuhan produk atau inovasi teknologi, melainkan juga mengoptimalkan pengelolaan sumber daya manusia (SDM) untuk memenangkan persaingan pasar. Dalam konteks inilah, retensi dan kepuasan karyawan menjadi indikator kunci dari keberhasilan dan stabilitas jangka panjang. Tingginya angka turnover tidak hanya mengganggu stabilitas operasional, tetapi juga mengakibatkan biaya rekrutmen, pelatihan, dan penurunan produktivitas yang signifikan.

Perusahaan yang sadar akan pentingnya SDM mulai mengadopsi pendekatan berbasis data (data-driven) untuk mengungkap pola-pola yang tersembunyi di balik keputusan karyawan untuk meninggalkan perusahaan. Dengan memanfaatkan kumpulan data menyeluruh yang mencakup aspek demografi, kompensasi, dan kepuasan kerja, manajemen dapat mengidentifikasi faktor-faktor utama, seperti intensitas lembur, perjalanan dinas, dan integrasi pengalaman kerja, yang secara signifikan mempengaruhi tingkat attrition. Analisis mendalam ini memungkinkan tim HR untuk mengambil langkah-langkah proaktif: mulai dari perbaikan kebijakan kerja, penyesuaian struktur gaji, hingga inisiatif peningkatan kesejahteraan sehingga mampu mengurangi risiko turnover.

Bisnis ini menetapkan fondasi melalui data analytics yang tidak hanya menginformasikan tentang “siapa” yang berisiko keluar, tetapi juga “mengapa” hal itu terjadi. Pendekatan ini menciptakan peluang strategis untuk menurunkan biaya operasional, meningkatkan loyalitas, dan pada gilirannya, mengoptimalkan kinerja organisasi secara keseluruhan. Dengan transformasi digital yang terus berkembang, perusahaan dapat bergerak melampaui intuisi tradisional dan membuat keputusan yang lebih tepat dan terukur, sehingga membangun lingkungan kerja yang lebih stabil dan kompetitif dalam jangka panjang.

---

Latar belakang bisnis ini menggarisbawahi urgensi untuk mengoptimalkan manajemen SDM dengan menghasilkan insight melalui data science. Pendekatan ini tidak hanya menawarkan solusi teknis, tetapi juga mengubah paradigma bisnis untuk menciptakan nilai tambah yang signifikan melalui retensi karyawan yang lebih baik dan lingkungan kerja yang lebih responsif terhadap dinamika pasar.

---

### Cakupan Proyek

1. **Pengumpulan dan Pemahaman Data**
   - **Sumber Data:** Mengambil dataset HR yang lengkap dengan 35 atribut dari aspek keuangan, demografi, dan pengalaman kerja karyawan.
   - **Analisis Awal:** Melakukan pemeriksaan mendalam terhadap struktur data, distribusi statistik, missing value, dan konsistensi data guna memahami kondisi awal dan tantangan kualitas data yang ada.

2. **Pembersihan dan Praproses Data**
   - **Penanganan Missing Value:** Mengidentifikasi serta mengeliminasi atau mengimputasi missing value, terutama pada variabel target *Attrition* yang krusial untuk analisis prediktif.
   - **Encoding Data Kategorikal:** Mengubah variabel berbasis teks (misalnya, *BusinessTravel*, *Department*, *OverTime*, dll.) ke format numerik melalui teknik one-hot encoding untuk memastikan kompatibilitas dengan algoritma machine learning.
   - **Skalasi dan Normalisasi:** Menerapkan standardisasi atau normalisasi pada fitur-fitur numerik sehingga skala data seragam dan menghindari bias model.

3. **Eksploratory Data Analysis (EDA)**
   - **Visualisasi dan Analisis Deskriptif:** Melakukan visualisasi mendalam dengan histogram, boxplot, countplot, heatmap, dan pairplot untuk mengeksplorasi hubungan antar fitur dan melihat pola tersembunyi yang mungkin menjadi indikator utama terjadinya attrition.
   - **Analisis Statistik:** Menjalankan uji statistik (seperti uji chi-square) untuk mengonfirmasi signifikansi hubungan antar fitur dan keputusan karyawan.

4. **Feature Engineering dan Seleksi Fitur**
   - **Penciptaan Fitur Baru:** Mengolah dan mengkombinasikan beberapa variabel untuk membentuk fitur yang lebih representatif (misalnya, segmentasi berdasarkan usia atau tingkat pengalaman kerja) guna memperkuat sinyal prediktif.
   - **Analisis Feature Importance:** Menggunakan model prediktif seperti Logistic Regression—serta metode interpretasi canggih seperti SHAP—untuk mengidentifikasi fitur-fitur yang memberikan kontribusi signifikan terhadap risiko attrition.

5. **Pengembangan Model Prediktif**
   - **Pemodelan Machine Learning:** Membangun dan melatih model prediktif (Logistic Regression atau model berbasis ensemble) untuk memprediksi likelihood terjadinya attrition.
   - **Hyperparameter Tuning:** Mengoptimalkan model melalui teknik Grid Search atau Randomized Search dengan cross-validation agar mendapatkan performa terbaik.
   - **Evaluasi Model:** Mengukur kinerja model menggunakan metrik seperti accuracy, precision, recall, f1-score, confusion matrix, dan ROC-AUC.

6. **Insight Bisnis dan Rekomendasi Strategis**
   - **Interpretasi Hasil Model:** Menguraikan hasil analisis dan evaluasi model, menyoroti fitur-fitur kunci yang berpengaruh dalam keputusan karyawan untuk keluar.
   - **Rekomendasi Tindakan:** Menyusun strategi actionable untuk tim HR, misalnya, perbaikan kebijakan overtime, penyesuaian skala kompensasi, serta program kesejahteraan khusus yang dapat menurunkan tingkat turnover dan meningkatkan loyalitas karyawan.

7. **Pelaporan dan Dashboard Interaktif Menggunakan Looker Studio**  
   - **Integrasi Data:** Koneksikan data hasil praproses ke Google Data Studio (sekarang dikenal sebagai Looker Studio) melalui platform data warehouse seperti Google BigQuery atau lainnya.  
   - **Desain Dashboard:**  
     - **Visualisasi KPI Utama:** Menampilkan metrik kritis seperti attrition rate, rata-rata pendapatan bulanan, dan tren turnover secara real-time.  
     - **Visualisasi Interaktif:** Menggunakan diagram batang, diagram lingkaran, dan garis tren untuk menggambarkan distribusi attrition berdasarkan departemen, status OverTime, serta fitur lainnya.  
     - **Filter dan Interaktivitas:** Menyediakan opsi filter (misalnya, berdasarkan departemen, usia, atau job role) agar manajemen dapat melakukan drill-down pada insight yang lebih spesifik.  
   - **Dokumentasi Dashboard:** Menyusun laporan dan dokumentasi penggunaan dashboard yang memudahkan stakeholder dalam mengambil keputusan berbasis data.

6. **Dokumentasi Proyek dan Rekomendasi Bisnis**  
   - **Laporan Komprehensif:** Menyusun dokumentasi yang merangkum setiap tahap proyek, mulai dari pengumpulan data hingga analisis dan pemodelan.  
   - **Insight dan Rekomendasi Strategis:** Menyajikan hasil analisis beserta rekomendasi actionable—seperti perbaikan kebijakan lembur dan strategi retensi—untuk membantu perusahaan mengurangi turnover dan meningkatkan produktivitas.

---

Cakupan proyek ini dirancang untuk mengubah data mentah yang kompleks menjadi insight yang mendalam dan actionable. Pendekatan komprehensif ini, yang diakhiri dengan dashboard interaktif berbasis Looker Studio, akan memungkinkan tim manajemen untuk memantau secara real-time indikator kritis dan melakukan keputusan strategis yang tepat. 

---
Berikut adalah contoh "Persiapan" proyek yang dioptimalkan dan disusun dengan gaya yang kuat—menekankan sumber data serta setup environment menggunakan Google Colab. Tulisan ini dirancang untuk memberikan fondasi yang utuh, jelas, dan siap pakai dalam mengidentifikasi penyebab utama attrition melalui analisis data yang komprehensif.

---

## Persiapan Proyek

### Sumber Data

Dalam proyek ini, menggunakan dataset HR yang sangat lengkap dan terverifikasi, yang diberikan oleh perusahaan **"Jaya Jaya Maju"**. Dataset ini terdiri dari 35 atribut yang mencakup:
- **Aspek Demografi:** Usia, Gender, Pendidikan, dan informasi personal lainnya.
- **Aspek Finansial dan Kompensasi:** DailyRate, MonthlyIncome, MonthlyRate, dan variabel kompensasi lainnya.
- **Aspek Pengalaman dan Kinerja:** TotalWorkingYears, YearsAtCompany, JobRole, serta metrik kepuasan kerja dan keterlibatan karyawan.

Data ini diunduh langsung dari sumber tepercaya:
```python
data_url = "https://raw.githubusercontent.com/dicodingacademy/dicoding_dataset/refs/heads/main/employee/employee_data.csv"
```
Dengan sumber data yang begitu komprehensif, kita memiliki dasar yang kuat untuk menggali insight mendalam mengenai faktor-faktor yang mempengaruhi keputusan karyawan untuk bertahan atau meninggalkan perusahaan.

---

### Setup Environment

Google Colab merupakan platform yang ideal untuk proyek ini karena menyediakan lingkungan komputasi berbasis cloud yang interaktif dan lengkap. Berikut adalah langkah-langkah setup environment yang telah dioptimalkan untuk kolaborasi dan efisiensi:

1. **Google Colab sebagai Platform Utama**  
   Manfaatkan Google Colab untuk menjelajahi data secara interaktif, menjalankan pemodelan, dan membuat visualisasi secara langsung. Colab sudah menyediakan banyak library utama (seperti Pandas, NumPy, Matplotlib, dan Seaborn) yang sudah terinstal. Namun, untuk memastikan bahwa semua dependensi tersedia, jalankan sel berikut di awal notebook:

   ```python
   # Instal library tambahan (jika belum terpasang)
   !pip install shap scikit-learn
   ```

2. **Pengaturan Library dan Import Modul**  
   Impor semua library penting yang akan digunakan untuk pengambilan data, pembersihan data, analisis eksplorasi, dan pemodelan:
   
   ```python
   import pandas as pd
   import numpy as np
   import matplotlib.pyplot as plt
   import seaborn as sns
   from sklearn.model_selection import train_test_split
   from sklearn.linear_model import LogisticRegression
   from sklearn.metrics import accuracy_score, classification_report
   import shap

   # Set pengaturan visualisasi default untuk grafik
   %matplotlib inline
   sns.set(style="whitegrid")
   ```

3. **Muat dan Praproses Data**  
   Muat data langsung dari URL menggunakan Pandas, dan simpan data dalam variabel yang akan digunakan di seluruh notebook. Langkah ini memastikan bahwa data terbaru selalu diperbarui secara real-time dalam lingkungan Colab.
   
   ```python
   # Memuat dataset dari URL sumber data
   data = pd.read_csv(data_url)
   print("Dataset loaded with shape:", data.shape)
   ```

4. **Struktur Kode dan Dokumentasi**  
   Atur notebook dengan menggunakan markdown dan komentar yang mendetail di setiap sel. Ini akan memudahkan kolaborasi dan memastikan bahwa setiap tahap, mulai dari EDA, pembersihan data, hingga pemodelan, dapat ditelusuri secara logis dan transparan.

5. **Integrasi dengan Platform Pelaporan**  
   Meskipun analisis dilakukan di Google Colab, hasil akhir (termasuk visualisasi interaktif dan insight) akan diintegrasikan dengan Looker Studio untuk dashboard reporting real-time.

---

Dengan setup environment yang telah dioptimalkan di Google Colab dan sumber data yang komprehensif, proyek ini siap melangkah ke tahap selanjutnya. Dapat melakukan eksplorasi mendalam, membangun model prediktif, dan menyusun dashboard interaktif yang menyajikan insight strategis mengenai attrition karyawan.

---

