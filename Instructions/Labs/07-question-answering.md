---
lab:
  title: Menggunakan Jawaban atas Pertanyaan dengan Language Studio
---

# Menggunakan Jawaban atas Pertanyaan dengan Studio Bahasa

Dalam latihan ini Anda akan menggunakan Studio Bahasa untuk membuat dan melatih basis pengetahuan tentang pertanyaan dan jawaban  Konten untuk pangkalan pengetahuan akan berasal dari halaman FAQ yang ada dari situs web Margie's Travel, agen perjalanan fiktif. Anda kemudian akan menggunakan Language Studio untuk melihat cara kerjanya saat digunakan oleh pelanggan.

Azure AI Bahasa mencakup kemampuan *jawaban atas pertanyaan*, yang akan Anda gunakan untuk membuat pangkalan pengetahuan. Pangkalan pengetahuan dapat dibuat baik dengan memasukkan pasangan pertanyaan dan jawaban secara manual, atau dari dokumen atau halaman web yang ada. Margie's Travel ingin menggunakan dokumen FAQ yang ada.

Fitur jawaban atas pertanyaan layanan Bahasa memungkinkan Anda membuat pangkalan pengetahuan dengan cepat, baik dengan memasukkan pasangan pertanyaan dan jawaban atau dari dokumen atau halaman web yang ada. Layanan ini kemudian dapat menggunakan beberapa kemampuan pemrosesan bahasa alami bawaan untuk menafsirkan pertanyaan dan menemukan jawaban yang tepat.

## Membuat sumber daya *Bahasa*

Untuk menggunakan jawaban atas pertanyaan, Anda memerlukan sumber daya **Bahasa**.

