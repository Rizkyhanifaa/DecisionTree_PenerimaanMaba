# Decision Tree: Prediksi Penerimaan Mahasiswa Baru

## 📝 Deskripsi Proyek

Repositori ini berisi implementasi **algoritma Decision Tree** yang dibangun dengan tujuan utama adalah untuk melakukan klasifikasi dan memprediksi hasil kelulusan calon mahasiswa baru berdasarkan data.

Model akan memprediksi status calon mahasiswa menjadi dua kategori: **"Diterima"** atau **"Tidak Diterima"**. Prediksi ini didasarkan pada beberapa variabel yaitu latar belakang pendidikan (jurusan SMA), pilihan jurusan di universitas, prioritas pilihan, serta performa akademik (rata-rata nilai dan skor ujian).

## ✨ Fitur Utama

-   **Implementasi Murni**: Algoritma Decision Tree dibuat dari nol tanpa bantuan library
-   **Kriteria Pembagian (Split Criterion)**: Menggunakan **Information Gain** yang dihitung dari **Entropi** untuk menentukan fitur terbaik di setiap cabang pohon.
-   **Penanganan Data**: Mampu menangani data kategorikal (seperti jurusan) dan numerik (seperti skor ujian).
-   **Prediksi Interaktif**: Dilengkapi dengan antarmuka baris perintah (CLI) sederhana yang memungkinkan pengguna memasukkan data baru untuk mendapatkan prediksi.
-   **Evaluasi Model**: Kinerja model dievaluasi menggunakan **F1-Score**, yang memberikan gambaran seimbang antara presisi dan recall. Data secara otomatis dibagi menjadi 80% data latih dan 20% data uji.

## 🚀 Cara Penggunaan

Untuk menjalankan skrip dan melihat cara kerja model, ikuti langkah-langkah berikut:

1.  **Clone repositori ini ke komputer Anda:**
2.  **Buka terminal dan navigasi ke direktori proyek**
3.  **Jalankan skrip Python:**
    ```bash
    python main.py
    ```
4.  **Lihat hasilnya:**
    -   Program pertama-tama akan mencetak struktur pohon keputusan yang berhasil dibuat.
    -   Selanjutnya, Anda akan diminta untuk memasukkan data seorang calon mahasiswa secara interaktif.
    -   Setelah semua data diisi, program akan menampilkan hasil prediksi beserta skor evaluasi F1 dari model.

## 📊 Contoh Output

Berikut adalah contoh sesi saat program dijalankan di terminal:

```
============ Pohon Keputusan ============

Skor_Ujian <= 65.0
   True:
     Jurusan_Pilihan == IPS
        True:
          [Label: Diterima]
        False:
          Skor_Ujian <= 45.0
             True:
               [Label: Tidak Diterima]
             False:
               [Label: Diterima]
   False:
     [Label: Diterima]

----- Masukkan data untuk prediksi: -----

Jurusan SMA (IPA/IPS)            : IPS
Jurusan Pilihan (IPA/IPS/Kejuruan) : IPA
Pilihan Keberapa (1/2/3)           : 1
Rata-rata Nilai Akhir              : 8.5
Skor Ujian UTBK                    : 75

Hasil Prediksi                     : Diterima

--- F1-Score Model pada Data Pengujian: 0.9412 ---
```

---
