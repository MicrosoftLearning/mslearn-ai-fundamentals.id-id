---
lab:
  title: Jelajahi Layanan Azure AI
---

# Jelajahi Layanan Azure AI

Layanan Azure AI membantu pengguna membuat aplikasi AI dengan API dan model yang siap pakai dan dapat disesuaikan sebelumnya. Dalam latihan ini Anda akan melihat salah satu layanan, Keamanan Konten Azure AI, di Studio Keamanan Konten.

Studio Keamanan Konten memungkinkan Anda menjelajahi bagaimana konten teks dan gambar dapat dimoderasi. Anda dapat menjalankan pengujian pada sampel teks atau gambar dan mendapatkan skor tingkat keparahan mulai dari yang aman hingga tinggi untuk setiap kategori. Dalam latihan lab ini Anda akan membuat sumber daya layanan tunggal di Studio Keamanan Konten dan menguji fungsionalitasnya. 

> **Catatan** Tujuan dari latihan ini adalah untuk mendapatkan gambaran umum tentang bagaimana layanan Azure AI disediakan dan digunakan. Keamanan Konten digunakan sebagai contoh, tetapi Anda tidak diharapkan untuk mendapatkan pengetahuan komprehensif tentang keamanan konten dalam latihan ini!

## Menavigasi Studio Keamanan Konten 

![Cuplikan layar halaman arahan studio keamanan konten.](./media/content-safety/content-safety-getting-started.png)

