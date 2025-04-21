---
lab:
  title: Menjelajahi AI generatif di portal Azure AI Foundry
---

# Menjelajahi AI generatif di portal Azure AI Foundry

AI Generatif menjelaskan kategori kemampuan dalam AI yang membuat konten. Orang biasanya berinteraksi dengan AI generatif yang telah dibangun ke dalam aplikasi obrolan. Dalam latihan ini, Anda mencoba AI generatif di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas. 

## Membuat proyek di portal Azure AI Foundry

1. Di tab browser, navigasikan ke [Azure AI Foundry](https://ai.azure.com?azure-portal=true).

1. Masuk dengan akun Anda. 

1. Pada halaman beranda portal Azure AI Foundry, pilih **Buat proyek**. Di Azure AI Foundry, proyek adalah kontainer yang membantu mengatur pekerjaan Anda.  

    ![Cuplikan layar beranda Azure AI Foundry dengan membuat proyek yang dipilih.](./media/azure-ai-foundry-home-page.png)

1. Pada panel *Buat proyek* , Anda akan melihat nama proyek yang dihasilkan, yang bisa Anda simpan apa adanya. Bergantung pada apakah Anda telah membuat hub sebelumnya, Anda akan melihat daftar sumber daya Azure *baru* yang akan dibuat atau daftar menurun hub yang ada. Jika Anda melihat daftar menurun hub yang ada, pilih *Buat hub baru*, buat nama unik untuk hub Anda, dan pilih *Berikutnya*.  
 
    ![Cuplikan layar panel buat proyek dengan nama yang dihasilkan secara otomatis untuk hub dan proyek.](./media/azure-ai-foundry-create-project.png)

> **Penting**: Anda akan memerlukan sumber daya layanan Azure AI yang disediakan di lokasi tertentu untuk menyelesaikan lab lainnya.

1. Di panel *Buat proyek * yang sama, pilih** Sesuaikan** dan pilih salah satu **Lokasi** berikut: AS Timur, Prancis Tengah, Korea Tengah, Eropa Barat, atau AS Barat untuk menyelesaikan lab lainnya. Lalu pilih **buat**. 

1. Perhatikan sumber daya yang dibuat: 
- Layanan Azure AI
- Hub Azure AI
- Proyek Azure AI
- Akun penyimpanan
- Brankas kunci
- Grup sumber daya  
 
1. Setelah sumber daya dibuat, Anda akan dibawa ke halaman* Gambaran Umum* proyek Anda. Di menu sebelah kiri pada layar, pilih **Playgrounds**.
 
    ![Cuplikan layar menu sebelah kiri pada layar proyek dengan Layanan AI dipilih.](./media/azure-ai-foundry-playgrounds.png)  

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