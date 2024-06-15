---
lab:
  title: Menganalisis teks dengan Language Studio
---

# Menganalisis teks dengan Language Studio

Pada latihan ini Anda akan mengeksplorasi kemampuan Azure AI Bahasa dengan menganalisis beberapa contoh ulasan hotel. Anda akan menggunakan Language Studio untuk memahami apakah ulasan sebagian besar positif atau negatif.

Pemrosesan Bahasa Alami (NLP) adalah cabang dari AI yang berhubungan dengan bahasa tulis dan lisan. Anda dapat menggunakan NLP untuk membuat solusi yang mengekstrak makna semantik dari teks atau ucapan, atau yang memformulasikan respons bermakna dalam bahasa alami.

Misalnya, agen perjalanan fiktif Margie's Travel mendorong pelanggan untuk mengirimkan ulasan tentang masa inap di hotel. Anda dapat menggunakan layanan Bahasa untuk mengidentifikasi frasa kunci, menentukan ulasan mana yang positif dan yang negatif, atau menganalisis teks ulasan untuk menyebutkan entitas yang dikenal seperti lokasi atau orang.

Layanan Azure AI Bahasa mencakup analisis teks dan kemampuan NLP. Ini termasuk identifikasi frasa kunci dalam teks, dan klasifikasi teks berdasarkan sentimen.

## Membuat sumber daya *Bahasa*

Anda dapat menggunakan banyak fitur Azure AI Bahasa dengan sumber daya **Bahasa** atau **Layanan Azure AI**. Ada beberapa contoh yang khusus untuk penggunaan sumber daya Bahasa. Untuk latihan di bawah ini, kami akan menggunakan sumber daya **Bahasa**. Jika belum melakukannya, buat sumber daya **Bahasa** di langganan Azure Anda.

