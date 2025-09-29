---
lab:
  title: Menjelajahi ucapan di portal Azure AI Foundry
---

# Menjelajahi ucapan di portal Azure AI Foundry

Azure AI Speech mentranskripsikan ucapan menjadi teks dan mengubah teks menjadi ucapan yang dapat didengar. Anda dapat menggunakan Azure AI Speech untuk membuat aplikasi yang dapat mentranskripsikan notulensi rapat atau menghasilkan teks dari rekaman wawancara, atau untuk mendukung asisten AI interaktif yang dapat menanggapi perintah dan kueri lisan.

Dalam latihan ini, Anda akan menggunakan Azure AI Speech di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk menjelajahi kemampuan utama Azure AI Speech. 

Latihan ini memakan waktu sekitar **15** menit.

## Membuat proyek di portal Azure AI Foundry

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup semua tips atau panel mulai cepat yang terbuka saat pertama kali Anda masuk, dan jika perlu, gunakan logo **Azure AI Foundry** di kiri atas untuk menavigasi ke beranda, yang tampilannya mirip dengan gambar berikut (tutup panel **Bantuan** jika terbuka):

    ![Cuplikan layar beranda portal Azure AI Foundry.](./media/ai-foundry-portal.png)

1. Gulir ke bagian bawah halaman, dan pilih petak **Jelajahi Layanan Azure AI**.

    ![Cuplikan layar petak Jelajahi Layanan Azure AI.](./media/ai-services.png)

1. Di halaman Layanan Azure AI, pilih petak **Ucapan**.

    ![Cuplikan layar petak Ucapan.](./media/speech.png)

1. Pada halaman **Ucapan**, pilih **Buka playground Ucapan**. Kemudian, saat diminta, buat proyek baru dengan pengaturan berikut:
    - **Nama proyek**: *Masukkan nama yang valid untuk proyek Anda.*
    - **Pengaturan tingkat lanjut**:
        - **Langganan**: *Langganan Azure Anda*
        - **Grup sumber daya**: *Buat atau pilih grup sumber daya*
        - **Wilayah**: *Pilih wilayah **AI Foundry yang direkomendasikan***
        - **AI Foundry atau Azure OpenAI** *Buat sumber daya Azure AI Foundry baru dengan nama yang valid*

1. Pilih **Buat**. Tunggu proyek Anda dibuat. Proses ini memerlukan waktu beberapa menit.

1. Saat proyek dibuat, Anda akan dibawa ke playground **Ucapan** (jika tidak, di panel tugas di sebelah kiri, pilih **Playground** dan buka playground Ucapan dari sana.)

    Speech playground adalah antarmuka pengguna yang memungkinkan Anda mencoba beberapa kemampuan Azure AI Speech.  

## Jelajahi ucapan ke teks di Azure AI Foundry's Speech Playground

Mari kita coba *ucapan ke teks* di Azure AI Foundry's Speech Playground.

1. Di tab browser baru, unduh **[speech.zip](https://aka.ms/mslearn-speech-files)** dari `https://aka.ms/mslearn-speech-files` di tab browser baru. Setelah diunduh, ekstrak file ke folder lokal. 

1. Kembali ke portal Azure AI Foundry, di halaman Ucapan, pada tab **Ucapan ke teks**, pilih **Transkripsi real time**.

1. Di bawah **Unggah file**, pilih **Telusuri file** dan unggah **WhatAICanDo.m4a** dari folder untuk diunduh dan diekstrak.

    Layanan Ucapan mentranskripsikan dan menampilkan teks secara real time. Jika Anda memiliki audio di komputer, Anda dapat mendengarkan rekaman saat teks sedang ditranskripsikan.

    ![Cuplikan layar antarmuka Transkripsi real time di playground Ucapan.](./media/real-time-transcription.png)

1. Tinjau output. 

    >*Tips*: Untuk melihat output lengkap, Anda mungkin perlu meminimalkan panel *Konfigurasi*. Untuk meminimalkan, pilih ikon di sebelah kanan judul*Konfigurasi*.

    Dalam output, di bawah **Teks**, Anda dapat melihat audio yang ditranskripsi menjadi teks.

## Menjelajahi kemampuan teks ke ucapan di Playground Ucapan Azure AI Foundry

Mari kita lihat bagaimana Azure AI Speech dapat menghasilkan ucapan yang dapat didengar dari teks.

1. Di playground Ucapan, pilih tab **Teks ke ucapan** dan pastikan **Galeri suara** dipilih.
1. Lihat suara yang tersedia, dan pilih satu suara (seperti *Ava Multibahasa*).
1. Di panel **Detail suara**, pilih tab **Coba**. Kemudian masukkan beberapa teks (misalnya, `The rain in Spain stays mainly in the plain`) dan gunakan tombol **Putar** untuk menghasilkan ucapan dari teks.

    ![Cuplikan layar antarmuka Galeri suara di playground Ucapan.](./media/voice-gallery.png)

    Teks diucapkan menggunakan suara yang dipilih. Anda dapat mencoba suara lain untuk membandingkan output ucapan.

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih **Hapus grup sumber daya**, lalu **masukkan nama grup sumber daya** untuk mengonfirmasi. Grup sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Latihan ini hanya menunjukkan beberapa kemampuan layanan Ucapan. Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman Ucapan](https://azure.microsoft.com/services/cognitive-services/speech-services).
