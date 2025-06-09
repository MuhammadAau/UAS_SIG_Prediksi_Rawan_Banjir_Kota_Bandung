# Prediksi Rawan Banjir Kota Bandung

# 📌 Deskripsi

Proyek ini mengembangkan model prediktif untuk mengidentifikasi wilayah-wilayah yang berpotensi mengalami banjir di Kota Bandung. Model mempertimbangkan berbagai variabel spasial dan non-spasial, antara lain:

  - Rata-rata curah hujan tahunan per kecamatan

  - Data kepadatan dan jumlah penduduk

  - Data penggunaan lahan (persentase permukiman dan ruang terbuka hijau)

  - Riwayat kejadian banjir historis

  - Lokasi spasial kecamatan (koordinat pusat)

Proyek ini diintegrasikan ke dalam sebuah peta interaktif berbasis Folium, yang menampilkan visualisasi prediksi risiko banjir per kecamatan dalam bentuk petak berwarna dan label dinamis.

# 📊 Data yang Digunakan

Proyek ini memanfaatkan 5 dataset utama, yaitu:

1. Data Curah Hujan
1_Bandung_curah_hujan_full.csv:
Rata-rata curah hujan tahunan per kecamatan dalam milimeter (mm).

2. Data Non-Spasial
2_Bandung_non_spasial_full.csv:
Berisi data jumlah penduduk, kepadatan penduduk per km², dan variabel lain yang bersifat demografis.

3. Data Historis Banjir
3_Bandung_riwayat_banjir_full.csv:
Jumlah kejadian banjir yang pernah tercatat per kecamatan.

4. Data Penggunaan Lahan
4_Bandung_penggunaan_lahan_full.csv:
Persentase penggunaan lahan untuk permukiman dan ruang terbuka hijau.

5. Data Target Prediksi
5_Bandung_prediksi_banjir_full.csv:
Kategori tingkat kerawanan banjir (Rendah, Sedang, Tinggi) berdasarkan penilaian awal/labeling.

# 🤖 Model Machine Learning
Model yang digunakan adalah Random Forest Classifier, karena kemampuannya dalam menangani data tabular yang kompleks dan tidak linier.

# 🎯 Kinerja Model
Dengan parameter default dan pelatihan awal, model menunjukkan akurasi tinggi:

markdown
Salin
Edit
Akurasi: 93%
Classification Report:

              precision    recall  f1-score   support

    Rendah       0.95      0.95      0.95        12
    Sedang       0.89      0.89      0.89         9
    Tinggi       0.90      0.90      0.90         9
Interpretasi:
Model sangat andal dalam memetakan wilayah aman (Rendah) maupun wilayah rawan banjir (Tinggi), dengan rata-rata f1-score mencapai 91%.

# 🔍 Analisis Faktor Penting
Fitur yang paling berpengaruh terhadap prediksi berdasarkan analisis feature importance adalah:

  1. Jumlah Kejadian Banjir

  2. Curah Hujan Tahunan (mm)

  3. Kepadatan Penduduk per km²

  4. Persentase Lahan Permukiman

  5. Persentase Ruang Terbuka Hijau

# 🗺️ Output
Proyek ini menghasilkan dua output utama:

1. Model prediksi banjir yang dapat digunakan untuk input data baru.

2. Visualisasi peta interaktif dalam file peta_banjir_bandung.html:

    - Menampilkan setiap kecamatan sebagai kotak warna sesuai tingkat risikonya (hijau, oranye, merah)
    
    - Dilengkapi popup info dan label nama kecamatan
    
    - Disertai legenda visual yang menjelaskan arti warna

# 💡 Cara Penggunaan
Proyek ini dirancang dalam format Google Colab. Untuk menjalankannya kembali, ikuti langkah berikut:

1. Buka file notebook Sig_Ai_Banjir_Bandung.ipynb di Google Colab.

2. Unduh 5 file dataset yang dibutuhkan.

3. Jalankan semua sel secara berurutan:

    - Pemrosesan data

    - Pelatihan model

    - Evaluasi

4. Pembuatan peta

Di bagian akhir, file peta peta_banjir_bandung.html akan otomatis tersimpan dan dapat di-download.