1. Di tab browser yang lain, buka portal Azure di [https://portal.azure.com](https://portal.azure.com?azure-portal=true), lalu masuk dengan akun Microsoft yang terkait dengan langganan Azure Anda.

1. Klik **&#65291;Buat tombol sumber daya** dan cari *Layanan Bahasa*. Pilih **buat** paket **Layanan Bahasa**. Anda akan dibawa ke suatu halaman untuk **Memilih fitur tambahan**. Pertahankan pilihan default dan klik **Lanjutkan untuk membuat sumber daya Anda**. 

1. Pada halaman **Buat Bahasa**, konfigurasikan hal tersebut dengan pengaturan berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Wilayah**: *Pilih wilayah geografis terdekat. Jika berada di AS timur, gunakan "US Timur 2"*.
    - **Nama**: *Masukkan nama unik*.
    - **Tingkat harga**: *F0 atau S gratis jika F0 Gratis tidak tersedia*
    - **Dengan mencentang kotak ini, saya menyatakan bahwa saya telah membaca dan memahami semua ketentuan di bawah ini**: *Dipilih*.

1. Pilih **Tinjau + buat**, lalu **Buat** dan tunggu hingga penyebaran selesai.

## Mengonfigurasi sumber daya Anda di Azure AI Language Studio

1. Pada tab browser lain, buka **Language Studio** di [https://language.cognitive.azure.com](https://language.cognitive.azure.com?azure-portal=true) dan masuk.

1. Saat diminta dengan **Pilih sumber daya Azure**, lakukan konfigurasi berikut:
    - **Direktori Azure**: *Direktori Default, direktori yang Anda gunakan*
    - **Langganan Azure**: *Pilih langganan yang Anda gunakan*
    - **Tipe sumber daya**: Bahasa
    - **Nama sumber daya**: *pilih sumber daya layanan Bahasa yang baru saja Anda buat*

Kemudian pilih **Selesai**.

> **Penting**: Mulai Juli 2023, layanan Azure AI mencakup semua yang sebelumnya dikenal sebagai Cognitive Services dan Azure Applied AI Services. Beberapa antarmuka pengguna masih memperbarui referensinya dari `Cognitive Services` ke `Azure AI services`. Kedua nama tersebut merujuk pada tipe sumber daya yang sama.

> **Catatan**: Jika Anda ***tidak*** diminta untuk memilih sumber daya bahasa, itu mungkin karena Anda memiliki beberapa sumber daya Bahasa dalam langganan Anda; dalam hal ini:
> 1. Pada bilah di bagian atas halaman, pilih **Pengaturan (&#9881;)**. 
> 1. Pada halaman **Pengaturan**, lihat tab **Sumber Daya**.
> 1. Pilih sumber daya yang baru saja Anda buat, lalu pilih **Alihkan sumber daya**. Pastikan Identitas terkelola **Diaktifkan**.
> ![Aktifkan sumber daya bahasa.](media/analyze-text-language-service/language-resource-enabled.png)
> 1. Di bagian atas halaman, pilih **Language Studio** untuk kembali ke beranda Language Studio.

## Menganalisis ulasan di Language Studio

1. Di browser web, navigasikan ke **Language Studio** di [https://language.cognitive.azure.com](https://language.cognitive.azure.com?azure-portal=true).

1. Di halaman arahan **Selamat datang di Language Studio**, pilih tab **Klasifikasikan teks**, lalu pilih ubin **Analisis sentimen dan gali opini**.

1. Pada *Pilih bahasa teks*, pilih **Inggris**.

1. Pada *Pilih sumber daya Azure Anda*, pilih sumber daya Anda.

1. Pada *Masukkan teks Anda sendiri, unggah file, atau gunakan salah satu contoh teks kami*, salin dan tempel ulasan berikut:

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. Centang kotak untuk mengonfirmasi bahwa demo akan dihitung sebagai penggunaan dan mungkin dikenakan biaya, lalu pilih **Jalankan**.

1. Tinjau output. Perhatikan bahwa *dokumen* dianalisis sentimennya, serta per *kalimat*. Pilih **Kalimat 1** untuk menampilkan analisis sentimen kalimat tersebut. 

Perhatikan bahwa terdapat sentimen keseluruhan yang diikuti dengan skor dalam tiga kategori: *skor positif*, *skor netral*, dan *skor negatif*. Di setiap kategori, diberi skor antara 0 dan 1. Skor keyakinan ini menunjukkan seberapa besar probabilitas teks yang diberikan merupakan sentimen tertentu. 

Pilih **Kalimat 1** lagi untuk menutup.

1. Gulir ke atas untuk memilih **Bersihkan kotak teks**, lalu salin dan tempel ulasan berikut:

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```
    
    
1. Pilih **Jalankan**. Tinjau output dan tinjau tingkat sentimen dan keyakinannya.

1. Pilih kotak **Bersihkan teks** lagi, lalu salin dan tempel ulasan berikut:

    >Sangat bising dan kamarnya kecil The Lombard Hotel, San Francisco, USA 9/5/2018 Hotel ini berada di jalan Lombard yang merupakan jalan ENAM lajur yang sangat sibuk langsung dari Jembatan Golden Gate. Lalu lintas dari pagi hingga larut malam terutama di akhir pekan. Kebisingan tidak akan begitu buruk jika kamarnya terisolasi dengan baik, tetapi faktanya tidak. Harus meletakkan bola kapas di telinga agar bisa tertidur - terlalu lelah untuk menikmati kota keesokan harinya. Kamarnya kecil. Saya memilih kamar ini karena berisi dua tempat tidur ukuran besar - tetapi kamarnya hampir kehabisan ruang untuk tipe tempat tidur tersebut. Kamarnya terlalu sempit untuk keluarga empat orang. Kesimpulannya, kamarnya bersih dan mereka telah berusaha untuk memperbaruinya. Hotel ini berada di distrik Marina dengan banyak tempat makan yang bagus, dan sangat dekat dengan Presidio. Hotel ini mungkin cocok bagi remaja dengan anggaran terbatas

1. Pilih **Jalankan** dan tinjau sentimen beserta tingkat keyakinannya. Lihat teks dan bandingkan teks dengan analisis sentimen yang dihasilkan oleh layanan.

Dalam latihan ini Anda menggunakan Language Studio untuk membuat sumber daya Bahasa baru atau menggunakan sumber daya Bahasa yang sudah ada. Anda mengaktifkan sumber daya di Pengaturan sebelum mencoba Layanan penggalian opini dan sentimen. Kemudian, Anda menguji layanan tersebut dengan tiga potong teks.

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Ini untuk menghindari akumulasi biaya yang tidak perlu.

1. Buka **portal Azure** di [https://portal.azure.com](https://portal.azure.com) dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.
1. Pilih sumber daya dan pilih **Hapus**, lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman layanan Bahasa](https://learn.microsoft.com/azure/ai-services/language-service/overview).
