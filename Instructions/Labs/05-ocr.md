---
lab:
  title: Membaca teks di Vision Studio
---

# Membaca teks di Vision Studio

Dalam latihan ini Anda akan menggunakan layanan Azure AI untuk menjelajahi kemampuan pengenalan karakter optik Azure AI Visual. Anda akan menggunakan Vision Studio untuk bereksperimen dengan mengekstrak teks dari gambar, tanpa harus menulis kode sama sekali.

Tantangan visi komputer yang umum adalah mendeteksi dan menafsirkan teks yang tersemat dalam gambar. Hal ini disebut pengenalan karakter optik (OCR). Dalam latihan ini Anda akan menggunakan sumber daya layanan Azure AI, yang mencakup layanan Azure AI Visual. Anda kemudian akan menggunakan Vision Studio untuk mencoba OCR dengan berbagai jenis gambar.

## Buat sumber daya *Layanan Azure AI*

Anda dapat menggunakan kemampuan OCR Azure AI Visual dengan sumber daya multi-layanan **Layanan Azure AI**. Jika Anda belum melakukannya, buat sumber daya **Layanan Azure AI** di langganan Azure Anda.

1. Di tab browser yang lain, buka **portal Azure** di [https://portal.azure.com](https://portal.azure.com?azure-portal=true), lalu masuk dengan akun Microsoft yang terkait dengan langganan Azure Anda.

1. Klik tombol **＋Buat sumber daya**dan cari *layanan Azure AI*. Pilih **buat** paket **layanan Azure AI**. Anda akan diarahkan ke halaman untuk membuat sumber daya layanan Azure AI. Konfigurasikan dengan pengaturan berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Wilayah**: *Pilih wilayah geografis terdekat. Jika di AS timur, gunakan "US Timur 2"*.
    - **Nama**: *Masukkan nama unik*.
    - **Tingkat harga**: *Standar S0.*
    - **Dengan mencentang kotak ini, saya menyatakan bahwa saya telah membaca dan memahami semua persyaratan di bawah ini**: *Dipilih*.

1. Pilih **Tinjau + buat** lalu **Buat** dan tunggu hingga penyebaran selesai.

## Sambungkan sumber daya layanan Azure AI Anda ke Vision Studio

Selanjutnya, sambungkan sumber daya layanan Azure AI yang Anda provisikan di atas ke Vision Studio.

1. Di tab browser yang lain, navigasikan ke **Vision Studio** di [https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com?azure-portal=true).

1. Masuk dengan akun Anda dan pastikan Anda menggunakan direktori yang sama dengan direktori tempat Anda membuat sumber daya layanan Azure AI Anda.

1. Di beranda Vision Studio, pilih **Tampilkan semua sumber daya** di bawah judul **Mulai menggunakan Vision**.

    ![Tautan Lihat semua sumber daya disorot di bawah Mulai menggunakan Vision di Vision Studio.](./media/analyze-images-vision/vision-resources.png)

1. Pada halaman **Pilih sumber daya yang akan digunakan**, arahkan kursor mouse Anda ke atas sumber daya yang Anda buat di atas dalam daftar, lalu centang kotak di sebelah kiri nama sumber daya, lalu pilih **Pilih sebagai sumber daya default**.

    > **Catatan** : Jika sumber daya Anda tidak tercantum, Anda mungkin perlu **Merefresh** halaman.

    ![Dialog Pilih sumber daya yang akan digunakan ditampilkan dengan sumber daya Cognitive Services cog-ms-learn-vision-SUFFIX yang disorot dan dicentang. Tombol Pilih sebagai sumber daya default disorot.](./media/analyze-images-vision/default-resource.png)

1. Tutup halaman pengaturan dengan memilih "x" di kanan atas layar.

## Mengekstrak teks dari gambar di Vision Studio
    
1. Di browser web, navigasikan ke **Vision Studio** di [https://portal.vision.cognitive.azure.com](https://portal.vision.cognitive.azure.com?azure-portal=true).

1. Pada halaman arahan **Mulai menggunakan Vision**, pilih **Pengenalan karakter optik**, lalu pilih ubin **Ekstrak teks dari gambar**.

1. Di bawah subjudul **Coba**, setujui kebijakan penggunaan sumber daya dengan membaca dan mencentang kotak.  

1. Pilih [**https://aka.ms/mslearn-ocr-images**](https://aka.ms/mslearn-ocr-images) untuk mengunduh **ocr-images.zip**. Kemudian, buka folder.

1. Di portal, pilih **Telusuri file** dan navigasikan ke folder di komputer tempat Anda mengunduh **ocr-images.zip**. Pilih **advert.jpg** dan pilih **Buka**.

1. Sekarang tinjau hasilnya:
    - Dalam **Atribut yang terdeteksi**, teks yang ditemukan dalam gambar diatur ke dalam struktur hierarki wilayah, garis, dan kata.
    - Pada gambar, lokasi teks ditunjukkan oleh kotak pembatas, seperti yang diperlihatkan di sini:

    ![Gambar teks dalam gambar yang diuraikan.](media/read-text-computer-vision/advert-bounding-boxes.jpg)

1. Anda sekarang dapat mencoba gambar lain. Pilih **Telusuri file** dan navigasikan ke folder tempat Anda menyimpan file dari GitHub. Pilih **letter.jpg**.

    ![Gambar dari huruf ketik.](media/read-text-computer-vision/letter.jpg)

1. Tinjau hasil gambar kedua. Ini akan menampilkan teks dan kotak pembatas teks. Jika sempat, coba **note.jpg** dan **receipt.jpg**.

## Penghapusan

Jika Anda tidak berniat untuk melakukan lebih banyak latihan, hapus sumber daya apa pun yang tidak lagi Anda butuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka **portal Azure** di [https://portal.azure.com](https://portal.azure.com?azure-portal=true) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Untuk mempelajari selengkapnya tentang hal yang dapat Anda lakukan dengan layanan ini, lihat dokumentasi Azure AI Vision tentang [pengenalan karakter optik](https://learn.microsoft.com/azure/ai-services/computer-vision/overview-ocr).
