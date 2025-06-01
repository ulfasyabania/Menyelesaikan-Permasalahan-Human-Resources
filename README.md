# Proyek Akhir: Menyelesaikan Permasalahan Manajemen Karyawan di Jaya Jaya Maju

## Business Understanding

**Latar Belakang Bisnis**  
Jaya Jaya Maju merupakan salah satu perusahaan multinasional yang telah berdiri sejak tahun 2000, dan kini mempekerjakan lebih dari 1000 karyawan yang tersebar di seluruh penjuru negeri. Walaupun telah mencapai skala besar, perusahaan ini masih menghadapi tantangan serius dalam mengelola karyawan. Salah satu indikator utama dari permasalahan tersebut adalah tingginya attrition rate—yakni rasio karyawan yang keluar dibandingkan dengan total karyawan—yang mencapai lebih dari 10%. Masalah ini memiliki dampak besar terhadap stabilitas operasional dan produktivitas perusahaan.

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
- Data karyawan yang berisi informasi pribadi, riwayat kerja, performa, dan feedback.
- Data historis terkait attrition, kompensasi, dan kepuasan karyawan.  
*(Dataset lengkap dapat diunduh melalui tautan yang disediakan oleh pihak Jaya Jaya Maju.)*

**Setup Environment:**  
- **Bahasa Pemrograman:** Python 3.x  
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
[Link Dashboard Jaya Jaya Maju](https://example.com/dashboard)  
*(Ganti dengan link akses aktual jika sudah tersedia.)*

## Conclusion

Dari hasil analisis data dan model prediktif yang telah dikembangkan, dapat disimpulkan bahwa:
- **Faktor-Faktor Kunci:** Beberapa faktor, seperti kepuasan kerja yang rendah, kompensasi yang kurang kompetitif, dan kurangnya peluang pengembangan karir, memiliki pengaruh signifikan terhadap tingginya attrition di Jaya Jaya Maju.
- **Model Prediktif Efektif:** Model machine learning yang dibangun (termasuk Logistic Regression, Random Forest, dan XGBoost) berhasil mengidentifikasi karyawan berisiko tinggi attrition, meskipun diperlukan optimalisasi lebih lanjut (misalnya, penyesuaian threshold dan penanganan data imbalanced) untuk meningkatkan sensitivitas model, terutama pada kelas minoritas.
- **Dashboard sebagai Alat Monitoring:** Business dashboard yang telah dibuat memberikan alat monitoring yang komprehensif, memungkinkan manajer HR untuk melakukan evaluasi dan pengambilan keputusan berbasis data secara real time.

## Rekomendasi Action Items

Untuk menurunkan attrition rate dan meningkatkan retensi karyawan, disarankan agar perusahaan melakukan beberapa langkah strategis, antara lain:
- **Action Item 1:** Tingkatkan program kesejahteraan karyawan dan sistem reward yang didasarkan pada kinerja dan loyalitas, serta menawarkan kesempatan pengembangan karir yang lebih baik.  
- **Action Item 2:** Optimalkan struktur kompensasi agar lebih kompetitif dengan benchmark industri, melalui survey dan analisis perbandingan dengan perusahaan sejenis.  
- **Action Item 3:** Implementasikan penggunaan dashboard secara rutin untuk memonitor indikator-indikator utama, sehingga intervensi dapat dilakukan secara proaktif berdasarkan insight data yang diperoleh.

---
