# Proyek Pertama: Menyelesaikan Permasalahan Human Resources

## Business Understanding
**Perusahaan:** Jaya Jaya Maju  
**Latar Belakang:**  
Jaya Jaya Maju adalah perusahaan multinasional yang berdiri sejak tahun 2000 dengan lebih dari 1.000 karyawan yang tersebar di seluruh negeri. Meskipun berkembang, perusahaan mengalami manajemen karyawan yang kurang optimal, sehingga menyebabkan attrition rate (rasio karyawan yang keluar) mencapai lebih dari 10%.

**Tujuan Proyek:**  
Menganalisis dataset karyawan untuk:
- Mengidentifikasi faktor-faktor yang mempengaruhi tingginya attrition rate.
- Menyusun insight yang dapat mendukung pengambilan keputusan di departemen HR.
- Membangun business dashboard yang memonitor metrik-metrik kunci.

---

## Permasalahan Bisnis
1. **Attrition Rate Tinggi:**  
   Kebanyakan karyawan mengundurkan diri, sehingga berdampak pada produktivitas dan biaya operasional perusahaan.

2. **Faktor Penyebab:**  
   Diperlukan analisis untuk mengetahui apakah faktor seperti usia, departemen, masa kerja, dan variabel demografi lainnya berpengaruh pada attrition rate.

---

## Cakupan Proyek
Proyek ini mencakup:
- Pengumpulan dan pembersihan data karyawan.
- Eksplorasi data untuk menemukan pola dan hubungan antar variabel.
- Pembuatan business dashboard sebagai alat monitoring.
- (Opsional) Pembuatan model prediksi menggunakan machine learning untuk mengidentifikasi karyawan yang berpotensi keluar.

---

## Setup Environment
- **Bahasa Pemrograman:** Python 3.x  
- **Library:** pandas, numpy, scikit-learn (jika membuat model)  
- **Tool BI:** Metabase  
- **Deployment:** Metabase dijalankan lokal menggunakan Docker.  
- **Perintah Docker (Metabase):**
  ```bash
  docker pull metabase/metabase:v0.46.4
  docker run -p 3000:3000 --name metabase metabase/metabase
