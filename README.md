# 🎓Judul:Klasifikasi Kebutuhan Pendampingan Belajar Mahasiswa Berdasarkan Aktivitas Akademik Menggunakan Decision Tree, Random Forest, KNN, dan Naive Bayes untuk Mendukung SDG

## 📌 Deskripsi

Proyek ini merupakan penerapan **Artificial Intelligence (AI) dan Machine Learning** untuk membantu mengidentifikasi apakah seorang mahasiswa **memerlukan pendampingan belajar atau tidak**.

Sistem melakukan klasifikasi berdasarkan beberapa indikator performa akademik mahasiswa, seperti:

* Study Hours
* Attendance
* Assignment Completion
* Online Courses
* Discussions
* Exam Score
* Final Grade

Target klasifikasi yang digunakan adalah:

* **Ya** → Mahasiswa memerlukan pendampingan
* **Tidak** → Mahasiswa belum memerlukan pendampingan

Proyek ini dikembangkan sebagai bagian dari penerapan **SDGs 4 – Quality Education (Pendidikan Berkualitas)**, khususnya dalam mendukung proses identifikasi mahasiswa yang membutuhkan pendampingan akademik.

---
## 🎯 Latar Belakang

Tidak semua mahasiswa memiliki aktivitas dan performa akademik yang sama. Beberapa mahasiswa memiliki kehadiran rendah, kurang menyelesaikan tugas, waktu belajar yang sedikit, atau nilai ujian yang rendah sehingga berpotensi membutuhkan pendampingan belajar.

Oleh karena itu, proyek ini menggunakan Machine Learning untuk mengklasifikasikan mahasiswa menjadi *"Perlu Pendampingan"* atau *"Tidak Perlu Pendampingan"* berdasarkan data akademiknya.

## 🎯 Tujuan

Tujuan dari proyek ini adalah:

1. Mengembangkan model Machine Learning untuk mengklasifikasikan kebutuhan pendampingan belajar mahasiswa.
2. Membandingkan performa beberapa algoritma klasifikasi.
3. Mengidentifikasi faktor-faktor yang berpengaruh terhadap kebutuhan pendampingan.
4. Memberikan rekomendasi pendampingan berdasarkan kondisi akademik mahasiswa.

---

## 📊 Dataset

Dataset yang digunakan adalah:

`student_performance_clean.csv`

Dataset berisi informasi mengenai performa mahasiswa yang digunakan sebagai fitur untuk proses klasifikasi.

### Fitur yang digunakan

| Fitur                | Keterangan                        |
| -------------------- | --------------------------------- |
| StudyHours           | Jumlah jam belajar                |
| Attendance           | Persentase kehadiran              |
| AssignmentCompletion | Persentase penyelesaian tugas     |
| OnlineCourses        | Aktivitas mengikuti kursus online |
| Discussions          | Aktivitas diskusi                 |
| ExamScore            | Nilai ujian                       |
| FinalGrade           | Nilai akhir                       |

### Target

Target dibuat berdasarkan beberapa kondisi akademik:

* Attendance < 70
* AssignmentCompletion < 60
* ExamScore < 60
* StudyHours < 10

Jika salah satu kondisi tersebut terpenuhi, mahasiswa dikategorikan sebagai:

**Perlu Pendampingan = Ya**

Jika tidak ada kondisi yang terpenuhi:

**Perlu Pendampingan = Tidak**

---

## 🤖 Algoritma yang Digunakan

Pada proyek ini digunakan 4 algoritma klasifikasi:

### 1. Decision Tree

Decision Tree digunakan untuk membuat model klasifikasi berdasarkan aturan keputusan dari fitur-fitur yang tersedia.

### 2. Random Forest

Random Forest merupakan algoritma ensemble yang menggunakan beberapa Decision Tree untuk menghasilkan prediksi.

### 3. K-Nearest Neighbors (KNN)

KNN melakukan klasifikasi berdasarkan kedekatan data dengan data lainnya. Pada proyek ini dilakukan standardisasi data sebelum digunakan oleh KNN.

### 4. Naive Bayes

Gaussian Naive Bayes digunakan sebagai salah satu model pembanding untuk melakukan klasifikasi kebutuhan pendampingan.

---

## ⚙️ Tahapan Proses

Proses dalam proyek ini terdiri dari beberapa tahap:

