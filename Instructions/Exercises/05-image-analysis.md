---
lab:
  title: Menganalisis gambar di portal Azure AI Foundry
---

# Menganalisis gambar di portal Azure AI Foundry

**Azure AI Visual** mencakup berbagai kemampuan untuk memahami konten dan konteks gambar serta mengekstrak informasi dari gambar. Dalam latihan ini, Anda akan menggunakan Azure AI Vision di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk menganalisis gambar menggunakan pengalaman pencobaan bawaan. 

Misalnya, retailer fiktif *Northwind Traders* memutuskan untuk menerapkan "toko pintar", yang mana layanan AI memantau toko untuk mengidentifikasi pelanggan yang memerlukan bantuan, dan mengarahkan karyawan untuk membantu mereka. Dengan menggunakan Azure AI Visual, gambar yang diambil oleh kamera di seluruh toko dapat dianalisis untuk memberikan deskripsi bermakna tentang isi gambar.

Latihan ini memakan waktu sekitar **20** menit.

## Membuat proyek di portal Azure AI Foundry

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup tips atau panel mulai cepat yang dibuka saat pertama kali Anda masuk. 

1. Di browser, navigasikan ke `https://ai.azure.com/managementCenter/allResources` dan pilih **Buat baru**. Lalu pilih opsi untuk membuat **sumber daya hub AI** baru.

1. Di wizard *Buat proyek* masukkan nama yang valid untuk proyek Anda dan jika disarankan hub yang sudah ada pilih opsi untuk membuat yang *baru*. 

1. Perluas *opsi Tingkat Lanjut* untuk menentukan pengaturan proyek Anda sebagai berikut:
    - **Subscription**: Langganan Azure Anda
    - **Grup sumber daya**: Buat atau pilih grup sumber daya
    - **Wilayah**: Pilih salah satu wilayah berikut:
        * AS Timur
        * Prancis Tengah
        * Korea Tengah
        * Eropa Barat
        * US Barat

    Pilih **Buat**. Tunggu sampai proyek dan hub Anda selesai dibuat. Proses ini memerlukan waktu beberapa menit.

1. Saat proyek dibuat, Anda akan dibawa ke *halaman Gambaran Umum* tentang detail proyek. Di menu sebelah kiri pada layar, pilih **Layanan AI**. 

    >*Catatan*: Perluas menu untuk membaca kontennya dengan mengklik ikon 'perluas' atas. 

1. Pada halaman *Layanan AI*, pilih petak *Visi + Dokumen* untuk mencoba kemampuan Azure AI Vision dan Dokumen.

    ![Tangkapan layar peta Visi dan petak Dokumen di Azure AI Foundry.](./media/vision-document-tile.png)

## Membuat keterangan untuk gambar

Mari kita gunakan fungsionalitas keterangan gambar Azure AI Vision untuk menganalisis gambar yang diambil oleh kamera di penyimpanan *Northwind Traders* . Keterangan gambar tersedia melalui fitur **Keterangan** dan **Keterangan Padat**.

1. Pada halaman *Visi + Dokumen* , gulir ke bawah dan pilih **Gambar** di bawah *Tampilkan semua kemampuan visi lainnya*. Lalu pilih petak **Keterangan gambar**.

    ![Cuplikan layar petak keterangan gambar di bagian gambar halaman Visi dan Dokumen.](./media/vision-image-captioning-tile.png)

1. Pada halaman **Tambahkan keterangan ke gambar**, di bawah menu pilihan *layanan Azure AI yang terhubung*, perhatikan bahwa sumber daya *layanan Azure AI* yang Anda buat telah dipilih. Anda tidak harus membuat perubahan. 

    >*Catatan*: jika tidak menyesuaikan lokasi sumber daya yang valid sebelumnya selama pembuatan sumber daya, Anda mungkin diminta untuk membuat sumber daya layanan Azure AI baru yang berada di wilayah yang valid. Anda harus membuat sumber daya baru untuk melanjutkan lab.  

1. Unduh **image-analysis.zip** dengan membuka URL `https://aka.ms/mslearn-images-for-analysis` di tab browser baru. Menggunakan URL akan otomatis mengunduh folder di komputer Anda. 

1. Buka folder *Download* di komputer Anda, lalu identifikasi folder yang diunduh. Klik kanan folder yang diunduh. Pilih *Ekstrak Semua...*. Lalu pilih *Ekstrak* untuk mengekstrak file-nya. Folder yang tidak di-zip akan muncul pada layar.  

1. Di folder yang tidak di-zip, cari file bernama **store-camera-1.jpg**; yang berisi gambar berikut:

    ![Gambar orang tua yang menggunakan kamera ponsel untuk mengambil gambar anak di toko](./media/analyze-images-vision/store-camera-1.jpg)

