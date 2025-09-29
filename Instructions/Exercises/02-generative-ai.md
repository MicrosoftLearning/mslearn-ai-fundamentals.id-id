---
lab:
  title: Menjelajahi AI generatif di portal Azure AI Foundry
---

# Menjelajahi AI generatif di Portal Azure AI Foundry

AI Generatif menjelaskan kategori kemampuan dalam AI yang membuat konten. Orang sering berinteraksi dengan AI generatif yang telah diintegrasikan ke dalam aplikasi obrolan. Dalam latihan ini, Anda mencoba AI generatif di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas. 

Latihan ini memakan waktu sekitar **20** menit.

## Membuat proyek di portal Azure AI Foundry

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup semua tips atau panel mulai cepat yang terbuka saat pertama kali Anda masuk, dan jika perlu, gunakan logo **Azure AI Foundry** di kiri atas untuk menavigasi ke beranda, yang tampilannya mirip dengan gambar berikut (tutup panel **Bantuan** jika terbuka):

    ![Cuplikan layar beranda portal Azure AI Foundry.](./media/ai-foundry-portal.png)

1. Di bagian **Jelajahi model dan kemampuan**, cari `gpt-4o`. Kemudian, dalam hasil pencarian, pilih model **gpt-4o** untuk melihat detailnya.

    ![Cuplikan layar halaman detail gpt-4o.](./media/gpt-4o-details.png)

1. Pilih **Gunakan model ini**.

1. Di wizard,**Buat proyek**dan masukkan nama yang valid untuk proyek Anda. Kemudian perluas **Opsi tingkat lanjut** untuk menentukan pengaturan berikut untuk proyek Anda:
    - **Sumber daya Azure AI Foundry**: *Masukkan nama yang valid untuk sumber daya AI Foundry Anda.*
    - **Langganan**: *Langganan Azure Anda*
    - **Grup sumber daya**: *Buat atau pilih grup sumber daya*
    - **Wilayah**: Pilih salah satu wilayah **AI Foundry yang direkomendasikan**\*
    
    \**Penyebaran model dibatasi oleh kuota regional. Jika memilih wilayah di mana kuota yang tersedia tidak mencukupi, Anda mungkin perlu memilih wilayah alternatif untuk sumber daya baru nanti.*

1. Pilih **Buat**. Tunggu proyek Anda dibuat. Proses ini memerlukan waktu beberapa menit.

    Jika Anda diminta untuk menyebarkan model ke wilayah lain, gunakan pengaturan default untuk melakukannya.

## Jelajahi AI generatif di playground Azure AI Foundry's chat

1. Setelah proyek dibuat, pilih **Playground** pada panel tugas di sebelah kiri. 

    >*Tips*: Jika perlu, perluas menu untuk membaca kontennya dengan mengklik ikon 'luaskan' atas.

1. Di halaman Playground Azure AI Foundry, pilih **Coba playground Obrolan**. Tutup panel tips atau mulai cepat yang dibuka.

    Playground Obrolan adalah antarmuka pengguna yang memungkinkan Anda mencoba membangun aplikasi obrolan dengan model AI generatif yang berbeda.

    ![Cuplikan layar halaman detail gpt-4o.](./media/chat-playground.png)

    >*Tips*: Jika Anda tidak melihat panel **Penyiapan** di layar playground Obrolan, luaskan ukuran jendela.  

1. Untuk menggunakan playground Obrolan, Anda perlu mengaitkannya dengan model yang disebarkan. Di panel **Penyiapan** playground Obrolan, pastikan bahwa model **gpt-4o** yang Anda sebarkan sebelumnya dipilih. 

    >*Catatan*: Anda perlu memilih **Terapkan perubahan** kapan saja Anda membuat perubahan di panel **Penyiapan**.

1. Di panel **Penyiapan**, perhatikan instruksi dan konteks default untuk model, yang seharusnya mirip dengan:

    `You are an AI assistant that helps people find information.`

    Instruksi semacam ini biasanya disebut sebagai *perintah sistem*, dan digunakan untuk memberikan panduan dan batasan untuk respons model.

1. Tinjau panel *Riwayat obrolan*, yang berisi beberapa contoh perintah untuk membantu Anda memulai dan kotak kueri untuk memasukkan perintah Anda sendiri. 

1. Mari kita coba menghasilkan respons menggunakan perintah dengan tujuan tertentu. Di kotak obrolan, masukkan prompt berikut ini:

    ```prompt
    I'm planning a trip to Paris in September. Can you help me?
    ```

1. Tinjau responsnya. Perlu diingat bahwa respons spesifik yang Anda terima dapat bervariasi karena sifat AI generatif.

1. Mari kita coba prompt yang lain. Masukkan yang berikut:

    ```prompt
    Where's a good location in the city to stay?
    ```

1. Tinjau tanggapan, yang harus menyediakan beberapa tempat menginap di Paris. Perhatikan bahwa sesi obrolan mempertahankan konteks dari perintah sebelumnya, sehingga model tahu bahwa "kota" yang dimaksud adalah Paris.

1. Iterasi berdasarkan perintah dan respons sebelumnya untuk menyempurnakan hasil. Masukkan perintah berikut:

    ```prompt
    Can you give me more information about dining options near the first location?
    ```

1. Tinjau respons, yang harus menyediakan pilihan bersantap di dekat lokasi dari respons sebelumnya. 

1. Berikan sumber untuk membumikan respons dalam cakupan informasi tertentu Masukkan yang berikut: 

    ```prompt
    Based on the information at https://en.wikipedia.org/wiki/History_of_Paris, what were the key events in the city's history?
    ```

1. Tinjau respons, yang harus memberikan informasi berdasarkan situs web yang disediakan. 

1. Mari kita coba tambahkan konteks untuk memaksimalkan relevansi respons. Masukkan perintah berikut: 

    ```prompt
    What three places do you recommend I stay in Paris to be within walking distance to historical attractions? Explain your reasoning.
    ```

1. Tinjau respons dan penalaran respons.  

1. Sekarang coba tetapkan ekspektasi yang jelas untuk responsnya. Masukkan perintah berikut:

    ```prompt
    What are the top 10 sights to see in Paris? Answer with a numbered list in order of popularity.
    ```

1. Tinjau respons, yang harus memberikan daftar bernomor dari pemandangan di Paris.

## Menampilkan kode klien

1. Di bagian atas halaman playground Obrolan, pilih **Tampilkan kode**.
1. Tinjau sampel kode, yang disediakan untuk beberapa bahasa pemrograman, SDK, dan opsi autentikasi.

    Sampel kode ini dapat membantu pengembang memulai dengan cepat saat membangun aplikasi klien yang mengobrol dengan model yang Anda sebarkan.

1. Tutup jendela kode sampel.

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka **portal Azure** di [https://portal.azure.com](https://portal.azure.com)dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih **Hapus grup sumber daya**, lalu **masukkan nama grup sumber daya** untuk mengonfirmasi. Grup sumber daya tersebut akan dihapus.
