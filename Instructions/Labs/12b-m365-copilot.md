---
lab:
  title: Jelajahi Copilot untuk Microsoft 365
---
# Jelajahi Copilot untuk Microsoft 365

Dalam latihan ini, Anda akan menjelajahi beberapa cara Microsoft Copilot dapat menggunakan AI generatif untuk membantu Anda menjadi lebih produktif saat membuat konten baru. Dalam skenario untuk latihan ini, Anda akan memulai dengan catatan tingkat tinggi untuk ide bisnis, dan menggunakan Copilot untuk Microsoft 365 di beberapa aplikasi seperti Word, PowerPoint, dan Excel untuk membantu Anda mengembangkan rencana bisnis dan presentasi untuk calon investor.

Latihan ini akan memakan waktu sekitar **40** menit untuk menyelesaikannya.

> **Catatan**: Latihan ini memerlukan lisensi **Copilot untuk Microsoft 365** dari organisasi Anda.

## Menggunakan Copilot untuk menjelajahi dokumen dan mencari ide

Untuk memulai eksplorasi AI generatif Anda, mari kita gunakan Copilot untuk Word untuk memeriksa dokumen yang ada dan mengekstrak wawasan dari dokumen itu.

1. Di browser web Anda, buka dokumen [Business Idea.docx](https://github.com/MicrosoftLearning/mslearn-ai-fundamentals/raw/main/data/generative-ai/Business%20Idea.docx) di `https://github.com/MicrosoftLearning/mslearn-ai-fundamentals/raw/main/data/generative-ai/Business%20Idea.docx`. 
1. Pilih **Unduh** untuk menyimpan file ke folder **Unduhan** PC Anda.
1. **Pindahkan** atau **Salin & Tempel** dokumen yang baru saja Anda unduh ke folder **OneDrive**.
1. Dari folder **OneDrive**, buka **Business Idea.docx** di Microsoft Word (tutup pesan selamat datang atau pemberitahuan fitur baru) dan tinjau dokumen, yang menjelaskan beberapa ide tingkat tinggi untuk bisnis kebersihan di Kota New York. Jika diminta, pilih **Aktifkan pengeditan** di bagian atas.
1. Temukan dan pilih ikon **Copilot** di toolbar Word untuk membuka panel Copilot, seperti yang diperlihatkan di sini (tema visual Anda mungkin berbeda):

    ![Cuplikan layar panel Copilot di Microsoft Word.](./media/generative-ai/copilot-word-pane.png)

1. Di panel Copilot, masukkan perintah berikut di area teks di bagian bawah:

    ```
    What is this document about?
    ```

1. Tinjau respons dari Copilot, yang akan merangkum poin-poin utama dalam dokumen, seperti yang ditunjukkan di sini:

    ![Cuplikan layar panel Copilot di Word dengan respons.](./media/generative-ai/copilot-response-word.png)

    > Respons spesifik yang Anda terima mungkin bervariasi karena sifat AI generatif.

1. Kembali ke panel Copilot untuk mengajukan pertanyaan berikut kepada Copilot:

    ```
    How do I setup a new business in New York?
    ```

1. Tinjau respons dan tindak lanjuti dengan pertanyaan tambahan sesuai kebutuhan. Saat Anda puas dengan respons, gunakan ikon **Salin** (&#128461;) di bawah respons untuk menyalinnya ke clipboard. Tempelkan ke dokumen Word, pilih semua teks lalu pilih ikon Copilot untuk memvisualisasikan teks sebagai tabel.

    ![Cuplikan layar meminta Copilot untuk memvisualisasikan dalam format tabel.](./media/generative-ai/copilot-rewrite-as-table.png)

1. Tinjau tabel dan minta Copilot untuk menambahkan lebih banyak informasi, seperti referensi untuk detail lebih lanjut.  Respons Anda akan terlihat seperti ini (Anda mungkin perlu menggunakan tombol **Regenerasi**):

    ![Cuplikan layar respons dari Copilot dalam format tabel.](./media/generative-ai/copilot-rewrite-as-table-response.png)

    > **Penting**: Respons yang dihasilkan AI didasarkan pada informasi yang tersedia secara publik di Web. Meskipun mungkin berguna untuk membantu Anda memahami langkah-langkah yang diperlukan untuk mendirikan bisnis, respons tersebut tidak dijamin 100% akurat dan tidak menggantikan kebutuhan akan saran profesional!

1. Saat Anda puas dengan tabel yang dihasilkan Copilot, pilih opsi **Simpan**.

## Menggunakan Copilot untuk membuat konten untuk rencana bisnis

Nah, setelah Anda melakukan pencarian awal, mari kita minta Copilot membantu Anda mengembangkan rencana bisnis untuk perusahaan kebersihan Anda.

1. Dengan dokumen **Business Idea.docx** masih terbuka, di panel Copilot, masukkan perintah berikut:

    ```
    Can you suggest a name for my cleaning business?
    ```

1. Tinjau saran dan pilih nama untuk perusahaan kebersihan Anda (atau lanjutkan memberikan perintah untuk menemukan nama yang Anda sukai).
1. Di dokumen Word, pilih ikon Copilot di margin untuk menyusun konten baru. Masukkan perintah berikut, ganti **Contoso Cleaning** dengan nama perusahaan pilihan Anda:

    ```
    Write a business plan for "Contoso Cleaning" based on the information in this document. Include an executive summary, market overview, and financial projections.
    ```

    ![Cuplikan layar Copilot menyusun rencana bisnis.](./media/generative-ai/copilot-draft-business-plan-prompt.png)

1. Tinjau tanggapan yang disusun oleh Copilot dan simpan, sesuaikan nada dan panjangnya, atau minta Copilot untuk menulis ulang dengan perintah baru. Terapkan judul dan gaya yang sesuai pada dokumen Anda agar terlihat profesional. Respons Anda akan terlihat seperti ini:

    ![Cuplikan layar dokumen Word dengan rencana bisnis yang dihasilkan Copilot.](./media/generative-ai/copilot-draft-business-plan-response.png)

1. Jika proyeksi keuangan dalam rencana bisnis tidak diformat sebagai tabel, pilih proyeksi dan gunakan Copilot untuk memvisualisasikan proyeksi itu sebagai tabel.
1. Pilih tabel proyeksi keuangan dan salin ke clipboard.
1. Simpan dokumen Word.

## Memvisualisasikan proyeksi keuangan di Copilot untuk Excel

Setelah memiliki rencana bisnis, mari kita ambil beberapa data tentang proyeksi keuangan dan minta Copilot di Excel untuk memvisualisasikan data tersebut untuk kita sehingga kita dapat menyertakannya dalam email atau presentasi kepada investor.

1. Di PC Anda, dengan aplikasi Microsoft 365 terinstal, buka **Excel** dan buat buku kerja kosong baru. Segera simpan buku kerja sebagai **Financial Projetions.xlsx** ke OneDrive, atau Copilot tidak akan berfungsi.
1. Tempelkan tabel proyeksi penjualan dari **Business Idea.docx** ke dalam spreadsheet Excel dan **format sebagai tabel**. Untuk melakukan ini:
    1. Pilih **sel** dalam data.
    1. Pilih **Beranda** dan pilih **Format sebagai Tabel** di bawah Gaya. 
    1. Pilih gaya untuk tabel.
    1. Di kotak dialog **Buat Tabel**, konfirmasi atau atur rentang sel Anda.
    1. Tandai jika tabel Anda memiliki header, dan pilih **OK**.
1. Dengan proyeksi penjualan yang diformat sebagai tabel, buka panel Copilot dari pita Excel dan masukkan perintah berikut:

    ```
    Suggest ways to visualize these financial projections.
    ```
    
1. Copilot akan menyarankan 1 atau 2 cara untuk memvisualisasikan data dan menawarkan untuk menambahkan bagan pivot ke lembar baru.

    ![Cuplikan layar Copilot di Excel memvisualisasikan proyeksi keuangan.](./media/generative-ai/copilot-excel-visualize-projections.png)

1. Namun, Anda mungkin ingin melihat lebih banyak data dalam bagan untuk menunjukkan perubahan tahun ke tahun, jadi masukkan perintah berikut untuk menambahkannya:

    ```
    Visualize these financial projections in a line chart to show year-over-year revenue and profits.
    ```

    ![Cuplikan layar Copilot di Excel memvisualisasikan proyeksi keuangan.](./media/generative-ai/copilot-excel-visualize-more.png)

1. Tambahkan bagan pivot ke lembar baru dan buka. Pilih bagan, lalu pilih **Desain** untuk menerapkan gaya, mengubah tipe bagan, dan tindakan lainnya. Di akhir, Anda harus mendapatkan hasil yang mirip dengan ini:

    ![Cuplikan layar Copilot di Excel menambahkan PivotChart.](./media/generative-ai/copilot-excel-chart-design.png)

1. Simpan file ke OneDrive dan tutup Excel.

Anda baru saja menggunakan data yang dibuat dari Copilot di Word untuk divisualisasikan di Excel. Dalam latihan berikutnya, Anda akan melanjutkan menggunakan Copilot di Outlook untuk menulis dan mengirim email tentang pekerjaan yang telah Anda lakukan.

## Menggunakan Copilot untuk menulis email

Anda telah membuat beberapa materi pemasaran untuk membantu Anda memulai bisnis Anda. Sekarang saatnya untuk menjangkau investor untuk mencari pendanaan perusahaan rintisan.

1. Di PC Anda dengan aplikasi Microsoft 365 terinstal, buka **Outlook**. Jika Anda belum menyiapkan Outlook dengan akun Microsoft 365 Anda, lihat [Menyiapkan dan menggunakan Outlook - Dukungan Microsoft](https://support.microsoft.com/office/set-up-and-use-outlook-4636f361-d5e3-4a87-9cd4-382858de55fa).
1. Aktifkan pengalaman **Outlook baru**. Untuk mendapatkan fitur Copilot terbaru di Outlook, Anda harus menggunakan pengalaman "Outlook Baru". Untuk melihat versi yang Anda gunakan, lihat [Versi Outlook apa yang saya miliki? - Dukungan Microsoft](https://support.microsoft.com/office/what-version-of-outlook-do-i-have-b3a9568c-edb5-42b9-9825-d48d82b2257c).
1. Buat email baru, dan isi kotak **Kepada** dengan alamat email Anda sendiri.
1. Anda dapat mulai menyusun email dari panel Copilot atau langsung dari dalam isi email:

    ![Cuplikan layar Outlook dan opsi untuk menyusun email dengan Copilot.](./media/generative-ai/copilot-draft-email-outlook.png)
    
1. Masukkan perintah berikut dan sesuaikan nadanya menjadi "Formal" serta panjangnya menjadi "Sedang":

    ```
    Request a meeting with an investment bank to discuss funding for a commercial cleaning business.
    ```

    ![Cuplikan layar menyusun email dengan Copilot di Outlook.](./media/generative-ai/copilot-draft-email-adjust-tone-outlook.png)

1. Pilih **Buat draf**, dan tinjau output yang dihasilkan. Sesuaikan nada atau beri tahu Copilot apa yang ingin Anda ubah tentang email tersebut.

    ![Cuplikan layar email yang dihasilkan dengan Copilot di Outlook.](./media/generative-ai/copilot-draft-email-results-outlook.png)

1. Anda dapat mengirim email ke diri Anda sendiri jika Anda mau!

## Menggunakan Copilot untuk membuat konten presentasi

Dengan bantuan Copilot, Anda telah membuat draf rencana bisnis untuk ide bisnis kebersihan, menyiapkan proyeksi keuangan, dan mengirim email untuk meminta pertemuan dengan calon investor. Sekarang Anda memerlukan presentasi yang efektif untuk menyampaikan manfaat bisnis Anda.

1. Buka **PowerPoint** dan buat **presentasi kosong** baru. Tutup panel **Desainer** jika terbuka secara otomatis.

    ![Cuplikan layar pembuatan presentasi kosong baru di PowerPoint.](./media/generative-ai/powerpoint-create-blank-presentation.png)

1. Simpan presentasi sebagai **Cleaning Company.pptx** di folder OneDrive Anda.
1. Pilih **tombol Copilot** di **tab Beranda** pada pita, pilih **Buat presentasi tentang...**, kemudian lengkapi perintah di panel Copilot sebagai berikut:

    ```
    Create a presentation about a corporate cleaning service in New York City.
    ```

1. Copilot akan membuat slide dalam presentasi.  Proses ini mungkin memakan waktu beberapa menit dan output Anda akan terlihat menyerupai ini dengan tema yang berbeda:

    ![Cuplikan layar presentasi PowerPoint yang dibuat oleh Copilot dari dokumen Word.](./media/generative-ai/copilot-powerpoint-create-image.png)

1. Pilih slide kedua terakhir dalam presentasi. Kemudian, di panel Copilot, mintalah untuk menambahkan slide baru menggunakan perintah ini:

    ```
    Add a slide that describes the benefits of an eco-friendly approach to cleaning. 
    ```

    ![Cuplikan layar presentasi PowerPoint membuat slide baru.](./media/generative-ai/copilot-powerpoint-add-new-slide.png)

1. Simpan presentasi.

## Latihan

Nah, Anda telah mempelajari cara menggunakan Copilot untuk Microsoft 365 dalam beberapa aplikasi berbeda untuk mencari ide dan menghasilkan konten, mengapa tidak mencoba menjelajahi lebih lanjut? Coba gunakan Copilot untuk merencanakan acara untuk meningkatkan literasi anak-anak di perpustakaan lokal. Beberapa hal yang dapat Anda coba meliputi:

- Cari beberapa tip untuk mendorong anak membaca pada usia dini.
- Buat selebaran atau poster untuk acara tersebut.
- Buat email kampanye untuk mengundang penulis anak-anak setempat untuk datang dan berbicara di acara tersebut.
- Buat presentasi untuk memulai acara.

Usahakan sekreatif mungkin, dan jelajahi cara Copilot dapat membantu Anda dengan menemukan informasi, menghasilkan dan menyempurnakan teks, membuat gambar, dan menjawab pertanyaan.

## Kesimpulan

Dalam latihan ini, Anda telah menggunakan [Copilot untuk Microsoft 365](https://www.microsoft.com/microsoft-365/enterprise/copilot-for-microsoft-365) untuk menemukan informasi dan menghasilkan konten. Semoga Anda telah melihat bagaimana menggunakan AI generatif dalam Copilot dapat membantu produktivitas dan kreativitas. Microsoft 365 memungkinkan Anda menghadirkan kekuatan AI generatif ke data dan proses bisnis Anda, sementara tetap terintegrasi ke dalam infrastruktur TI yang sudah ada untuk memastikan solusi dapat dikelola dan aman.
