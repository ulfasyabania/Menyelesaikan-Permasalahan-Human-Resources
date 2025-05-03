# Membuat Model Machine Learning untuk Jaya Jaya Maju

## 1. Pendahuluan
Jaya Jaya Maju adalah perusahaan multinasional yang menghadapi tantangan dalam mengelola karyawan. Tingginya **attrition rate** menjadi masalah utama yang perlu dianalisis menggunakan pendekatan **machine learning**.

## 2. Dataset
Dataset yang digunakan berasal dari sumber berikut:
- **Nama Dataset**: Employee Data
- **Sumber**: [Dicoding Dataset](https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee)
- **Fitur Penting**:
  - `Age`: Usia karyawan
  - `MonthlyIncome`: Gaji bulanan
  - `TotalWorkingYears`: Total tahun bekerja
  - `YearsAtCompany`: Lama bekerja di perusahaan
  - `Attrition`: Status keluar atau tetap (0 = tetap, 1 = keluar)

---

## 3. Persiapan Data (Data Preparation & Feature Engineering)
Langkah-langkah preprocessing yang dilakukan:
```python
import pandas as pd
df = pd.read_csv("https://raw.githubusercontent.com/dicodingacademy/dicoding_dataset/refs/heads/main/employee/employee_data.csv")

# Menghapus nilai kosong
df.dropna(subset=['Attrition'], inplace=True)

# Konversi nilai kategorikal
df['Attrition'] = df['Attrition'].map({'Yes': 1, 'No': 0})
```

---

## 4. Eksplorasi Data dan Analisis Korelasi
### **Heatmap Korelasi Antar Fitur**
```python
import seaborn as sns
import matplotlib.pyplot as plt

df_numeric = df.select_dtypes(include=['number'])
corr_matrix = df_numeric.corr()

plt.figure(figsize=(10, 8))
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title("Korelasi Antar Fitur")
plt.show()
```

### **Distribusi Pendapatan berdasarkan Attrition**
```python
sns.boxplot(x=df['Attrition'], y=df['MonthlyIncome'])
plt.title("Distribusi MonthlyIncome berdasarkan Attrition")
plt.show()
```

---

## 5. Model Machine Learning
Model yang digunakan dalam analisis ini adalah **XGBoost** dan **Bayesian Optimization**

```python
from bayes_opt import BayesianOptimization
from sklearn.metrics import accuracy_score

def xgb_evaluate(n_estimators, max_depth, learning_rate):
    model = XGBClassifier(
        n_estimators=int(n_estimators),
        max_depth=int(max_depth),
        learning_rate=learning_rate,
        random_state=42
    )
    model.fit(X_train_scaled, y_train)
    accuracy = accuracy_score(y_test, model.predict(X_test_scaled))
    return accuracy

param_bounds = {'n_estimators': (50, 200), 'max_depth': (3, 10), 'learning_rate': (0.01, 0.2)}
optimizer = BayesianOptimization(f=xgb_evaluate, pbounds=param_bounds, random_state=42)
optimizer.maximize(init_points=5, n_iter=20)

print("Best Parameters from Bayesian Optimization:", optimizer.max)

```

---

## 6. Evaluasi Model
Hasil evaluasi model menggunakan **akurasi**:
```python
best_params = optimizer.max['params']

final_xgb = XGBClassifier(
    n_estimators=int(best_params['n_estimators']),
    max_depth=int(best_params['max_depth']),
    learning_rate=best_params['learning_rate'],
    random_state=42
)
final_xgb.fit(X_train_scaled, y_train)
y_pred_final = final_xgb.predict(X_test_scaled)

print("Final Model Accuracy:", accuracy_score(y_test, y_pred_final))

```

---

## 7. **SHAP Analysis (Explainability Model)**
SHAP digunakan untuk memahami fitur mana yang paling berpengaruh dalam keputusan model:
```python
import shap

explainer = shap.TreeExplainer(xgb_model)
shap_values = explainer.shap_values(X_test_scaled)

# Visualisasi SHAP
shap.summary_plot(shap_values, X_test_scaled)
```

```python
# Visualisasi SHAP untuk satu sampel
shap.force_plot(explainer.expected_value, shap_values[0], X_test_scaled[0])
```

---

## 8. **Dashboard Interaktif dengan Looker Studio**
Untuk membantu visualisasi hasil model dalam bentuk dashboard interaktif:
URL: https://lookerstudio.google.com/reporting/ab305826-1b90-4ded-ae78-a96b77d3a686

