---
lab:
  title: Menjelajahi Ucapan di portal Azure AI Foundry
---

# Menjelajahi Ucapan di portal Azure AI Foundry

Layanan **Azure AI Speech** mentranskripsikan ucapan ke dalam teks, dan teks ke dalam ucapan yang dapat didengar. Anda dapat menggunakan AI Speech untuk membuat aplikasi yang dapat mentranskripsikan catatan rapat atau menghasilkan teks dari rekaman wawancara.

Dalam latihan ini, Anda akan menggunakan Azure AI Speech di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk mentranskripsikan audio menggunakan pengalaman mencoba-coba bawaan. 

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
 
1. Setelah sumber daya dibuat, Anda akan dibawa ke halaman* Gambaran Umum* proyek Anda. Di menu sebelah kiri pada layar, pilih **Layanan AI**.
 
    ![Cuplikan layar menu sebelah kiri pada layar proyek dengan Layanan AI dipilih.](./media/azure-ai-foundry-ai-services.png)  

1. Pada halaman *Layanan AI*, pilih petak *Ucapan* untuk mencoba kemampuan Azure AI Speech.

    ![Cuplikan layar petak Ucapan dipilih di halaman Layanan AI.](./media/speech-tile.png)

## Jelajahi ucapan ke teks di Azure AI Foundry's Speech Playground

Mari coba *ucapan ke teks real time* di Playground Azure AI Foundry Speech. 

1. Pada halaman *Ucapan*, gulir ke bawah dan pilih **Ucapan ke teks real-time** di bawah *Coba Kemampuan ucapan*. Anda akan dibawa ke *Speech Playground*. 

1. Pilih [**https://aka.ms/mslearn-speech-files**](https://aka.ms/mslearn-speech-files) untuk mengunduh **speech.zip**. Buka folder . 

1. Di bawah *Pilih file audio*, pilih **Telusuri file** dan navigasikan ke folder tempat Anda menyimpan file. Pilih **WhatAICanDo.m4a** lalu **Buka**.

    ![Telusuri file](media/recognize-synthesize-speech/browse-files-speech.png)

1. Layanan Ucapan mentranskripsikan dan menampilkan teks secara real time. Jika Anda memiliki audio di komputer, Anda dapat mendengarkan rekaman saat teks sedang ditranskripsikan.

1. Tinjau output, yang seharusnya berhasil mengenali dan mentranskripsikan audio ke dalam teks.

Dalam latihan ini Anda mencoba layanan Azure AI Speech di Azure AI Foundry's Speech Playground. Anda kemudian menggunakan layanan ucapan ke teks real time untuk mentranskripsikan rekaman audio. Anda dapat melihat transkripsi teks yang dihasilkan saat file audio diputar.

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Latihan ini hanya menunjukkan beberapa kemampuan layanan Ucapan. Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman Ucapan](https://azure.microsoft.com/services/cognitive-services/speech-services).
