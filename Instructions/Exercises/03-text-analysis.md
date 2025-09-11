---
lab:
  title: Menganalisis teks di portal Azure AI Foundry
---

# Menganalisis teks di portal Azure AI Foundry

Pemrosesan Bahasa Alami (NLP) adalah cabang dari AI yang berhubungan dengan bahasa tulis dan lisan. Anda dapat menggunakan NLP untuk membuat solusi yang mengekstrak makna semantik dari teks atau ucapan, atau yang memformulasikan respons bermakna dalam bahasa alami.

Layanan Bahasa Azure AI mencakup Analitik Teks, dengan kemampuan seperti pengenalan entitas, ekstraksi frasa kunci, ringkasan, dan analisis sentimen. Misalnya, agen perjalanan fiktif Margie's Travel mendorong pelanggan untuk mengirimkan ulasan tentang masa inap di hotel. Anda dapat menggunakan layanan Bahasa untuk mengekstrak entitas bernama, mengidentifikasi frasa kunci, meringkas teks, dan banyak lagi.

Dalam latihan ini, Anda akan menggunakan Bahasa Azure AI di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk menganalisis ulasan hotel. 

Latihan ini memakan waktu sekitar **20** menit.

## Membuat proyek di portal Azure AI Foundry

1. Di browser web, buka [portal Azure AI Foundry](https://ai.azure.com) di `https://ai.azure.com` dan masuk menggunakan kredensial Azure Anda. Tutup tips atau panel mulai cepat yang dibuka saat pertama kali Anda masuk. 

1. Di browser, navigasikan ke `https://ai.azure.com/managementCenter/allResources` dan pilih **Buat baru**. Lalu pilih opsi untuk membuat **sumber daya Azure AI Foundry**.

1. Di wizard,*Buat proyek*dan masukkan nama yang valid untuk proyek Anda.

1. Perluas *opsi Tingkat Lanjut* untuk menentukan pengaturan proyek Anda sebagai berikut:
    - **Subscription**: Langganan Azure Anda
    - **Grup sumber daya**: Buat atau pilih grup sumber daya
    - **Wilayah**: Pilih salah satu wilayah berikut:
        * AS Timur
        * Prancis Tengah
        * Korea Tengah
        * Eropa Barat
        * US Barat

    Pilih **Buat**. Tunggu proyek Anda dibuat. Proses ini memerlukan waktu beberapa menit.

1. Saat proyek dibuat, Anda akan dibawa ke *halaman Gambaran Umum* tentang detail proyek.

1. Di menu sebelah kiri pada layar, pilih **Playgrounds**. 

    >*Catatan*: Perluas menu untuk membaca kontennya dengan mengklik ikon 'perluas' atas.

1. Di halaman Playground Azure AI Foundry, pilih **Coba Playground bahasa**. Playground bahasa adalah antarmuka pengguna yang memungkinkan Anda mencoba beberapa kemampuan Azure AI Bahasa.  

## Mengekstrak entitas bernama dengan Azure AI Bahasa di portal Azure AI Foundry

*Entitas bernama* adalah kata-kata yang menggambarkan orang, tempat, dan objek dengan nama yang tepat. Mari kita gunakan kemampuan ekstraksi entitas bernama Azure AI Bahasa untuk mengidentifikasi jenis informasi dalam ulasan.

1. Di playground Bahasa, pilih **Ekstrak informasi**. Kemudian pilih petak **Ekstrak entitas bernama**. 

1. Di bawah *Sampel*, salin dan tempel tinjauan berikut:

    ```
    Tired hotel with poor service
    The Royal Hotel, London, United Kingdom
    5/6/2018
    This is an old hotel (has been around since 1950's) and the room furnishings are average - becoming a bit old now and require changing. The internet didn't work and had to come to one of their office rooms to check in for my flight home. The website says it's close to the British Museum, but it's too far to walk.
    ```

1. Pilih **Jalankan**. Tinjau output. Perhatikan di bagian *Detail* bagaimana entitas yang diekstrak dilengkapi dengan informasi tambahan seperti jenis dan skor keyakinan. Skor keyakinan mewakili kemungkinan bahwa jenis yang diidentifikasi benar-benar termasuk dalam kategori tersebut.

## Mengekstrak frasa kunci dengan Azure AI Bahasa di portal Azure AI Foundry

*Frasa kunci* adalah bagian informasi terpenting dalam teks. Mari kita gunakan kemampuan ekstraksi frasa kunci Azure AI Bahasa untuk menarik informasi penting dari ulasan.

1. Di playground Bahasa, pilih **Ekstrak informasi**. Lalu pilih petak **Ekstrak frasa kunci**. 

1. Di bawah *Sampel*, salin dan tempel tinjauan berikut:

    ```
    Good Hotel and staff
    The Royal Hotel, London, UK
    3/2/2018
    Clean rooms, good service, great location near Buckingham Palace and Westminster Abbey, and so on. We thoroughly enjoyed our stay. The courtyard is very peaceful and we went to a restaurant which is part of the same group and is Indian ( West coast so plenty of fish) with a Michelin Star. We had the taster menu which was fabulous. The rooms were very well appointed with a kitchen, lounge, bedroom and enormous bathroom. Thoroughly recommended.
    ```

1. Pilih **Jalankan**. Tinjau output. Perhatikan berbagai frasa yang diekstrak di bagian *Detail* . Frasa ini harus berkontribusi paling besar terhadap arti teks.

## Meringkas teks dengan Azure AI Bahasa di portal Azure AI Foundry
 
1. Mari kita lihat kemampuan ringkasan Azure AI Bahasa. Di playground Bahasa, pilih *Ringkas informasi*, lalu pilih petak **Ringkas teks**.

1. Di bawah *Sampel*, salin dan tempel tinjauan berikut:
    
    ```
    Very noisy and rooms are tiny
    The Lombard Hotel, San Francisco, USA
    9/5/2018
    Hotel is located on Lombard street which is a very busy SIX lane street directly off the Golden Gate Bridge. Traffic from early morning until late at night especially on weekends. Noise would not be so bad if rooms were better insulated but they are not. Had to put cotton balls in my ears to be able to sleep--was too tired to enjoy the city the next day. Rooms are TINY. I picked the room because it had two queen size beds--but the room barely had space to fit them. With family of four in the room it was tight. With all that said, rooms are clean and they've made an effort to update them. The hotel is in Marina district with lots of good places to eat, within walking distance to Presidio. May be good hotel for young stay-up-late adults on a budget
    ```

1. Pilih **Jalankan**. Tinjau output. Perhatikan *Ringkasan ekstraktif* dalam *Detail* yang memberikan skor peringkat untuk kalimat yang paling penting.   

## Penghapusan

Jika Anda tidak berniat untuk melakukan latihan lagi, hapus sumber daya yang tidak lagi dibutuhkan. Hal ini menghindari akumulasi biaya yang tidak perlu.

1. Buka **portal Azure** di [https://portal.azure.com](https://portal.azure.com)dan pilih grup sumber daya yang berisi sumber daya yang Anda buat.

1. Pilih sumber daya dan pilih **Hapus** lalu **Ya** untuk mengonfirmasi. Sumber daya tersebut akan dihapus.

## Pelajari lebih lanjut

Untuk mempelajari selengkapnya tentang apa yang dapat Anda lakukan dengan layanan ini, lihat [halaman layanan Bahasa](https://learn.microsoft.com/azure/ai-services/language-service/overview).
