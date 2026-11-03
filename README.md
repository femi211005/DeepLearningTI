# Analisis Perbandingan Model Deep Learning: 1D CNN vs RNN (LSTM) pada Dataset IMDb Reviews

Repositori ini berisi tugas individu mata kuliah **Deep Learning** yang mengimplementasikan dan membandingkan dua arsitektur jaringan saraf tiruan yang berbeda (*1D Convolutional Neural Network* dan *Recurrent Neural Network - LSTM*) pada satu dataset teks yang sama (*IMDb Reviews*) untuk tugas analisis sentimen.

## 👤 Informasi Mahasiswa
* **Nama:** Femilia Padaunan
* **NIM:** H071241012
* **Kelas:** Deep Learning 

---

## 📊 Ringkasan Proyek
Proyek ini dirancang untuk membandingkan performa antara **1D CNN** dan **RNN (LSTM)** dalam memahami teks ulasan film dan mengklasifikasikannya ke dalam sentimen positif atau negatif secara adil menggunakan satu sumber data yang seragam.

1. **Dataset:** 
   * **IMDb Reviews** (diambil melalui TensorFlow Datasets / `tf.keras.datasets.imdb`)
   * Melibatkan 10.000 kata teratas dengan panjang maksimum sekuens diseragamkan (*padding*) hingga 200 kata per kalimat.
   
2. **Arsitektur Model:**
   * **Model 1 (1D CNN):** Menggunakan *Embedding Layer*, *Conv1D*, *MaxPooling1D*, *Flatten*, dan *Dense Layer* dengan *Dropout* untuk menangkap pola fitur lokal dari teks.
   * **Model 2 (RNN - LSTM):** Menggunakan *Embedding Layer*, *LSTM Layer* (dengan mekanisme *recurrent dropout*), dan *Dense Layer* untuk menangkap konteks urutan kalimat secara sekuensial.

---

## 📌 Kesimpulan Perbandingan Model

Berdasarkan implementasi, pelatihan, dan pengujian yang telah dilakukan, berikut adalah ringkasan perbandingan kinerjanya:

| Parameter / Metrik | 1D CNN | RNN - LSTM |
| :--- | :--- | :--- |
| **Fokus Utama** | Ekstraksi pola/fitur lokal & kombinasi frasa kata | Pemeliharaan konteks & urutan kalimat jangka panjang |
| **Kecepatan Training** | Cenderung lebih cepat (komputasi paralel) | Sedikit lebih lambat (proses sekuensial) |
| **Karakteristik Hasil** | Sangat baik dalam mendeteksi kata kunci penting | Sangat andal dalam memahami alur konteks kalimat utuh |

**Kesimpulan Akhir:**
Kedua arsitektur berhasil diterapkan dengan sangat baik pada dataset teks *IMDb Reviews*. **RNN (LSTM)** unggul dalam hal pemahaman konteks urutan teks secara utuh, sementara **1D CNN** menawarkan keunggulan pada efisiensi kecepatan komputasi dan penangkapan pola lokal. Pemilihan arsitektur dapat disesuaikan berdasarkan skala prioritas antara kecepatan pelatihan atau ketepatan pemahaman sekuensial.

---
*Dibuat untuk memenuhi Tugas Individu Deep Learning 2026.*
