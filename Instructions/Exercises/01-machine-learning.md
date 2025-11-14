---
lab:
  title: Jelajahi Pembelajaran Mesin Otomatis
---

# Jelajahi Pembelajaran Mesin Otomatis

Dalam latihan ini, Anda akan menggunakan pembelajaran mesin otomatis untuk melatih dan mengevaluasi model pembelajaran mesin. Kemudian, Anda akan menyebarkan dan menguji model terlatih.

> **Catatan**: Latihan ini dirancang untuk memandu Anda melalui langkah-langkah untuk melatih dan menguji model menggunakan ***Azure Machine Learning***. Jika memiliki langganan Azure dengan izin akses yang memadai, Anda dapat menyediakan ruang kerja Azure Machine Learning dan menggunakannya untuk latihan. Namun, Azure Machine Learning dirancang untuk solusi pembelajaran mesin skala perusahaan yang melibatkan sejumlah besar data dan komputasi berbasis cloud. Beberapa operasi di Azure Machine Learning memerlukan komputasi provisi, yang dapat memakan waktu cukup lama. Jika Anda tidak memiliki akses ke Azure, atau memiliki waktu terbatas untuk menyelesaikan latihan, aplikasi ***ML Lab*** berbasis browser yang memiliki fungsionalitas inti Azure ML yang digunakan dalam latihan ini juga disediakan. Anda juga dapat menggunakannya untuk melatih dan menguji model pembelajaran mesin nyata, seperti yang dilakukan di Azure ML. Meskipun tidak *identik* dengan Azure Machine Learning, antarmuka pengguna di ML Lab cukup mirip untuk membuat transisi ke Azure Machine Learning intuitif. Perhatikan bahwa aplikasi ML Lab dijalankan di browser, jadi memuat ulang halaman kapan saja akan membuat aplikasi di-restart!

Latihan ini memerlukan waktu sekitar **35** menit untuk diselesaikan (lebih cepat jika Anda menggunakan aplikasi ML Lab berbasis browser).

## Membuat ruang kerja

Ruang kerja digunakan untuk menyimpan semua sumber daya pembelajaran mesin Anda di satu tempat, sehingga memudahkan pengelolaan data, kode, model, dan aset lainnya.

