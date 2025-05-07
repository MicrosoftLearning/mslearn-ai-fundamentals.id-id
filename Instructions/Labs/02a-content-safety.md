---
lab:
  title: Menjelajahi Keamanan Konten Azure AI Foundry
---

# Menjelajahi Keamanan Konten Azure AI Foundry

Layanan Azure AI membantu pengguna membuat aplikasi AI dengan API dan model yang siap pakai dan dapat disesuaikan sebelumnya. Dalam latihan ini Anda akan melihat salah satu layanan, Keamanan Konten Azure AI, yang memungkinkan Anda memoderasi konten teks dan gambar. Di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, Anda akan menggunakan Azure AI Content Safety untuk mengategorikan teks dan menetapkan skor tingkat keparahannya. 

> **Catatan** Tujuan dari latihan ini adalah untuk mendapatkan gambaran umum tentang bagaimana layanan Azure AI disediakan dan digunakan. Keamanan Konten digunakan sebagai contoh, tetapi Anda tidak diharapkan untuk mendapatkan pengetahuan komprehensif tentang keamanan konten dalam latihan ini!

## Membuat proyek di portal Azure AI Foundry

1. Di tab browser, navigasikan ke [portal Azure AI Foundry](https://ai.azure.com?azure-portal=true).

2. Masuk dengan akun Anda. 

3. Pada halaman beranda portal Azure AI Foundry, pilih **Buat proyek**. Di Azure AI Foundry, proyek adalah kontainer yang membantu mengatur pekerjaan Anda.  

    ![Cuplikan layar beranda Azure AI Foundry dengan membuat proyek yang dipilih.](./media/azure-ai-foundry-home-page.png)

4. Pada panel *Buat proyek* , Anda akan melihat nama proyek yang dihasilkan, yang bisa Anda simpan apa adanya. Bergantung pada apakah Anda telah membuat hub sebelumnya, Anda akan melihat daftar sumber daya Azure *baru* yang akan dibuat atau daftar menurun hub yang ada. Jika Anda melihat daftar menurun hub yang ada, pilih *Buat hub baru*, buat nama unik untuk hub Anda, dan pilih *Berikutnya*.  
 
    ![Cuplikan layar panel buat proyek dengan nama yang dihasilkan secara otomatis untuk hub dan proyek.](./media/azure-ai-foundry-create-project.png)

> **Penting**: Anda akan memerlukan sumber daya layanan Azure AI yang disediakan di lokasi tertentu untuk menyelesaikan lab lainnya.

5. Di panel *Buat proyek * yang sama, pilih** Sesuaikan** dan pilih salah satu **Lokasi** berikut: AS Timur, Prancis Tengah, Korea Tengah, Eropa Barat, atau AS Barat untuk menyelesaikan lab lainnya. Lalu pilih **buat**. 

1. Perhatikan sumber daya yang dibuat: 
- Layanan Azure AI
- Hub Azure AI
- Proyek Azure AI
- Akun penyimpanan
- Brankas kunci
- Grup sumber daya  

6. Setelah sumber daya dibuat, Anda akan dibawa ke halaman* Gambaran Umum* proyek Anda. 

7. Untuk menggunakan Keamanan Konten, Anda perlu membuat pembaruan izin ke sumber daya *hub Azure AI* Anda. Untuk melakukan ini, buka [portal Azure](https://portal.azure.com?portal-azure=true) dan masuk dengan langganan yang sama dengan yang Anda gunakan untuk membuat sumber daya AI Foundry Anda.  

8. Di portal Azure, gunakan bilah pencarian di bagian atas halaman untuk mencari dan memilih **Azure AI Foundry**. Di halaman sumber daya, pilih sumber daya yang baru saja Anda buat yang merupakan *jenis***hub Azure AI**.  

9. Di portal Azure, pada panel sebelah kiri, pilih **Kontrol Akses (IAM)**. Kemudian, pada panel yang terbuka, pilih **Tambahkan** di samping tanda tambah, dan pilih **Tambahkan penetapan peran**. 

![Cuplikan layar tempat untuk memilih tambahkan penetapan peran di panel Kontrol Akses.](./media/content-safety/access-control-step-one.png)

10. Cari **Azure AI Safety Evaluator** dalam daftar peran, lalu pilih itu. Kemudian pilih **Berikutnya**. 

11. Gunakan pengaturan berikut untuk menetapkan peran tersebut ke diri Anda: 
    - **Tetapkan akses ke**: pilih *pengguna, grup, atau prinsipal layanan*
    - **Anggota**: klik *pilih anggota*
        - Pada panel *Pilih anggota* yang terbuka, temukan nama Anda. Klik ikon plus di sebelah nama Anda. Lalu klik **Pilih**.
    - **Deskripsi**: *biarkan kosong*

12. Pilih **Tinjau dan Tetapkan**, lalu pilih **Tinjau dan Tetapkan** lagi untuk menambahkan penetapan peran.    

13. Di browser Anda, kembali ke [portal Azure AI Foundry](https://ai.azure.com?azure-portal=true). Pilih proyek Anda. 

14. Di menu sebelah kiri pada layar, pilih **Layanan AI**.
 
    ![Cuplikan layar menu sebelah kiri pada layar proyek dengan Layanan AI dipilih.](./media/azure-ai-foundry-ai-services.png)  

15. Pada halaman *Layanan AI*, pilih petak *Visi + Dokumen* untuk mencoba kemampuan Azure AI Vision dan Dokumen.
    
    ![Cuplikan layar petak Keamanan Konten.](./media/content-safety-tile.png)

## Mencoba moderasi teks dengan Keamanan Konten di portal Azure AI Foundry 

1. Pada halaman *Keamanan Konten*, di bawah *Filter konten teks*, pilih **Moderasi konten teks**.

2. Pada halaman *Moderasi konten teks*, di bawah judul *Cobalah*, pilih sumber daya layanan Azure AI yang baru saja Anda buat dari menu tarik-turun.   

3. Di bawah *Jalankan pengujian sederhana*, pilih petak **Konten Aman**. Perhatikan bahwa teks ditampilkan dalam kotak di bawah ini. 

4. Klik **Jalankan pengujian**. Menjalankan pengujian memanggil model pembelajaran mendalam Layanan Keamanan Konten. Model pembelajaran mendalam telah dilatih untuk mengenali konten yang tidak aman.

5. Di panel *Hasil*, periksa hasilnya. Ada empat tingkat keparahan dari aman ke tinggi, dan empat jenis konten berbahaya. Apakah layanan AI Keamanan Konten menganggap sampel ini dapat diterima atau tidak? Yang penting untuk dicatat adalah bahwa hasilnya berada dalam interval keyakinan. Model yang terlatih dengan baik, seperti salah satu model siap pakai Azure AI, dapat mengembalikan hasil yang memiliki probabilitas tinggi kecocokan dengan apa yang akan diberi label oleh manusia. Setiap kali Anda menjalankan pengujian, Anda memanggil model lagi. 

6. Sekarang coba sampel lain. Pilih teks di bawah Konten kekerasan dengan salah eja. Periksa apakah konten ditampilkan dalam kotak di bawah ini.

7. Klik **Jalankan pengujian** dan periksa hasilnya di panel Hasil lagi. 

Anda dapat menjalankan pengujian pada semua sampel yang disediakan, lalu memeriksa hasilnya.

## Pembersihan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Latihan ini hanya menunjukkan beberapa kemampuan layanan Keamanan Konten. Untuk mempelajari lebih lanjut tindakan yang dapat Anda lakukan dengan layanan ini, lihat [halaman Keamanan Konten](https://learn.microsoft.com/azure/ai-services/content-safety/overview).