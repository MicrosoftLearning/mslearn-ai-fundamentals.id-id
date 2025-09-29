---
lab:
  title: Mengekstrak data dengan Pemahaman Konten di portal Azure AI Foundry
---

# Mengekstrak data dengan Pemahaman Konten di portal Azure AI Foundry

Pemahaman Konten Azure AI menyediakan analisis multimodal dokumen, file audio, video, dan gambar untuk mengekstrak informasi.

Dalam latihan ini, Anda akan menggunakan Pemahaman Konten Azure AI di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk mengekstrak informasi dari faktur. 

Latihan ini membutuhkan waktu sekitar **25** menit.

## Membuat proyek Azure AI Foundry untuk pemahaman konten

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup semua tips atau panel mulai cepat yang terbuka saat pertama kali Anda masuk, dan jika perlu, gunakan logo **Azure AI Foundry** di kiri atas untuk menavigasi ke beranda, yang tampilannya mirip dengan gambar berikut (tutup panel **Bantuan** jika terbuka):

    ![Cuplikan layar beranda portal Azure AI Foundry.](./media/ai-foundry-portal.png)

1. Gulir ke bagian bawah halaman, dan pilih petak **Jelajahi Layanan Azure AI**.

    ![Cuplikan layar petak Jelajahi Layanan Azure AI.](./media/ai-services.png)

1. Pada halaman Layanan Azure AI, pilih **Coba Pemahaman Konten**.

    ![Cuplikan layar tombol Coba Pemahaman Konten.](./media/try-content-understanding.png)

1. Di halaman Pemahaman Konten, pilih **Buat proyek untuk memulai**. Kemudian dalam dialog **Buat proyek**, pilih jenis sumber daya yang direkomendasikan (**sumber daya Azure AI Foundry**):

    ![Cuplikan layar hasil analisis.](./media/resource-type.png)

1. Pada halaman **Berikutnya**, masukkan nama yang valid untuk proyek Anda. Lalu pilih **Opsi tingkat lanjut** dan tentukan pengaturan berikut:
    - **Sumber daya Azure AI Foundry**: *Nama yang valid untuk sumber daya Azure AI Foundry Anda*
    - **Langganan**: *Langganan Azure Anda*
    - **Grup sumber daya**: *Buat atau pilih grup sumber daya*
    - **Wilayah**: Pilih salah satu lokasi berikut\*:
        * US Barat
        * Swedia Tengah
        * Australia Timur

    \**Pada saat penulisan konten ini, Pemahaman Konten didukung di wilayah-wilayah ini.*

    ![Cuplikan layar pengaturan proyek.](./media/content-project-settings.png)

1. Pilih **Buat**. Tunggu hingga proses penyiapan selesai. Proses ini memerlukan waktu beberapa menit.

## Mengekstrak informasi dari faktur

1. Unduh [contoso-invoice-1.pdf](https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-1.pdf) dari `https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/refs/heads/main/data/contoso-invoice-1.pdf`. 

1. Pada halaman Pemahaman Konten, pilih tab **Coba**, lalu pilih petak **Ekstraksi Data Faktur**.

    ![Cuplikan layar halaman "Coba" Pemahaman Konten.](./media/content-understanding-invoice.png)

    Sampel faktur disediakan.

1. Pilih sampel faktur dan gunakan tombol **Jalankan analisis** untuk mengekstrak informasi dari faktur tersebut. Jika analisis sudah selesai, lihat hasilnya.

    ![Cuplikan layar hasil analisis sampel faktur.](./media/sample-invoice-analysis.png)

1. Gunakan tautan **Telusuri file** untuk mengunggah dokumen **contoso-invoice-1.pdf** yang Anda unduh sebelumnya, dan jalankan analisis pada file tersebut.

    ![Cuplikan layar hasil analisis faktur Contoso.](./media/contoso-invoice-analysis.png)

    Perhatikan bahwa penganalisis Pemahaman Konten dapat mengekstrak informasi dari faktur ini, meskipun diformat secara berbeda dari sampel.

1. Di panel sebelah kanan tempat bidang yang diekstrak ditampilkan, lihat tab **Hasil** untuk melihat respons JSON yang akan dikirim ke aplikasi klien. Pengembang akan menulis kode untuk memproses respons ini dan melakukan sesuatu dengan bidang yang diekstrak.

    ![Cuplikan layar hasil analisis faktur Contoso.](./media/invoice-analysis-json.png)

## Penghapusan

Jika Anda sudah selesai bekerja dengan layanan Pemahaman Konten, Anda harus menghapus sumber daya yang telah Anda buat dalam latihan ini untuk menghindari timbulnya biaya Azure yang tidak perlu.

- Di portal Azure, hapus grup sumber daya yang Anda buat dalam latihan ini.
