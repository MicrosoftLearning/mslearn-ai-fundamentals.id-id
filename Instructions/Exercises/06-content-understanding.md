---
lab:
  title: Mengekstrak data dengan Pemahaman Konten di portal Azure AI Foundry
---

# Mengekstrak data dengan Pemahaman Konten di portal Azure AI Foundry

**Pemahaman Konten Azure AI (pratinjau)** menggunakan AI generatif untuk memproses konten dari berbagai jenis (dokumen, gambar, video, dan audio) menjadi format output yang ditentukan pengguna.

Dalam latihan ini, Anda akan menggunakan Pemahaman Konten Azure AI di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk mengenali data dari faktur. 

Latihan ini membutuhkan waktu sekitar **25** menit.

## Membuat proyek Azure AI Foundry dan tugas pemahaman konten

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup semua tips atau panel mulai cepat yang terbuka saat pertama kali Anda masuk, dan jika perlu, gunakan logo **Azure AI Foundry** di kiri atas untuk menavigasi ke beranda, yang tampilannya mirip dengan gambar berikut (tutup panel **Bantuan** jika terbuka):

    ![Tnagkapan layar beranda Azure AI Foundry dengan agen terpilih.](./media/azure-ai-foundry-home-page.png)

1. Di jendela browser baru, buka [halaman eksplorasi Layanan Azure AI](https://ai.azure.com/explore/aiservices).

1. Pada halaman *Layanan AI*, pilih petak *Coba Pemahaman Konten*.

1. Pilih **Pilih atau buat proyek untuk memulai**. 

1. Pilih **+ Buat proyek**.

1. Di wizard, masukkan nama yang valid untuk proyek Anda. 

1. Klik **Opsi Tingkat Lanjut** dan tentukan pengaturan berikut:
    - **Sumber daya Azure AI Foundry**: *Pertahankan nama default*
    - **Langganan**: *Langganan Azure Anda*
    - **Grup sumber daya**: *Buat atau pilih grup sumber daya*
    - **Wilayah**: Pilih salah satu wilayah berikut:
        * US Barat
        * Swedia Tengah
        * Australia Timur

1. Pilih **Buat**. Tunggu hingga proses penyiapan selesai. Proses ini memerlukan waktu beberapa menit.

    >**Catatan**: Jika Anda mendapat kesalahan izin, pilih tombol **Perbaiki** untuk menambahkan izin yang sesuai untuk melanjutkan.

1. Setelah proyek Anda dibuat, Anda akan diarahkan secara default ke jendela pembuatan tugas pemahaman konten. Gunakan pengaturan berikut untuk membuat tugas pemahaman konten:
    - **Nama tugas**: `contoso-invoice`
    - **Deskripsi**: `An invoice analysis task`
    - *Pilih Analisis konten file tunggal*
    - **Pengaturan tingkat lanjut**: *pertahankan default*.

1. Pilih **Create**, dan tunggu tugas Anda dibuat. 

1. Pilih tugas **contoso-invoice** Anda. 

## Menganalisis faktur dengan Pemahaman Konten Azure AI di Azure AI Foundry 

Misalkan Anda ingin mengekstrak data dari banyak faktur dan memasukkan data ke dalam database. Anda dapat menggunakan Pemahaman Konten Azure AI untuk menganalisis satu faktur dan membuat penganalisis Anda sendiri yang dapat menganalisis faktur serupa lainnya. Mari mulai dengan menentukan skema Anda.

#### Tentukan skema Anda 

1. Pada halaman *Define Schema* , Anda dapat menambahkan file uji. Unduh [contoso-invoice-1.pdf](https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-1.pdf) dari `https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-1.pdf`. 

1. Unggah file ke halaman **define schema**. Pilih templat **Ekstraksi data faktur**. Templat ekstraksi data faktur memiliki bidang data yang telah dipilih sebelumnya yang akan coba dideteksi oleh penganalisis. 

    ![Cuplikan layar halaman define schema di alat pemahaman konten.](./media/content-understanding/define-schema.png)

1. Pilih **Buat**. Sekarang Anda memiliki kemampuan untuk mengubah skema dengan menambahkan atau menghapus bidang. Setelah selesai meninjau bidang, pilih **Save**.

    ![Cuplikan layar halaman define schema yang ditentukan setelah memilih create.](./media/content-understanding/define-schema-2.png)

1. Tunggu analisisnya berjalan. Ini mungkin memerlukan waktu beberapa saat.

#### Uji Penganalis 

1. Setelah analisis selesai, Anda dapat melihat bagaimana kinerja penganalisis di halaman *Test Analyzer* . Tinjau tab *Bidang* (*Catatan*: Anda mungkin perlu memperluas jendela untuk melihat hasil lengkapnya). Apakah data ini telah sesuai dengan yang ada di faktur? 
    ![Cuplikan layar halaman test analzyer dengan tab hasil bidang disorot.](./media/content-understanding/test-analyzer-fields.png)

1. Perhatikan *skor keyakinan* di samping setiap bidang. Skor keyakinan menunjukkan seberapa yakin model tersebut memiliki hasil yang akurat. Hasil dengan skor keyakinan yang mendekati 100% menunjukkan keyakinan yang lebih besar dalam prediksi.

1. Tinjau tab *Hasil*. Informasi yang sama yang Anda lihat dirender di tab bidang, ada di tab hasil dalam format JSON. JSON menunjukkan bagaimana tampilan informasi saat dikirim ke dan dari aplikasi klien. 

    ![Cuplikan layar halaman test analzyer dengan tab hasil disorot.](./media/content-understanding/test-analyzer-result.png)

1. Layanan Pemahaman Konten seharusnya telah mengidentifikasi dengan benar teks yang sesuai dengan bidang dalam skema. Jika belum melakukannya, Anda dapat menggunakan halaman *Data label* untuk mengunggah formulir sampel lain dan secara eksplisit mengidentifikasi teks yang benar untuk setiap bidang. Ketika sudah puas dengan kemampuan penganalisis dalam mendeteksi data dalam faktur, pilih tab **Daftar penganalisis**. 

#### Membuat penganalisis Anda 

Sekarang, setelah Anda melatih model untuk mengekstrak bidang dari contoh faktur, Anda dapat membuat penganalisis untuk digunakan dengan formulir serupa. Dengan membuat penganalisis, Anda dapat menyebarkan model dan menggunakannya untuk mengotomatiskan tugas faktur lainnya.

1. Di tab *Daftar penganalisis*, pilih **+ Buat Penganalisis**. Masukkan yang berikut: 
    - **Nama**: `invoice-analyzer`
    - **Deskripsi**: `An invoice analyzer`

    ![Cuplikan layar dari halaman build analzyer.](./media/content-understanding/build-analyzer.png)

1. Pilih **Kompilasi**. Tunggu hingga penganalisis baru siap (gunakan tombol Refresh untuk memeriksa). Penganalisis Anda menggunakan model prediktif yang didasarkan pada skema yang telah Anda tentukan dan mengujinya di langkah-langkah sebelumnya. 
1. Sekarang mari kita coba menguji penganalisis yang Anda buat. Unduh faktur yang berbeda dari Contoso [contoso-invoice-2.pdf](https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-2.pdf) dari `https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-2.pdf`.
1. Kembali ke halaman *Daftar penganalisis* dan pilih tautan penganalisis faktur. Bidang yang ditentukan dalam skema penganalisis akan ditampilkan.
1. Di halaman invoice-analyzer, pilih *Test*.
1. Gunakan tombol **+ Upload test files** untuk mengunggah *contoso-receipt-2.pdf*. Pilih **Run analysis** untuk mengekstrak data bidang dari formulir pengujian. Tinjau hasil dari pengujian.

    ![Cuplikan layar hasil pengujian untuk penganalisis yang telah Anda buat.](./media/content-understanding/build-analyzer-2.png)

1. Pilih tab *Code example*. Cari *endpoint* dalam kode. Dalam fase *Build analyzer* dalam proses ini, Anda menyebarkan model pemahaman konten ke titik akhir. Titik akhir dapat digunakan dalam kode yang mirip dengan apa yang Anda lihat dalam contoh untuk menggabungkan model ke dalam proses yang dapat diulang dalam aplikasi.  

    ![Cuplikan layar contoh kode untuk penganalisis yang telah Anda buat.](./media/content-understanding/code-example.png)

## Penghapusan

Jika Anda sudah selesai bekerja dengan layanan Pemahaman Konten, Anda harus menghapus sumber daya yang telah Anda buat dalam latihan ini untuk menghindari timbulnya biaya Azure yang tidak perlu.

- Di portal Azure AI Foundry, navigasikan ke proyek contoso-receipt, lalu hapus.
- Di portal Azure, hapus grup sumber daya yang Anda buat dalam latihan ini.