1. Buka portal untuk lingkungan yang ingin Anda gunakan di lab ini, dan masuk jika diminta:
    - [Azure Machine Learning Studio](https://ml.azure.com){:target="_blank"} berbasis Azure di `https://ml.azure.com`
    - [ML Lab](https://aka.ms/ml-lab){:target="_blank"} berbasis browser di `https://aka.ms/ml-lab`

    > **Tips**: Jika studio Azure Machine Learning terbuka di ruang kerja yang sudah ada, navigasikan ke halaman **Semua ruang kerja**.

1. Buat ruang kerja baru dengan nama yang sesuai.

    Jika menggunakan Azure Machine Learning, Anda tidak memerlukan *Hub* untuk latihan ini. Pilih pengaturan tingkat lanjut yang sesuai berdasarkan batasan kebijakan apa pun di langganan Azure Anda.

1. Setelah ruang kerja dibuat, pilih ruang kerja tersebut untuk menampilkan halaman **Beranda**.

    Perhatikan bahwa ruang kerja memiliki beberapa halaman yang ditampilkan di panel navigasi di sebelah kiri. Anda dapat memperluas dan menciutkan panel ini dengan menggunakan menu **&#9776;** di bagian atas.

## Mengunduh data

Dalam latihan ini, Anda akan menggunakan himpunan data penjualan es krim untuk melatih model yang memprediksi permintaan es krim pada hari tertentu, berdasarkan fitur musiman dan meteorologi.

1. Di tab browser baru, unduh **[ml-data.zip](https://aka.ms/mslearn-ml-data)** dari `https://aka.ms/mslearn-ml-data` ke komputer lokal Anda.
1. Ekstrak arsip **ml-data.zip** yang diunduh untuk melihat file yang ada di dalamnya. Perhatikan bahwa ada file **ice-cream.csv** di antara file-file tersebut, yang berisi data penjualan es krim yang diperlukan untuk latihan ini.

## Menggunakan pembelajaran mesin otomatis untuk melatih model

Pembelajaran mesin otomatis memungkinkan Anda mencoba beberapa algoritma dan parameter untuk melatih beberapa model serta mengidentifikasi model yang terbaik untuk data Anda.

1. Di portal, lihat halaman **ML Otomatis** (di bawah **Penulisan**).

1. Buat pekerjaan ML Otomatis baru dengan pengaturan berikut, dengan menggunakan **Berikutnya** sesuai kebutuhan untuk maju melalui antarmuka pengguna:

    > **Tips**: Jika tidak ada informasi eksplisit untuk pengaturan yang disediakan dalam langkah-langkah di bawah ini, gunakan nilai default.

    **Pengaturan dasar**:

    - Tetapkan **nama tugas** unik untuk tugas pembelajaran mesin otomatis Anda

   **Tipe tugas & data**:

    - Atur tipe tugas ke **Regresi**.
    - Buat aset data ***tabular*** baru bernama **ice-cream**
        - Unggah file **ice-cream.csv** lokal ke penyimpanan ruang kerja default.
        - Sertakan <u>hanya</u> kolom berikut (*Tanggal* tidak sama untuk setiap baris dan menambahkan sedikit kemampuan prediktif dengan sendirinya):
            - **DayOfWeek**
            - **Bulan**
            - **Suhu**
          
            - **Rainfall**
            - **IceCreamsSold**
        - Buat aset data.
    - Pastikan aset data **ice-cream** yang baru dibuat dipilih sebelum melanjutkan ke langkah berikutnya

    > **Catatan**: Jika Anda bukan administrator di langganan Azure yang digunakan, akses berbasis kunci ke penyimpanan mungkin telah dilarang oleh kebijakan. Jika demikian, Anda harus berkolaborasi dengan administrator untuk mengizinkan akses berbasis kunci atau mengonfigurasi ulang ruang kerja Azure Machine Learning Anda untuk menggunakan autentikasi Entra ID untuk mengakses penyimpanan. Jika Anda tidak dapat melakukan ini, gunakan aplikasi ***ML Lab*** berbasis browser untuk latihan ini.

    **Pengaturan tugas**:

    - Atur **kolom target** (label yang ingin diprediksi model) ke **IceCreamsSold**.
    - Atur **Pengaturan konfigurasi tambahan**:
        - Atur **Metrik utama** ke metrik yang ingin Anda gunakan untuk mengevaluasi performa model. Dalam latihan ini, gunakan skor *R<sup>2</sup>*.
        - Pilih algoritma model yang ingin Anda coba (atau biarkan semuanya dipilih)
    - Atur **Pengaturan fiturisasi**:
        - Gunakan pengaturan ini untuk menyesuaikan fiturisasi (cara fitur data disiapkan untuk pelatihan model)
    - Atur **Batas**:
        - Gunakan batas untuk mengakhiri tugas pelatihan lebih awal berdasarkan kriteria tertentu. Dalam latihan ini, atur batas berikut:
            - **Ambang skor metrik**: 0.9
            - **Batas waktu eksperimen (menit)**: 15
        
        > **Perhatikan** Penting untuk menetapkan batas ini saat menggunakan Azure Machine Learning, karena menjalankan tugas pelatihan untuk setiap kemungkinan kombinasi algoritma dan fiturisasi berpotensi memakan waktu berjam-jam!

    **Komputasi:**

    - Gunakan komputasi **Tanpa Server**

    **Tinjau**
          

    - Tinjau pengaturan dan periksa dengan saksama. Kemudian kirimkan tugas pelatihan. Proses ini dimulai secara otomatis.

1. Tunggu pekerjaan selesai.

    > **Tips**: Mungkin diperlukan waktu yang cukup lama jika Anda menggunakan Azure Machine Learning. Sekarang mungkin saat yang tepat untuk minum kopi!

## Meninjau model terbaik

Ketika pekerjaan pembelajaran mesin otomatis telah selesai, Anda dapat meninjau model terbaik yang dilatih.

1. Pada tab **Gambaran Umum** di halaman detail tugas, lihat informasi tentang tugas dan perhatikan ringkasan model terbaik.
  
1. Pilih **nama Algoritme** untuk model terbaik untuk melihat detailnya. Kemudian pada halaman detail tugas turunan, lihat tab berikut:
    - **Gambaran Umum**: Detail umum untuk tugas turunan.
    - **Model**: Informasi tentang model yang dilatih.
    - Metrik dan visualisasi Evaluasi **Metrik** untuk model berdasarkan data pengujian yang digunakan selama proses pelatihan.
    - **Output dan log**: Informasi yang dicatat selama proses pelatihan.

## Terapkan dan uji model

1. Pada tab **Model** untuk model terbaik yang dilatih oleh tugas pembelajaran mesin otomatis Anda, pilih **Sebarkan** untuk menyebarkan model ke titik akhir Real-time.

    Pilih opsi **Instans** dan **Mesin virtual** yang sesuai untuk komputasi tempat titik akhir yang disebarkan akan dijalankan (yang mungkin bergantung pada kuota yang tersedia di langganan Azure Anda), dan tetapkan **titik akhir** dan nama **penyebaran** yang sesuai.

1. Tunggu pemberitahuan bahwa penyebaran telah selesai.

    > **Tips**: Di studio Azure Machine Learning, penyebaran titik akhir mungkin memerlukan waktu 5-10 menit.

## Menguji layanan yang disebarkan

Sekarang Anda dapat menguji layanan yang disebarkan.

1. Di menu navigasi, pilih halaman **Titik Akhir** dan buka titik akhir real time yang Anda buat.

1. Pada halaman titik akhir, lihat tab **Pengujian**.

1. Di panel **Input data ke titik akhir pengujian**, ganti templat JSON dengan data input berikut:

    ```json
   {
     "input_data": {
        "columns": [
            "DayOfWeek",
            "Month",
            "Temperature",
            "Rainfall"
        ],
        "index": [0],
        "data": [["Wednesday","June",70.5,0.05]]
     }
   }
    ```

1. Klik tombol **Uji**.

1. Tinjau hasil pengujian, yang mencakup perkiraan jumlah persewaan berdasarkan fitur input - mirip dengan ini:

    ```JSON
   [
       120.16208168753236
   ]
    ```

    Panel pengujian mengambil data input dan menggunakan model yang Anda latih untuk menampilkan perkiraan jumlah persewaan.

## Tampilkan kode untuk menggunakan model

Setelah Anda memiliki model prediktif, pengembang dapat membangun aplikasi yang menggunakannya.

1. Pada halaman titik akhir real time tampilkan tab **Konsumsi**.
1. Tinjau kode sampel untuk menggunakan model Anda.

## Jika waktu memungkinkan

Jika Anda ingin bereksperimen lebih lanjut dengan pembelajaran mesin otomatis, coba latih model **klasifikasi** berdasarkan file **penguins.csv** yang disertakan dalam arsip **ml-data.zip** yang Anda unduh sebelumnya. Gunakan semua kolom dalam himpunan data ini.

Setelah melatih dan menyebarkan model klasifikasi, Anda dapat mengujinya di titik akhir dengan JSON berikut:

```json
{
    "input_data": {
    "columns": [
        "CulmenLength",
        "CulmenDepth",
        "FlipperLength",
        "BodyMass"
    ],
    "index": [0],
    "data": [[45.2,13.8,215,4750]]
    }
}
```

## Pembersihan

Jika menggunakan Azure Machine Learning untuk menyelesaikan latihan ini, Anda harus menghapus sumber daya yang dibuat untuk menghindari akumulasi penggunaan Azure yang tidak perlu.

1. Di [studio Azure Machine Learning](https://ml.azure.com), di tab **Titik Akhir**, pilih titik akhir yang Anda sebarkan. Kemudian pilih **Hapus** dan konfirmasikan bahwa Anda ingin menghapus titik akhir.

    Menghapus komputasi memastikan langganan Anda tidak akan ditagih untuk sumber daya komputasi. Namun, Anda akan dikenakan biaya kecil untuk penyimpanan data selama ruang kerja Azure Machine Learning ada di langganan Anda. Jika telah selesai menjelajahi Azure Machine Learning, Anda dapat menghapus ruang kerja Azure Machine Learning dan sumber daya terkait.

Untuk menghapus ruang kerja Anda:

1. Di [portal Microsoft Azure](https://portal.azure.com), di halaman **Grup sumber daya**, buka grup sumber daya yang Anda tentukan saat membuat ruang kerja Azure Machine Learning Anda.
2. Klik **Hapus grup sumber daya**, ketik nama grup sumber daya untuk mengonfirmasi bahwa Anda ingin menghapusnya, dan pilih **Hapus**.
