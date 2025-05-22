---
lab:
  title: Menjelajahi AI generatif di portal Azure AI Foundry
---

# Menjelajahi AI generatif di Portal Azure AI Foundry

AI Generatif menjelaskan kategori kemampuan dalam AI yang membuat konten. Orang biasanya berinteraksi dengan AI generatif yang telah dibangun ke dalam aplikasi obrolan. Dalam latihan ini, Anda mencoba AI generatif di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas. 

## Membuat proyek di portal Azure AI Foundry

Mari kita mulai dengan membuat proyek Azure AI Foundry.

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup semua tips atau panel mulai cepat yang terbuka saat pertama kali Anda masuk, dan jika perlu, gunakan logo **Azure AI Foundry** di kiri atas untuk menavigasi ke beranda, yang tampilannya mirip dengan gambar berikut (tutup panel **Bantuan** jika terbuka):

    ![Tnagkapan layar beranda Azure AI Foundry dengan agen terpilih.](./media/azure-ai-foundry-home-page.png)

1. Di beranda, pilih **+ Buat agen**.

1. Di wizard **Buat agen**, masukkan nama yang valid untuk proyek Anda. 

1. Klik **Opsi Tingkat Lanjut** dan tentukan pengaturan berikut:
    - **Sumber daya Azure AI Foundry**: *Pertahankan nama default*
    - **Langganan**: *Langganan Azure Anda*
    - **Grup sumber daya**: *Buat atau pilih grup sumber daya*
    - **Wilayah**: Pilih salah satu wilayah berikut:
        * AS Timur
        * Prancis Tengah
        * Korea Tengah
        * Eropa Barat
        * US Barat

1. Pilih **Buat** dan tinjau konfigurasi Anda. Tunggu hingga proses penyiapan selesai.

    >**Catatan**: Jika Anda mendapat kesalahan izin, pilih tombol **Perbaiki** untuk menambahkan izin yang sesuai untuk melanjutkan.

1. Saat proyek Anda dibuat, Anda akan dibawa secara default ke playground Agen di portal Azure AI Foundry, yang akan terlihat mirip dengan gambar berikut:

    ![Tangkapan layar detail proyek Azure AI di portal Azure AI Foundry.](./media/ai-foundry-project-2.png)

1. Di menu sebelah kiri pada layar, pilih **Playgrounds**.

## Jelajahi AI generatif di playground Azure AI Foundry's chat

1. Di halaman Playground Azure AI Foundry, pilih **Coba playground Obrolan**. Playground Obrolan adalah antarmuka pengguna yang memungkinkan Anda mencoba membangun aplikasi obrolan dengan model AI generatif yang berbeda.  

1. Untuk menggunakan playground Obrolan, Anda perlu mengaitkannya dengan model yang disebarkan. Di playground Obrolan, pilih **Buat penyebaran**. Cari dan pilih** gpt-4**. 

1. Di jendela *Sebarkan model* , pertahankan penamaan dan pilihan default lalu pilih **Sebarkan**. Mungkin perlu waktu sejenak bagi model tersebut untuk disebarkan. Anda dapat memeriksa status penyebaran Anda dengan memilih *Model dan titik akhir* di menu sebelah kiri di bawah *Aset saya*.
1. Di playground obrolan, Anda dapat menggunakan model yang disebarkan saat muncul di menu pilihan *Penyebaran*. Pastikan model yang Anda sebarkan dipilih. Yang penting, Anda perlu memilih **Terapkan perubahan** setelah membuat perubahan apa pun pada *Penyiapan*. 

1. Pertimbangkan cara berikut untuk meningkatkan respons dari asisten AI generatif:
    - Mulailah dengan tujuan spesifik tentang apa yang Anda ingin untuk dilakukan asisten
    - Iterasi berdasarkan perintah dan respons sebelumnya untuk menyempurnakan hasil
    - Berikan sumber untuk  membumikan respons dalam cakupan informasi tertentu
    - Menambahkan konteks untuk memaksimalkan kesamaan dan relevansi respons
    - Menetapkan ekspektasi yang jelas untuk respons

1. Mari kita coba menghasilkan respons menggunakan perintah dengan tujuan tertentu. Di kotak obrolan, masukkan prompt berikut ini:

    ```prompt
    I'm planning a trip to Paris in September. Can you help me?
    ```

1. Tinjau responsnya. **Catatan**: Perlu diingat bahwa respons spesifik yang Anda terima dapat bervariasi karena sifat AI generatif.
 
1. Mari kita coba prompt yang lain. Masukkan yang berikut:

    ```prompt
    Where's a good location in Paris to stay? 
    ```

1. Tinjau tanggapan, yang harus menyediakan beberapa tempat menginap di Paris.

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

1. Setelah selesai, Anda dapat menutup jendela browser.
