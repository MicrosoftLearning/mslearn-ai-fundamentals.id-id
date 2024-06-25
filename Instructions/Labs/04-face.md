---
lab:
  title: Deteksi wajah di Vision Studio
---

# Deteksi wajah di Vision Studio

Solusi visual sering kali mengharuskan AI untuk dapat mendeteksi wajah manusia. Misalnya, perusahaan ritel fiktif Northwind Traders ingin menemukan pelanggan yang ada di toko untuk membantu pelanggan dengan baik. Salah satu cara untuk mencapainya adalah dengan menentukan apakah ada wajah dalam gambar, dan jika demikian, lalu memberikan koordinat kotak pembatas yang menunjukkan lokasi mereka.

Untuk menguji kemampuan deteksi wajah layanan Azure AI Face, Anda akan menggunakan [Azure Vision Studio](https://portal.vision.cognitive.azure.com/). Ini adalah platform berbasis UI yang memungkinkan Anda menjelajahi fitur Azure AI Visual tanpa perlu menulis kode apa pun.

## Buat sumber daya *Layanan Azure AI*

Anda dapat menggunakan layanan Azure AI Face dengan sumber daya multi-layanan **Layanan Azure AI**. Jika Anda belum melakukannya, buat sumber daya **Layanan Azure AI** di langganan Azure Anda.

1. Di tab browser yang lain, buka portal Azure di [https://portal.azure.com](https://portal.azure.com?azure-portal=true), lalu masuk dengan akun Microsoft yang terkait dengan langganan Azure Anda.

1. Klik tombol **＋Buat sumber daya**dan cari *layanan Azure AI*. Pilih **buat** paket **layanan Azure AI**. Anda akan diarahkan ke halaman untuk membuat sumber daya layanan Azure AI. Konfigurasikan dengan pengaturan berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Wilayah**: *Pilih wilayah geografis terdekat. Jika di AS timur, gunakan "US Timur 2"*.
    - **Nama**: *Masukkan nama unik*.
    - **Tingkat harga**: *S0 Standar.*
    - **Dengan mencentang kotak ini, saya menyatakan bahwa saya telah membaca dan memahami semua persyaratan di bawah ini**: *Dipilih*.

1. Pilih **Tinjau + buat** lalu **Buat** dan tunggu hingga penyebaran selesai.

## Sambungkan sumber daya layanan Azure AI Anda ke Vision Studio

Selanjutnya, sambungkan sumber daya layanan Azure AI yang Anda provisikan di atas ke Vision Studio.

1. Di tab browser yang lain, navigasikan ke **Vision Studio** di https://portal.vision.cognitive.azure.com[](https://portal.vision.cognitive.azure.com?azure-portal=true).

1. Masuk dengan akun Anda dan pastikan Anda menggunakan direktori yang sama dengan direktori tempat Anda membuat sumber daya layanan Azure AI Anda.

1. Di beranda Vision Studio, pilih **Tampilkan semua sumber daya** di bawah judul **Mulai menggunakan Vision**.

    ![Tautan Lihat semua sumber daya disorot di bawah Mulai menggunakan Vision di Vision Studio.](./media/analyze-images-vision/vision-resources.png)

1. Pada halaman **Pilih sumber daya yang akan digunakan**, arahkan kursor mouse Anda ke atas sumber daya yang Anda buat di atas dalam daftar, lalu centang kotak di sebelah kiri nama sumber daya, lalu pilih **Pilih sebagai sumber daya default**.

    > **Catatan** : Jika sumber daya Anda tidak tercantum, Anda mungkin perlu **Merefresh** halaman.

    ![Dialog Pilih sumber daya yang akan digunakan ditampilkan dengan sumber daya Cognitive Services cog-ms-learn-vision-SUFFIX yang disorot dan dicentang. Tombol Pilih sebagai sumber daya default disorot.](./media/analyze-images-vision/default-resource.png)

1. Tutup halaman pengaturan dengan memilih "x" di kanan atas layar.

## Deteksi wajah di Vision Studio 

1. Di browser web, navigasikan ke **Vision Studio** di [https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com?azure-portal=true).

1. Pada halaman **Mulai menggunakan Vision**, pilih tab **Wajah** lalu pilih ubin **Deteksi Wajah dalam gambar**.

1. Di bawah subjudul **Coba**, setujui kebijakan penggunaan sumber daya dengan membaca dan mencentang kotak.  

1. Pilih setiap gambar sampel dan amati data deteksi wajah yang dihasilkan.

1. Sekarang, mari kita coba dengan beberapa gambar kita sendiri. Pilih [**https://aka.ms/mslearn-detect-faces**](https://aka.ms/mslearn-detect-faces) untuk mengunduh **detect-faces.zip.** Kemudian, buka folder di komputer Anda.

1. Temukan file bernama **store-camera-1.jpg**; yang berisi gambar berikut:

    ![Gambar orang di toko.](./media/create-face-solutions/store-camera-1.jpg)

1. Unggah **store-camera-1.jpg** dan tinjau detail deteksi wajah yang dihasilkan.

1. Temukan file bernama **store-camera-2.jpg**; yang berisi gambar berikut:

    ![Gambar berisi lebih banyak orang di toko.](./media/create-face-solutions/store-camera-2.jpg)

1. Unggah **store-camera-2.jpg** dan tinjau detail deteksi wajah yang dihasilkan.

1. Temukan file bernama **store-camera-3.jpg**; yang berisi gambar berikut:

    ![Gambar orang di toko yang terhalang oleh tanaman.](./media/create-face-solutions/store-camera-3.jpg)

1. Unggah **store-camera-3.jpg** dan tinjau detail deteksi wajah yang dihasilkan. Perhatikan bahwa Azure AI Face tidak mendeteksi wajah yang dikaburkan.

Dalam latihan ini, Anda telah menjelajahi cara layanan Azure AI dapat mendeteksi wajah dalam gambar. Jika Anda punya waktu, jangan ragu untuk mencoba gambar sampel atau beberapa gambar Anda sendiri.

## Penghapusan

Jika Anda tidak berniat untuk melakukan lebih banyak latihan, hapus sumber daya apa pun yang tidak lagi Anda butuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka **portal Azure** di [https://portal.azure.com](https://portal.azure.com?azure-portal=true) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman layanan Azure AI Face](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-identity).
