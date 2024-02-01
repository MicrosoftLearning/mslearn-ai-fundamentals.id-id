---
lab:
  title: Menganalisis gambar di Vision Studio
---

# Menganalisis gambar di Vision Studio 

**Azure AI Vision** mencakup banyak kemampuan untuk memahami konten dan konteks gambar dan mengekstrak informasi dari gambar. Azure AI Vision Studio memungkinkan Anda mencoba banyak kemampuan analisis gambar. 

Dalam latihan ini, Anda akan menggunakan Vision Studio untuk menganalisis gambar menggunakan pengalaman try-it-out bawaan. Misalkan peritel *fiktif Northwind Traders* telah memutuskan untuk menerapkan "toko pintar", di mana layanan AI memantau toko untuk mengidentifikasi pelanggan yang membutuhkan bantuan, dan mengarahkan karyawan untuk membantu mereka. Dengan menggunakan Azure AI Vision, gambar yang diambil oleh kamera di seluruh penyimpanan dapat dianalisis untuk memberikan deskripsi yang bermakna tentang apa yang digambarkannya.

## Buat sumber daya *Layanan Azure AI*

Anda dapat menggunakan kemampuan analisis gambar Azure AI Vision dengan **sumber daya multi-layanan layanan** Azure AI. Jika Anda belum melakukannya, buat sumber daya **Layanan Azure AI** di langganan Azure Anda.

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

