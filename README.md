---

## 💡 Predictive Analytics: Deteksi Penyakit Jantung

### 1. Pendahuluan

Penyakit jantung merupakan salah satu penyebab utama kematian di seluruh dunia. Deteksi dini terhadap risiko penyakit jantung sangat penting untuk mencegah komplikasi yang lebih serius. Dalam proyek ini, kami membangun model machine learning untuk memprediksi kemungkinan seseorang menderita penyakit jantung berdasarkan data medis.

---

### 2. Tujuan Proyek

Membuat model klasifikasi untuk memprediksi risiko penyakit jantung berdasarkan fitur-fitur medis menggunakan algoritma machine learning.

---

### 3. Dataset

* Dataset: [Heart Disease Dataset](https://www.kaggle.com/datasets/cherngs/heart-disease-cleveland-uci)
* Jumlah sampel: 270
* Jumlah fitur: 13
* Target: `Heart Disease` (0 = Sehat, 1 = Mengidap Penyakit Jantung)

---

### 4. Business Understanding

#### Problem Statement

Bagaimana cara mengidentifikasi risiko penyakit jantung berdasarkan data medis pasien?

#### Goals

Memprediksi kondisi penyakit jantung menggunakan algoritma klasifikasi.

#### Solution Statement

* Membangun dan membandingkan model:

  * Logistic Regression
  * Random Forest
  * XGBoost
* Memilih model terbaik berdasarkan metrik evaluasi (accuracy, recall, f1-score)
* Menampilkan ROC Curve untuk membandingkan performa model secara visual.

---

### 5. Data Understanding

#### Fitur dalam dataset:

| Fitur                   | Deskripsi                                               |
| ----------------------- | ------------------------------------------------------- |
| Age                     | Usia pasien                                             |
| Sex                     | Jenis kelamin                                           |
| Chest pain type         | Jenis nyeri dada                                        |
| BP                      | Tekanan darah                                           |
| Cholesterol             | Kadar kolesterol                                        |
| FBS over 120            | Gula darah puasa > 120 mg/dl                            |
| EKG results             | Hasil EKG                                               |
| Max HR                  | Detak jantung maksimum                                  |
| Exercise angina         | Nyeri dada saat olahraga                                |
| ST depression           | Penurunan segmen ST                                     |
| Slope of ST             | Kemiringan segmen ST                                    |
| Number of vessels fluro | Jumlah pembuluh darah yang terlihat melalui fluoroskopi |
| Thallium                | Hasil tes thallium                                      |
| Heart Disease           | Target (0 = Sehat, 1 = Sakit)                           |

---

### 6. Data Preparation

* Tidak ditemukan nilai null
* Label encoding untuk kolom `Heart Disease`
* Split data ke `train` dan `test` (80:20)
* StandardScaler digunakan untuk normalisasi fitur numerik

---

### 7. Modeling & Evaluasi

#### 📌 Logistic Regression

* Accuracy: 85%
* F1-score: 0.85
* Confusion Matrix:

  ```
  [[24  6]
   [ 2 22]]
  ```

#### 📌 Random Forest

* Accuracy: 81%
* F1-score: 0.80
* Confusion Matrix:

  ```
  [[24  6]
   [ 4 20]]
  ```

#### 📌 XGBoost

* Accuracy: 81%
* F1-score: 0.80
* Confusion Matrix:

  ```
  [[24  6]
   [ 4 20]]
  ```

#### 📊 ROC Curve

Model Logistic Regression menunjukkan area ROC terbesar dibanding model lain.

---

### 8. Model Terbaik

Dipilih: **Logistic Regression**
Alasan:

* Akurasi dan f1-score tertinggi (85%)
* Model yang lebih ringan dan mudah di-deploy

---

### 9. Kesimpulan

* Model machine learning mampu memprediksi penyakit jantung dengan baik berdasarkan data medis.
* Logistic Regression adalah model terbaik dalam studi ini.
* Untuk pengembangan lanjutan, dataset yang lebih besar dan fitur tambahan (seperti gaya hidup atau riwayat keluarga) dapat meningkatkan akurasi prediksi.

---
