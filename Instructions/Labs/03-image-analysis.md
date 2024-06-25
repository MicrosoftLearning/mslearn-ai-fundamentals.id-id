---
lab:
  title: Menganalisis gambar di Vision Studio
---

# Menganalisis gambar di Vision Studio 

**Azure AI Visual** mencakup berbagai kemampuan untuk memahami konten dan konteks gambar serta mengekstrak informasi dari gambar. Azure AI Vision Studio memungkinkan Anda mencoba banyak kemampuan analisis gambar. 

Dalam latihan ini, Anda akan menggunakan Vision Studio untuk menganalisis gambar menggunakan pengalaman uji coba bawaan. Misalnya, retailer fiktif *Northwind Traders* memutuskan untuk menerapkan "toko pintar", yang mana layanan AI memantau toko untuk mengidentifikasi pelanggan yang memerlukan bantuan, dan mengarahkan karyawan untuk membantu mereka. Dengan menggunakan Azure AI Visual, gambar yang diambil oleh kamera di seluruh toko dapat dianalisis untuk memberikan deskripsi bermakna tentang isi gambar.

## Buat sumber daya *Layanan Azure AI*

Anda dapat menggunakan kemampuan analisis gambar dari Azure AI Visual dengan sumber daya multi-layanan **Layanan Azure AI**. Jika Anda belum melakukannya, buat sumber daya **Layanan Azure AI** di langganan Azure Anda.