# Distribusi karyawan berdasarkan usia dan pendapatan
fig = px.scatter(df, x="Age", y="MonthlyIncome", color="Attrition", title="Distribusi Pendapatan vs Usia Berdasarkan Attrition")
fig.show()
```

```python
# Histogram Attrition
fig = px.histogram(df, x="Attrition", title="Distribusi Attrition")
fig.show()
```

---

## 9. ### **Kesimpulan dan Rekomendasi untuk HRD Jaya Jaya Maju**  
Berdasarkan analisis SHAP, kita dapat mengidentifikasi faktor-faktor yang paling berpengaruh terhadap prediksi karyawan keluar (**attrition**). Model Bayesian Optimization yang digunakan menunjukkan bahwa **MonthlyIncome, YearsAtCompany, dan YearsSinceLastPromotion** adalah fitur utama yang mempengaruhi keputusan resign.

---

## **Kesimpulan: Faktor-Faktor yang Berkontribusi terhadap Attrition**
1. **Pendapatan Bulanan (MonthlyIncome) Berpengaruh Signifikan**  
   - Karyawan dengan **pendapatan lebih rendah** memiliki kemungkinan lebih tinggi untuk keluar.  
   - SHAP menunjukkan bahwa **nilai MonthlyIncome yang tinggi** cenderung **mengurangi risiko attrition**.  

2. **Masa Kerja di Perusahaan (YearsAtCompany) dan Stagnasi Promosi (YearsSinceLastPromotion)**  
   - Karyawan dengan **masa kerja lama tetapi tanpa promosi** lebih rentan terhadap attrition.  
   - **Kurangnya pertumbuhan karier** menjadi salah satu pemicu utama resign.  

3. **TotalWorkingYears dan YearsInCurrentRole**  
   - SHAP menunjukkan bahwa **karyawan yang bekerja lama tetapi tetap dalam peran yang sama tanpa perubahan signifikan** lebih berisiko keluar.  
   - Perusahaan perlu memastikan adanya **rotasi jabatan atau peluang pengembangan**.  

---

## **Rekomendasi untuk HRD Jaya Jaya Maju**
1. **Strategi Kenaikan Gaji Berdasarkan Masa Kerja dan Performa**  
   - Menawarkan **kenaikan gaji** atau **bonus berbasis kontribusi** untuk meningkatkan retensi karyawan.  
   - Memastikan skema kompensasi tetap kompetitif, terutama bagi karyawan dengan masa kerja lebih dari 3-5 tahun.  

2. **Program Pengembangan Karier dan Promosi**  
   - Meningkatkan kesempatan **promosi dan rotasi jabatan** agar karyawan tidak stagnan dalam posisi yang sama.  
   - Menyediakan jalur karier yang jelas dengan **target promosi berdasarkan performa**.  

3. **Intervensi Dini untuk Karyawan Berisiko Tinggi Keluar**  
   - Menggunakan hasil prediksi model untuk **memantau karyawan dengan risiko tinggi keluar**.  
   - Melakukan **mentoring** atau **penyesuaian peran** bagi karyawan yang menunjukkan tanda-tanda ketidakpuasan.  

4. **Optimalisasi Sistem Evaluasi Kinerja**  
   - Mengurangi masa tunggu untuk promosi bagi karyawan berprestasi.  
   - Menyediakan **insentif berbasis prestasi** dan meningkatkan transparansi dalam sistem penilaian kinerja.  

5. **Meningkatkan Budaya dan Kesejahteraan Karyawan**  
   - Mengembangkan **work-life balance** agar karyawan lebih puas dengan lingkungan kerja mereka.  
   - Memperkuat budaya apresiasi terhadap kontribusi karyawan dengan **penghargaan rutin dan feedback yang lebih sering diberikan**.  

---

## **Next Steps**
1. **Integrasi Model ke Dashboard HR untuk Analisis Real-Time**  
   - Menggunakan Looker Studio atau Power BI untuk **memantau pola attrition secara langsung**.  

2. **Pelaksanaan Program Retensi Berdasarkan Hasil Prediksi**  
   - Memberikan **mentoring khusus** atau **bonus tambahan** bagi karyawan yang teridentifikasi berisiko tinggi resign.  

3. **Monitoring Model Secara Berkala**  
   - Memperbarui prediksi setiap kuartal untuk melihat perubahan pola kerja dan meningkatkan akurasi model.  

Dengan menerapkan rekomendasi ini, **HRD Jaya Jaya Maju dapat mengidentifikasi pola resign lebih dini dan menyusun strategi retensi karyawan yang lebih efektif**.