1. Buka [Studio Keamanan Konten](https://contentsafety.cognitive.azure.com?azure-portal=true). Jika Anda tidak masuk, Anda harus masuk. Pilih **Masuk** di kanan atas layar. Gunakan email dan kata sandi yang terkait dengan langganan Azure Anda untuk masuk. 

1. Studio Keamanan Konten disiapkan seperti banyak studio lain untuk layanan Azure AI. Pada menu di bagian atas layar, klik ikon di sebelah kiri *Azure AI*. Anda akan melihat daftar drop-down studio lain yang dirancang untuk pengembangan dengan layanan Azure AI. Anda dapat mengeklik ikon lagi untuk menyembunyikan daftar.

![Cuplikan layar menu Studio Keamanan Konten dengan pilihan pengalih terbuka untuk beralih ke studio lain.](./media/content-safety/studio-toggle-icon.png)  

## Mengaitkan sumber daya dengan studio 

Sebelum menggunakan studio, Anda perlu mengaitkan sumber daya layanan Azure AI dengan studio. Bergantung pada studio, Anda mungkin menemukan bahwa Anda memerlukan sumber daya layanan tunggal tertentu, atau dapat menggunakan sumber daya multi-layanan umum. Dalam kasus Studio Keamanan Konten, Anda dapat menggunakan layanan dengan membuat sumber daya *Keamanan Konten* layanan tunggal atau *layanan Azure AI* sumber daya multi-layanan umum. Dalam langkah-langkah di bawah ini, kami akan membuat sumber daya Keamanan Konten layanan tunggal. 

1. Di kanan atas layar, klik ikon **Pengaturan**. 

![Cuplikan layar ikon pengaturan di kanan atas layar, di samping bel, tanda tanya, dan ikon senyum.](./media/content-safety/settings-toggle.png)

2. Pada halaman **Pengaturan**, Anda akan melihat tab *Direktori* dan tab *Sumber Daya*. Pada tab *Sumber Daya* , pilih **Buat sumber daya baru**. Ini akan membawa Anda ke halaman untuk membuat sumber daya di Portal Microsoft Azure.

> **Catatan** Tab *Direktori* memungkinkan pengguna memilih direktori yang berbeda untuk membuat sumber daya. Anda tidak perlu mengubah pengaturannya kecuali Anda ingin menggunakan direktori yang berbeda. 

![Cuplikan layar tempat memilih buat sumber daya baru dari halaman pengaturan Studio Keamanan Konten.](./media/content-safety/create-new-resource-from-studio.png)

3. Pada halaman *Buat Keamanan Konten* di [Portal Azure](https://portal.azure.com?azure-portal=true), Anda perlu mengonfigurasi beberapa detail untuk membuat sumber daya Anda. Konfigurasikan dengan pengaturan berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Wilayah**: *Pilih wilayah yang tersedia. Jika di AS timur, gunakan "US Timur 2"*.
    - **Nama**: *Masukkan nama unik*.
    - **Tingkat harga**: Gratis F0

4. Pilih **Tinjau + Buat** dan tinjau konfigurasi. Lalu pilih **Buat**. Layar akan menunjukkan kapan penyebaran selesai. 

*Selamat! Anda baru saja membuat, atau menyediakan sumber daya layanan Azure AI. Yang Anda sediakan khususnya adalah sumber daya layanan Content Safety satu layanan.*

5. Setelah penyebaran selesai, buka tab baru dan kembali ke [Studio Keamanan Konten](https://contentsafety.cognitive.azure.com?azure-portal=true). 

6. Pilih ikon **Pengaturan** di kanan atas layar lagi. Kali ini Anda akan melihat bahwa sumber daya yang baru dibuat telah ditambahkan ke daftar.  

>**Catatan**: Jika menggunakan langganan Cloud Slice, Anda dapat melompati langkah #7-12 dan menuju ke langkah #13. Jika tidak, lanjutkan ke langkah #7.

7. Pilih **Tampilkan semua properti di portal Azure** di bagian bawah layar *Pengaturan*. 

![Cuplikan layar tautan tampilkan semua properti di portal Azure.](./media/content-safety/view-all-properties.png)

8. Di portal Azure, pilih sumber daya *Keamanan Konten* yang baru saja Anda buat. Kemudian, pada panel sebelah kiri, pilih **Kontrol Akses (IAM)**. Kemudian, pada panel yang terbuka, pilih **Tambahkan** di samping tanda tambah, dan pilih **Tambahkan penetapan peran**. 

![Cuplikan layar tempat untuk memilih tambahkan penetapan peran di panel Kontrol Akses.](./media/content-safety/access-control-step-one.png)

9. Cari **Pengguna Cognitive Services** dalam daftar peran, dan pilih pengguna tersebut. Kemudian pilih **Berikutnya**. 

10. Gunakan pengaturan berikut untuk menetapkan peran tersebut ke diri Anda: 
    - **Tetapkan akses ke**: pilih *pengguna, grup, atau prinsipal layanan*
    - **Anggota**: klik *pilih anggota*
        - Pada panel *Pilih anggota* yang terbuka, temukan nama Anda. Klik ikon plus di sebelah nama Anda. Lalu klik **Pilih**.
    - **Deskripsi**: *biarkan kosong*

11. Pilih **Tinjau dan Tetapkan**, lalu pilih **Tinjau dan Tetapkan** lagi untuk menambahkan penetapan peran.    

12. Kembali ke Content Safety Studio pada [https://contentsafety.cognitive.azure.com](https://contentsafety.cognitive.azure.com). Kemudian, pilih ikon **Pengaturan** di bagian kanan atas layar. 

![Cuplikan layar ikon pengaturan di kanan atas layar, di samping bel, tanda tanya, dan ikon senyum.](./media/content-safety/settings-toggle.png)
 
13. Pilih sumber daya layanan Azure AI yang baru saja Anda buat. Pastikan pada *Penetapan peran saat ini* Anda melihat *Pengguna Cognitive Services*, dan *Pemilik*.

![Cuplikan layar penetapan peran saat ini.](./media/content-safety/access-control-check-step.png)

14. Klik **Gunakan sumber daya** di bagian bawah layar. Anda akan dibawa kembali ke halaman beranda studio. Sekarang Anda dapat mulai menggunakan studio dengan sumber daya yang baru dibuat.

## Mencoba moderasi teks di Studio Keamanan Konten

1. Pada beranda Studio Keamanan Konten, di bawah *Jalankan pengujian moderasi*, navigasikan ke kotak **Moderasikan** konten teks dan klik **Cobalah**.
1. Di bawah jalankan pengujian sederhana, klik **Konten Aman**. Perhatikan bahwa teks ditampilkan dalam kotak di bawah ini. 
1. Klik **Jalankan pengujian**. Menjalankan pengujian memanggil model pembelajaran mendalam Layanan Keamanan Konten. Model pembelajaran mendalam telah dilatih untuk mengenali konten yang tidak aman.
1. Di panel *Hasil*, periksa hasilnya. Ada empat tingkat keparahan dari aman ke tinggi, dan empat jenis konten berbahaya. Apakah layanan AI Keamanan Konten menganggap sampel ini dapat diterima atau tidak? Yang penting untuk dicatat adalah bahwa hasilnya berada dalam interval keyakinan. Model yang terlatih dengan baik, seperti salah satu model siap pakai Azure AI, dapat mengembalikan hasil yang memiliki probabilitas tinggi kecocokan dengan apa yang akan diberi label oleh manusia. Setiap kali Anda menjalankan pengujian, Anda memanggil model lagi. 
1. Sekarang coba sampel lain. Pilih teks di bawah Konten kekerasan dengan salah eja. Periksa apakah konten ditampilkan dalam kotak di bawah ini.
1. Klik **Jalankan pengujian** dan periksa hasilnya di panel Hasil lagi. 

Anda dapat menjalankan pengujian pada semua sampel yang disediakan, lalu memeriksa hasilnya.

## Lihat kunci dan titik akhir

Kemampuan yang Anda uji ini dapat diprogram ke dalam semua jenis aplikasi. Kunci dan titik akhir yang digunakan untuk pengembangan aplikasi dapat ditemukan baik di Studio Keamanan Konten maupun Portal Microsoft Azure. 

1. Di Studio Keamanan Konten, navigasi kembali ke halaman **Pengaturan**, dengan memilih tab *Sumber Daya*. Cari sumber daya yang Anda gunakan. Gulir ke samping untuk melihat titik akhir dan kunci untuk sumber daya Anda. 
1. Di Portal Microsoft Azure, Anda akan melihat bahwa ini adalah titik akhir yang *sama* dan kunci yang *berbeda* untuk sumber daya Anda. Untuk memeriksanya, buka [portal Azure](https://portal.azure.com?auzre-portal=true). Cari *Konten Aman* di bilah pencarian teratas. Temukan sumber daya Anda dan klik sumber daya tersebut. Di menu sebelah kiri, lihat di bawah * Resource Management* untuk *Kunci dan Titik Akhir*. Pilih **Kunci dan Titik Akhir** untuk melihat titik akhir dan kunci untuk sumber daya Anda. 

Setelah selesai, Anda dapat menghapus sumber daya Keamanan Konten dari Portal Microsoft Azure. Menghapus sumber daya adalah cara untuk mengurangi biaya yang bertambah ketika sumber daya ada dalam langganan. Untuk melakukan ini, navigasikan ke halaman **Gambaran umum** sumber daya Keamanan Konten Anda. Pilih **Hapus** di bagian atas layar.

