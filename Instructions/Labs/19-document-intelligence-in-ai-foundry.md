---
lab:
  title: 'Mengekstrak data dari dokumen di Azure AI Foundry '
---

# Mengekstrak data dari dokumen di Azure AI Foundry 

Layanan **Azure AI Document Intelligence** dapat menganalisis dan mengekstrak informasi dari formulir dan dokumen, lalu mengidentifikasi nama bidang dan data. 

Bagaimana Document Intelligence meningkatkan pengenalan karakter optik (OCR)? Meskipun OCR dapat membaca dokumen cetak atau tulisan tangan, OCR mengekstrak teks dalam format yang tidak terstruktur sehingga sulit untuk disimpan dalam database atau dianalisis. Document Intelligence memahami data yang tidak terstruktur dengan menangkap struktur dari teks, seperti bidang data dan informasi dalam tabel. 

Dalam latihan ini, Anda akan menggunakan model bawaan Azure AI Document Intelligence di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk mengenali data dari tanda terima. 

## Membuat proyek di portal Azure AI Foundry

1. Di tab browser, navigasikan ke [Azure AI Foundry](https://ai.azure.com?azure-portal=true).

1. Masuk dengan akun Anda. 

1. Pada halaman beranda portal Azure AI Foundry, pilih **Buat proyek**. Di Azure AI Foundry, proyek adalah kontainer yang membantu mengatur pekerjaan Anda.  

    ![Cuplikan layar beranda Azure AI Foundry dengan membuat proyek yang dipilih.](./media/azure-ai-foundry-home-page.png)

1. Pada panel *Buat proyek* , Anda akan melihat nama proyek yang dihasilkan, yang bisa Anda simpan apa adanya. Bergantung pada apakah Anda telah membuat hub sebelumnya, Anda akan melihat daftar sumber daya Azure *baru* yang akan dibuat atau daftar menurun hub yang ada. Jika Anda melihat daftar menurun hub yang ada, pilih *Buat hub baru*, buat nama unik untuk hub Anda, dan pilih *Berikutnya*.  
 
    ![Cuplikan layar panel buat proyek dengan nama yang dihasilkan secara otomatis untuk hub dan proyek.](./media/azure-ai-foundry-create-project.png)

> **Penting**: Anda akan memerlukan sumber daya layanan Azure AI yang disediakan di lokasi tertentu untuk menyelesaikan lab lainnya.

1. Di panel *Buat proyek * yang sama, pilih** Sesuaikan** dan pilih salah satu **Lokasi** berikut: AS Timur, Prancis Tengah, Korea Tengah, Eropa Barat, atau AS Barat untuk menyelesaikan lab lainnya. Lalu pilih **buat**. 

1. Perhatikan sumber daya yang dibuat: 
- Layanan Azure AI
- Hub Azure AI
- Proyek Azure AI
- Akun penyimpanan
- Brankas kunci
- Grup sumber daya  
 
1. Setelah sumber daya dibuat, Anda akan dibawa ke halaman* Gambaran Umum* proyek Anda. Di menu sebelah kiri pada layar, pilih **Layanan AI**.
 
    ![Cuplikan layar menu sebelah kiri pada layar proyek dengan Layanan AI dipilih.](./media/azure-ai-foundry-ai-services.png)  

1. Pada halaman *Layanan AI*, pilih petak *Visi + Dokumen* untuk mencoba kemampuan Azure AI Document Intelligence.

    ![Cuplikan layar petak Visi dan Dokumen dipilih di halaman Layanan AI.](./media/vision-document-tile.png)

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
