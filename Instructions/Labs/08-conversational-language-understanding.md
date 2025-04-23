---
lab:
  title: Menggunakan Pemahaman Bahasa Percakapan dengan Language Studio
---

# Menggunakan Pemahaman Bahasa Percakapan dengan Language Studio

Lambat laun, kami mengharapkan komputer dapat menggunakan AI untuk memahami perintah bahasa alami, baik yang diucapkan atau diketik. Misalnya, Anda mungkin ingin sistem otomatisasi rumah mengontrol perangkat di rumah Anda dengan menggunakan perintah suara seperti "nyalakan lampu" atau "nyalakan kipas." Perangkat yang didukung AI dapat memahami perintah ini dan mengambil tindakan yang sesuai.

Dalam latihan ini, Anda akan menggunakan Language Studio untuk membuat dan menguji proyek yang mengirim instruksi ke perangkat seperti lampu atau kipas. Anda akan menggunakan kemampuan layanan Pemahaman Bahasa Percakapan untuk mengonfigurasi proyek Anda. 

## Membuat sumber daya *Bahasa*

Anda dapat menggunakan banyak fitur Azure AI Bahasa dengan sumber daya **Bahasa** atau **Layanan Azure AI**. Ada beberapa contoh yang khusus untuk penggunaan sumber daya Bahasa. Untuk latihan di bawah ini, kami akan menggunakan sumber daya **Bahasa**. Jika belum melakukannya, buat sumber daya **Bahasa** di langganan Azure Anda.

