---
lab:
  title: Mengekstrak data formulir di Document Intelligence Studio
---

# Mengekstrak data formulir di Document Intelligence Studio

Azure AI Document Intelligence dapat menganalisis dan mengekstrak informasi dari formulir dan dokumen, lalu mengidentifikasi nama bidang dan data. 

Bagaimana Document Intelligence meningkatkan pengenalan karakter optik (OCR)? Meskipun OCR dapat membaca dokumen cetak atau tulisan tangan, OCR mengekstrak teks dalam format yang tidak terstruktur sehingga sulit untuk disimpan dalam database atau dianalisis. Document Intelligence memahami data yang tidak terstruktur dengan menangkap struktur teks, seperti pasangan kunci/nilai dan informasi dalam tabel. 

Dalam latihan ini, Anda akan melihat model bawaan di Document Intelligence yang dilatih untuk mengenali data tanda terima. 

> **CATATAN** Azure AI Document Intelligence merupakan nama baru untuk Azure Form Recognizer. Anda mungkin masih melihat Azure Form Recognizer di portal Azure atau Document Intelligence Studio.

## Membuat sumber daya *Document Intelligence*

Anda dapat menggunakan Azure AI Document Intelligence dengan membuat sumber daya *Document Intelligence* atau sumber daya *layanan Azure AI*. Dalam latihan ini, Anda akan membuat sumber daya *Document Intelligence*, jika belum memilikinya.

1. Di tab browser lain, buka [Document Intelligence Studio](https://formrecognizer.appliedai.azure.com/studio), lalu masuk dengan akun Microsoft Anda.
1. Pilih **Pengaturan**, lalu pilih tab **Sumber Daya**. Pilih **Buat sumber daya baru**.
1. Pada kotak dialog Buat sumber daya, masukkan informasi berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Nama sumber daya baru**: *Masukkan nama yang unik*.
    - **Lokasi**: *Pilih wilayah. Jika berada di AS Timur, gunakan "US Timur 2"*.
    - **Tingkat harga**: *FO Gratis (jika tersedia, pilih SO Standar jika tidak tersedia)*.
1. Pilih **Lanjutkan**, lalu **Selesai**. Tunggu hingga sumber daya disebarkan.

    >**Catatan** Jika sumber daya belum ditampilkan, Anda mungkin perlu **Me-refresh** halaman.

Biarkan Document Intelligence Studio tetap terbuka.

## Menganalisis tanda terima di Document Intelligence Studio

Kini Anda siap menganalisis tanda terima untuk perusahaan ritel fiktif Northwind Traders.

1. Pilih [**https://aka.ms/mslearn-receipt**](https://aka.ms/mslearn-receipt) untuk mengunduh dokumen sampel ke komputer Anda. Buka folder . 
1. Pilih **Document Intelligence Studio** untuk kembali ke halaman **Mulai Menggunakan Document Intelligence Studio**, dan di bawah Tanda Terima pilih **Coba**.
1. Di Daftar menurun bawaan, pastikan **Tanda Terima** telah dipilih.
1. Pilih **Telusuri file** dan buka folder tempat Anda menyimpan gambar. Pilih gambar tanda terima, lalu **Buka**. Gambar akan muncul di sebelah kiri layar.

    ![Cuplikan layar tanda terima northwind.](media/document-intelligence/receipt.jpg)

1. Di sebelah kanan, pilih **Jalankan analisis**.
1. Setelah analisis dijalankan, hasilnya akan diberikan. Perhatikan bahwa layanan telah mengenali bidang data tertentu, seperti nama penjual, alamat, nomor telepon, dan tanggal dan waktu transaksi, serta item baris, subtotal, pajak, dan jumlah total. Di samping setiap bidang adalah persentase peluang yang menunjukkan tingkat akurasi bidang.

Dalam latihan ini, Anda telah menggunakan Document Intelligence Studio untuk membuat sumber daya Document Intelligence. Anda kemudian menggunakan layanan untuk menganalisis tanda terima. Hasil yang diberikan menunjukkan bagaimana Document Intelligence mampu mengidentifikasi bidang tertentu sehingga memungkinkan data dari dokumen sehari-hari diproses dengan lebih mudah. Sebelum menutup Document Intelligence Studio, pertimbangkan untuk mencoba beberapa sampel tanda terima, termasuk sampel dalam berbagai bahasa.

## Penghapusan

Jika Anda tidak berniat melakukan latihan lagi, hapus semua sumber daya yang tidak dibutuhkan lagi. Dengan cara ini, Anda dapat menghindari pengeluaran biaya yang tidak perlu.

1. Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus**, lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Latihan ini hanya menunjukkan beberapa kemampuan layanan AI Document Intelligence. Untuk mempelajari selengkapnya tentang kemampuan layanan ini, lihat halaman [Document Intelligence](https://learn.microsoft.com/azure/ai-services/document-intelligence/overview?view=doc-intel-3.1.0).
