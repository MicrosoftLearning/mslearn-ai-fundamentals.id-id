---
lab:
  title: Jelajahi Layanan Azure AI
---

# Jelajahi Layanan Azure AI

Layanan Azure AI membantu pengguna membuat aplikasi AI dengan API dan model yang siap pakai dan dapat disesuaikan sebelumnya. Dalam latihan ini, Anda akan membuat sumber daya di portal Azure dan mencoba layanan Azure AI. Tujuan dari latihan ini adalah untuk mendapatkan pemahaman umum tentang bagaimana layanan Azure AI disediakan dan digunakan.

## Membuat sumber daya *Layanan AI Azure* di portal Azure

1. Di tab browser, buka portal Azure di [https://portal.azure.com](https://portal.azure.com?azure-portal=true), masuk dengan akun Microsoft yang terkait dengan langganan Azure Anda.

1. Klik tombol **＋Buat sumber daya**dan cari *layanan Azure AI*. Pilih **buat** paket **layanan Azure AI**. Anda akan diarahkan ke halaman untuk membuat sumber daya layanan Azure AI. Konfigurasikan dengan pengaturan berikut:
    - **Langganan**: *Langganan Azure Anda*.
    - **Grup sumber daya**: *Pilih atau buat grup sumber daya dengan nama unik*.
    - **Wilayah**: *Pilih wilayah geografis terdekat. Jika berada di AS timur, gunakan "US Timur 2"*.
    - **Nama**: *Masukkan nama unik*.
    - **Tingkat harga**: *Standar S0.*
    - **Dengan mencentang kotak ini, saya menyatakan bahwa saya telah membaca dan memahami semua ketentuan di bawah ini**: *Dipilih*.

1. Pilih **Tinjau + buat**, lalu **Buat** dan tunggu hingga penyebaran selesai.

    *Selamat! Anda baru saja membuat, atau menyediakan, sumber daya layanan Azure AI. Sumber daya yang Anda sediakan khususnya adalah sumber daya multi-layanan.*

1. Setelah penyebaran selesai, pilih *Buka Sumber daya*. 

## Lihat kunci dan titik akhir

Untuk menggabungkan layanan Azure AI ke dalam aplikasi, pengembang memerlukan kunci layanan dan titik akhir Kunci dan titik akhir yang digunakan untuk pengembangan aplikasi dapat ditemukan di Portal Azure. 

1. Di Azure Portal, pilih sumber daya Anda. Di menu sebelah kiri, lihat di bawah * Resource Management* untuk *Kunci dan Titik Akhir*. Pilih **Kunci dan Titik Akhir** untuk melihat titik akhir dan kunci untuk sumber daya Anda. 

## Lihat layanan Azure AI beraksi

Mari kita mulai dengan membuat proyek Azure AI Foundry.

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup tips atau panel mulai cepat yang dibuka saat pertama kali Anda masuk.
 
1. Di jendela browser baru, buka [halaman eksplorasi Layanan Azure AI](https://ai.azure.com/explore/aiservices).

1. Pada halaman *Layanan AI*, pilih petak *Visi + Dokumen* untuk mencoba kemampuan Azure AI Vision dan Dokumen.

    ![Cuplikan layar petak Visi dan Dokumen dipilih di halaman Layanan AI.](./media/vision-document-tile.png)

1. Di bawah *Lihat semua kemampuan Vision* pilih tab **Wajah**. 

1. Pilih petak demo *Mendeteksi wajah dalam gambar*. 

1. Cobalah layanan Wajah, yang merupakan salah satu dari sekian banyak layanan Azure AI. Klik pada gambar dan periksa atribut yang terdeteksi. 

    ![Cuplikan layar dari demo pendeteksian wajah di portal Azure AI Foundry.](./media/detect-faces-demo.png)

1. Gulir ke bawah ke bagian **Jalankan kode**. Pilih **Lihat Kode**. Gulir ke bawah ke bagian yang dimulai dengan *impor os*. Pada contoh kode yang disediakan, Anda akan melihat placeholder tempat Anda dapat menaruh kunci dan titik akhir.

    ![Cuplikai layar dari layar lihat kode dengan tampilan placeholder kode untuk kunci dan titik akhir.](./media/view-code-example.png) 

1. Jika Anda ingin membuat aplikasi yang menggunakan layanan Azure AI, Anda dapat memulai dengan kode yang disediakan. Dengan mengganti placeholder dengan kunci dan titik akhir layanan Anda sendiri, aplikasi Anda akan dapat mengirim permintaan dan menerima respons yang memanfaatkan layanan Azure AI. Dalam kasus layanan Wajah, *permintaan* adalah agar layanan Wajah menganalisis gambar. *Responsnya* adalah atribut yang terdeteksi. 

    >**Catatan** Anda tidak perlu mengetahui pemrograman untuk menyelesaikan latihan apa pun dalam kursus ini. Kami akan terus melihat layanan Azure AI yang sedang beraksi melalui portal Azure AI Foundry.  
 
## Penghapusan 

Setelah selesai, Anda dapat menghapus sumber daya layanan Azure AI dari Azure Portal. Menghapus sumber daya adalah cara untuk mengurangi biaya yang bertambah ketika sumber daya ada dalam langganan. Untuk melakukan ini, buka halaman **Gambaran Umum** pada sumber daya layanan Azure AI Anda. Pilih **Hapus** di bagian atas layar.