1. Di tab browser yang lain, buka portal Azure di [https://portal.azure.com](https://portal.azure.com?azure-portal=true), lalu masuk dengan akun Microsoft yang terkait dengan langganan Azure Anda.

1. Klik **&#65291;Buat tombol sumber daya** dan cari *Layanan Bahasa*. Pilih **buat** paket **Layanan Bahasa**. Anda akan dibawa ke suatu halaman untuk **Memilih fitur tambahan**. Gunakan pengaturan berikut:
    - **Pilih Fitur Tambahan**:
        - **Fitur bawaan**: *Pertahankan fitur bawaan*.
        - **Fitur kustom**: *Pilih jawaban atas pertanyaan kustom*.
     - Pilih **Lanjutkan untuk membuat sumber daya Anda**
    ![ Membuat sumber daya Layanan Bahasa dengan jawaban atas pertanyaan kustom diaktifkan.](media/create-a-bot/create-language-service-resource.png)

1. Pada halaman **Buat Bahasa**, tentukan pengaturan berikut:
    - **Detail Proyek**
        - **Langganan**: *Langganan Azure Anda*.
        - **Grup sumber daya**: *Pilih grup sumber daya yang ada atau buat yang baru*.
    - **Detail Instans**
        - **Wilayah**: *Pilih wilayah. Jika di AS timur, gunakan "US Timur 2"*      
        - **Nama**: *Nama unik untuk sumber daya Bahasa Anda*.
        - **Tingkat harga**: S (1K Panggilan per menit)
    - **Jawaban atas pertanyaan kustom**
        - **Wilayah pencarian Azure**: *Lokasi apa pun yang tersedia*.
        - **Tingkat harga pencarian Azure**: F Gratis (3 Indeks) - (*Jika tingkat ini tidak tersedia, pilih Dasar*)
    - **Pemberitahuan AI yang Bertanggung Jawab**
        - **Dengan mencentang kotak ini, saya menyatakan bahwa saya telah meninjau dan menyetujui persyaratan dalam Pemberitahuan AI yang Bertanggung Jawab**: *Dipilih*.

1. Pilih **Tinjau dan Buat** lalu pilih **Buat**. Tunggu penyebaran layanan Bahasa yang akan mendukung pangkalan pengetahuan jawaban atas pertanyaan kustom Anda.

    > **Catatan** Jika Anda telah menyediakan sumber daya **Azure Cognitive Search** tingkat gratis, kuota Anda mungkin tidak memungkinkan Anda untuk membuat sumber daya lain. Dalam hal ini, pilih tingkat selain **F Gratis**.

## Membuat proyek baru

1. Di tab browser baru, buka portal Language Studio di [https://language.azure.com](https://language.azure.com?azure-portal=true) dan masuk menggunakan akun Microsoft yang terkait dengan langganan Azure Anda.
1. Jika diminta untuk memilih sumber daya Bahasa, pilih pengaturan berikut:
    - **Azure directory**: *Azure directory yang berisi langganan Anda*.
    - **Langganan Azure**: *Langganan Azure Anda*.
    - **Sumber daya bahasa**: *Sumber daya Bahasa yang Anda buat sebelumnya.*

    Jika Anda ***tidak*** diminta untuk memilih sumber daya bahasa, hal tersebut mungkin karena Anda memiliki beberapa sumber daya Bahasa dalam langganan Anda; dalam hal ini:
    1. Pada bilah di bagian atas halaman, pilih **Pengaturan (&#9881;)**.      
    1. Pada halaman **Pengaturan**, lihat tab **Sumber Daya**.
    1. Pilih sumber daya bahasa yang baru saja Anda buat, dan pilih **Beralih sumber daya**.
    1. Di bagian atas halaman, pilih **Language Studio** untuk kembali ke beranda Language Studio.

1. Di bagian atas portal Language Studio, di menu **Buat baru**, pilih **Jawaban atas pertanyaan kustom**.

    ![Jawaban atas pertanyaan kustom](media/create-a-bot/create-custom-question-answering.png)

1. Pada halaman **Pilih pengaturan bahasa untuk sumber daya *sumber daya Anda***, pilih **Saya ingin memilih bahasa saat membuat proyek di sumber daya ini** dan klik **Berikutnya**.
  ![Saya ingin memilih bahasa](media/create-a-bot/create-project.png)

1. Pada halaman **Masukkan informasi dasar**, masukkan detail berikut dan klik **Berikutnya**:
    - **Sumber daya bahasa**: *pilih sumber daya bahasa Anda*.  
    - **Sumber daya penelusuran Azure**: *pilih sumber daya penelusuran Azure Anda*.
    - **Nama**: `MargiesTravel`
    - **Deskripsi**: `A simple knowledge base`
    - **Bahasa sumber**: Ba Inggris
    - **Jawaban default ketika tidak ada jawaban yang diberikan**: `No answer found`
1. Pada halaman **Tinjau dan selesai**, pilih **Buat proyek**.
1. Anda akan dibawa ke halaman **Kelola sumber**. Pilih **&#65291;Tambahkan sumber** dan pilih **URL**.
1. Dalam kotak **Tambahkan URL**, pilih **+ Tambahkan URL**. Ketik seperti berikut dan pilih **Tambahkan semua**:
    - **Nama URL**: `MargiesKB`
    - **URL**: `https://raw.githubusercontent.com/MicrosoftLearning/mslearn-ai-fundamentals/main/data/natural-language/margies_faq.docx`
    - **Klasifikasikan struktur file**: *Deteksi otomatis*
1. Pilih **Tambahkan semua.**  

 ![Tambahkan URL](media/create-a-bot/add-url.png)

## Mengedit Pangkalan Pengetahuan

Pangkalan Pengetahuan Anda didasarkan pada detail dalam dokumen FAQ dan beberapa tanggapan yang ditentukan sebelumnya. Anda dapat menambahkan pasangan tanya jawab kustom untuk melengkapinya.

1. Perluas panel kiri dan pilih **Edit pangkalan pengetahuan**. Lalu pilih **+** untuk menambahkan pasangan pertanyaan baru.
1. Dalam kotak dialog **Tambahkan pasangan jawaban pertanyaan baru**, di jenis**Pertanyaan** `Hello`, dan di jenis**Jawaban** `Hi`, lalu pilih **Selesai**.
1. Perluas **Pertanyaan alternatif** dan pilih **+ Tambahkan pertanyaan alternatif**. Kemudian masukkan `Hiya`sebagai frasa alternatif untuk "Halo".
1. Di bagian atas panel **Pasangan jawaban pertanyaan**, pilih **Simpan** untuk menyimpan pangkalan pengetahuan Anda.

## Melatih dan menguji pangkalan pengetahuan

Sekarang setelah Anda memiliki pangkalan pengetahuan, Anda dapat mengujinya.

1. Di bagian atas panel **Pasangan jawaban pertanyaan**, pilih **Uji** untuk menguji pangkalan pengetahuan Anda.
1. Di panel uji, di bagian bawah masukkan pesan `Hi`. Respons *Hai* harus diberikan.
1. Di panel uji, di bagian bawah masukkan pesan `I want to book a flight`. Respons yang tepat dari FAQ akan muncul.

    > **Catatan** Respons mencakup *jawaban singkat* serta *bagian jawaban* yang lebih bertele-tele - bagian jawaban menampilkan teks lengkap dalam dokumen FAQ untuk pertanyaan yang paling cocok, sedangkan jawaban singkatnya diambil secara cerdas dari bagian tersebut. Anda dapat mengontrol apakah jawaban singkat berasal dari respons dengan menggunakan kotak centang **Tampilkan jawaban singkat** di bagian atas panel uji.

1. Coba pertanyaan lain, seperti `How can I cancel a reservation?`
1. Setelah selesai menguji pangkalan pengetahuan, pilih **Uji** untuk menutup panel pengujian.

## Menyebarkan proyek Anda

Anda dapat menyebarkan basis pengetahuan sebagai aplikasi klien untuk menjawab pertanyaan.

1. Di panel kiri, pilih **Sebarkan pangkalan pengetahuan**.
1. Di bagian atas halaman, pilih **Sebarkan**. Kotak dialog akan menanyakan apakah Anda ingin menyebarkan proyek. Pilih **Sebarkan.**

 ![Menyebarkan pangkalan pengetahuan.](media/create-a-bot/deploy-knowledge-base.png)

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat. 
1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

- Untuk mempelajari selengkapnya tentang layanan Jawaban Atas Pertanyaan, lihat [dokumentasi](https://docs.microsoft.com/azure/cognitive-services/language-service/question-answering/overview).
