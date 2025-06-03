# Proyek Akhir: Menyelesaikan Permasalahan Perusahaan Edutech

## Business Understanding

**Latar Belakang Bisnis**  
Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000, dan kini mempekerjakan lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. Walaupun telah mencapai skala besar, perusahaan ini masih menghadapi tantangan serius dalam mengelola karyawan. Salah satu indikator utama dari permasalahan tersebut adalah tingginya attrition rate yakni rasio karyawan yang keluar dibandingkan dengan total karyawan yang mencapai lebih dari 10%. Masalah ini memiliki dampak besar terhadap stabilitas operasional dan produktivitas perusahaan.

## Permasalahan Bisnis

Beberapa permasalahan bisnis yang harus diselesaikan adalah:
- **Tingginya Attrition Rate:** Melihat attrition rate yang tinggi (lebih dari 10%), perusahaan mengalami kebocoran sumber daya manusia yang signifikan.
- **Kesulitan dalam Mengidentifikasi Faktor Penyebab:** Belum ada pemahaman yang mendalam mengenai faktor-faktor spesifik yang memicu tingginya attrition, seperti kepuasan kerja, sistem kompensasi, dan budaya perusahaan.
- **Kurangnya Alat Monitoring yang Efektif:** Departemen HR belum memiliki sebuah sistem atau dashboard yang dapat memonitor secara real-time indikator-indikator kunci yang mempengaruhi retensi karyawan, sehingga menghambat intervensi yang cepat dan tepat.

## Cakupan Proyek

Proyek ini mencakup ruang lingkup berikut:
- **Analisis Data Karyawan:** Mengeksplorasi dan menganalisis data karyawan untuk mengungkap pola, tren, dan faktor-faktor yang berkontribusi terhadap tingginya attrition.
- **Pengembangan Model Prediktif:** Membangun dan mengoptimasi model machine learning untuk memprediksi kemungkinan karyawan yang berisiko keluar, sehingga memungkinkan intervensi yang lebih dini.
- **Pembuatan Business Dashboard:** Mengembangkan dashboard interaktif yang menampilkan metrik-metrik kunci dan insight dari analisis data, sehingga departemen HR dapat memonitor situasi secara real time.
- **Rekomendasi Strategis:** Menyusun rekomendasi berbasis data untuk mendukung kebijakan retensi karyawan dan menurunkan attrition rate.

## Persiapan

**Sumber Data:**
- Data historis terkait attrition, kompensasi, dan kepuasan karyawan.  
[*(Dataset lengkap dapat diunduh melalui tautan yang disediakan oleh pihak Perusahaan.)*](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee)

**Setup Environment:**  
- **Bahasa Pemrograman:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn, dan library pendukung lainnya.  
- **IDE/Platform:** Jupyter Notebook, Google Colab, atau VS Code.  
- **Tools Pendukung:** Git untuk version control dan Docker (jika diperlukan untuk deployment).

## Business Dashboard

Dashboard bisnis yang telah dikembangkan meliputi fitur-fitur berikut:
- **Monitoring Attrition Rate:** Visualisasi trend attrition rate dari waktu ke waktu, termasuk segmentasi berdasarkan divisi atau lokasi.
- **Analisis Faktor Penyebab:** Menampilkan grafik dan analisis statistik yang mengungkap hubungan antara faktor-faktor seperti kepuasan kerja, kompensasi, dan faktor lingkungan kerja dengan tingkat attrition.
- **Prediksi Risiko:** Hasil output dari model machine learning untuk mengidentifikasi karyawan yang memiliki risiko tinggi keluar, sehingga intervensi dapat dilakukan lebih dini.
- **Interaktivitas:** Dashboard yang interaktif memungkinkan manajer HR untuk mengklik dan menganalisis subset data tertentu, seperti melihat karyawan berdasarkan jabatan atau departemen.