1. Di tab browser lain, navigasikan ke [Vision Studio](https://portal.vision.cognitive.azure.com?azure-portal=true).

1. Masuk dengan akun Anda dan pastikan Anda menggunakan direktori yang sama dengan direktori tempat Anda membuat sumber daya layanan Azure AI Anda.

1. Pada beranda Vision Studio, pilih **Tampilkan semua sumber daya** di **bawah judul Memulai visi** .

    ![Tautan Lihat semua sumber daya disorot di bawah Mulai menggunakan Vision di Vision Studio.](./media/analyze-images-vision/vision-resources.png)

1. Pada halaman **Pilih sumber daya untuk bekerja dengan** , arahkan kursor mouse Anda ke atas sumber daya yang Anda buat di atas dalam daftar lalu centang kotak di sebelah kiri nama sumber daya, lalu pilih **Pilih sebagai sumber daya** default.

    > **Catatan** : Jika sumber daya Anda tidak tercantum, Anda mungkin perlu **Merefresh** halaman.

    ![Dialog Pilih sumber daya untuk dikerjakan ditampilkan dengan sumber daya Cognitive Services cog-ms-learn-vision-SUFFIX yang disorot dan diperiksa. Tombol Pilih sebagai sumber daya default disorot.](./media/analyze-images-vision/default-resource.png)

1. Tutup halaman pengaturan dengan memilih "x" di kanan atas layar.

## Membuat keterangan untuk gambar

Sekarang Anda siap menggunakan Vision Studio untuk menganalisis gambar yang diambil oleh kamera di *toko Northwind Traders* .

Mari kita lihat fungsionalitas keterangan gambar Azure AI Vision. Keterangan gambar tersedia melalui **fitur Keterangan** dan **Keterangan** Padat.

1. Di browser web, navigasikan ke [Vision Studio](https://portal.vision.cognitive.azure.com?azure-portal=true).

1. Pada halaman **Mulai menggunakan arahan Visi** , pilih tab **Analisis** gambar lalu pilih **petak Tambahkan keterangan ke gambar** .

    ![Pada beranda Vision Studio, tab Analisis gambar dipilih dan disorot. Petak Tambahkan keterangan ke gambar disorot.](./media/analyze-images-vision/add-captions.png)

1. **Di bawah subjudul Coba Keluar**, akui kebijakan penggunaan sumber daya dengan membaca dan mencentang kotak.  

1. Pilih [**https://aka.ms/mslearn-images-for-analysis](https://aka.ms/mslearn-images-for-analysis)** untuk mengunduh **image-analysis.zip.** Buka folder di komputer Anda dan temukan file bernama **store-camera-1.jpg**; yang berisi gambar berikut:

    ![Gambar orang tua yang menggunakan kamera ponsel untuk mengambil gambar anak di toko](./media/analyze-images-vision/store-camera-1.jpg)

1. **Unggah gambar store-camera-1.jpg** dengan menyeretnya ke kotak **Seret dan letakkan file di sini**, atau dengan menelusurinya di sistem file Anda.

1. Amati teks keterangan yang dihasilkan, terlihat di **panel Atribut** yang terdeteksi di sebelah kanan gambar.

    Fungsionalitas **** Keterangan menyediakan satu kalimat bahasa Inggris yang dapat dibaca manusia yang menjelaskan konten gambar.

1. Selanjutnya, gunakan gambar yang sama untuk melakukan **keterangan padat**. Kembali ke **beranda Vision Studio** , dan seperti yang Anda lakukan sebelumnya, pilih tab **Analisis** gambar, lalu pilih **petak peta Keterangan** padat.

    Fitur **Keterangan** Padat berbeda dari **kemampuan Keterangan** karena memberikan beberapa keterangan yang dapat dibaca manusia untuk gambar, satu menggambarkan konten gambar dan lainnya, masing-masing mencakup objek penting yang terdeteksi dalam gambar. Setiap objek yang terdeteksi menyertakan kotak pembatas, yang menentukan koordinat piksel dalam gambar yang terkait dengan objek.

1. Arahkan mouse ke atas salah satu keterangan dalam **daftar Atribut yang terdeteksi** dan amati apa yang terjadi dalam gambar.

    ![Gambar dan keterangannya ditampilkan.](./media/analyze-images-vision/dense-captioning.png)

    Pindahkan kursor mouse Anda ke atas keterangan lain dalam daftar, dan perhatikan bagaimana kotak pembatas bergeser dalam gambar untuk menyoroti bagian gambar yang digunakan untuk menghasilkan keterangan.

## Memberi tag pada gambar

Fitur berikutnya yang akan Anda coba adalah **fungsi ekstrak Tag** . Tag ekstrak didasarkan pada ribuan objek yang dapat dikenali, termasuk makhluk hidup, pemandangan, dan tindakan.

1. Kembali ke beranda Vision Studio, lalu pilih **petak Ekstrak tag umum dari gambar** di bawah tab **Analisis** gambar.

2. **Di pilih model yang ingin Anda coba**, biarkan **Model** bawaan vs. kesenjangan dipilih. Di pilih **bahasa** Anda, pilih **Bahasa Inggris** atau bahasa preferensi Anda.

3. Buka folder yang berisi gambar yang Anda unduh dan temukan file bernama **store-image-2.jpg**, yang terlihat seperti ini:

    ![Gambar orang dengan keranjang belanja di supermarket](./media/analyze-images-vision/store-camera-2.jpg)

4. **Unggah file store-camera-2.jpg**.

5. Tinjau daftar tag yang diekstrak dari gambar dan skor keyakinan untuk masing-masing di panel atribut yang terdeteksi. Di sini skor keyakinan adalah kemungkinan teks untuk atribut yang terdeteksi menjelaskan apa yang sebenarnya ada dalam gambar. Perhatikan dalam daftar tag bahwa tag tersebut tidak hanya mencakup objek, tetapi tindakan, seperti *belanja*, *penjualan*, dan *berdiri*.

    ![Cuplikan layar panel deteksi atribut di Vision Studio dengan skor teks dan keyakinan ditampilkan di samping gambar asli.](./media/analyze-images-vision/detect-attributes.png)

## Deteksi objek

Dalam tugas ini, Anda menggunakan **fitur Deteksi** objek dari Analisis Gambar. Deteksi objek mendeteksi dan mengekstrak kotak pembatas berdasarkan ribuan objek dan makhluk hidup yang dapat dikenali.

1. Kembali ke beranda Vision Studio, lalu pilih petak **Deteksi objek umum dalam gambar** di bawah tab **Analisis** gambar.

1. **Di pilih model yang ingin Anda coba**, biarkan **Model** bawaan vs. kesenjangan dipilih.

1. Buka folder yang berisi gambar yang Anda unduh dan temukan file bernama **store-camera-3.jpg**, yang terlihat seperti ini:

    ![Gambar orang dengan troli belanja](./media/analyze-images-vision/store-camera-3.jpg)

1. **Unggah file store-camera-3.jpg**.

1. Dalam kotak **Atribut** yang terdeteksi, amati daftar objek yang terdeteksi dan skor keyakinannya.

1. Arahkan kursor mouse Anda ke atas objek dalam **daftar Atribut yang terdeteksi untuk menyoroti kotak pembatas** objek dalam gambar.

1. Pindahkan **penggeser Nilai** ambang hingga nilai 70 ditampilkan di sebelah kanan penggeser. Amati apa yang terjadi pada objek dalam daftar. Penggeser ambang menentukan bahwa hanya objek yang diidentifikasi dengan skor keyakinan atau probabilitas yang lebih besar dari ambang batas yang harus ditampilkan.

## Penghapusan

Jika Anda tidak berniat untuk melakukan lebih banyak latihan, hapus sumber daya apa pun yang tidak lagi Anda butuhkan. Ini menghindari akumulasi biaya yang tidak perlu.

1.  [Buka portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat. 
1.  Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya kemudian dihapus.

## Pelajari selengkapnya

Untuk mempelajari selengkapnya tentang apa yang bisa Anda lakukan dengan layanan ini, lihat [halaman](https://learn.microsoft.com/azure/ai-services/computer-vision/overview) Azure AI Vision.
