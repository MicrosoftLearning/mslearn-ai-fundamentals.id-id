---
lab:
  title: Menjelajahi Ucapan di portal Azure AI Foundry
---

# Menjelajahi Ucapan di portal Azure AI Foundry

Layanan **Azure AI Speech** mentranskripsikan ucapan ke dalam teks, dan teks ke dalam ucapan yang dapat didengar. Anda dapat menggunakan AI Speech untuk membuat aplikasi yang dapat mentranskripsikan catatan rapat atau menghasilkan teks dari rekaman wawancara.

Dalam latihan ini, Anda akan menggunakan Azure AI Speech di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk mentranskripsikan audio menggunakan pengalaman mencoba-coba bawaan. 

## Membuat proyek di portal Azure AI Foundry

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup tips atau panel mulai cepat yang dibuka saat pertama kali Anda masuk. 

1. Di browser, navigasikan ke `https://ai.azure.com/managementCenter/allResources`dan pilih **Create**. Lalu pilih opsi untuk membuat *sumber daya hub AI baru*.

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

    Tunggu sampai proyek dan hub Anda selesai dibuat.

1. Saat proyek dibuat, Anda akan dibawa ke *halaman Gambaran Umum* tentang detail proyek.
 
1. Di menu sebelah kiri pada layar, pilih **Playgrounds**.

1. Pada halaman *Playground*, pilih petak **playground Bahasa** untuk mencoba beberapa kemampuan Azure AI Speech.

## Jelajahi ucapan ke teks di Azure AI Foundry's Speech Playground

Mari kita coba *ucapan ke teks* di Azure AI Foundry's Speech Playground. 

1. Pada halaman *Ucapan*, gulir ke bawah dan pilih **Transkripsi real-time** di bawah *Coba Kemampuan Ucapan*. Anda akan dibawa ke *Speech Playground*. 

1. Pilih [**https://aka.ms/mslearn-speech-files**](https://aka.ms/mslearn-speech-files) untuk mengunduh **speech.zip**. Buka folder . 

1. Di bawah *Pilih file audio*, pilih **Telusuri file** dan navigasikan ke folder tempat Anda menyimpan file. Pilih **WhatAICanDo.m4a** lalu **Buka**.

    ![Telusuri file](media/recognize-synthesize-speech/browse-files-speech.png)

1. Layanan Ucapan mentranskripsikan dan menampilkan teks secara real time. Jika Anda memiliki audio di komputer, Anda dapat mendengarkan rekaman saat teks sedang ditranskripsikan.

1. Tinjau output, yang seharusnya berhasil mengenali dan mentranskripsikan audio ke dalam teks.

Dalam latihan ini Anda mencoba layanan Azure AI Speech di Azure AI Foundry's Speech Playground. Anda kemudian menggunakan transkripsi Real-time untuk mentranskripsikan rekaman audio. Anda dapat melihat transkripsi teks yang dihasilkan saat file audio diputar.

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Latihan ini hanya menunjukkan beberapa kemampuan layanan Ucapan. Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman Ucapan](https://azure.microsoft.com/services/cognitive-services/speech-services).
