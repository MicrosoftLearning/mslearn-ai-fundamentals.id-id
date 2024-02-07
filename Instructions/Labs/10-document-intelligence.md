---
lab:
  title: Mengekstrak data formulir di Studio Kecerdasan Dokumen
---

# Mengekstrak data formulir di Studio Kecerdasan Dokumen

Kecerdasan Dokumen Azure AI dapat menganalisis dan mengekstrak informasi dari formulir dan dokumen, lalu mengidentifikasi nama bidang dan data. 

Bagaimana Kecerdasan Dokumen dibangun berdasarkan pengenalan karakter optik (OCR)? Meskipun OCR dapat membaca dokumen cetak atau tulisan tangan, OCR mengekstrak teks dalam format yang tidak terstruktur yang sulit disimpan dalam database atau menganalisis. Kecerdasan dokumen memahami data yang tidak terstruktur dengan menangkap struktur teks, seperti pasangan kunci/nilai dan informasi dalam tabel. 

Dalam latihan ini, Anda akan melihat model bawaan di Kecerdasan Dokumen yang dilatih untuk mengenali data tanda terima. 

> **CATATAN** Azure AI Document Intelligence adalah nama baru untuk Azure Form Recognizer. Anda mungkin masih melihat Azure Form Recognizer di portal Azure atau Document Intelligence Studio.

## Membuat *sumber daya Kecerdasan* Dokumen

Anda dapat menggunakan Kecerdasan Dokumen Azure AI dengan membuat *sumber daya Kecerdasan* Dokumen atau *sumber daya layanan* Azure AI. Dalam latihan ini, Anda akan membuat *sumber daya Kecerdasan* Dokumen, jika Anda belum memilikinya.

1. Di tab browser lain, buka [Document Intelligence Studio](https://formrecognizer.appliedai.azure.com/studio), masuk dengan akun Microsoft Anda.
1. Pilih **Pengaturan** dan pilih tab **Sumber Daya**. Pilih **Buat sumber daya** baru.
1. Pada kotak dialog Buat sumber daya, masukkan yang berikut ini:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Nama** sumber daya baru: *Masukkan nama* unik.
    - **Lokasi**: *Pilih wilayah*.
    - **Tingkat** harga: *FO Gratis (jika tersedia, jika tidak pilih SO Standar)*.
1. Pilih **Lanjutkan** lalu **Selesai**. Tunggu hingga sumber daya disebarkan.

    >**Catatan** Jika sumber daya Anda belum ditampilkan, Anda mungkin perlu **Merefresh** halaman.

Biarkan Studio Kecerdasan Dokumen tetap terbuka.

## Menganalisis tanda terima di Document Intelligence Studio

Anda sekarang siap untuk menganalisis tanda terima untuk perusahaan ritel Northwind Traders fiktif.

1. Pilih [****https://aka.ms/mslearn-receipt](https://aka.ms/mslearn-receipt) untuk mengunduh dokumen sampel ke komputer Anda. Buka folder . 
1. Pilih **Form Recognizer Studio** untuk kembali ke **halaman Mulai menggunakan Studio** Kecerdasan Dokumen, dan di bawah Tanda Terima pilih **Cobalah**.
1. Di daftar drop-down Bawaan, pastikan Tanda **Terima** dipilih.
1. Pilih **Telusuri file** dan navigasi ke folder tempat Anda menyimpan gambar. Pilih gambar tanda terima lalu **Buka**. Gambar muncul di sisi kiri layar.

    ![Tanda terima Northwind.](media/document-intelligence/northwind-receipt.jpg)

1. Di sebelah kanan, pilih **Jalankan analisis**.
1. Ketika analisis telah berjalan, hasilnya dikembalikan. Perhatikan bahwa layanan telah mengenali bidang data tertentu seperti nama pedagang, alamat, nomor telepon, dan tanggal dan waktu transaksi, serta item baris, subtotal, pajak, dan jumlah total. Di samping setiap bidang adalah probabilitas persentase bahwa bidang sudah benar.

Dalam latihan ini Anda telah menggunakan Studio Kecerdasan Dokumen untuk membuat sumber daya Kecerdasan Dokumen. Anda kemudian menggunakan layanan untuk menganalisis tanda terima. Dari hasil yang dikembalikan, Anda melihat bagaimana Kecerdasan Dokumen dapat mengidentifikasi bidang tertentu, memungkinkan data dari dokumen sehari-hari menjadi lebih mudah diproses. Sebelum Anda menutup Document Intelligence Studio, mengapa tidak mencoba beberapa tanda terima sampel, termasuk yang dalam bahasa yang berbeda?

## Penghapusan

Jika Anda tidak berniat untuk melakukan lebih banyak latihan, hapus sumber daya apa pun yang tidak lagi Anda butuhkan. Ini menghindari akumulasi biaya yang tidak perlu.

1. [Buka portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya kemudian dihapus.

## Pelajari selengkapnya

Latihan ini hanya menunjukkan beberapa kemampuan layanan Kecerdasan Dokumen AI. Untuk mempelajari selengkapnya tentang apa yang bisa Anda lakukan dengan layanan ini, lihat halaman [Kecerdasan](https://learn.microsoft.com/azure/ai-services/document-intelligence/overview?view=doc-intel-3.1.0) Dokumen.
