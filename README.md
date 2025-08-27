
# Capstone Project: Analisis Prediksi Kelangsungan Hidup Pasien Penyakit Jantung

## 🎯 **Project Overview**

Proyek ini bertujuan untuk mengembangkan model analitik prediktif menggunakan data klinis dari pasien penyakit jantung. Tujuannya adalah untuk mengidentifikasi faktor-faktor risiko kunci yang memengaruhi kelangsungan hidup pasien dan memprediksi kemungkinan gagal jantung. Proyek ini tidak hanya menghasilkan model prediktif, tetapi juga memberikan wawasan yang dapat ditindaklanjuti untuk membantu profesional medis dalam pengambilan keputusan klinis.

Pendekatan yang saya gunakan mengikuti alur kerja *data science* standar:
1.  **Pengumpulan Data**: Menggunakan dataset publik yang relevan dari Kaggle.
2.  **Pra-pemrosesan Data**: Membersihkan dan menyiapkan data, termasuk penanganan nilai yang hilang dan pengodean fitur kategorikal.
3.  **Pemodelan**: Membangun model klasifikasi menggunakan algoritma Regresi Logistik, yang dikenal efisien dan mudah diinterpretasi.
4.  **Evaluasi Model**: Mengukur kinerja model menggunakan metrik standar seperti akurasi, presisi, *recall*, dan *F1-score*.
5.  **Interpretasi dengan AI**: Memanfaatkan model bahasa besar (LLM) IBM Granite untuk menerjemahkan hasil teknis menjadi wawasan yang mudah dipahami.

---

## 🔗 **Raw Dataset Link**

Dataset yang digunakan dalam proyek ini adalah **Heart Failure Prediction Dataset** yang tersedia secara publik di Kaggle. Data ini berisi 11 fitur klinis yang relevan dan satu variabel target yang mengindikasikan kelangsungan hidup pasien.

* **Link Dataset:** [https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)

---

## 💡 **Insight & Findings**

Analisis ini menghasilkan beberapa temuan penting yang memberikan pemahaman lebih dalam tentang faktor-faktor risiko penyakit jantung:

* **Akurasi Model Tinggi:** Model prediksi mencapai **akurasi 91%** pada data pengujian. Akurasi ini menunjukkan bahwa model memiliki kemampuan yang kuat dalam memprediksi kelangsungan hidup pasien.
* **Faktor Risiko Utama:** Dari analisis koefisien model, fitur-fitur yang memiliki pengaruh paling signifikan terhadap prediksi adalah **jenis nyeri dada (`cp`)**, **detak jantung maksimal (`thalachh`)**, dan **usia (`age`)**. Temuan ini sejalan dengan pengetahuan medis, memperkuat validitas model.
* **Pentingnya Metrik Recall:** Analisis mendalam menunjukkan bahwa model memiliki **recall 89%** untuk pasien yang benar-benar mengalami gagal jantung (kelas 1). Dalam konteks medis, ini adalah metrik yang paling kritis. **Recall** yang tinggi berarti model sangat efektif dalam mengidentifikasi sebagian besar pasien yang berisiko, yang sangat penting untuk mencegah misdiagnosis yang fatal. 
* **Hubungan Kolesterol dan Usia:** Visualisasi data menunjukkan bahwa pasien yang mengalami gagal jantung cenderung memiliki tingkat kolesterol yang lebih tinggi. Selain itu, distribusi usia pasien dengan gagal jantung terlihat lebih beragam, tetapi rata-rata usia mereka sedikit lebih tinggi.

---

## 🤖 **AI Support Explanation**

Proyek ini menggunakan LLM **IBM Granite** untuk meningkatkan nilai dari analisis data. AI tidak digunakan untuk pemodelan prediktif, melainkan untuk interpretasi dan klarifikasi hasil analisis.

1.  **Interpretasi Hasil Teknis:** Setelah model klasifikasi selesai dievaluasi, lalu mengirimkan laporan metrik evaluasi (`precision`, `recall`, `f1-score`) ke LLM. AI menjelaskan arti dari metrik-metrik ini dalam bahasa yang non-teknis dan mudah dipahami oleh dokter atau manajer rumah sakit.
2.  **Klarifikasi Kontekstual:** AI menjelaskan **mengapa *recall* sangat penting dalam diagnosis penyakit**. Jawaban dari AI memberikan konteks kritis, menunjukkan bahwa tingginya *recall* berarti model sangat baik dalam menghindari "salah negatif" (pasien sakit yang tidak terdeteksi), yang merupakan hal paling vital dalam bidang kesehatan.

Dengan cara ini, AI berfungsi sebagai alat bantu intelektual yang mengubah data dan angka teknis menjadi wawasan naratif yang memiliki dampak dan makna di dunia nyata.
