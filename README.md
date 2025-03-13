# Simulasi Pengisian Daya Kendaraan Listrik

## Dataset
Dataset yang digunakan adalah **Electric Vehicle Charging Patterns** dari Kaggle. Dataset ini berisi 1.320 sampel sesi pengisian daya dengan fitur-fitur seperti:
- **ID Pengguna**
- **Model Kendaraan**
- **Kapasitas Baterai (kWh)**
- **Lokasi Stasiun Pengisian**
- **Waktu Mulai dan Selesai Pengisian**
- **Energi yang Digunakan (kWh)**
- **Durasi Pengisian (jam)**
- **Jenis Pengisi Daya (Level 1, Level 2, DC Fast Charger)**
- **Tipe Pengguna (Komuter, Pengguna Jarak Jauh)**

## Steps Project
1. Dataset diunduh menggunakan API Kaggle
2. Analisis statistik dasar dan visualisasi data (Eksplorasi Data)
3. Implementasi simulasi antrian menggunakan SimPy untuk memodelkan pengisian daya di stasiun pengisian
4. Perhitungan metrik kinerja seperti rata-rata durasi pengisian dan utilisasi stasiun
5. Penyesuaian parameter seperti jumlah stasiun untuk meningkatkan efisiensi (Optimasi)
6. Visualisasi untuk memahami pola pengisian dan hubungan antar variabel

## Hasil/Temuan
- Rata-rata Durasi Pengisian 2.27 jam
- Waktu Puncak Pengisian yaitu Evening
- Utilisasi Stasiun: 3.86% (sebelum optimasi) dan 3.82% (setelah optimasi)
- Kendaraan paling banyak adalah Tesla Model 3

## Cara Menjalankan Simulasi
1. Pastikan Python dan library yang diperlukan terinstal
   ```bash
   pip install -r requirements.txt
2. Unduh dataset
   ```bash
   import kagglehub
   path = kagglehub.dataset_download("valakhorasani/electric-vehicle-charging-patterns")
3. Jalankan kode Python yang disediakan untuk analisis dan simulasi
