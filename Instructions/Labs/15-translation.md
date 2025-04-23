---
lab:
  title: Menjelajahi Azure AI Penerjemah
---

# Menjelajahi Azure AI Penerjemah

> **Catatan** Untuk menyelesaikan lab ini, Anda memerlukan [langganan Azure](https://azure.microsoft.com/free?azure-portal=true) dengan akses administrator.

Kecerdasan Buatan (AI) dapat membantu menyederhanakan terjemahan antar bahasa untuk membantu menghapus hambatan komunikasi lintas-negara dan budaya.

Untuk menguji kemampuan layanan Azure AI Penerjemah, kita akan melihatnya beraksi di Portal Microsoft Azure. Prinsip dan fungsi yang sama berlaku dalam solusi dunia nyata, seperti situs web atau aplikasi ponsel.

## Membuat sumber daya *Penerjemah*

Anda dapat menggunakan layanan Penerjemah dengan membuat sumber daya **Penerjemah** atau sumber daya **Layanan Azure AI**.

Untuk latihan ini, buat **sumber daya Penerjemah** di langganan Azure Anda.

1. Di tab browser lain, buka portal Microsoft Azure di [https://portal.azure.com](https://portal.azure.com?azure-portal=true), masuk dengan akun Microsoft Anda.

1. Klik **&#65291;Buat tombol sumber daya** dan cari *Penerjemah*. Pilih **Buat**. Anda akan diarahkan ke halaman untuk membuat sumber daya Penerjemah. Konfigurasikan dengan pengaturan berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Wilayah**: *Pilih wilayah yang tersedia*.
    - **Nama**: *Masukkan nama unik*.
    - **Tingkat harga**: Standar S0

1. Tinjau dan buat sumber daya, dan tunggu hingga penyebaran selesai. Lalu pergi ke sumber daya yang disebarkan.

## Menjelajah layanan Penerjemah 

Kita dapat menjelajahi kemampuan layanan Penerjemah di Portal Azure. 

1. Di portal Azure, di sumber daya yang disebarkan, tinjau *halaman Ringkasan*.

    ![Tangkapan layar halaman ringkasan untuk sumber daya Penerjemah.](media/use-translator/translator-azure-portal.png)

1. Di bagian *Coba* di halaman Ikhtisar, di bawah *Dari bagian Deteksi* otomatis, ketik teks `Welcome to Azure AI Fundamentals`. Perhatikan JSON yang muncul dalam korespondensi di bagian *Tampilkan permintaan* . 

1. Di bagian *Tampilkan respons* , lihat JSON. Di balik layar, *permintaan* telah dikirim ke layanan Penerjemah. *Respons* mencakup bahasa sumber yang terdeteksi dengan skor keyakinan, terjemahan menggunakan alfabet bahasa target, dan kode bahasa target. 

1. Demo di bagian *Coba* menunjukkan seperti apa tampilannya jika Anda membuat aplikasi terjemahan sederhana dengan antarmuka pengguna. Dalam kasus demo, segera setelah Anda mengetik teks, permintaan dibuat ke layanan Penerjemah. Bagaimana Anda bisa membuat permintaan ini? Periksa *tab Kode* Sampel. Di sini Anda melihat contoh kode dalam berbagai bahasa pemrograman berbeda yang dapat digunakan untuk membuat permintaan. 

1. Mengidentifikasi baris dalam sampel kode tempat Anda perlu menyertakan **Kunci** Layanan Penerjemah dan **Titik Akhir **. Dengan kunci dan titik akhir, Anda akan dapat mengirim permintaan ke layanan Penerjemah, dan menerima respons seperti yang Anda lihat dalam demo. 

1. Navigasi ke menu di sebelah kiri. Di bawah *Pengelolaan Sumber Daya*, pilih *Kunci dan Titik Akhir*. Jika Anda membuat aplikasi, Anda akan menemukan kunci dan titik akhir Anda di sini. 

## Pembersihan

1. Hapus sumber daya setelah Anda selesai menggunakannya. 

## Pelajari lebih lanjut

Untuk mempelajari lebih lanjut tindakan yang dapat Anda lakukan dengan layanan ini, lihat [Halaman Penerjemah](https://learn.microsoft.com/en-us/azure/ai-services/translator/translator-overview).
