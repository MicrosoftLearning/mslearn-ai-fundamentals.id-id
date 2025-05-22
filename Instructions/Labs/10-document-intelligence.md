---
lab:
  title: 'Mengekstrak data dari dokumen di Azure AI Foundry '
---

# Mengekstrak data dari dokumen di Azure AI Foundry 

Layanan **Azure AI Document Intelligence** dapat menganalisis dan mengekstrak informasi dari formulir dan dokumen, lalu mengidentifikasi nama bidang dan data. 

Bagaimana Document Intelligence meningkatkan pengenalan karakter optik (OCR)? Meskipun OCR dapat membaca dokumen cetak atau tulisan tangan, OCR mengekstrak teks dalam format yang tidak terstruktur sehingga sulit untuk disimpan dalam database atau dianalisis. Document Intelligence memahami data yang tidak terstruktur dengan menangkap struktur dari teks, seperti bidang data dan informasi dalam tabel. 

Dalam latihan ini, Anda akan menggunakan model bawaan Azure AI Document Intelligence di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk mengenali data dari tanda terima. 

## Membuat proyek di portal Azure AI Foundry

Mari kita mulai dengan membuat proyek Azure AI Foundry.

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup semua tips atau panel mulai cepat yang terbuka saat pertama kali Anda masuk, dan jika perlu, gunakan logo **Azure AI Foundry** di kiri atas untuk menavigasi ke beranda, yang tampilannya mirip dengan gambar berikut (tutup panel **Bantuan** jika terbuka):

    ![Tnagkapan layar beranda Azure AI Foundry dengan agen terpilih.](./media/azure-ai-foundry-home-page.png)

1. Di beranda, pilih **+ Buat agen**.

1. Di wizard **Buat agen**, masukkan nama yang valid untuk proyek Anda. 

1. Klik **Opsi Tingkat Lanjut** dan tentukan pengaturan berikut:
    - **Sumber daya Azure AI Foundry**: *Pertahankan nama default*
    - **Langganan**: *Langganan Azure Anda*
    - **Grup sumber daya**: *Buat atau pilih grup sumber daya*
    - **Wilayah**: Pilih salah satu wilayah berikut:
        * AS Timur
        * Prancis Tengah
        * Korea Tengah
        * Eropa Barat
        * US Barat

1. Pilih **Buat** dan tinjau konfigurasi Anda. Tunggu hingga proses penyiapan selesai.

    >**Catatan**: Jika Anda mendapat kesalahan izin, pilih tombol **Perbaiki** untuk menambahkan izin yang sesuai untuk melanjutkan.

1. Saat proyek Anda dibuat, Anda akan dibawa secara default ke playground Agen di portal Azure AI Foundry, yang akan terlihat mirip dengan gambar berikut:

    ![Tangkapan layar detail proyek Azure AI di portal Azure AI Foundry.](./media/ai-foundry-project-2.png)

1. Di jendela browser baru, buka [halaman eksplorasi Layanan Azure AI](https://ai.azure.com/explore/aiservices).

1. Pada halaman *Layanan AI*, pilih petak *Visi + Dokumen* untuk mencoba kemampuan Azure AI Vision dan Dokumen.

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
