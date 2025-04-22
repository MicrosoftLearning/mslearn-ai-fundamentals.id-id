---
lab:
  title: Menganalisis teks di portal Azure AI Foundry
---

# Menganalisis teks di portal Azure AI Foundry

Pemrosesan Bahasa Alami (NLP) adalah cabang dari AI yang berhubungan dengan bahasa tulis dan lisan. Anda dapat menggunakan NLP untuk membuat solusi yang mengekstrak makna semantik dari teks atau ucapan, atau yang memformulasikan respons bermakna dalam bahasa alami.

Layanan Bahasa Azure AI mencakup Analitik Teks, dengan kemampuan seperti pengenalan entitas, ekstraksi frasa kunci, ringkasan, dan analisis sentimen. Misalnya, agen perjalanan fiktif Margie's Travel mendorong pelanggan untuk mengirimkan ulasan tentang masa inap di hotel. Anda dapat menggunakan layanan Bahasa untuk mengekstrak entitas bernama, mengidentifikasi frasa kunci, meringkas teks, dan banyak lagi.

Dalam latihan ini, Anda akan menggunakan Bahasa Azure AI di portal Azure AI Foundry, platform Microsoft untuk membuat aplikasi cerdas, untuk menganalisis ulasan hotel. 

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
 
1. Setelah sumber daya dibuat, Anda akan dibawa ke halaman* Gambaran Umum* proyek Anda. Di menu sebelah kiri pada layar, pilih **Playgrounds**.
 
    ![Cuplikan layar menu sebelah kiri pada layar proyek dengan playground dipilih.](./media/azure-ai-foundry-playgrounds.png)  

1. Pada halaman *Playgrounds*, pilih petak **playground Bahasa** untuk mencoba beberapa kemampuan Azure AI Bahasa.

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
