# Simulasi Antrian Pengisian Daya Kendaraan Listrik Berbasis Data

Proyek ini bertujuan untuk menganalisis dan mensimulasikan pola antrian di stasiun pengisian daya kendaraan listrik (EV) menggunakan pendekatan berbasis data (*data-driven*) dengan SimPy.

---

## Daftar Isi

1.  [Latar Belakang](#latar-belakang)
2.  [Tujuan Proyek](#tujuan-proyek)
3.  [Dataset](#dataset)
4.  [Alur Kerja Proyek](#alur-kerja-proyek)
5.  [Hasil dan Temuan Utama](#hasil-dan-temuan-utama)
6.  [Tech Stack](#tech-stack)
7.  [Cara Menjalankan Simulasi](#cara-menjalankan-simulasi)

---

## Latar Belakang

Dengan meningkatnya adopsi kendaraan listrik, efisiensi stasiun pengisian daya menjadi krusial. Antrian yang panjang dan waktu tunggu yang tidak efisien dapat mengurangi kenyamanan pengguna. Proyek ini menggunakan simulasi untuk memodelkan proses pengisian daya, menganalisis kinerja stasiun, dan mencari cara untuk mengoptimalkan operasionalnya berdasarkan pola penggunaan nyata.

## Tujuan Proyek

-   Menganalisis pola kedatangan dan durasi pengisian daya kendaraan listrik berdasarkan data historis.
-   Membangun model simulasi antrian menggunakan **SimPy** untuk mereplikasi kondisi di stasiun pengisian.
-   Mengevaluasi metrik kinerja stasiun, seperti waktu tunggu rata-rata dan tingkat utilisasi.
-   Memberikan rekomendasi berbasis data untuk optimasi jumlah stasiun pengisian.

---

## Dataset

Dataset yang digunakan adalah **"Electric Vehicle Charging Patterns"** dari Kaggle. Dataset ini berisi 1.320 sampel sesi pengisian daya dengan fitur-fitur seperti:
-   **ID Pengguna**
-   **Model Kendaraan**
-   **Kapasitas Baterai (kWh)**
-   **Lokasi Stasiun Pengisian**
-   **Waktu Mulai dan Selesai Pengisian**
-   **Energi yang Digunakan (kWh)**
-   **Durasi Pengisian (jam)**
-   **Jenis Pengisi Daya (Level 1, Level 2, DC Fast Charger)**
-   **Tipe Pengguna (Komuter, Pengguna Jarak Jauh)**

---

## Alur Kerja Proyek

1.  **Pengambilan Data**: Dataset diunduh secara otomatis menggunakan API dari Kaggle.
2.  **Eksplorasi Data (EDA)**: Melakukan analisis statistik dasar dan visualisasi untuk memahami distribusi data, seperti pola waktu puncak pengisian dan model kendaraan yang paling umum.
3.  **Implementasi Simulasi**: Membangun model simulasi antrian menggunakan **SimPy** untuk memodelkan proses kedatangan mobil dan pengisian daya di stasiun.
4.  **Analisis Kinerja**: Menghitung metrik kinerja utama seperti rata-rata waktu tunggu, durasi pengisian, dan utilisasi stasiun.
5.  **Optimasi**: Menyesuaikan parameter simulasi (seperti jumlah stasiun) untuk melihat dampaknya terhadap efisiensi dan menemukan konfigurasi yang lebih optimal.

---

## Hasil dan Temuan Utama

-   **Waktu Puncak Pengisian**: Mayoritas pengguna melakukan pengisian daya pada **sore hari (Evening)**.
-   **Rata-rata Durasi Pengisian**: Durasi rata-rata untuk satu sesi pengisian adalah sekitar **2.27 jam**.
-   **Model Kendaraan Terpopuler**: **Tesla Model 3** adalah kendaraan yang paling sering tercatat dalam data.
-   **Utilisasi Stasiun**:
    -   **Sebelum Optimasi**: 3.86%
    -   **Setelah Optimasi**: 3.82%
    *(Utilisasi yang rendah mengindikasikan bahwa kapasitas stasiun masih sangat memadai untuk beban saat ini).*

---

## Tech Stack

-   **Bahasa Pemrograman**: Python
-   **Library Simulasi**: SimPy
-   **Library Analisis Data**: Pandas, NumPy, KaggleHub
-   **Library Visualisasi**: Matplotlib, Seaborn

---

## Cara Menjalankan Simulasi

1.  **Pastikan Python dan `pip` terinstal.**

2.  **Clone Repositori Ini**
    ```bash
    git clone https://github.com/haaahabib/data-driven-simulation.git
    ```

3.  **Masuk ke Direktori Proyek**
    ```bash
    cd data-driven-simulation
    ```

4.  **Install Library yang Diperlukan**
    (Pastikan Anda memiliki file `requirements.txt` atau install secara manual).
    ```bash
    pip install pandas numpy simpy matplotlib seaborn kagglehub
    ```

5.  **Konfigurasi API Kaggle**
    Pastikan file `kaggle.json` Anda berada di lokasi yang benar (`~/.kaggle/kaggle.json`) agar skrip dapat mengunduh dataset.

6.  **Jalankan Notebook atau Skrip Python**
    Buka dan jalankan file notebook (`.ipynb`) atau skrip (`.py`) utama untuk memulai analisis dan simulasi.
