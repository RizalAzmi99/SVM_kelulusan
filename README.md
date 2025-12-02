# Prediksi Kelulusan Mahasiswa Menggunakan Support Vector Machine (SVM)

## 📌 Identitas Mahasiswa
**Nama:** Muhammad Rizal Azmi  
**NPM:** 2457201002412  
**Kelas/Mata Kuliah:** Machine Learning

---

## 📖 Deskripsi Proyek
Proyek ini bertujuan untuk memprediksi status kelulusan mahasiswa (TEPAT WAKTU atau TERLAMBAT) berdasarkan data historis akademik menggunakan algoritma *Supervised Learning* yaitu **Support Vector Machine (SVM)**.

Analisis ini penting untuk membantu institusi pendidikan mengidentifikasi mahasiswa yang berisiko terlambat lulus lebih awal, sehingga dapat diberikan intervensi yang tepat.

---

## 📂 Dataset
Dataset yang digunakan adalah `datakelulusanmahasiswa.csv`.
- **Sumber:** Data internal akademik (disamarkan).
- **Fitur Utama:** IPK, Status Nikah, IPS 1-8, Umur, Jenis Kelamin, dll.
- **Target Label:** `STATUS KELULUSAN` (TEPAT / TERLAMBAT).

---

## ⚙️ Langkah Pengerjaan (Methodology)
Proyek ini diselesaikan dengan alur kerja *Machine Learning* standar:

1.  **Exploratory Data Analysis (EDA):**
    - Memeriksa distribusi data dan statistik deskriptif.
    - Visualisasi hubungan antara IPK dan status kelulusan.
    - Pengecekan *missing values*.

2.  **Preprocessing Data:**
    - **Cleaning:** Menangani nilai yang hilang (*Imputation*).
    - **Encoding:** Mengubah variabel kategorikal (seperti 'Status Nikah', 'Jenis Kelamin') menjadi numerik.
    - **Scaling:** Normalisasi fitur menggunakan `StandardScaler` agar performa SVM optimal.

3.  **Modeling (Support Vector Machine):**
    - Melatih model menggunakan kernel **Linear** dan **RBF**.
    - Melakukan *Hyperparameter Tuning* (GridSearchCV) untuk mencari kombinasi terbaik dari parameter `C` dan `Gamma`.

4.  **Evaluasi:**
    - Menggunakan metrik Akurasi, Confusion Matrix, dan Classification Report.
    - Interpretasi fitur terpenting yang mempengaruhi kelulusan.

---

## 📊 Hasil Evaluasi Model
Berdasarkan hasil training, berikut adalah performa model terbaik:

- **Model Terbaik:** SVM dengan Kernel [ISI: RBF atau Linear]
- **Parameter Terbaik:** C=[ISI ANGKA], Gamma=[ISI ANGKA]
- **Akurasi Model:** [ISI PERSEN AKURASI, misal: 92%]

**Temuan Analitis:**
- Mahasiswa dengan IPK rendah cenderung memiliki probabilitas lebih tinggi untuk lulus terlambat.
- Fitur akademik (IPK/IPS) memiliki pengaruh paling dominan dibandingkan fitur demografis.

*(Sertakan Screenshot Confusion Matrix di sini jika ada)*

---

## 🚀 Cara Menjalankan Notebook
1.  Clone repository ini:
    ```bash
    git clone [LINK GITHUB KAMU]
    ```
2.  Buka file `SVM_kelulusan.ipynb` menggunakan Google Colab atau Jupyter Notebook.
3.  Pastikan file dataset `datakelulusanmahasiswa.csv` berada satu folder dengan notebook.
4.  Jalankan setiap sel ("Run All") untuk melihat hasil prediksi.

---
**Dibuat untuk memenuhi Tugas Project Machine Learning (100 Menit).**