1. Di tab browser yang lain, buka portal Azure di [https://portal.azure.com](https://portal.azure.com?azure-portal=true), lalu masuk dengan akun Microsoft yang terkait dengan langganan Azure Anda.

1. Klik tombol **＋Buat sumber daya**dan cari *layanan Azure AI*. Pilih **buat** paket **layanan Azure AI**. Anda akan diarahkan ke halaman untuk membuat sumber daya layanan Azure AI. Konfigurasikan dengan pengaturan berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Wilayah**: *Pilih wilayah geografis terdekat. Jika berada di AS timur, gunakan "US Timur 2"*.
    - **Nama**: *Masukkan nama unik*.
    - **Tingkat harga**: *Standar S0.*
    - **Dengan mencentang kotak ini, saya menyatakan bahwa saya telah membaca dan memahami semua ketentuan di bawah ini**: *Dipilih*.

1. Pilih **Tinjau + buat**, lalu **Buat** dan tunggu hingga penyebaran selesai.

## Menyambungkan sumber daya layanan Azure AI Anda ke Vision Studio

Berikutnya, sambungkan sumber daya layanan Azure AI yang Anda provisikan di atas ke Vision Studio.

1. Di tab browser yang lain, navigasikan ke [Vision Studio](https://portal.vision.cognitive.azure.com?azure-portal=true).

1. Masuk dengan akun Anda dan pastikan Anda menggunakan direktori yang sama dengan direktori tempat Anda membuat sumber daya layanan Azure AI Anda.

1. Di beranda Vision Studio, pilih **Tampilkan semua sumber daya** pada judul **Mulai menggunakan Visual**.

    ![Tautan Tampilkan semua sumber daya disorot pada Mulai menggunakan Visual di Vision Studio.](./media/analyze-images-vision/vision-resources.png)

1. Pada halaman **Pilih sumber daya yang akan digunakan**, arahkan kursor mouse pada sumber daya yang Anda buat di atas dalam daftar, lalu centang kotak di sebelah kiri nama sumber daya, lalu pilih **Pilih sebagai sumber daya default**.

    > **Catatan**: Jika sumber daya Anda tidak tercantum, Anda mungkin perlu **Me-refresh** halaman.

    ![Dialog Pilih sumber daya yang akan digunakan ditampilkan dengan sumber daya Cognitive Services cog-ms-learn-vision-SUFFIX yang disorot dan dicentang. Tombol Pilih sebagai sumber daya default disorot.](./media/analyze-images-vision/default-resource.png)

1. Tutup halaman pengaturan dengan memilih "x" di kanan atas layar.

## Membuat keterangan untuk gambar

Anda kini siap menggunakan Vision Studio untuk menganalisis gambar yang diambil oleh kamera di toko *Northwind Traders*.

Mari lihat fungsionalitas pembuatan keterangan gambar Azure AI Visual. Keterangan gambar tersedia melalui fitur **Keterangan** dan **Keterangan Padat**.

1. Di browser web, navigasikan ke [Vision Studio](https://portal.vision.cognitive.azure.com?azure-portal=true).

1. Pada halaman arahan **Mulai menggunakan Visual**, pilih tab **Analisis gambar**, lalu pilih ubin **Tambahkan keterangan ke gambar**.

    ![Pada beranda Vision Studio, tab Analisis gambar dipilih dan disorot. Ubin Tambahkan keterangan ke gambar disorot.](./media/analyze-images-vision/add-captions.png)

1. Pada subjudul **Coba**, setujui kebijakan penggunaan sumber daya dengan membaca dan mencentang kotak.  

1. Pilih [**https://aka.ms/mslearn-images-for-analysis**](https://aka.ms/mslearn-images-for-analysis) untuk mengunduh **image-analisis.zip**. Buka folder di komputer Anda dan temukan file bernama **store-camera-1.jpg**; yang berisi gambar berikut:

    ![Gambar orang tua yang menggunakan kamera ponsel untuk mengambil gambar anak di toko](./media/analyze-images-vision/store-camera-1.jpg)

1. Unggah gambar **store-camera-1.jpg** dengan menyeretnya ke kotak **Seret dan lepaskan file di sini**, atau dengan menelusurinya di sistem file Anda.

1. Amati teks keterangan yang dihasilkan, yang terlihat pada panel **Atribut terdeteksi** di sebelah kanan gambar.

    Fungsionalitas **Keterangan** menyediakan satu kalimat bahasa Inggris yang dapat dibaca manusia yang menjelaskan konten gambar.

1. Berikutnya, gunakan gambar yang sama untuk melakukan **Pembuatan keterangan padat**. Kembali ke beranda **Vision Studio**, dan seperti yang Anda lakukan sebelumnya, pilih tab **Analisis gambar**, lalu pilih ubin **Pembuatan keterangan padat**.

    Fitur **Keterangan Padat** berbeda dari kemampuan **Keterangan** karena fitur ini memberikan beberapa teks gambar yang dapat dibaca manusia, satu menjelaskan konten gambar dan lainnya, masing-masing mencakup objek penting yang terdeteksi di gambar. Setiap objek yang terdeteksi menyertakan kotak pembatas, yang menentukan koordinat piksel dalam gambar yang terkait dengan objek tersebut.

1. Arahkan kursor ke salah satu keterangan dalam daftar atribut **Terdeteksi** dan amati apa yang terjadi dalam gambar.

    ![Gambar dan keterangannya ditampilkan.](./media/analyze-images-vision/dense-captioning.png)

    Gerakkan kursor mouse Anda ke keterangan lain dalam daftar, dan perhatikan bagaimana kotak pembatas bergeser pada gambar untuk menyorot bagian gambar yang digunakan untuk menghasilkan keterangan.

## Memberi tag pada gambar

Fitur berikutnya yang akan Anda coba adalah fungsi **Ekstrak Tag**. Ekstrak tag didasarkan pada ribuan objek yang dapat dikenali, termasuk makhluk hidup, lingkungan, dan tindakan.

1. Kembali ke beranda Vision Studio, lalu pilih ubin **Ekstrak tag umum dari gambar** pada tab **Analisis gambar**.

2. Pada **Pilih model yang ingin Anda coba**, biarkan **Produk bawaan vs. model gap** tetap dipilih. Pada **Pilih bahasa Anda**, pilih **Inggris** atau bahasa pilihan Anda.

3. Buka folder yang berisi gambar yang Anda unduh dan temukan file bernama **store-image-2.jpg**, yang terlihat seperti ini:

    ![Gambar orang dengan keranjang belanja di supermarket](./media/analyze-images-vision/store-camera-2.jpg)

4. Unggah file **store-camera-2.jpg**.

5. Tinjau daftar tag yang diekstrak dari gambar dan skor kepercayaan untuk tiap tag di panel atribut terdeteksi. Skor keyakinan di sini merupakan probabilitas bahwa teks untuk atribut yang terdeteksi menggambarkan apa yang sebenarnya ada dalam gambar. Perhatikan dalam daftar tag bahwa tag tersebut tidak hanya mencakup objek, tetapi juga tindakan, seperti *berbelanja*, *berjualan*, dan *berdiri*.

    ![Cuplikan layar panel deteksi atribut di Vision Studio dengan teks dan skor keyakinan ditampilkan di sebelah gambar asli.](./media/analyze-images-vision/detect-attributes.png)

## Deteksi objek

Dalam tugas ini, Anda menggunakan fitur **Deteksi objek** dari Analisis Gambar. Deteksi objek mendeteksi dan mengekstrak kotak pembatas berdasarkan ribuan objek dan makhluk hidup yang dapat dikenali.

1. Kembali ke beranda Vision Studio, lalu pilih ubin **Deteksi objek umum dalam gambar** pada tab **Analisis gambar**.

1. Pada **Pilih model yang ingin Anda coba**, biarkan **Produk bawaan vs. model gap** tetap dipilih.

1. Buka folder yang berisi gambar yang Anda unduh dan temukan file bernama **store-camera-3.jpg**, yang terlihat seperti ini:

    ![Gambar orang dengan troli belanja](./media/analyze-images-vision/store-camera-3.jpg)

1. Unggah file **store-camera-3.jpg**.

1. Pada kotak **Atribut terdeteksi**, amati daftar objek yang terdeteksi dan skor keyakinannya.

1. Arahkan kursor mouse ke objek dalam daftar **Atribut terdeteksi** untuk menyorot kotak pembatas objek pada gambar.

1. Pindahkan penggeser **Nilai ambang** hingga nilai 70 ditampilkan di sebelah kanan penggeser. Amati apa yang terjadi pada objek dalam daftar. Penggeser ambang menentukan bahwa hanya objek yang diidentifikasi dengan skor keyakinan atau probabilitas yang lebih besar dari ambang yang harus ditampilkan.

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1.  Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat. 
1.  Pilih sumber daya dan pilih **Hapus**, lalu pilih **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman Azure AI Visual](https://learn.microsoft.com/azure/ai-services/computer-vision/overview).
