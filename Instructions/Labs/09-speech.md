---
lab:
  title: Menjelajahi Speech Studio
---

# Menjelajahi Speech Studio

Layanan **Azure AI Speech** mentranskripsikan ucapan ke dalam teks, dan teks ke dalam ucapan yang dapat didengar. Anda dapat menggunakan AI Speech untuk membuat aplikasi yang dapat mentranskripsikan catatan rapat atau menghasilkan teks dari rekaman wawancara.

Dalam latihan ini, Anda akan mencoba kemampuan Azure AI Speech menggunakan Azure AI Speech Studio. 

## Membuat sumber daya *Azure AI Speech*

Anda dapat menggunakan layanan Ucapan dengan membuat sumber daya **Ucapan** atau sumber daya **layanan Azure AI**.

Dalam latihan ini, Anda akan membuat sumber daya AI Speech, kecuali Anda sudah memiliki sumber daya yang dapat Anda gunakan.

1. Di tab browser lain, buka [Azure AI Speech Studio](https://speech.microsoft.com/), masuk dengan akun Microsoft Anda.

1. Pilih **Pengaturan** lalu **Buat sumber daya.** Konfigurasikan dengan pengaturan berikut:
    - **Nama sumber daya baru**: *Masukkan nama yang unik*.
    - **Langganan**: *Langganan Azure Anda*.
    - **Wilayah**: *Pilih [wilayah yang didukung](https://learn.microsoft.com/azure/ai-services/speech-service/regions)*.
    - **Tingkat harga**: *FO Gratis (jika tersedia, jika tidak pilih S0 Standar).*
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
1. Pilih **Buat sumber daya**. Tunggu hingga sumber daya dibuat lalu pilih **Gunakan sumber daya**. Halaman Mulai menggunakan Ucapan ditampilkan.

## Menjelajahi ucapan ke teks di Speech Studio

1. Pilih [**https://aka.ms/mslearn-speech-files**](https://aka.ms/mslearn-speech-files) untuk mengunduh **speech.zip**. Buka folder . 

1. Pada halaman Mulai menggunakan Ucapan, di bawah *Ucapan ke teks* temukan *Ucapan ke teks real-time*. Pilih **Coba Ucapan ke teks real time**.

    ![Mulai menggunakan Ucapan](media/recognize-synthesize-speech/try-out-speech-to-text.png)

1. Di bawah *Pilih file audio*, pilih **Telusuri file** dan navigasikan ke folder tempat Anda menyimpan file. Pilih **WhatAICanDo.m4a** lalu **Buka**.

    ![Telusuri file](media/recognize-synthesize-speech/browse-files-speech.png)

1. Layanan Ucapan mentranskripsikan dan menampilkan teks secara real time. Jika Anda memiliki audio di komputer, Anda dapat mendengarkan rekaman saat teks sedang ditranskripsikan.
1. Tinjau output, yang seharusnya berhasil mengenali dan mentranskripsikan audio ke dalam teks.

    > **Catatan** Jika Anda mendapatkan pesan kesalahan, tunggu beberapa menit sebelum mencoba lagi. Dibutuhkan sedikit waktu agar sumber daya Ucapan tersedia untuk digunakan pertama kali.

Dalam latihan ini Anda membuat sumber daya AI Speech di Speech Studio. Anda kemudian menggunakan layanan ucapan ke teks real time untuk mentranskripsikan rekaman audio. Anda dapat melihat transkripsi teks yang dihasilkan saat file audio diputar.

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Latihan ini hanya menunjukkan beberapa kemampuan layanan Ucapan. Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman Ucapan](https://azure.microsoft.com/services/cognitive-services/speech-services).
