---
lab:
  title: Mendeteksi wajah di Vision Studio
---

# Mendeteksi wajah di Vision Studio

Solusi penglihatan sering kali mengharuskan AI untuk dapat mendeteksi wajah manusia. Misalkan perusahaan ritel fiktif Northwind Traders ingin menemukan di mana pelanggan berdiri di toko untuk membantu mereka. Salah satu cara untuk mencapai hal ini adalah dengan menentukan apakah ada wajah dalam gambar, dan jika demikian, untuk mengembalikan koordinat kotak pembatas yang menunjukkan lokasinya.

Untuk menguji kemampuan deteksi wajah layanan Azure AI Face, Anda akan menggunakan [Azure Vision Studio](https://portal.vision.cognitive.azure.com/). Ini adalah platform berbasis UI yang memungkinkan Anda menjelajahi fitur Azure AI Vision tanpa perlu menulis kode apa pun.

## Buat sumber daya *Layanan Azure AI*

Anda dapat menggunakan layanan Azure AI Face dengan **sumber daya multi-layanan layanan** Azure AI. Jika Anda belum melakukannya, buat sumber daya **Layanan Azure AI** di langganan Azure Anda.

1. Di tab browser lain, buka portal Azure di [https://portal.azure.com](https://portal.azure.com?azure-portal=true), masuk dengan akun Microsoft yang terkait dengan langganan Azure Anda.

1. Klik tombol **＋Buat sumber daya**dan cari *layanan Azure AI*. Pilih **buat** paket **layanan Azure AI**. Anda akan diarahkan ke halaman untuk membuat sumber daya layanan Azure AI. Konfigurasikan dengan pengaturan berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Wilayah**: US Timur.
    - **Nama**: *Masukkan nama unik*.
    - **Tingkat** harga: *S0 Standar.*
    - **Dengan mencentang kotak ini saya mengakui bahwa saya telah membaca dan memahami semua istilah di bawah ini**: *Dipilih*.

1. Pilih **Tinjau + buat** lalu **Buat** dan tunggu penyebaran selesai.

## Koneksi sumber daya layanan Azure AI Anda ke Vision Studio

Selanjutnya, sambungkan sumber daya layanan Azure AI yang Anda provisikan di atas ke Vision Studio.

1. Di tab browser lain, navigasikan ke **Vision Studio** dihttps://portal.vision.cognitive.azure.com[](https://portal.vision.cognitive.azure.com?azure-portal=true) .

1. Masuk dengan akun Anda dan pastikan Anda menggunakan direktori yang sama dengan direktori tempat Anda membuat sumber daya layanan Azure AI Anda.

1. Pada beranda Vision Studio, pilih **Tampilkan semua sumber daya** di **bawah judul Memulai visi** .

    ![Tautan Lihat semua sumber daya disorot di bawah Mulai menggunakan Vision di Vision Studio.](./media/analyze-images-vision/vision-resources.png)

1. Pada halaman **Pilih sumber daya untuk bekerja dengan** , arahkan kursor mouse Anda ke atas sumber daya yang Anda buat di atas dalam daftar lalu centang kotak di sebelah kiri nama sumber daya, lalu pilih **Pilih sebagai sumber daya** default.

    > **Catatan** : Jika sumber daya Anda tidak tercantum, Anda mungkin perlu **Merefresh** halaman.

    ![Dialog Pilih sumber daya untuk dikerjakan ditampilkan dengan sumber daya Cognitive Services cog-ms-learn-vision-SUFFIX yang disorot dan diperiksa. Tombol Pilih sebagai sumber daya default disorot.](./media/analyze-images-vision/default-resource.png)

1. Tutup halaman pengaturan dengan memilih "x" di kanan atas layar.

## Mendeteksi wajah di Vision Studio 

1. Di browser web, navigasikan ke **Vision Studio** dihttps://portal.vision.cognitive.azure.com[](https://portal.vision.cognitive.azure.com?azure-portal=true) .

1. Pada halaman **Mulai menggunakan arahan Visi** , pilih tab **Wajah** lalu pilih petak **Deteksi Wajah dalam petak gambar** .

1. **Di bawah subjudul Coba Keluar**, akui kebijakan penggunaan sumber daya dengan membaca dan mencentang kotak.  

1. Pilih setiap gambar sampel dan amati data deteksi wajah yang dikembalikan.

1. Sekarang mari kita coba dengan beberapa gambar kita sendiri. Pilih [**https://aka.ms/mslearn-detect-faces](https://aka.ms/mslearn-detect-faces)** untuk mengunduh **detect-faces.zip.** Kemudian buka folder di komputer Anda.

1. Temukan file bernama **store-camera-1.jpg**; yang berisi gambar berikut:

    ![Gambar orang di toko.](./media/create-face-solutions/store-camera-1.jpg)

1. Unggah **store-camera-1.jpg** dan tinjau detail deteksi wajah yang dikembalikan.

1. Temukan file bernama **store-camera-2.jpg**; yang berisi gambar berikut:

    ![Gambar lebih banyak orang di toko.](./media/create-face-solutions/store-camera-2.jpg)

1. Unggah **store-camera-2.jpg** dan tinjau detail deteksi wajah yang dikembalikan.

1. Temukan file bernama **store-camera-3.jpg**; yang berisi gambar berikut:

    ![Gambar orang-orang di toko dengan tanaman mengaburkan wajah.](./media/create-face-solutions/store-camera-3.jpg)

1. Unggah **store-camera-3.jpg** dan tinjau detail deteksi wajah yang dikembalikan. Perhatikan bagaimana Azure AI Face tidak mendeteksi wajah yang dikaburkan.

Dalam latihan ini Anda telah menjelajahi bagaimana layanan Azure AI dapat mendeteksi wajah dalam gambar. Jika Anda punya waktu, jangan ragu untuk mencoba gambar sampel atau beberapa gambar Anda sendiri.

## Penghapusan

Jika Anda tidak berniat untuk melakukan lebih banyak latihan, hapus sumber daya apa pun yang tidak lagi Anda butuhkan. Ini menghindari akumulasi biaya yang tidak perlu.

1. **Buka portal Azure** di [https://portal.azure.com](https://portal.azure.com?azure-portal=true) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya kemudian dihapus.

## Pelajari selengkapnya

Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-identity) layanan Azure AI Face.