Dashboard ini dapat diakses secara online melalui link berikut:  
[**Link Dashboard**](https://lookerstudio.google.com/reporting/75f90d63-0782-44e5-b46c-22eded578b1a)

## Conclusion

Berdasarkan hasil analisis data dan pengembangan model prediktif, dapat disimpulkan bahwa:

- **Faktor-Faktor Kunci:**  
  Analisis mendalam mengungkapkan bahwa variabel-variabel seperti usia, penghasilan bulanan, pola lembur (OverTime), beban kerja harian, dan total tahun kerja memainkan peranan penting dalam mempengaruhi risiko attrition. Hal ini menandakan bahwa karyawan pada kelompok tertentu —misalnya, dengan beban kerja tinggi atau gaji yang kurang kompetitif—memiliki kecenderungan lebih tinggi untuk keluar.

- **Model Prediktif Efektif:**  
  Tiga model machine learning yang telah dikembangkan (Logistic Regression, Random Forest, dan XGBoost) secara kolektif mampu mendeteksi karyawan berisiko attrition. Meskipun akurasi keseluruhan cukup memuaskan, performa pada kelas minoritas (karyawan yang keluar) masih perlu dioptimalkan melalui penyesuaian threshold, pengaturan parameter model (misalnya, penggunaan class_weight atau scale_pos_weight), serta penerapan teknik cost-sensitive learning.

- **Dashboard Bisnis sebagai Alat Monitoring:**  
  Business dashboard interaktif yang dikembangkan memberikan visualisasi real-time dari metrik utama, termasuk trend attrition dan faktor-faktor penyebabnya. Dashboard ini memungkinkan tim HR untuk melakukan analisis mendalam dan pengambilan keputusan dengan cepat berdasarkan insight yang ada.

---

## Rekomendasi Action Items

Untuk menurunkan attrition rate dan meningkatkan retensi karyawan, disarankan agar perusahaan mempertimbangkan langkah-langkah strategis berikut:

1. **Optimalisasi Program Kesejahteraan dan Pengembangan Karyawan:**  
   - Tingkatkan program kesejahteraan yang mencakup aspek kesehatan, keseimbangan kerja-hidup, dan dukungan psikologis.  
   - Tawarkan kesempatan pengembangan karir melalui pelatihan, mentoring, dan peningkatan kompetensi agar karyawan merasa dihargai dan memiliki prospek jangka panjang.

2. **Penyesuaian Struktur Kompensasi:**  
   - Lakukan survey dan analisis benchmarking untuk memastikan bahwa paket kompensasi dan benefit perusahaan kompetitif dibandingkan dengan industri sejenis.  
   - Pertimbangkan skema reward tambahan berbasis kinerja dan loyalitas untuk meningkatkan motivasi dan retensi karyawan.

3. **Penggunaan Dashboard Secara Rutin:**  
   - Implementasikan penggunaan business dashboard dalam kegiatan rutin HR untuk memonitor indikator utama secara real-time.  
   - Gunakan dashboard sebagai alat pengambil keputusan untuk segera mengidentifikasi dan mengintervensi area dengan risiko attrition tinggi.

4. **Optimasi Model Prediktif:**  
   - Lanjutkan eksplorasi teknik machine learning dengan penyesuaian threshold, cost-sensitive learning, serta pengaturan parameter tambahan untuk meningkatkan sensitivitas model terhadap kelas minoritas.  
   - Evaluasi performa model secara berkala dengan metrik seperti ROC-AUC, F1-score, dan precision-recall curve untuk memastikan model tetap akurat dalam mendeteksi karyawan berisiko.

5. **Pendekatan Proaktif dalam Manajemen SDM:**  
   - Gunakan insight dari analisis data untuk mengidentifikasi potensi permasalahan internal lainnya yang mungkin memicu turnover, sehingga intervensi tidak hanya reaktif tetapi juga preventif.  
   - Libatkan berbagai stakeholder (manajemen, tim HR, dan pimpinan lini) dalam menyusun strategi retensi yang berbasis data dan terus melakukan monitoring atas implementasi strategi tersebut.

---
