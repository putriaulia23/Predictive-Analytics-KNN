# Predictive-Analytics-KNN

Repository ini berisi dokumentasi dan kode implementasi model **K-Nearest Neighbors (KNN)** untuk mengklasifikasikan kualitas tanah (Baik/Buruk) pada lahan pertanian hortikultura. Proyek ini mencakup proses analisis data prediktif (*Predictive Analytics*) hingga evaluasi performa model saat diintegrasikan ke dalam sistem monitoring berbasis Android.

---

## 📊 Project Overview & Dataset

* **Sumber Data:** Data real-time yang dikumpulkan langsung dari sensor IoT di area pertanian hortikultura **UD Hershyfa**.
* **Jumlah Data:** 1.473 records data sensor terintegrasi.
* **Fitur Utama (Sensor):**
  * Sensor **DHT22** (Mengukur Suhu Udara & Kelembaban Udara)
  * Sensor **FC-28** (Mengukur Kelembaban Tanah)
  * Sensor **pH Tanah**
* **Tujuan Analisis:** Membangun model klasifikasi cerdas untuk menentukan apakah kondisi kualitas tanah tergolong **Baik** atau **Buruk** guna mengoptimalkan perawatan tanaman hortikultura.

---

## 🧪 Model Development & Optimization

Untuk mendapatkan performa model terbaik, telah dilakukan eksperimen intensif sebanyak **36 percobaan kombinasi parameter model KNN**.

### Hasil Parameter Terbaik:
* **Jumlah Tetangga (k):** 4
* **Metrik Jarak:** *Manhattan Distance*

### Performa Model (Data Training & Testing):
* 🎯 **Akurasi:** 95%
* 🎯 **Presisi:** 93%
* 🎯 **Recall:** 100% *(Sangat baik dalam meminimalkan kesalahan deteksi tanah buruk)*

---

## 📱 Android System Implementation

Model KNN yang telah dioptimasi ini berhasil diimplementasikan ke dalam **Sistem Monitoring Kualitas Tanah Hortikultura Berbasis Android**. 

Sistem secara *real-time* mengklasifikasikan kualitas tanah menjadi **Kualitas Baik** atau **Kualitas Buruk** berdasarkan 3 kriteria input sensor utama:
1. Kelembaban Tanah
2. Suhu Udara
3. pH Tanah

---

## ⚡ System Testing & Evaluation (Confusion Matrix)

Setelah model diintegrasikan ke dalam sistem monitoring Android, pengujian performa sistem akhir dilakukan menggunakan metode **Confusion Matrix** untuk memvalidasi akurasi deteksi di lapangan.

### Hasil Pengujian Sistem:
* 📉 **Akurasi Sistem:** 93,95%
* 📉 **Presisi Sistem:** 83,33%
* 📉 **Recall Sistem:** 94,59%

Hasil ini membuktikan bahwa model KNN memiliki tingkat ketahanan (*robustness*) yang sangat tinggi dan valid saat dijalankan pada perangkat *mobile* untuk membantu petani mengambil keputusan secara data-driven.

---

## 🛠️ Tech Stack & Tools Used
* **Language:** Python
* **Environment:** Jupyter Notebook (`.ipynb`)
* **Libraries:** Pandas, NumPy, Scikit-Learn, Matplotlib/Seaborn
* **Deployment Platform:** Android (Java/Kotlin) & IoT Sensors integration