```text
Dataset
   ↓
Data Preparation
   ↓
Menentukan Target
   ↓
Pemilihan Fitur
   ↓
Train-Test Split
   ↓
Standardisasi Data
   ↓
Training 4 Algoritma
   ↓
Testing
   ↓
Evaluasi Model
   ↓
Perbandingan Performa
   ↓
Prediksi Mahasiswa Baru
   ↓
Rekomendasi Pendampingan
```

---

## 📈 Evaluasi Model

Performa masing-masing algoritma dievaluasi menggunakan beberapa metrik:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-Score**
* **Confusion Matrix**

Hasil evaluasi dari keempat algoritma kemudian dibandingkan untuk melihat perbedaan performa model.

---

## 🔍 Analisis Feature Importance

Proyek ini juga melakukan analisis **feature importance** pada:

* Decision Tree
* Random Forest

Analisis tersebut digunakan untuk melihat kontribusi relatif fitur yang digunakan dalam proses klasifikasi.

---

## 👨‍🎓 Prediksi Mahasiswa Baru

Model juga digunakan untuk melakukan simulasi prediksi terhadap data mahasiswa baru.

Data mahasiswa baru kemudian diproses menggunakan:

* Decision Tree
* Random Forest
* KNN
* Naive Bayes

Hasil prediksi dari setiap algoritma ditampilkan untuk mengetahui klasifikasi kebutuhan pendampingan.

---

## 💡 Rekomendasi Pendampingan

Sistem juga menghasilkan rekomendasi berdasarkan kondisi mahasiswa, antara lain:

* Pendampingan untuk meningkatkan kehadiran
* Pendampingan manajemen tugas
* Pendampingan manajemen waktu belajar
* Tutoring atau pendampingan akademik
* Belum diperlukan pendampingan khusus

---

## 💾 Output Model

Beberapa model dan hasil yang dihasilkan oleh notebook antara lain:

```text
model_decision_tree_pendampingan.pkl
model_random_forest_pendampingan.pkl
model_knn_pendampingan.pkl
model_naive_bayes_pendampingan.pkl
scaler_knn.pkl
dataset_pendampingan_mahasiswa.csv
hasil_perbandingan_algoritma.csv
```

---

## 🛠️ Teknologi yang Digunakan

Proyek ini dibuat menggunakan:

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* Joblib

---

## 📁 Struktur Repository

```text
projek-AI-SDGs4-Kualitas-Pendidikan/
│
├── projek_AI_SDGs4_KUALITAS_PENDIDIKAN.ipynb
├── student_performance_clean.csv
├── dataset_pendampingan_mahasiswa.csv
├── hasil_perbandingan_algoritma.csv
│
├── model_decision_tree_pendampingan.pkl
├── model_random_forest_pendampingan.pkl
├── model_knn_pendampingan.pkl
├── model_naive_bayes_pendampingan.pkl
├── scaler_knn.pkl
│
└── README.md
```

---

## 🌍 Kaitan dengan SDGs 4

Proyek ini berkaitan dengan **Sustainable Development Goals (SDGs) nomor 4: Quality Education**.

Pemanfaatan Machine Learning dalam proyek ini diarahkan untuk membantu proses identifikasi mahasiswa yang memiliki indikator kebutuhan pendampingan belajar. Dengan adanya sistem klasifikasi, data performa mahasiswa dapat digunakan sebagai salah satu pendukung dalam proses pemberian pendampingan akademik.

---

## 👥 Pengembangan

Proyek ini dapat dikembangkan lebih lanjut dengan:

* Menggunakan dataset yang lebih besar.
* Menambahkan fitur akademik lainnya.
* Melakukan optimasi hyperparameter.
* Mengembangkan aplikasi berbasis web.
* Membuat sistem prediksi secara real-time.
* Menambahkan visualisasi dashboard.
* Mengembangkan sistem rekomendasi pendampingan yang lebih terperinci.

---

## 📌 Kesimpulan

Proyek ini menerapkan beberapa algoritma Machine Learning untuk melakukan klasifikasi kebutuhan pendampingan belajar mahasiswa berdasarkan data performa akademik.

Empat algoritma yang digunakan adalah **Decision Tree, Random Forest, KNN, dan Naive Bayes**. Setiap model dievaluasi menggunakan Accuracy, Precision, Recall, F1-Score, dan Confusion Matrix untuk mengetahui performanya.

Hasil proyek dapat digunakan sebagai dasar pengembangan sistem pendukung untuk membantu mengidentifikasi mahasiswa yang membutuhkan pendampingan akademik.