1. Di tab browser yang lain, buka portal Azure di [https://portal.azure.com](https://portal.azure.com?azure-portal=true), lalu masuk dengan akun Microsoft yang terkait dengan langganan Azure Anda.

1. Klik **&#65291;Buat tombol sumber daya** dan cari *Layanan Bahasa*. Pilih **buat** paket **Layanan bahasa**. Anda akan dibawa ke halaman ke *Pilih fitur tambahan**. Pertahankan pilihan default dan klik **Lanjutkan untuk membuat sumber daya Anda**. 

1. Pada halaman **Buat Bahasa**, konfigurasikan hal tersebut dengan pengaturan berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Wilayah**: *Pilih wilayah geografis terdekat. Jika berada di AS timur, gunakan "US Timur 2"*.
    - **Nama**: *Masukkan nama unik*.
    - **Tingkat harga**: *F0 atau S gratis jika F0 Gratis tidak tersedia*
    - **Dengan mencentang kotak ini, saya menyatakan bahwa saya telah membaca dan memahami semua ketentuan di bawah ini**: *Dipilih*.

1. Pilih **Tinjau + buat** lalu **Buat** dan tunggu hingga penyebaran selesai.


### Membuat Aplikasi Pemahaman Bahasa Percakapan

Untuk menerapkan pemahaman bahasa alami dengan Pemahaman Bahasa Percakapan, Anda membuat aplikasi; lalu tambahkan entitas, niat, dan ucapan untuk menentukan perintah yang Anda inginkan agar dijalankan oleh aplikasi.

1. Di tab browser baru, buka portal Language Studio di [https://language.azure.com](https://language.azure.com?azure-portal=true) dan masuk menggunakan akun Microsoft yang terkait dengan langganan Azure Anda.

1. Jika diminta untuk memilih sumber daya Bahasa, pilih pengaturan berikut:
    - **Azure directory**: *Azure directory yang berisi langganan Anda*.
    - **Langganan Azure**: *Langganan Azure Anda*.
    - **Sumber daya bahasa**: *Sumber daya Bahasa yang Anda buat sebelumnya.*

   Jika Anda ***tidak*** diminta untuk memilih sumber daya bahasa, hal tersebut mungkin karena Anda memiliki beberapa sumber daya Bahasa dalam langganan Anda; dalam hal ini:
    1. Pada bilah di bagian atas halaman, pilih **Pengaturan (&#9881;)**.
    2. Pada halaman **Pengaturan**, lihat tab **Sumber Daya**.
    3. Pilih sumber daya bahasa yang baru saja Anda buat, dan pilih **Beralih sumber daya**.
    4. Di bagian atas halaman, pilih **Language Studio** untuk kembali ke beranda Language Studio.

1. Di bagian atas portal, di menu **Buat baru**, pilih **Pemahaman bahasa percakapan**.

1. Dalam kotak dialog **Buat proyek**, di halaman **Masukkan informasi dasar**, masukkan detail berikut dan pilih **Berikutnya**:
    - **Nama**: *Membuat nama unik*
    - **Bahasa utama ujaran**: *Inggris*
    - **Aktifkan beberapa bahasa dalam proyek:***Jangan pilih*
    - **Deskripsi**: `Simple home automation`

    > **Tips**: Catat *nama proyek*Anda, Anda akan menggunakannya nanti.

1. Pada halaman **Tinjau dan selesai**, pilih **Buat**.

### Membuat niat, ucapan, dan entitas

*Tujuan* adalah tindakan yang ingin Anda lakukan - misalnya, Anda mungkin ingin menyalakan lampu, atau mematikan kipas. Dalam hal ini, Anda akan menentukan dua tujuan: satu untuk mengaktifkan perangkat, dan satu lagi untuk mematikan perangkat. Untuk setiap niat, Anda akan menentukan contoh *ungkapan* yang menunjukkan jenis bahasa yang digunakan untuk mengindikasikan maksud.

1. Di panel **Definisi skema**, pastikan bahwa **Niat** dipilih lalu pilih **Tambahkan**, lalu tambahkan niat dengan nama `switch_on` (dengan huruf kecil) dan pilih **Tambahkan niat**.

    ![Pilih tambahkan di bawah Niat pada panel Bangun Skema.](media/conversational-language-understanding/build-schema.png)

    ![Tambahkan tujuan pengaktifan lalu pilih Tambahkan tujuan.](media/conversational-language-understanding/add-intent.png)

1. Pilih niat **switch_on**. Panel akan membawa Anda ke halaman **Pelabelan data**. Di menu dropdown **Tujuan**, pilih **switch_on**. Di samping niat **switch_on**, ketik ujaran `turn the light on` dan tekan **Enter** untuk mengirimkan ujaran ini ke daftar.

    ![Tambahkan ucapan ke set pelatihan dengan mengetik "nyalakan lampu" di bagian Ucapan.](media/conversational-language-understanding/add-utterance-on.png)

1. Layanan bahasa membutuhkan setidaknya lima contoh ucapan yang berbeda untuk setiap tujuan guna melatih model bahasa secara memadai. Tambahkan lima contoh ucapan lainnya ke niat **switch_on**:  
    - `switch on the fan`
    - `put the fan on`
    - `put the light on`
    - `switch on the light`
    - `turn the fan on`

1. Pada panel **Beri label entitas untuk pelatihan** di sisi kanan layar, pilih **Label**, lalu pilih **Tambahkan entitas**. Ketik `device` (dengan huruf kecil), pilih **Daftar** dan pilih **Tambahkan entitas**.

    ![Tambahkan entitas dengan memilih Tag pada entitas Pemberian tag untuk panel pelatihan, lalu pilih Tambahkan entitas.](media/conversational-language-understanding/add-entity.png)

    ![Ketik perangkat di bagian Nama entitas dan pilih Daftar, lalu pilih Tambahkan entitas.](media/conversational-language-understanding/add-entity-device.png)

1. Pada ucapan ***nyalakan kipas angin***, sorot kata "kipas angin". Kemudian dalam daftar yang muncul, di kotak *Cari entitas* pilih **perangkat**.

    ![Sorot kata kipas dalam ucapan dan pilih perangkat.](media/conversational-language-understanding/switch-on-entity.png)

1. Lakukan hal yang sama untuk semua ucapan. Beri label ucapan *kipas* atau *lampu* lainnya dengan entitas **perangkat**. Setelah selesai, verifikasi bahwa Anda memiliki ucapan berikut dan pastikan untuk memilih **Simpan perubahan**:

    | **tujuan** | **ucapan** | **entitas** |
    | --------------- | ------------------ | ------------------ |
    | switch_on   | Nyalakan kipas angin      | Perangkat - *pilih kipas* |
    | switch_on   | Nyalakan lampu    | Perangkat - *pilih lampu* |
    | switch_on   | Nyalakan lampu | Perangkat - *pilih lampu* |
    | switch_on   | Nyalakan kipas angin     | Perangkat - *pilih kipas* |
    | switch_on   | Nyalakan kipas angin   | Perangkat - *pilih kipas* |
    | switch_on   | Nyalakan lampu   | Perangkat - *pilih lampu* |

    ![Setelah selesai, pilih Simpan perubahan.](media/conversational-language-understanding/save-changes.png) 

1. Di panel di sebelah kiri, pilih **Definisi skema** dan verifikasi bahwa niat **switch_on** Anda tercantum. Lalu pilih **Tambahkan** dan tambahkan niat baru dengan nama `switch_off` (dengan huruf kecil).

    ![Kembali ke layar Bangun Skema dan tambahkan tujuan switch_off.](media/conversational-language-understanding/add-switch-off.png) 

1. Pilih niat **switch_off**. Panel akan membawa Anda ke halaman **Pelabelan data**. Di menu dropdown **Tujuan**, pilih **switch_off**. Di samping niat **switch_off**, tambahkan ujaran `turn the light off`.

1. Tambahkan empat contoh ucapan lainnya ke niat **switch_off**.
    - `switch off the fan`
    - `put the fan off`
    - `put the light off`
    - `turn off the light`
    - `switch the fan off`

1. Beri label kata-kata *lampu* atau *kipas* dengan entitas **perangkat**. Setelah selesai, verifikasi bahwa Anda memiliki ucapan berikut dan pastikan untuk memilih **Simpan perubahan**:  

    | **tujuan** | **ucapan** | **entitas** | 
    | --------------- | ------------------ | ------------------ |
    | switch_off   | Matikan kipas    | Perangkat - *pilih kipas* | 
    | switch_off   | Matikan lampu  | Perangkat - *pilih lampu* |
    | switch_off   | Matikan lampu | Perangkat - *pilih lampu* |
    | switch_off   | Matikan kipas angin | Perangkat - *pilih kipas* |
    | switch_off   | Matikan kipas angin | Perangkat - *pilih kipas* |
    | switch_off   | Matikan lampu | Perangkat - *pilih lampu* |

### Melatih model

Sekarang Anda siap menggunakan niat dan entitas yang ditentukan untuk melatih model bahasa percakapan untuk aplikasi Anda.

1. Di sisi kiri Studio Bahasa, pilih **Pekerjaan pelatihan**, lalu pilih **Mulai pekerjaan pelatihan**. Gunakan pengaturan berikut:
    - **Latih model baru:***Dipilih dan pilih nama model*
    - **Mode pelatihan**: Pelatihan standar (gratis)
    - **Pemisahan Data**: *pilih Pisahkan kumpulan pengujian secara otomatis dari data pelatihan, pertahankan persentase default*
    - Pilih **Latih** di bagian bawah halaman.

1. Tunggu hingga pelatihan selesai.

### Terapkan dan uji model

Untuk menggunakan model terlatih Anda dalam aplikasi klien, Anda harus menerapkannya sebagai titik akhir tempat aplikasi klien dapat mengirim ucapan baru; tempat tujuan dan entitas akan diprediksi.

1. Di sisi kiri Language Studio, pilih **Menyebarkan model**.

1. Pilih nama model Anda lalu **Tambahkan penyebaran**. Gunakan pengaturan ini:
    - **Buat atau pilih nama penyebaran yang ada**: *Pilih buat nama penyebaran baru. Tambahkan nama unik*.
    - **Tetapkan model terlatih ke nama penyebaran Anda**: *Pilih nama model terlatih*.
    - Pilih **Sebarkan**

    > **Tips**: Catat *nama penyebaran* Anda, Anda akan menggunakannya nanti. 

1. Saat model disebarkan, pilih **Menguji penyebaran** di sisi kiri halaman, lalu pilih model yang Anda sebarkan di bawah **Nama penyebaran**.

1. Masukkan teks berikut, lalu pilih **Jalankan pengujian**:

    `switch the light on`

    ![Uji model Anda dengan memilih model yang disebarkan, lalu masukkan teks dan pilih Jalankan pengujian.](media/conversational-language-understanding/test-model.png) 

    Tinjau hasil yang ditampilkan, dengan mencatat bahwa hasil tersebut mencakup tujuan yang diprediksi (yakni **switch_on**) dan entitas yang diprediksi (**perangkat**) dengan skor keyakinan yang menunjukkan probabilitas yang dihitung model untuk niat dan entitas yang diprediksi. Tab JSON menunjukkan keyakinan komparatif untuk setiap niat potensial (yang memiliki skor kepercayaan tertinggi adalah tujuan yang diprediksi)

1. Kosongkan kotak teks dan uji model dengan ucapan berikut di bagian *Masukkan teks Anda sendiri, atau unggah dokumen teks*:
    - `turn off the fan`
    - `put the light on`
    - `put the fan off`

Anda sekarang telah berhasil mengonfigurasi proyek bahasa percakapan, dan menentukan entitas, niat, dan ujaran. Anda telah melihat cara melatih dan menyebarkan model di Language Studio. Dan Anda telah mencobanya dengan kedua ujaran yang Anda tentukan, dan beberapa yang tidak Anda tentukan secara eksplisit tetapi model dapat mengetahui.

> **CATATAN**: Pemahaman bahasa percakapan memberikan kecerdasan untuk menafsirkan niat input tetapi tidak melakukan tindakan apa pun seperti menyalakan lampu atau kipas angin. Pengembang perlu membuat aplikasi yang menggunakan model Pemahaman Bahasa Percakapan untuk menentukan niat pengguna, lalu mengotomatiskan tindakan yang sesuai.

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1.Buka [portal Azure]( https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat. 1.Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Aplikasi ini hanya menampilkan beberapa kemampuan fitur Pemahaman Bahasa Percakapan dari layanan Bahasa. Untuk mempelajari selengkapnya tindakan yang dapat Anda lakukan dengan layanan ini, lihat [Halaman Pemahaman Bahasa Percakapan](https://docs.microsoft.com/azure/cognitive-services/language-service/conversational-language-understanding/overview).