1. Unggah gambar **store-camera-1.jpg** dengan memilih *Telusuri file*. Anda dapat menemukan gambar di folder *Download* pada sistem file Anda.

1. Amati teks keterangan yang dihasilkan, yang terlihat pada panel **Atribut terdeteksi** di sebelah kanan gambar.

    Fungsionalitas **Keterangan** menyediakan satu kalimat bahasa Inggris yang dapat dibaca manusia yang menjelaskan konten gambar.

1. Berikutnya, gunakan gambar yang sama untuk melakukan **Pembuatan keterangan padat**. Kembali ke halaman **Visi + Dokumen** dengan memilih panah *belakang* di bagian atas halaman. Pada halaman *Visi + Dokumen* , pilih tab **Gambar**, lalu pilih petak**Teks padat** .

    Fitur **Keterangan Padat** berbeda dari kemampuan **Keterangan** karena fitur ini memberikan beberapa teks gambar yang dapat dibaca manusia, satu menjelaskan konten gambar dan lainnya, masing-masing mencakup objek penting yang terdeteksi di gambar. Setiap objek yang terdeteksi menyertakan kotak pembatas, yang menentukan koordinat piksel dalam gambar yang terkait dengan objek tersebut.

1. Arahkan kursor ke salah satu keterangan dalam daftar atribut **Terdeteksi** dan amati apa yang terjadi dalam gambar.

    ![Gambar dan keterangannya ditampilkan.](./media/analyze-images-vision/dense-captioning.png)

    Gerakkan kursor mouse Anda ke keterangan lain dalam daftar, dan perhatikan bagaimana kotak pembatas bergeser pada gambar untuk menyorot bagian gambar yang digunakan untuk menghasilkan keterangan.

## Memberi tag pada gambar 

Fitur berikutnya yang akan Anda coba adalah fungsi *Ekstrak Tag*. Ekstrak tag didasarkan pada ribuan objek yang dapat dikenali, termasuk makhluk hidup, lingkungan, dan tindakan.

1. Kembali ke halaman *Visi + Dokumen* Azure AI Foundry, lalu pilih tab **Gambar**, dan pilih petak **Ekstraksi tag umum**.

1. Buka folder yang berisi gambar yang Anda unduh dan temukan file bernama **store-image-2.jpg**, yang terlihat seperti ini:

    ![Gambar orang dengan keranjang belanja di supermarket](./media/analyze-images-vision/store-camera-2.jpg)

1. Unggah file **store-camera-2.jpg**.

1. Tinjau daftar tag yang diekstrak dari gambar dan skor kepercayaan untuk tiap tag di panel atribut terdeteksi. Skor keyakinan di sini merupakan probabilitas bahwa teks untuk atribut yang terdeteksi menggambarkan apa yang sebenarnya ada dalam gambar. Perhatikan dalam daftar tag bahwa tag tersebut tidak hanya mencakup objek, tetapi juga tindakan, seperti *berbelanja*, *berjualan*, dan *berdiri*.

    ![Cuplikan layar panel deteksi atribut di Vision Studio dengan teks dan skor keyakinan ditampilkan di sebelah gambar asli.](./media/analyze-images-vision/detect-attributes.png)

## Deteksi objek

Dalam tugas ini, Anda menggunakan fitur **Deteksi objek** dari Analisis Gambar. Deteksi objek mendeteksi dan mengekstrak kotak pembatas berdasarkan ribuan objek dan makhluk hidup yang dapat dikenali.

1. Kembali ke halaman *Visi + Dokumen* Azure AI Foundry, lalu pilih tab **Gambar**, dan pilih **petak Deteksi objek umum**.

1. Buka folder yang berisi gambar yang Anda unduh dan temukan file bernama **store-camera-3.jpg**, yang terlihat seperti ini:

    ![Gambar orang dengan troli belanja](./media/analyze-images-vision/store-camera-3.jpg)

1. Unggah file **store-camera-3.jpg**.

1. Pada kotak **Atribut terdeteksi**, amati daftar objek yang terdeteksi dan skor keyakinannya.

1. Arahkan kursor mouse ke objek dalam daftar **Atribut terdeteksi** untuk menyorot kotak pembatas objek pada gambar.

1. Pindahkan penggeser **Nilai ambang** hingga nilai 70 ditampilkan di sebelah kanan penggeser. Amati apa yang terjadi pada objek dalam daftar. Penggeser ambang menentukan bahwa hanya objek yang diidentifikasi dengan skor keyakinan atau probabilitas yang lebih besar dari ambang yang harus ditampilkan.

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat. 
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman Azure AI Visual](https://learn.microsoft.com/azure/ai-services/computer-vision/overview).
