---
lab:
  title: 'Mengekstrak data dari dokumen di Azure AI Foundry '
---

# Mengekstrak data dari dokumen di Azure AI Foundry 

Layanan **Azure AI Document Intelligence** dapat menganalisis dan mengekstrak informasi dari formulir dan dokumen, lalu mengidentifikasi nama bidang dan data. 

Bagaimana Document Intelligence meningkatkan pengenalan karakter optik (OCR)? Meskipun OCR dapat membaca dokumen cetak atau tulisan tangan, OCR mengekstrak teks dalam format yang tidak terstruktur sehingga sulit untuk disimpan dalam database atau dianalisis. Document Intelligence memahami data yang tidak terstruktur dengan menangkap struktur dari teks, seperti bidang data dan informasi dalam tabel. 

Dalam latihan ini, Anda akan menggunakan model bawaan Azure AI Document Intelligence di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk mengenali data dari tanda terima. 

## Membuat proyek di portal Azure AI Foundry

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup tips atau panel mulai cepat yang dibuka saat pertama kali Anda masuk. 

1. Di browser, navigasikan ke `https://ai.azure.com/managementCenter/allResources`dan pilih **Create**. Lalu pilih opsi untuk membuat *sumber daya hub AI* baru.

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

    Tunggu sampai proyek dan hub Anda selesai dibuat.

1. Saat proyek dibuat, Anda akan dibawa ke *halaman Gambaran Umum* tentang detail proyek. Di menu sebelah kiri pada layar, pilih **Layanan AI**. 

1. Pada halaman *Layanan AI*, pilih petak *Visi + Dokumen* untuk mencoba kemampuan Azure AI Vision dan Dokumen.

    ![Tangkapan layar peta Visi dan petak Dokumen di Azure AI Foundry.](./media/vision-document-tile.png)

## Menganalisis tanda terima dengan Kecerdasan Dokumen Azure AI di Azure AI Foundry 

Kini Anda siap menganalisis tanda terima untuk perusahaan ritel fiktif Northwind Traders.

1. Pada halaman *Visi + Dokumen* , gulir ke bawah dan pilih **Dokumen**. Di bawah *Model bawaan untuk dokumen tertentu*, pilih petak **Tanda Terima**.

1. Di daftar menurun di bawah *Cobalah*, perhatikan bahwa sumber daya layanan Azure AI Anda telah dipilih. Biarkan apa adanya.

1. Di komputer Anda, gunakan [**https://aka.ms/mslearn-receipt**](https://aka.ms/mslearn-receipt)untuk membuka gambar sampel tanda terima. Simpan file ke desktop atau folder Unduhan Anda. 
 
1. Dalam Azure AI Foundry, pada halaman*Tanda terima*, pilih **Telusuri file** dan navigasi ke folder tempat Anda menyimpan gambar. Pilih gambar tanda terima, lalu **Buka**. Gambar akan muncul di sebelah kiri layar.

    ![Cuplikan layar tanda terima northwind.](media/document-intelligence/receipt.jpg)

1. Di sebelah kanan, pilih **Jalankan analisis**.

1. Setelah analisis dijalankan, hasilnya akan diberikan. Perhatikan bahwa layanan telah mengenali bidang data tertentu, seperti nama penjual, alamat, nomor telepon, dan tanggal dan waktu transaksi, serta item baris, subtotal, pajak, dan jumlah total. Di samping setiap bidang adalah persentase peluang yang menunjukkan tingkat akurasi bidang.

    ![Cuplikan layar hasil analisis tanda terima di portal Azure AI Foundry, memperlihatkan kotak pembatas di sekitar bidang data dan teksnya di bidang yang diekstrak tersebut.](media/receipt-lab-result.png)

Dalam latihan ini Anda telah menggunakan model tanda terima bawaan Azure AI Document Intelligence di portal Azure AI Foundry. Hasil yang diberikan menunjukkan bagaimana Document Intelligence mampu mengidentifikasi bidang tertentu sehingga memungkinkan data dari dokumen sehari-hari diproses dengan lebih mudah. Sebelum menutup demonya, mengapa tidak mencoba untuk mencoba beberapa sampel tanda terima, termasuk sampel dalam berbagai bahasa?

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Latihan ini hanya menunjukkan beberapa kemampuan layanan AI Document Intelligence. Untuk mempelajari selengkapnya tentang kemampuan layanan ini, lihat halaman [Document Intelligence](https://learn.microsoft.com/azure/ai-services/document-intelligence/overview?view=doc-intel-3.1.0).
