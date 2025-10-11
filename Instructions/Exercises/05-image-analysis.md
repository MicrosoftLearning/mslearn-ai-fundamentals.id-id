---
lab:
  title: Menganalisis gambar di portal Azure AI Foundry
---

# Menganalisis gambar di portal Azure AI Foundry

**Azure AI Visual** mencakup berbagai kemampuan untuk memahami konten dan konteks gambar serta mengekstrak informasi dari gambar. Dalam latihan ini, Anda akan menggunakan Azure AI Vision di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk menganalisis gambar menggunakan pengalaman pencobaan bawaan. 

Misalnya, retailer fiktif *Northwind Traders* memutuskan untuk menerapkan "toko pintar", yang mana layanan AI memantau toko untuk mengidentifikasi pelanggan yang memerlukan bantuan, dan mengarahkan karyawan untuk membantu mereka. Dengan menggunakan Azure AI Visual, gambar yang diambil oleh kamera di seluruh toko dapat dianalisis untuk memberikan deskripsi bermakna tentang isi gambar.

Latihan ini memakan waktu sekitar **20** menit.

## Mengunduh dan mengekstrak file gambar

1. Unduh **[image-analysis.zip](https://aka.ms/mslearn-images-for-analysis)** dari `https://aka.ms/mslearn-images-for-analysis`.
1. Ekstrak file .zip yang diunduh ke folder di komputer Anda.

## Membuat proyek di portal Azure AI Foundry

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup semua tips atau panel mulai cepat yang terbuka saat pertama kali Anda masuk, dan jika perlu, gunakan logo **Azure AI Foundry** di kiri atas untuk menavigasi ke beranda, yang tampilannya mirip dengan gambar berikut (tutup panel **Bantuan** jika terbuka):

    ![Cuplikan layar beranda portal Azure AI Foundry.](./media/ai-foundry-portal.png)

1. Gulir ke bagian bawah halaman, dan pilih petak **Jelajahi Layanan Azure AI**.

    ![Cuplikan layar petak Jelajahi Layanan Azure AI.](./media/ai-services.png)

1. Pada halaman Layanan Azure AI, pilih petak **Visual + Dokumen**.

    ![Cuplikan layar petak Visual + Dokumen.](./media/vision-tile.png)

1. Pada halaman **Visual + Dokumen**, lihat tab **Gambar** dan pilih petak **Keterangan gambar**.

    ![Cuplikan layar petak Keterangan gambar.](./media/image-captioning-tile.png)

1. Di panel **Tambahkan keterangan ke gambar**, gunakan tombol **pilih hub** untuk **membuat hub baru** dengan pengaturan berikut:
    - **Nama hub**: *Masukkan nama yang valid untuk hub Anda.*
    - **Langganan**: *Langganan Azure Anda*
    - **Grup sumber daya**: *Buat atau pilih grup sumber daya*
    - **Lokasi**: *Pilih salah satu lokasi berikut*/*:
        - AS Timur
        - Prancis Tengah
        - Korea Tengah
        - Eropa Barat
        - US Barat
    - **Sambungkan Layanan Azure AI**: *Membuat sumber daya Layanan Azure AI baru dengan nama yang valid*
    - **Menyambungkan Azure AI Search**: Lewati koneksi

    \**Pada saat penulisan, Azure AI Visual didukung di hub di wilayah-wilayah ini*.

1. Saat hub dibuat, Anda akan diminta untuk membuat proyek. Masukkan nama proyek yang sesuai, lalu pilih **Buat proyek**.

## Membuat keterangan untuk gambar

Mari kita gunakan fungsionalitas keterangan gambar Azure AI Vision untuk menganalisis gambar yang diambil oleh kamera di penyimpanan *Northwind Traders* . Keterangan gambar tersedia melalui fitur **Keterangan** dan **Keterangan Padat**.

1. Pilih **Layanan AI** di panel navigasi kiri.

    *Sekarang Anda perlu mengulangi langkah-langkah yang sebelumnya untuk kembali ke antarmuka keterangan gambar dan menggunakan proyek berbasis hub baru.*

1. Pada halaman **Layanan AI**, pilih petak **Visual + Dokumen**. Kemudian, di halaman **Visual + Dokumen**, pada tab **Gambar**, pilih petak **Keterangan gambar**.

1. Pada halaman **Tambahkan keterangan ke gambar**, di bawah menu pilihan *Layanan Azure AI Terhubung*, pastikan sumber daya layanan Azure AI yang Anda buat di hub Anda telah dipilih.

1. Gunakan tautan **Telusuri file** untuk mengunggah gambar **store-camera-1.jpg** dari file yang telah diunduh dan diekstrak sebelumnya.

1. Amati teks keterangan yang dihasilkan, yang terlihat pada panel **Atribut terdeteksi** di sebelah kanan gambar.

    ![Cuplikan layar halaman Tambahkan keterangan ke gambar dengan gambar yang dianalisis.](./media/image-captioning.png)

    Fungsionalitas **Keterangan** menyediakan satu kalimat bahasa Inggris yang dapat dibaca manusia yang menjelaskan konten gambar.

1. Berikutnya, gunakan gambar yang sama untuk melakukan **Pembuatan keterangan padat**. Kembali ke halaman **Visual + Dokumen** dengan memilih panah **&larr;** *kembali* di bagian atas halaman; lalu pada halaman **Visual + Dokumen**, pada tab **Gambar**, pilih petak **Teks padat**.

    Fitur **Keterangan Padat** berbeda dari kemampuan **Keterangan** karena fitur ini memberikan beberapa teks gambar yang dapat dibaca manusia, satu menjelaskan konten gambar dan lainnya, masing-masing mencakup objek penting yang terdeteksi di gambar. Setiap objek yang terdeteksi menyertakan kotak pembatas, yang menentukan koordinat piksel dalam gambar yang terkait dengan objek tersebut.

1. Unggah gambar **store-camera-1.jpg** lagi, dan lihat hasil teks keterangan padat.

    ![Cuplikan layar hasil teks keterangan padat.](./media/dense-captioning.png)

    Arahkan mouse ke atas salah satu keterangan dalam daftar **Atribut terdeteksi** dan amati bahwa keterangan dihasilkan untuk setiap objek yang terdeteksi dalam gambar.

## Memberi tag pada gambar 

Fitur berikutnya yang akan Anda coba adalah fungsi *Ekstrak Tag*. Ekstrak tag didasarkan pada ribuan objek yang dapat dikenali, termasuk makhluk hidup, lingkungan, dan tindakan.

1. Kembali ke halaman **Visual + Dokumen** dengan memilih panah **&larr;** *kembali* di bagian atas halaman. Kemudian pada halaman **Visual + Dokumen**, pada tab **Gambar**, pilih petak **Ekstraksi tag umum**.
1. Unggah file **store-camera-2.jpg** dari folder yang Anda ekstrak sebelumnya.
1. Tinjau daftar tag yang diekstrak dari gambar dan skor kepercayaan untuk tiap tag di panel atribut terdeteksi. Skor keyakinan di sini merupakan probabilitas bahwa teks untuk atribut yang terdeteksi menggambarkan apa yang sebenarnya ada dalam gambar. Perhatikan dalam daftar tag bahwa tag tersebut tidak hanya mencakup objek, tetapi juga tindakan, seperti *berbelanja*, *berjualan*, dan *berdiri*.

    ![Cuplikan layar panel deteksi atribut di Vision Studio dengan teks dan skor keyakinan ditampilkan di sebelah gambar asli.](./media/analyze-images-vision/detect-attributes.png)

## Deteksi objek

Dalam tugas ini, Anda menggunakan fitur **Deteksi objek** dari Analisis Gambar. Deteksi objek mendeteksi dan mengekstrak kotak pembatas berdasarkan ribuan objek dan makhluk hidup yang dapat dikenali.

1. Kembali ke halaman **Visual + Dokumen** dengan memilih panah **&larr;** *kembali* di bagian atas halaman. Kemudian pada tab **Gambar**, pilih petak **Deteksi objek umum**.

1. Unggah file **store-camera-3.jpg**.

1. Pada kotak **Atribut terdeteksi**, amati daftar objek yang terdeteksi dan skor keyakinannya.

    ![Cuplikan layar hasil teks keterangan padat.](./media/object-detection.png)

1. Coba deteksi objek dalam **store-camera-4.jpg**

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat. 
1. Pilih **Hapus grup sumber daya**, lalu **masukkan nama grup sumber daya** untuk mengonfirmasi. Grup sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman Azure AI Visual](https://learn.microsoft.com/azure/ai-services/computer-vision/overview).
