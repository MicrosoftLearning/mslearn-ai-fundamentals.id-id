---
lab:
  title: Jelajahi Pembelajaran Mesin Otomatis di Azure Machine Learning
---

# Jelajahi Pembelajaran Mesin Otomatis di Azure Machine Learning

Dalam latihan ini, Anda akan menggunakan fitur pembelajaran mesin otomatis di Azure Machine Learning untuk melatih dan mengevaluasi model pembelajaran mesin. Kemudian, Anda akan menyebarkan dan menguji model terlatih.

Latihan ini seharusnya memakan waktu sekitar **35** menit untuk menyelesaikannya.

## Membuat ruang kerja Pembelajaran Mesin Microsoft Azure

Untuk menggunakan Azure Machine Learning, Anda perlu menyediakan ruang kerja Azure Machine Learning di langganan Azure Anda. Kemudian, Anda akan dapat menggunakan studio Azure Machine Learning untuk bekerja dengan sumber daya di ruang kerja Anda.

> **Tips**: Jika Anda sudah memiliki ruang kerja Azure Machine Learning, Anda dapat menggunakannya dan melompat ke tugas berikutnya.

1. Masuk ke [portal Azure](https://portal.azure.com) di `https://portal.azure.com` menggunakan kredensial Microsoft Anda.

1. Pilih **+ Buat sumber daya**, cari *Azure Machine Learning*, dan buat sumber daya **Azure Machine Learning** baru dengan pengaturan berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Buat atau pilih grup sumber daya*.
    - **Nama**: *Masukkan nama yang unik untuk ruang kerja Anda*.
    - **Wilayah**: AS Timur
    - **Akun penyimpanan**: *Perhatikan akun penyimpanan default baru yang akan dibuat untuk ruang kerja Anda*.
    - **Key vault**: *Perhatikan key vault baru bawaan yang akan dibuat untuk ruang kerja Anda*.
    - **Application insights**: *Perhatikan sumber daya application insights baru bawaan yang akan dibuat untuk ruang kerja Anda*.
    - **Registri kontainer**: Tidak ada (*kontainer akan dibuat secara otomatis saat pertama kali menyebarkan model ke kontainer*).

1. Pilih **Tinjau + buat**, lalu pilih **Buat**. Tunggu hingga ruang kerja Anda dibuat (dapat memakan waktu beberapa menit), lalu buka sumber daya yang disebarkan.

#### Luncurkan studio 

1. Dalam sumber daya ruang kerja Azure Machine Learning, Pilih **Luncurkan studio** (atau buka tab browser baru dan navigasikan ke [https://ml.azure.com](https://ml.azure.com?azure-portal=true), dan sign in ke studio Azure Machine Learning dengan menggunakan akun Microsoft Anda). Tutup pesan apa pun yang ditampilkan.

1. Di studio Azure Machine Learning, Anda akan melihat ruang kerja yang baru dibuat. Jika tidak, pilih **Semua ruang kerja** di menu sebelah kiri lalu pilih ruang kerja yang baru saja Anda buat.

## Menggunakan pembelajaran mesin otomatis untuk melatih model

Pembelajaran mesin otomatis memungkinkan Anda mencoba beberapa algoritma dan parameter untuk melatih beberapa model serta mengidentifikasi model yang terbaik untuk data Anda. Dalam latihan ini, Anda akan menggunakan himpunan data detail persewaan sepeda historis untuk melatih model yang memprediksi jumlah persewaan sepeda yang diharapkan pada hari tertentu, berdasarkan fitur musiman dan meteorologi.

> **Kutipan**: *Data yang digunakan dalam latihan ini berasal dari [Capital Bikeshare](https://www.capitalbikeshare.com/system-data) dan digunakan sesuai dengan [perjanjian lisensi](https://www.capitalbikeshare.com/data-license-agreement)* data yang diterbitkan.

1. Di [studio Azure Machine Learning](https://ml.azure.com?azure-portal=true), lihat halaman **ML Otomatis** (di bawah **Penulisan**).

1. Buat pekerjaan ML Otomatis baru dengan pengaturan berikut, dengan menggunakan **Berikutnya** sesuai kebutuhan untuk maju melalui antarmuka pengguna:

    **Pengaturan dasar**:

    - **Nama Pekerjaan** Bidang nama pekerjaan harus sudah diisi sebelumnya dengan nama unik. Simpan apa adanya.
    - **Nama eksperimen baru**: `mslearn-bike-rental`
    - **Deskripsi**: Pembelajaran mesin otomatis untuk prediksi penyewaan sepeda
    - **Tag**: *tidak ada*

   **Tipe tugas & data**:

    - **Pilih jenis tugas**: Regresi
    - **Pilih himpunan data**: Buat himpunan data baru dengan pengaturan berikut:
        - **Jenis data**:
            - **Nama**: `bike-rentals`
            - **Deskripsi**: `Historic bike rental data`
            - **Jenis**: Tabel (mltable)
        - **Sumber data**:
            - Pilih **Dari file lokal**
        - **Jenis penyimpanan tujuan**:
            - **Jenis datastore**: Azure Blob Storage
            - **Nama**: workspaceblobstore
        - **Pilihan MLtable**:
            - **Unggah folder**: *Unduh dan unzip folder yang berisi dua file yang perlu Anda unggah* `https://aka.ms/bike-rentals`

        Pilih **Buat**. Setelah himpunan data dibuat, pilih himpunan data **bike-rentals** untuk terus mengirimkan pekerjaan ML Otomatis.

    **Pengaturan tugas**:

    - **Jenis tugas**: Regresi
    - **Himpunan data**: bike-rentals
    - **Kolom target**: penyewaan (bilangan bulat)
    - **Setelan konfigurasi tambahan:**
        - **Metrik utama**: NormalizedRootMeanSquaredError
        - **Jelaskan model terbaik**: *Tidak dipilih*
        - **Aktifkan tumpukan ansambel**: *Tidak dipilih*
        - **Gunakan semua model yang didukung**: <u>Tidak</u>dipilih. *Anda akan membatasi pekerjaan untuk mencoba hanya beberapa algoritma tertentu.*
        - **Model yang diizinkan**: *Pilih hanya **RandomForest** dan **LightGBM** — biasanya Anda ingin mencoba sebanyak mungkin, tetapi setiap model yang ditambahkan akan menambah waktu yang dibutuhkan untuk menjalankan pekerjaan.*
    - **Batas**: *Luaskan bagian ini*
        - **Uji coba maksimum**: `3`
        - **Uji coba serentak maksimum**: `3`
        - **Node maksimum**: `3`
        - **Ambang skor metrik**: `0.085` (*sehingga jika model mencapai skor metrik kesalahan kuadrat rata-rata akar yang dinormalisasi sebesar 0,085 atau kurang, pekerjaan berakhir.*)
        - **Batas waktu eksperimen :**: `15`
        - **Batas waktu Iterasi**: `15`
        - **Aktifkan penghentian dini**: *Dipilih*
    - **Validasi dan pengujian**:
        - **Jenis validasi**: Pembagian validasi kereta
        - **Persentase data validasi**: 10
        - **Menguji himpunan data**: Tidak ada

    **Komputasi:**

    - **Pilih jenis komputasi**: Tanpa server
    - **Jenis mesin virtual**: CPU
    - **Tingkatan mesin virtual**: Khusus
    - **Ukuran mesin virtual**: Standard_DS3_V2\*
    - **Jumlah instans**: 1

    \* *Jika langganan Anda membatasi ukuran VM yang tersedia untuk Anda, pilih ukuran mana pun yang tersedia.*

1. Kirim pekerjaan pelatihan. Proses ini dimulai secara otomatis.

1. Tunggu pekerjaan selesai. Mungkin perlu waktu — sekarang mungkin saat yang tepat untuk istirahat sejenak!

## Meninjau model terbaik

Ketika pekerjaan pembelajaran mesin otomatis telah selesai, Anda dapat meninjau model terbaik yang dilatih.

1. Di tab **Ringkasan** tugas pembelajaran mesin otomatis, perhatikan ringkasan model terbaik.
    ![Cuplikan layar ringkasan model terbaik dari tugas pembelajaran mesin otomatis dengan kotak di sekitar nama algoritma.](./media/use-automated-machine-learning/complete-run.png)
  
1. Pilih teks di bawah **Nama algoritma** untuk model terbaik guna melihat detailnya.

1. Pilih tab **Metrik** dan pilih bagan **residuals** dan **predicted_true** jika belum dipilih.

    Tinjau grafik yang menunjukkan performa model. Bagan **residual** menunjukkan *residual* (perbedaan antara nilai yang diprediksi dan nilai sebenarnya) dalam histogram. Bagan **predicted_true** membandingkan nilai yang diprediksi dengan nilai true.

## Terapkan dan uji model

1. Pada tab **Model** untuk model terbaik yang dilatih oleh pekerjaan pembelajaran mesin otomatis Anda, pilih **Sebarkan** dan gunakan opsi **Titik akhir real-time** untuk menyebarkan model dengan pengaturan berikut:
    - **Komputer virtual**: Standard_DS3_v2
    - **Jumlah instans**: 3
    - **Titik akhir**: Baru
    - **Nama titik akhir**: *Biarkan default atau pastikan unik secara global*
    - **Nama penyebaran**: *Biarkan default*
    - **Inferensi pengumpulan data**: *Nonaktifkan*
    - **Model Paket**: *Nonaktifkan*

    > **Catatan** Jika Anda menerima pesan bahwa tidak ada cukup kuota untuk memilih mesin virtual *Standard_DS3_v2*, pilih mesin virtual yang berbeda.

1. Tunggu penyebaran dimulai - ini mungkin memakan waktu beberapa detik. **Status penyebaran** untuk titik akhir**predict-rentals** akan ditunjukkan di bagian utama halaman sebagai *Berjalan*.
1. Tunggu hingga **Status penyebaran** berubah menjadi *Berhasil*. Proses ini dapat memakan waktu 5-10 menit.

## Menguji layanan yang disebarkan

Sekarang Anda dapat menguji layanan yang disebarkan.

1. Di studio Azure Machine Learning, di menu sebelah kiri, pilih **Titik akhir** dan buka titik akhir real time **predict-rentals**.

1. Pada halaman titik akhir real time **predict-rentals** tampilkan tab **Pengujian**.

1. Di panel **Input data ke titik akhir pengujian**, ganti templat JSON dengan data input berikut:

    ```json
      {
     "input_data": {
       "columns": [
         "day",
         "mnth",
         "year",
         "season",
         "holiday",
         "weekday",
         "workingday",
         "weathersit",
         "temp",
         "atemp",
         "hum",
         "windspeed"
       ],
       "index": [0],
       "data": [[1,1,2022,2,0,1,1,2,0.3,0.3,0.3,0.3]]
     }
    }

    ```

1. Klik tombol **Uji**.

1. Tinjau hasil pengujian, yang mencakup perkiraan jumlah persewaan berdasarkan fitur input - mirip dengan ini:

    ```JSON
    [
      352.3564674945718
    ]
    ```

    Panel pengujian mengambil data input dan menggunakan model yang Anda latih untuk menampilkan perkiraan jumlah persewaan.

Mari kita tinjau yang telah Anda lakukan. Anda menggunakan himpunan data tentang data penyewaan sepeda historis untuk melatih model. Model ini memprediksi jumlah penyewaan sepeda yang diharapkan pada hari tertentu, berdasarkan *fitur* musiman dan meteorologi.

## Pembersihan

Layanan web yang Anda buat dihost dalam *Azure Container Instance*. Jika tidak berniat untuk bereksperimen dengan ini lebih lanjut, Anda harus menghapus titik akhir untuk menghindari mengumpulkan penggunaan Azure yang tidak perlu.

1. Di [studio Azure Machine Learning](https://ml.azure.com?azure-portal=true), di tab **Titik Akhir**, pilih titik akhir **predict-rentals**. Kemudian pilih **Hapus** dan konfirmasikan bahwa Anda ingin menghapus titik akhir.

    Menghapus komputasi memastikan langganan Anda tidak akan ditagih untuk sumber daya komputasi. Namun, Anda akan dikenakan biaya kecil untuk penyimpanan data selama ruang kerja Azure Machine Learning ada di langganan Anda. Jika telah selesai menjelajahi Azure Machine Learning, Anda dapat menghapus ruang kerja Azure Machine Learning dan sumber daya terkait.

Untuk menghapus ruang kerja Anda:

1. Di [portal Microsoft Azure](https://portal.azure.com?azure-portal=true), di halaman **Grup sumber daya**, buka grup sumber daya yang Anda tentukan saat membuat ruang kerja Azure Machine Learning Anda.
2. Klik **Hapus grup sumber daya**, ketik nama grup sumber daya untuk mengonfirmasi bahwa Anda ingin menghapusnya, dan pilih **Hapus**.
