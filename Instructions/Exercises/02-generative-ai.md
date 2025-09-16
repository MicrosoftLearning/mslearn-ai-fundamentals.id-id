---
lab:
  title: Menjelajahi AI generatif di portal Azure AI Foundry
---

# Menjelajahi AI generatif di Portal Azure AI Foundry

AI Generatif menjelaskan kategori kemampuan dalam AI yang membuat konten. Orang biasanya berinteraksi dengan AI generatif yang telah dibangun ke dalam aplikasi obrolan. Dalam latihan ini, Anda mencoba AI generatif di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas. 

Latihan ini memakan waktu sekitar **20** menit.

## Membuat proyek di portal Azure AI Foundry

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup tips atau panel mulai cepat yang dibuka saat pertama kali Anda masuk. 

1. Di browser, navigasikan ke `https://ai.azure.com/managementCenter/allResources` dan pilih **Buat baru**. Lalu pilih opsi untuk membuat **sumber daya Azure AI Foundry**.

1. Di wizard,*Buat proyek*dan masukkan nama yang valid untuk proyek Anda.

1. Perluas *opsi Tingkat Lanjut* untuk menentukan pengaturan proyek Anda sebagai berikut:
    - **Subscription**: Langganan Azure Anda
    - **Grup sumber daya**: Buat atau pilih grup sumber daya
    - **Wilayah**: Pilih salah satu wilayah berikut:
        * AS Timur
        * Prancis Tengah
        * Korea Tengah
        * Eropa Barat
        * US Barat

    Pilih **Buat**. Tunggu proyek Anda dibuat. Proses ini memerlukan waktu beberapa menit.

1. Saat proyek dibuat, Anda akan dibawa ke *halaman Gambaran Umum* tentang detail proyek.

1. Di menu sebelah kiri pada layar, pilih **Playgrounds**. 

    >*Catatan*: Perluas menu untuk membaca kontennya dengan mengklik ikon 'perluas' atas.

## Jelajahi AI generatif di playground Azure AI Foundry's chat

1. Di halaman Playground Azure AI Foundry, pilih **Coba playground Obrolan**. Playground Obrolan adalah antarmuka pengguna yang memungkinkan Anda mencoba membangun aplikasi obrolan dengan model AI generatif yang berbeda.  

    >*Catatan*: Jika Anda tidak melihat panel *Penyiapan* muncul di layar Playground obrolan, perluas ukuran jendela.  

1. Untuk menggunakan playground Obrolan, Anda perlu mengaitkannya dengan model yang disebarkan. Di panel *Penyiapan* Playground obrolan, pilih **+ Buat penyebaran**. Jika diminta, pilih *Dari model dasar*, jika tidak, lanjutkan ke langkah berikutnya. 

1. Cari model **gpt-4o** dari daftar, lalu pilih **Konfirmasi**. Pertahankan nama model default, jenis penyebaran, dan detail penyebaran. Kemudian, plih **Sebarkan**.

1. Di playground obrolan, Anda dapat menggunakan model yang disebarkan saat muncul di menu pilihan *Penyebaran*. Tutup panel tips atau mulai cepat yang dibuka. 

    >*Catatan*: Anda perlu memilih **Terapkan perubahan** setiap kali membuat perubahan pada *Penyiapan*. 

1. Buka panel *Riwayat obrolan*. Anda akan menggunakan kotak kueri untuk memasukkan perintah Anda. 

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

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka **portal Azure** di [https://portal.azure.com](https://portal.azure.com)dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.

1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.
